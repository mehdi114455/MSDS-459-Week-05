# Part 2 - Graph Database Review: Memgraph


Memgraph is an open source graph database built around the property graph model and queried using Cypher. It is commonly positioned for real-time / streaming graph analytics, where fast updates and fast traversals matter. Memgraph highlights integration with streaming systems and running algorithms (via its ecosystem) over graph data. (Memgraph 2026a; Memgraph 2026b; memgraph/memgraph 2026)


### 1) Property graph model + Cypher query language
Memgraph supports the property graph paradigm (nodes + relationships, both with properties) and uses Cypher, which is widely used across graph platforms. This lowers adoption friction for anyone already familiar with Cypher based querying. (memgraph/memgraph 2026)

### 2) Streaming ingestion (Kafka/Redpanda/Pulsar)
Memgraph documents direct connectivity to streaming infrastructure so that new events can be ingested continuously and immediately become queryable as a graph. This supports “graph as a live model” use cases (fraud, network monitoring, real-time recommendations). (Memgraph 2026a; Memgraph 2026b)

### 3) “Real-time” performance orientation (in memory first design emphasis)
Memgraph is frequently described as optimized for speed and real time graph workloads, often emphasizing an in memory first approach with durability mechanisms. This makes it attractive when you need fast traversals and updates rather than purely archival storage. (memgraph/memgraph 2026)

### 4) Integrations and tooling (ecosystem)
Memgraph provides tooling and documentation around operational workflows (management UI, connectors, and an ecosystem around algorithms/procedures). The practical benefit is reducing “glue code” for common pipelines. (Memgraph 2026a)


## References
Memgraph. 2026a. “Streams.” Memgraph Documentation. https://memgraph.com/docs/data-streams

Memgraph. 2026b. “Streams (Memgraph Lab).” Memgraph Documentation. https://memgraph.com/docs/memgraph-lab/features/streams

memgraph/memgraph. 2026. “Memgraph: Open-source Graph Database.” GitHub. https://github.com/memgraph/memgraph
