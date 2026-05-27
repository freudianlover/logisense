# logisense
Logistics intelligence pipeline ingesting news and Reddit posts, scoring sentiment and extracting entities. Built for monitoring Asia supply chain signals.
# LogiSense — Supply Chain Intelligence Pipeline

I noticed that the logistics operations team manually scans logistics news and Reddit threads to anticipate disruptions on Asia routes. LogiSense automates this: it ingests articles from specialized logistics outlets and Reddit communities, deduplicates them,
extracts named entities (ports, carriers, commodities), scores sentiment using
a transformer model, and alerts on negative signals about regions we care
about (Hong Kong, Sichuan, mainland China, key transit hubs).

## Status

**v1 (in progress, target 2026-06-11)**: Ingest pipeline (RSS + Reddit → 
PostgreSQL via Airflow).

**v2 (target 2026-06-25)**: Sentiment scoring (cardiffnlp/twitter-roberta) 
and entity extraction (spaCy).

**v3 (target 2026-07-31)**: Retrieval-augmented Q&A layer (pgvector + 
LangChain + LLM) for natural-language queries over the ingested corpus.

## Architecture

(architecture diagram coming when v1 is shipped)

## Tech stack

- Python 3.11+
- PostgreSQL 16 (normalized schema, 3NF)
- Apache Airflow 2.10 (orchestration)
- Docker + docker-compose (local environment)
- Hugging Face Transformers (sentiment)
- spaCy (entity extraction)
- Telegram Bot API (alerting)

## Run locally

(coming when Docker setup is done)

## Author

Karol Masiak — Junior Data Engineer in training
