# Gradium

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Gradium is a voice AI lab (Paris and Silicon Valley) building audio language models for real-time, low-latency Text-to-Speech, Speech-to-Text, and Speech-to-Speech translation. Founded in 2025 by ex-DeepMind / Meta / Kyutai researchers (Neil Zeghidour, Olivier Teboul, Laurent Mazaré, Alexandre Défossez), Gradium exposes a developer API over REST and WebSocket featuring instant voice cloning from a 10-second sample, custom pronunciation dictionaries, sub-300ms time-to-first-token streaming, and multilingual support (English, French, German, Spanish, Portuguese). It ships first-party Python and Rust SDKs, a `gradium` CLI, and the open-source gradbot voice-agent framework, and is available on AWS Marketplace / SageMaker. Backed by a $70M seed round with participation from Amplify Partners, Eric Schmidt, and Xavier Niel.

**Areas:** Company · Artificial Intelligence · Voice AI · Text-to-Speech · Speech-to-Text · Speech to Speech · Voice Cloning · Audio · Real-Time Streaming · WebSocket · Developer API · Voice Agents

## Gradium on APIs.io

Everything profiled for Gradium is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/gradium/](https://apis.io/providers/gradium/)** — or go straight to one of the APIs or properties below.

### APIs (6)

- [Gradium Metering API](https://apis.io/apis/gradium/gradium-metering-api/) — The metering API from Gradium — 1 operation(s) for metering.
- [Gradium Pronunciations API](https://apis.io/apis/gradium/gradium-pronunciations-api/) — Manage pronunciation dictionaries for custom text rewriting
- [Gradium S2S API](https://apis.io/apis/gradium/gradium-s2s-api/) — The S2S API from Gradium — 1 operation(s) for s2s.
- [Gradium STT API](https://apis.io/apis/gradium/gradium-stt-api/) — Speech-to-Text endpoints for converting audio to text
- [Gradium TTS API](https://apis.io/apis/gradium/gradium-tts-api/) — Text-to-Speech endpoints for converting text to audio
- [Gradium Voices API](https://apis.io/apis/gradium/gradium-voices-api/) — Manage custom voice clones

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Gradium Speech Streaming API](https://apis.io/asyncapis/gradium/gradium-speech-asyncapi/)

#### Event channels (3)

Individual events and webhooks the provider emits.

- [/speech/asr](https://apis.io/channels/gradium/speech-asr/)
- [/speech/s2s](https://apis.io/channels/gradium/speech-s2s/)
- [/speech/tts](https://apis.io/channels/gradium/speech-tts/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [gradium](https://apis.io/servers/gradium/gradium/)

#### Collections (6)

Postman and Open Collection request collections.

- [Gradium metering API](https://apis.io/collections/gradium/open-gradium-metering-api/)
- [Gradium metering Pronunciations API](https://apis.io/collections/gradium/open-gradium-pronunciations-api/)
- [Gradium metering S2S API](https://apis.io/collections/gradium/open-gradium-s2s-api/)
- [Gradium metering STT API](https://apis.io/collections/gradium/open-gradium-stt-api/)
- [Gradium metering TTS API](https://apis.io/collections/gradium/open-gradium-tts-api/)
- [Gradium metering Voices API](https://apis.io/collections/gradium/open-gradium-voices-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Gradium Openapi Overlay](https://apis.io/overlays/gradium/gradium-openapi-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Gradium Authentication](https://apis.io/security/gradium/gradium-authentication/)
- [Gradium Domain Security](https://apis.io/security/gradium/gradium-domain-security/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://gradium.ai)
- [Documentation](https://docs.gradium.ai/)
- [Getting started](https://docs.gradium.ai/guides/installation)
- [API reference](https://docs.gradium.ai/api-reference/introduction)
- [Pricing](https://gradium.ai/pricing)
- [Sign up](https://studio.gradium.ai/platform/subscription)
- [Blog](https://gradium.ai/blog)
- [Trust centre](https://trust.gradium.ai/)
- [Terms of service](https://www.gradium.ai/terms-of-service)
- [Privacy policy](https://www.gradium.ai/privacy)
- [GitHub](https://github.com/gradium-ai)
- [Status](https://gradium.statuspage.io/)

## API Evangelist rating

**Kin Score 47.0** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 53.0 |
| Contract governance | 4.5 |
| Operational transparency | 34.2 |
| Developer ergonomics | 78.0 |
| Access clarity | 31.6 |

**Agent readiness 29.8** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | — |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | derived (partial credit) |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | paginated |
| Operation Distinctiveness | distinct |

**Regulatory alignment 19.3** — AI & Biometrics

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/gradium/](https://apis.io/providers/gradium/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Gradium: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/gradium/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
