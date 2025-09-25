# Plasma Engine Brand

## Overview

**Plasma Engine Brand** is the brand monitoring and reputation management service. It provides:

- 📊 **Multi-Source Monitoring**: Social media, news, forums, reviews
- 📈 **Sentiment Analysis**: Real-time brand perception tracking
- 🔔 **Alert System**: Configurable triggers for brand mentions
- 📱 **Platform Integration**: X/Twitter, LinkedIn, Reddit, Google
- 📉 **Trend Detection**: Emerging topics and viral content
- 📋 **Reporting**: Automated dashboards and insights

## Tech Stack

- **Language**: Python 3.11
- **Framework**: FastAPI
- **Data Pipeline**: Apache Beam / Prefect
- **Stream Processing**: Kafka / Redis Streams
- **ML/NLP**: Transformers, spaCy
- **Database**: PostgreSQL + TimescaleDB
- **Cache**: Redis
- **Search**: Elasticsearch

## Quick Start

```bash
# Install dependencies
pip install -r requirements.txt

# Set up environment
cp .env.example .env

# Run migrations
alembic upgrade head

# Start development server
uvicorn app.main:app --reload

# Run tests
pytest

# Start data collectors
python -m app.collectors.start
```

## Architecture

```
Data Sources → Collectors → Stream Processing → Analysis → Storage
      ↓            ↓              ↓                ↓          ↓
   APIs/RSS    Rate Limit    Sentiment/NER    Insights   Dashboard
```

## Key Features

- **Real-time Processing**: Sub-minute latency for critical mentions
- **Historical Analysis**: Trend comparison and pattern recognition
- **Competitor Tracking**: Side-by-side brand comparison
- **Crisis Detection**: Anomaly detection for reputation threats
- **Custom Metrics**: Configurable KPIs and scoring

## Integrations

- **Social**: X/Twitter API, LinkedIn API, Reddit API
- **News**: NewsAPI, Google News RSS
- **Reviews**: Google My Business, Trustpilot
- **Forums**: Discord webhooks, Slack monitoring

## Development

See [Development Handbook](../plasma-engine-shared/docs/development-handbook.md) for guidelines.

## CI/CD

This repository uses GitHub Actions for CI/CD. All PRs are automatically:
- Linted and tested
- Security scanned
- Reviewed by CodeRabbit

See `.github/workflows/ci.yml` for details.