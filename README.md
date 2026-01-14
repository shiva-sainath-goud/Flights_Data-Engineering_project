# fliets-data_project

A flight data pipeline using medallion architecture (Bronze → Silver → Gold) with Airflow DAGs, scripts, and sample data.

## Quick start ✅

Prerequisites:
- Git
- Python 3.10+ (or your environment used for the project)
- Docker & Docker Compose (optional, if you use the included `docker-compose.yml`)

Local setup:
```bash
python -m venv .venv
.\.venv\Scripts\activate      # Windows
pip install -r requirements.txt
```

Run with Docker Compose (if desired):
```bash
docker-compose up -d
# then open Airflow UI at http://localhost:8080
```

Project layout:
- `dags/` — Airflow DAG definitions
- `scripts/` — pipeline scripts (bronze ingest, silver transform, gold aggregate)
- `data/` — sample data (DO NOT COMMIT large/production data)
- `docs/` — helpful documentation and setup notes

NOTE: Large data files should not be committed (see `.gitignore`).

## Publishing to GitHub 🔧

Commands to initialize and push the repo (run locally):
```bash
# initialize
git init
git add .
git commit -m "chore: initial commit"
# create remote (option A: GitHub CLI)
# gh repo create <YOUR_USERNAME>/fliets-data_project --public --source=. --remote=origin --push
# option B: manual (create repo on GitHub, then):
# git remote add origin git@github.com:<YOUR_USERNAME>/fliets-data_project.git
# git branch -M main
# git push -u origin main
```

If you'd like, I can run these commands for you (I will need you to authenticate `gh` or allow me to run git locally).

## License & Contributing
See `LICENSE` for license information. If you'd like a different license than MIT, let me know and I'll update it.

## Next steps I can help with 💡
- Create the GitHub repo and push it for you (public/private) using `gh` CLI
- Add a basic GitHub Actions CI workflow (lint & tests)
- Add badges to `README.md` (CI, license, coverage)

---

Happy to proceed — tell me whether you want the repo public or private and which license to use (MIT by default).