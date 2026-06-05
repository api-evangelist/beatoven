# Beatoven.ai (beatoven)

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
