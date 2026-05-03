# Thanos

Open-source, highly available Prometheus setup with long-term storage capabilities that provides a global query view across multiple Prometheus servers. Thanos is a CNCF Incubating project.

**Website:** https://thanos.io/
**GitHub:** https://github.com/thanos-io/thanos

## APIs

### [Thanos Query API](https://thanos.io/tip/components/query.md/)
Prometheus-compatible HTTP query interface with global view, deduplication, and partial response support. Base URL: `http://localhost:9090`

**Tags:** Metrics, Monitoring, PromQL, Query, Time Series

**Properties:**
- [Documentation](https://thanos.io/tip/components/query.md/)
- [OpenAPI](openapi/thanos-query-api.yml)
- [JSON Schema](json-schema/query-response.json)
- [JSON Schema](json-schema/store-info.json)
- [JSON-LD](json-ld/thanos-context.jsonld)

### [Thanos Store Gateway API](https://thanos.io/tip/components/store.md/)
Serves historical TSDB blocks from object storage (S3, GCS, Azure Blob) to Thanos Querier. Base URL: `http://localhost:10902`

### [Thanos Sidecar API](https://thanos.io/tip/components/sidecar.md/)
Deployed alongside Prometheus. Implements Store API on Prometheus remote-read and uploads blocks to object storage.

### [Thanos Ruler API](https://thanos.io/tip/components/rule.md/)
Evaluates Prometheus alerting and recording rules against Thanos Query, fires alerts to Alertmanager.

### [Thanos Receive API](https://thanos.io/tip/components/receive.md/)
Accepts metrics via Prometheus Remote Write protocol, stores in local TSDB, uploads to object storage.

### [Thanos Compact API](https://thanos.io/tip/components/compact.md/)
Applies compaction, downsampling (5m, 1h), and retention policies to TSDB blocks in object storage.

## Artifacts

### OpenAPI Specifications

- [openapi/thanos-query-api.yml](openapi/thanos-query-api.yml) — Thanos Query HTTP API (PromQL, stores, alerts, rules)
- [openapi/thanos-store-gateway-openapi.yml](openapi/thanos-store-gateway-openapi.yml) — Store Gateway HTTP API
- [openapi/thanos-sidecar-openapi.yml](openapi/thanos-sidecar-openapi.yml) — Sidecar HTTP API
- [openapi/thanos-ruler-openapi.yml](openapi/thanos-ruler-openapi.yml) — Ruler HTTP API
- [openapi/thanos-receive-openapi.yml](openapi/thanos-receive-openapi.yml) — Receive HTTP API
- [openapi/thanos-compact-openapi.yml](openapi/thanos-compact-openapi.yml) — Compact HTTP API

### Spectral Rules

- [rules/thanos-rules.yml](rules/thanos-rules.yml) — Spectral ruleset enforcing Thanos API conventions

### Naftiko Capabilities

**Shared Definitions:**
- [capabilities/shared/thanos-query.yaml](capabilities/shared/thanos-query.yaml) — Thanos Query API consumed definition

**Workflow Capabilities:**
- [capabilities/metrics-observability.yaml](capabilities/metrics-observability.yaml) — Unified metrics observability for SRE (7 MCP tools, REST on :8080)

### JSON Schema

- [json-schema/query-response.json](json-schema/query-response.json) — Thanos/Prometheus query response envelope
- [json-schema/store-info.json](json-schema/store-info.json) — Thanos store endpoint info schema

### JSON Structure

- [json-structure/thanos-query-structure.json](json-structure/thanos-query-structure.json) — Thanos API data structure documentation

### JSON-LD Context

- [json-ld/thanos-context.jsonld](json-ld/thanos-context.jsonld) — Linked data context for Thanos vocabulary

### Vocabulary

- [vocabulary/thanos-vocabulary.yml](vocabulary/thanos-vocabulary.yml) — Thanos domain vocabulary (16 terms covering components, query semantics, storage)

### Examples

- [examples/thanos-query-instant-query-example.json](examples/thanos-query-instant-query-example.json)
- [examples/thanos-query-range-query-example.json](examples/thanos-query-range-query-example.json)
- [examples/thanos-query-get-stores-example.json](examples/thanos-query-get-stores-example.json)

## Common Properties

- [Website](https://thanos.io/)
- [Documentation](https://thanos.io/tip/)
- [Getting Started](https://thanos.io/tip/thanos/getting-started.md/)
- [GitHub Repository](https://github.com/thanos-io/thanos)
- [GitHub Organization](https://github.com/thanos-io)
- [Community](https://thanos.io/tip/contributing/community.md/)
- [Troubleshooting](https://thanos.io/tip/operating/troubleshooting.md/)
- [License](https://www.apache.org/licenses/LICENSE-2.0)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
