# Part 3 — TimescaleDB Review (Project Context)


TimescaleDB is a PostgreSQL extension designed for managing and querying timeseries data at scale. It introduces abstractions such as hypertables, continuous aggregates, and automated data lifecycle policies while preserving full SQL compatibility. Because my term project models time as a first class concept, TimescaleDB is a natural candidate for storing financial time series and temporally indexed events.


## Key Features

### 1. Hypertables for time-series partitioning
TimescaleDB uses hypertables to automatically partition data across time (and optionally space). This allows efficient ingestion and querying of large volumes of time-stamped data without manual sharding.

Stock prices, trading volume, and derived financial indicators for healthcare firms are naturally modeled as time-series. Hypertables allow these signals to scale cleanly as the number of companies and time horizons increase.


### 2. Continuous aggregates for incremental analytics
Continuous aggregates maintain materialized rollups that are refreshed automatically as new data arrives. Unlike traditional materialized views, they update incrementally rather than recomputing from scratch.

This is well suited for computing rolling returns, volatility measures, or event-aligned market responses like average price movement after FDA announcements.


### 3. Automated retention and compression policies
TimescaleDB supports automated retention and compression policies that manage historical data without manual intervention.

This allows the project to retain high-resolution recent data while compressing or discarding older data, which is realistic for financial analytics pipelines.


## Advantages for my Project

- A good fit for financial timeseries data, which is a core component of the project.
- SQL-based access making integration with Python analytics and feature extraction pipelines straightforward.
- Operational simplicity, since TimescaleDB remains fully compatible with PostgreSQL tooling.

## Disadvantages and Limitations for my project

- Not graph-native: TimescaleDB does not support multi-hop relationship traversal, which limits its usefulness for entity centric reasoning.
- Schema rigidity: Frequent evolution of entity and relationship types can be cumbersome compared to graph databases.
- No native semantic reasoning: Ontology-level inference must be handled externally.

## References
Timescale. 2026. “Timescale Documentation.” https://www.timescale.com  
