---
name: Manage Gradium pronunciation dictionaries
description: Create and maintain language-specific pronunciation rewrite rules to control how Gradium TTS pronounces brand names, acronyms, and technical terms.
api: openapi/gradium-openapi-original.json
operations: [create_pronunciation_dictionary_pronunciations__post, list_pronunciation_dictionaries_pronunciations__get, get_pronunciation_dictionary_pronunciations__uid__get, update_pronunciation_dictionary_pronunciations__uid__put, delete_pronunciation_dictionary_pronunciations__uid__delete]
generated: '2026-07-19'
method: generated
---

# Manage Gradium pronunciation dictionaries

Pronunciation dictionaries hold language-specific rewrite rules so TTS says brand names, reference codes, and acronyms correctly.

## Auth
`x-api-key: gd_...`. Base URL: `https://api.gradium.ai/api`.

## Steps
1. **Create** — `create_pronunciation_dictionary_pronunciations__post` (`POST /pronunciations/`) with a set of `PronunciationRuleCreate` rewrite rules.
2. **List** — `list_pronunciation_dictionaries_pronunciations__get` (`GET /pronunciations/`). Paginate with `limit`/`offset`; filter by `language`.
3. **Retrieve** — `get_pronunciation_dictionary_pronunciations__uid__get` (`GET /pronunciations/{uid}`) to read a dictionary and its rules.
4. **Update** — `update_pronunciation_dictionary_pronunciations__uid__put` (`PUT /pronunciations/{uid}`).
5. **Delete** — `delete_pronunciation_dictionary_pronunciations__uid__delete` (`DELETE /pronunciations/{uid}`, returns 204).

## Rules
- Note pagination differs from Voices: pronunciations use `offset`, voices use `skip`.
- Reference the dictionary in TTS setup / voice settings to apply its rewrite rules.
- `422` on malformed rules; auth failures return code `1008`.
