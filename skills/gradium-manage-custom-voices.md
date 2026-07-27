---
name: Manage Gradium custom voices
description: Clone, list, update, and delete custom voices for Gradium Text-to-Speech.
api: openapi/gradium-openapi-original.json
operations: [create_voice_voices__post, get_voices_voices__get, get_voice_voices__voice_uid__get, update_voice_voices__voice_uid__put, delete_voice_voices__voice_uid__delete]
generated: '2026-07-19'
method: generated
---

# Manage Gradium custom voices

Use the Gradium Voices API to build and maintain a library of custom (cloned) voices for TTS.

## Auth
Send `x-api-key: gd_...` on every request (see `authentication/gradium-authentication.yml`). Base URL: `https://api.gradium.ai/api`.

## Steps
1. **Clone a voice** — `create_voice_voices__post` (`POST /voices/`). Upload a ~10-second audio sample plus name/description/language. A new voice returns `is_pending: true` until processing completes; poll until `has_audio: true`.
2. **List voices** — `get_voices_voices__get` (`GET /voices/`). Paginate with `skip` and `limit`; set `include_catalog` to include Gradium's flagship library alongside your custom voices.
3. **Inspect one** — `get_voice_voices__voice_uid__get` (`GET /voices/{voice_uid}`). Confirm `is_pending`/`has_audio`/`is_pro_clone` before using the `uid` as a `voice_id` in TTS.
4. **Update metadata** — `update_voice_voices__voice_uid__put` (`PUT /voices/{voice_uid}`).
5. **Delete** — `delete_voice_voices__voice_uid__delete` (`DELETE /voices/{voice_uid}`, returns 204).

## Rules
- Malformed bodies return `422` (HTTPValidationError). Auth failures return code `1008`.
- There is no idempotency-key contract — do not blind-retry `create_voice`; check the list first.
- Use the returned voice `uid` as the `voice_id` in TTS setup.
