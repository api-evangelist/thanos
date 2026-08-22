# Thanos (thanos)

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

Open-source, highly available Prometheus setup with long-term storage capabilities that provides a global query view across multiple Prometheus servers.

**APIs.json:** [https://thanos.io/](https://thanos.io/)

## Scope

- **Type:** Index

## Tags

- Metrics
- Monitoring
- Observability
- Prometheus
- Time Series Database

## Timestamps

- **Created:** 2025
- **Modified:** 2026-05-19

## APIs

### Thanos Query API

Prometheus-compatible HTTP API for querying metrics across multiple Prometheus servers and long-term storage backends with global query view, deduplication, and partial response support.

- **Human URL:** [https://thanos.io/tip/components/query.md/](https://thanos.io/tip/components/query.md/)
- **Base URL:** `http://localhost:9090`

#### Tags

- Metrics
- Monitoring
- PromQL
- Query
- Time Series

#### Properties

- [Documentation](https://thanos.io/tip/components/query.md/)
- [OpenAPI](openapi/thanos-query-api.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/thanos-query-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/thanos-query-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/query-response.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/store-info.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/thanos-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### Thanos Store Gateway API

gRPC-based Store API that serves metrics stored in object storage buckets, allowing Thanos Querier to access historical time series data from long-term storage backends such as S3, GCS, and Azure Blob Storage.

- **Human URL:** [https://thanos.io/tip/components/store.md/](https://thanos.io/tip/components/store.md/)
- **Base URL:** `http://localhost:10902`

#### Tags

- Metrics
- Monitoring
- Object Storage
- Store
- Time Series

#### Properties

- [Documentation](https://thanos.io/tip/components/store.md/)
- [OpenAPI](openapi/thanos-store-gateway-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/thanos-store-gateway.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/thanos-store-gateway.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Thanos Sidecar API

Component deployed alongside a Prometheus instance that implements the Thanos Store API on top of Prometheus remote-read API, enabling Queriers to access real-time Prometheus data and optionally uploading blocks to object storage.

- **Human URL:** [https://thanos.io/tip/components/sidecar.md/](https://thanos.io/tip/components/sidecar.md/)
- **Base URL:** `http://localhost:10902`

#### Tags

- Metrics
- Monitoring
- Prometheus
- Sidecar
- Store

#### Properties

- [Documentation](https://thanos.io/tip/components/sidecar.md/)
- [OpenAPI](openapi/thanos-sidecar-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/thanos-sidecar.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/thanos-sidecar.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Thanos Ruler API

Component that evaluates Prometheus recording and alerting rules against the Thanos Query API, exposes results as metrics via a Store API endpoint, and optionally uploads rule evaluation blocks to object storage.

- **Human URL:** [https://thanos.io/tip/components/rule.md/](https://thanos.io/tip/components/rule.md/)
- **Base URL:** `http://localhost:10902`

#### Tags

- Alerting
- Metrics
- Monitoring
- Prometheus
- Rules

#### Properties

- [Documentation](https://thanos.io/tip/components/rule.md/)
- [OpenAPI](openapi/thanos-ruler-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/thanos-ruler.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/thanos-ruler.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Thanos Receive API

Implements the Prometheus Remote Write API to accept metrics pushed from Prometheus instances, storing them in a local TSDB and optionally uploading blocks to object storage for long-term retention and horizontal scalability.

- **Human URL:** [https://thanos.io/tip/components/receive.md/](https://thanos.io/tip/components/receive.md/)
- **Base URL:** `http://localhost:10902`

#### Tags

- Metrics
- Monitoring
- Receive
- Remote Write
- Time Series

#### Properties

- [Documentation](https://thanos.io/tip/components/receive.md/)
- [OpenAPI](openapi/thanos-receive-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/thanos-receive.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/thanos-receive.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Thanos Compact API

Singleton process that applies Prometheus compaction procedures to block data stored in object storage, performing downsampling and retention policy enforcement to reduce storage costs and improve query performance over long time ranges.

- **Human URL:** [https://thanos.io/tip/components/compact.md/](https://thanos.io/tip/components/compact.md/)
- **Base URL:** `http://localhost:10902`

#### Tags

- Compaction
- Downsampling
- Monitoring
- Object Storage
- Retention

#### Properties

- [Documentation](https://thanos.io/tip/components/compact.md/)
- [OpenAPI](openapi/thanos-compact-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/thanos-compact.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/thanos-compact.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://thanos.io/)
- [JSON-LD](json-ld/thanos-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [JSON Schema](json-schema/query-response.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/store-info.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/thanos-query-structure.json)
- [Spectral Rules](rules/thanos-rules.yml)
- [Vocabulary](vocabulary/thanos-vocabulary.yml)
- [Getting Started](https://thanos.io/tip/thanos/getting-started.md/)
- [Documentation](https://thanos.io/tip/)
- [GitHub Repository](https://github.com/thanos-io/thanos)
- [GitHub Organization](https://github.com/thanos-io)
- [Community](https://thanos.io/tip/contributing/community.md/)
- [Troubleshooting](https://thanos.io/tip/operating/troubleshooting.md/)
- [License](https://www.apache.org/licenses/LICENSE-2.0)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
**URL:** http://apievangelist.com
