# Plasma Engine Brand

Data collectors, analytics, and reporting pipelines for Plasma Engine brand monitoring.

## Components

- Ingestion: Tavily, EXA, social APIs (Twitter/X, Reddit, YouTube, TikTok)
- Storage: Postgres, SQLite, S3-compatible object storage
- Analytics: Sentiment, topics, share-of-voice, trend detection
- Reporting: Jinja templates for executive summaries and quarterly reports

## CI

Uses shared workflows for lint/test and security scanning ([ci.yml](.github/workflows/ci.yml)). CodeRabbit is configured as an automatic reviewer.

## Local Setup

```bash
git clone https://github.com/xkonjin/plasma-engine-brand.git
cd plasma-engine-brand

python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt  # placeholder until scaffolding added
```

Ensure the shared Compose stack is running for Redis/Postgres support (see development handbook).

## Contribution Checklist

- [ ] Issue opened and linked to Program board (PE-XX)
- [ ] Test coverage updated for collectors/analytics modules
- [ ] Report templates validated before merge
- [ ] Docs updated (README/reporting guide)

Refer to the [Development Handbook](../plasma-engine-shared/docs/development-handbook.md) for detailed environment steps.
