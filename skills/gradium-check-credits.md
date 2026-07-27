---
name: Check Gradium credit balance
description: Read the authenticated subscription's Gradium credit balance before running TTS/STT/S2S workloads.
api: openapi/gradium-openapi-original.json
operations: [get_credits_usages_credits_get]
generated: '2026-07-19'
method: generated
---

# Check Gradium credit balance

Gradium meters usage in credits. Check the balance before large batch jobs so a session does not fail mid-stream.

## Auth
`x-api-key: gd_...`. Base URL: `https://api.gradium.ai/api`.

## Steps
1. **Get credits** — `get_credits_usages_credits_get` (`GET /usages/credits`) returns a `CreditsSummary` for the authenticated subscription.

## Cost model (plan for consumption)
- TTS: 1 credit per character (~750 chars/minute, ~45,000 credits/hour).
- STT: 3 credits per second.
- STT translation: 4 credits per second.
- S2S translation: 30 credits per second.

## Rules
- A single TTS/STT session lasts at most 300 seconds — chunk long content and re-check credits between batches.
- Auth failures return code `1008`.
