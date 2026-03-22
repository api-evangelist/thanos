# Thanos (thanos)
Open-source, highly available Prometheus setup with long-term storage capabilities that provides a global query view across multiple Prometheus servers.

**URL:** [Visit APIs.json URL](https://thanos.io/)

## Scope

- **Type:** Index 
- **Position:** Consuming 
- **Access:** 3rd-Party 

## Tags:

 - Monitoring, Observability, Prometheus, Time Series Database, Metrics

## Timestamps

- **Created:** 2025 
- **Modified:** 2026-03-18 

## APIs

### Thanos Query API
Prometheus-compatible HTTP API for querying metrics across multiple Prometheus servers and long-term storage backends with global query view, deduplication, and partial response support.

**Human URL:** [https://thanos.io/tip/components/query.md/](https://thanos.io/tip/components/query.md/)


#### Tags:

 - Monitoring, Metrics, PromQL, Query, Time Series

#### Properties

- [Documentation](https://thanos.io/tip/components/query.md/)
- [OpenAPI](openapi/thanos-query-api.yml)
- [JSONSchema](json-schema/query-response.json)
- [JSONSchema](json-schema/store-info.json)
- [JSONLD](json-ld/thanos-context.jsonld)

### Thanos Store Gateway API
gRPC-based Store API that serves metrics stored in object storage buckets, allowing Thanos Querier to access historical time series data from long-term storage backends such as S3, GCS, and Azure Blob Storage.

**Human URL:** [https://thanos.io/tip/components/store.md/](https://thanos.io/tip/components/store.md/)


#### Tags:

 - Monitoring, Metrics, Object Storage, Store, Time Series

#### Properties

- [Documentation](https://thanos.io/tip/components/store.md/)
- [OpenAPI](openapi/thanos-store-gateway-openapi.yml)

### Thanos Sidecar API
Component deployed alongside a Prometheus instance that implements the Thanos Store API on top of Prometheus remote-read API, enabling Queriers to access real-time Prometheus data and optionally uploading blocks to object storage.

**Human URL:** [https://thanos.io/tip/components/sidecar.md/](https://thanos.io/tip/components/sidecar.md/)


#### Tags:

 - Monitoring, Prometheus, Sidecar, Metrics, Store

#### Properties

- [Documentation](https://thanos.io/tip/components/sidecar.md/)
- [OpenAPI](openapi/thanos-sidecar-openapi.yml)

### Thanos Ruler API
Component that evaluates Prometheus recording and alerting rules against the Thanos Query API, exposes results as metrics via a Store API endpoint, and optionally uploads rule evaluation blocks to object storage.

**Human URL:** [https://thanos.io/tip/components/rule.md/](https://thanos.io/tip/components/rule.md/)


#### Tags:

 - Monitoring, Alerting, Rules, Prometheus, Metrics

#### Properties

- [Documentation](https://thanos.io/tip/components/rule.md/)
- [OpenAPI](openapi/thanos-ruler-openapi.yml)

### Thanos Receive API
Implements the Prometheus Remote Write API to accept metrics pushed from Prometheus instances, storing them in a local TSDB and optionally uploading blocks to object storage for long-term retention and horizontal scalability.

**Human URL:** [https://thanos.io/tip/components/receive.md/](https://thanos.io/tip/components/receive.md/)


#### Tags:

 - Monitoring, Remote Write, Metrics, Receive, Time Series

#### Properties

- [Documentation](https://thanos.io/tip/components/receive.md/)
- [OpenAPI](openapi/thanos-receive-openapi.yml)

### Thanos Compact API
Singleton process that applies Prometheus compaction procedures to block data stored in object storage, performing downsampling and retention policy enforcement to reduce storage costs and improve query performance over long time ranges.

**Human URL:** [https://thanos.io/tip/components/compact.md/](https://thanos.io/tip/components/compact.md/)


#### Tags:

 - Monitoring, Compaction, Object Storage, Downsampling, Retention

#### Properties

- [Documentation](https://thanos.io/tip/components/compact.md/)
- [OpenAPI](openapi/thanos-compact-openapi.yml)

## Common Properties

- [Website](https://thanos.io/)
- [JSON-LD](json-ld/thanos-context.jsonld)
- [JSONSchema](json-schema/query-response.json)
- [JSONSchema](json-schema/store-info.json)
- [Getting Started](https://thanos.io/tip/thanos/getting-started.md/)
- [Documentation](https://thanos.io/tip/)
- [GitHubRepository](https://github.com/thanos-io/thanos)
- [GitHub Organization](https://github.com/thanos-io)
- [Community](https://thanos.io/tip/contributing/community.md/)
- [Troubleshooting](https://thanos.io/tip/operating/troubleshooting.md/)
- [License](https://www.apache.org/licenses/LICENSE-2.0)

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
