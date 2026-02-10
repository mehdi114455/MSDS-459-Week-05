# Part 4 - ParadeDB Review (Project Context)


ParadeDB is a PostgreSQL extension that provides full text and relevance ranked search capabilities using BM25 style scoring. It is designed to bring search engine like behavior directly into Postgres without requiring an external system.

Given that my project relies heavily on news articles, regulatory announcements, and textual disclosures, ParadeDB is relevant as a document retrieval and exploration layer.


## Key Features

### 1. BM25 relevance scoring
ParadeDB implements BM25 ranking, which improves relevance compared to basic PostgreSQL full-text search.

This is valuable for retrieving the most relevant healthcare news articles or regulatory announcements associated with a company or event.

### 2. Postgres-native search integration
Search indexes are managed inside PostgreSQL, avoiding the need for Elasticsearch or OpenSearch.

This simplifies deployment for a course project and allows structured entity metadata and unstructured text to coexist in a single database.

### 3. Support for fuzzy search and highlighting
ParadeDB supports fuzzy matching and highlighting, which improves usability for exploratory analysis.

Healthcare firm names, drug names, and regulatory terms often vary slightly across documents. Fuzzy search helps mitigate this inconsistency.



## Advantages for my Project

- Strong document retrieval layer for news and regulatory text.
- Low operational overhead, making it suitable for a class project.
- Pairs well with structured metadata, such as company IDs and timestamps.

## Disadvantages and Limitations for my project

- Not a knowledge graph store: ParadeDB does not represent relationships explicitly.
- No semantic similarity: It relies on lexical matching rather than embeddings.
- Best suited as a supporting component, not the core KB.

##

ParadeDB is well suited as a textual access layer that supports discovery and filtering of documents prior to entity and relation extraction. In my project, it would complement the knowledge graph rather than replace it.


## References
ParadeDB. 2023. “Introducing pg_search.” https://www.paradedb.com  
