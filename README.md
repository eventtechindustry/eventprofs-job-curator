eventprofs-job-curator-gpt/
├── README.md               # High‑level docs (mirrors this guide)
├── requirements.txt        # Pinned deps – see §3
├── .env.example            # API keys & secrets template
├── .gitignore
├── .gitlab-ci.yml          # CI pipeline – see §10
├── app/
│   ├── __init__.py
│   ├── config.py           # Pydantic‑based settings
│   ├── main.py             # Typer CLI entry‑point
│   ├── data_models.py      # `JobPosting`, `ResumeProfile`, etc.
│   ├── jobs/
│   │   ├── scrapers/
│   │   │   ├── base.py
│   │   │   ├── linkedin.py
│   │   │   ├── indeed.py
│   │   │   ├── google_jobs.py
│   │   │   └── ...
│   │   ├── cleaner.py
│   │   ├── matcher.py
│   │   └── publisher.py
│   ├── dashboards/
│   │   └── trends.py
│   └── utils/
│       ├── scheduler.py    # APScheduler / Celery beat
│       └── logging.py
├── tests/
│   └── …                   # pytest unit tests
└── docs/                   # Optional MkDocs site
