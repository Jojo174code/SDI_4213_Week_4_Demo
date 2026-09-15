# SDI 4213 Week 4: Continuous Integration Demo Starter

This repository is designed for an instructor-led Week 4 demonstration of Continuous Integration with GitHub Actions.

## What is already included

- FastAPI inventory application
- Unit tests for application services
- API route tests
- `pytest` test configuration and reset fixture
- Pinned Python dependencies
- An inactive GitHub Actions workflow template in `demo-files/ci.yml`

The `.github/workflows/` folder intentionally does **not** contain an active CI workflow at the start. The instructor adds the workflow live during the demonstration.

## Local setup

Create a virtual environment:

```bash
python -m venv .venv
```

Activate on Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

Install dependencies:

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

Run the tests:

```bash
python -m pytest -v
```

Run the application:

```bash
python -m uvicorn app.main:app --reload
```

## Week 4 CI demonstration

The working workflow is located at:

```text
demo-files/ci.yml
```

During the demonstration, copy it to:

```text
.github/workflows/ci.yml
```

Commit the workflow on a feature branch and open a pull request to `main`. GitHub Actions should automatically install dependencies and run all tests.

See `docs/INSTRUCTOR_DEMO_QUICK_REFERENCE.md` for the demonstration sequence.
