# Customer Review Intelligence

Python FastAPI + Streamlit review intelligence service for e-commerce feedback.

Ingests buyer reviews over REST, scores sentiment with VADER, detects shipping/damage/quality/service pain points, and assigns triage priority for support dashboards.

## Stack

- **Backend:** Python 3.11+, FastAPI, Uvicorn, Pydantic
- **NLP:** VADER sentiment analysis
- **Storage:** SQLite (WAL mode)
- **Dashboard:** Streamlit

## Features

- Review ingest API with structured JSON responses
- Sentiment labels and compound scores
- Pain-point tagging across shipping, damage, quality, and service
- Priority triage: `URGENT` / `HIGH` / `NORMAL` / `LOW`
- Live operator dashboard with KPI charts

## Quick start

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
uvicorn main:app --reload --port 8000
```

In another terminal:

```bash
streamlit run app.py
```

API docs: http://localhost:8000/docs

## Author

Pooja Sharma — [Pooja101117](https://github.com/Pooja101117)
