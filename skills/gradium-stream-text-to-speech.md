---
name: Stream Gradium text-to-speech
description: Synthesize low-latency speech from text over the Gradium WebSocket using a chosen voice.
api: openapi/gradium-openapi-original.json
operations: [get_voices_voices__get]
generated: '2026-07-19'
method: generated
---

# Stream Gradium text-to-speech

Generate natural, low-latency audio from text over the Gradium real-time WebSocket (`wss://api.gradium.ai/api/speech/tts`). Time-to-first-token is below ~300ms when streaming.

## Auth
- Server-side: `x-api-key: gd_...`.
- Browser/mobile: never ship the API key. Exchange it server-side for a single-use token via `GET https://api.gradium.ai/api/api-keys/token` and connect with `?token=...` (see `authentication/gradium-authentication.yml`).

## Steps
1. **Pick a voice** — `get_voices_voices__get` (`GET /voices/`) to choose a `voice_id` (custom clone or flagship via `include_catalog`).
2. **Open the socket** — connect to `/speech/tts`.
3. **Send setup** — `{"type":"setup","voice_id":"<uid>","output_format":"pcm"}`. Wait for the `ready` message.
4. **Send text** — one or more `{"type":"text","text":"..."}` messages; stream LLM tokens in as they arrive to preserve prosody.
5. **Flush / end** — send `{"type":"flush"}` to force emission, then `{"type":"end_of_stream"}`.
6. **Read audio** — collect `{"type":"audio","audio":"<base64>"}` chunks until `end_of_stream`/close.

## Rules
- Output formats: `wav`, `pcm`, `opus`, sample-rate PCM variants (`pcm_16000`…`pcm_48000`), telephony `ulaw_8000`/`alaw_8000`.
- Session limit: 300 seconds — chunk longer text at sentence boundaries with a fresh setup per chunk.
- On `{"type":"error",...,"code":1008|1011}` the server closes the socket; open a new connection to retry.
- Cost: 1 credit per character (see `skills/gradium-check-credits.md`).
