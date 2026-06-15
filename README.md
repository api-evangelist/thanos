# Thanos (thanos)

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
