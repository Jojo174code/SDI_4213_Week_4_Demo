# Week 4 Instructor Demo Files

These files support the live Continuous Integration demonstration.

- `ci.yml` — working GitHub Actions CI workflow. During the demonstration, copy this file to `.github/workflows/ci.yml`.
- `ci-broken-command.yml` — optional alternative failure example that points pytest to a file that does not exist.

Recommended live failure demonstration: after the working CI workflow passes, change the expected health response in `tests/test_api.py` from `"ok"` to `"healthy"`. Commit and push that change to show a failed CI check. Then restore `"ok"`, commit, and push again to show recovery.
