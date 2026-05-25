# Beatoven.ai (beatoven)

Beatoven.ai is an Indian generative-music startup (Bengaluru, founded 2021)
building text-to-music and text-to-sound-effects models for video creators,
podcasters, game developers, and brands. Its Maestro Music and Maestro SFX
models render royalty-free background tracks and foley from natural-language
prompts, with downloads delivered as mp3, aac, or wav plus separately rendered
stems (bass, chords, melody, percussion). Beatoven is Fairly Trained certified.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/beatoven/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - AI, Artificial Intelligence, Music, Music Generation, Generative Audio, Text To Music, Text To SFX, Royalty-Free Music, Background Music, Video Creators, Podcasts, Stems, Fairly Trained, India

## Timestamps

- **Created:** 2026-05-24
- **Modified:** 2026-05-24

## APIs

### Beatoven Composition API

Asynchronous REST API for composing tracks from natural-language prompts.
`POST /api/v1/tracks/compose` returns a `task_id`; poll `GET /api/v1/tasks/{task_id}`
until status is `composed`. The completed response returns a master `track_url`
plus a `stems_url` object with bass, chords, melody, and percussion URLs.
Supports `mp3`, `aac`, and `wav` output and an optional `looping` flag.
Bearer-token auth.

**Base URL:** `https://public-api.beatoven.ai`

**Human URL:** [https://github.com/Beatoven/public-api/blob/main/docs/api-spec.md](https://github.com/Beatoven/public-api/blob/main/docs/api-spec.md)

- [Documentation - API Spec](https://github.com/Beatoven/public-api/blob/main/docs/api-spec.md)
- [Documentation - API product page](https://www.beatoven.ai/api)
- [OpenAPI](openapi/beatoven-composition-api-openapi.yml)
- [JSON Schema - Track](json-schema/beatoven-track-schema.json)
- [JSON Schema - Compose Request](json-schema/beatoven-compose-request-schema.json)
- [JSON-LD](json-ld/beatoven-context.jsonld)
- [Spectral Rules](rules/beatoven-composition-rules.yml)
- [Example - Compose Request](examples/beatoven-compose-request-example.json)
- [Example - Compose Response](examples/beatoven-compose-response-example.json)
- [Example - Task Status Response](examples/beatoven-task-status-response-example.json)
- [Naftiko Capability - Tracks (Compose)](capabilities/tracks-compose.yaml)
- [Naftiko Capability - Tasks (Status)](capabilities/tasks-status.yaml)
- [GitHub - public-api](https://github.com/Beatoven/public-api)
- [Python SDK](https://github.com/Beatoven/public-api/tree/main/sdk)
- [Python compose example](https://github.com/Beatoven/public-api/blob/main/examples/compose.py)
- [Make.com integration](https://apps.make.com/beatoven-ai)

## Endpoints

| Verb | Path | Operation |
|---|---|---|
| POST | /api/v1/tracks/compose | Compose A Track From A Prompt |
| GET | /api/v1/tasks/{task_id} | Get Composition Task Status |

## Plans, Rate Limits, and FinOps

- [Plans and Pricing](plans/beatoven-plans-pricing.yml) - Trial, Creator ($10/mo), Visionary ($20/mo), Pay-as-You-Go ($3/minute), and Public API (contract).
- [Rate Limits](rate-limits/beatoven-rate-limits.yml) - Per-customer quotas issued at API key provisioning. The public API spec does not document a 429 throttling response; clients must poll task status rather than retry compose.
- [FinOps](finops/beatoven-finops.yml) - FOCUS-aligned cost model. Two billing surfaces: per-seat subscription + downloaded-minutes (web product), and contract-priced enterprise (API).

## Authentication

HTTP `Authorization: Bearer <BEATOVEN_API_KEY>` on every request. Keys are
issued via the [API dashboard](https://sync.beatoven.ai/apiDashboard) or by
emailing `hello@beatoven.ai`.

```bash
curl -X POST https://public-api.beatoven.ai/api/v1/tracks/compose \
  -H "Authorization: Bearer ${BEATOVEN_API_KEY}" \
  -H "Content-Type: application/json" \
  -d '{"prompt":{"text":"30 seconds peaceful lo-fi chill hop track"},"format":"wav","looping":false}'
```

The response contains a `task_id`; poll until `composed`:

```bash
curl -H "Authorization: Bearer ${BEATOVEN_API_KEY}" \
  https://public-api.beatoven.ai/api/v1/tasks/${TASK_ID}
```

## SDKs and Integrations

- [Python SDK](https://github.com/Beatoven/public-api/tree/main/sdk) - async/await client, install via `pip install -e "git+https://github.com/Beatoven/public-api.git/#subdirectory=sdk"`.
- [Make.com](https://apps.make.com/beatoven-ai) - Create and Compose Track, Composition Status, and generic API Call modules.

## Maintainers

- Kin Lane - kin@apievangelist.com - [apievangelist.com](https://apievangelist.com)
