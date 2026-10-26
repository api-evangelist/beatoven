# Beatoven.ai (beatoven)

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

Beatoven.ai is an Indian generative-music startup (Bengaluru, founded 2021) building text-to-music and text-to-sound-effects models for video creators, podcasters, game developers, and brands. Its Maestro Music and Maestro SFX models render royalty-free background tracks and foley from natural-language prompts, with downloads delivered as mp3, aac, or wav plus separately rendered stems (bass, chords, melody, percussion). Beatoven is Fairly Trained certified - musicians whose work appears in the training corpus receive equitable compensation. The company exposes a public REST Composition API (public-api.beatoven.ai) plus an open-source Python SDK (github.com/Beatoven/public-api), a Make.com integration, and a self-serve API dashboard. The company has raised an ~$1.3M pre-Series A led by Capital 2B and IvyCap Ventures, claims 2M+ creators and 15M+ tracks generated, and reports 96% of its revenue from international markets.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/beatoven/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/beatoven/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Provider
- **Access:** 3rd-Party

## Tags

- AI
- Artificial Intelligence
- Music
- Music Generation
- Generative Audio
- Text To Music
- Text To SFX
- Royalty-Free Music
- Background Music
- Video Creators
- Podcasts
- Stems
- Fairly Trained
- India

## Timestamps

- **Created:** 2026-05-24
- **Modified:** 2026-05-24

## APIs

### Beatoven Composition API

Asynchronous REST API for composing tracks from natural-language prompts. POST a prompt to /api/v1/tracks/compose to receive a task_id, then poll GET /api/v1/tasks/{task_id} until status is "composed". The completed response includes a download URL for the master mix and separate URLs for the bass, chords, melody, and percussion stems. Supports mp3, aac, and wav output and an optional looping flag for loopable structure. Authentication is HTTP Bearer with an API key issued via sync.beatoven.ai/apiDashboard or by emailing hello@beatoven.ai.

- **Human URL:** [https://github.com/Beatoven/public-api/blob/main/docs/api-spec.md](https://github.com/Beatoven/public-api/blob/main/docs/api-spec.md)
- **Base URL:** `https://public-api.beatoven.ai`

#### Tags

- Music
- Composition
- Tracks
- Stems
- Text To Music

#### Properties

- [Documentation](https://github.com/Beatoven/public-api/blob/main/docs/api-spec.md)
- [Documentation](https://github.com/Beatoven/public-api/blob/main/docs/api-spec-old.md)
- [Documentation](https://www.beatoven.ai/api)
- [OpenAPI](openapi/beatoven-composition-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/beatoven-composition-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/beatoven-composition-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/beatoven-track-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/beatoven-compose-request-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/beatoven-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Spectral Rules](rules/beatoven-composition-rules.yml)
- [Examples](examples/beatoven-compose-request-example.json)
- [Examples](examples/beatoven-compose-response-example.json)
- [Examples](examples/beatoven-task-status-response-example.json)
- [Source Code](https://github.com/Beatoven/public-api)
- [SDK](https://github.com/Beatoven/public-api/tree/main/sdk)
- [Code Examples](https://github.com/Beatoven/public-api/blob/main/examples/compose.py)
- [Integration](https://apps.make.com/beatoven-ai)
- [Blog Post](https://www.beatoven.ai/blog/beatoven-ai-is-now-live-on-make-com-here-is-how-to-use-our-api/)
- [Blog Post](https://www.beatoven.ai/blog/introducing-beatoven-ai-sdk/)

## Common Properties

- [Portal](https://www.beatoven.ai)
- [Documentation](https://www.beatoven.ai/api)
- [Documentation](https://github.com/Beatoven/public-api)
- [Getting Started](https://sync.beatoven.ai/apiDashboard)
- [Sign Up](https://sync.beatoven.ai/)
- [Sign Up](https://sync.beatoven.ai/apiDashboard)
- [GitHub Organization](https://github.com/Beatoven)
- [SDK](https://github.com/Beatoven/public-api/tree/main/sdk)
- [Code Examples](https://github.com/Beatoven/public-api/tree/main/examples)
- [Integration](https://apps.make.com/beatoven-ai)
- [Blog](https://www.beatoven.ai/blog)
- [Pricing](https://www.beatoven.ai/pricing)
- [Plans](plans/beatoven-plans-pricing.yml)
- [Rate Limits](rate-limits/beatoven-rate-limits.yml)
- [Fin Ops](finops/beatoven-finops.yml)
- [Artists](https://www.beatoven.ai/artists)
- [Terms of Service](https://www.beatoven.ai/tos)
- [Privacy Policy](https://www.beatoven.ai/privacy)
- [Support](mailto:hello@beatoven.ai)
- [LinkedIn](https://www.linkedin.com/company/beatoven-ai)
- [Twitter](https://twitter.com/beatoven_ai)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
**URL:** https://apievangelist.com
