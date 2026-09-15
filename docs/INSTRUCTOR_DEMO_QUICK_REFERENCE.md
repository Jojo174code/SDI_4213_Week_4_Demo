# Week 4 CI Demonstration Quick Reference

## Starting state
- Automated tests already exist and pass locally.
- `.github/workflows/` contains only `.gitkeep`.
- The working CI workflow is stored in `demo-files/ci.yml` so it can be added live.

## Demonstration sequence
1. Run `python -m pytest -v` locally and confirm all tests pass.
2. Create or use a GitHub repository and push the starter code to `main`.
3. Create a branch: `git switch -c feature/add-ci`.
4. Copy `demo-files/ci.yml` to `.github/workflows/ci.yml`.
5. Explain `name`, `on`, `permissions`, `jobs`, `runs-on`, `steps`, `uses`, and `run`.
6. Commit and push the branch.
7. Open a pull request to `main` and watch the CI check run.
8. After it passes, merge the pull request.
9. Create a second branch: `git switch main && git pull && git switch -c demo/break-test`.
10. In `tests/test_api.py`, change the health assertion from `{"status": "ok"}` to `{"status": "healthy"}`.
11. Run `pytest` locally to show the failure.
12. Commit and push the broken test; open a pull request and show the red CI failure.
13. Open the GitHub Actions log and identify the failed test and assertion.
14. Restore `{"status": "ok"}`.
15. Run tests locally, commit, and push.
16. Refresh the pull request and show the CI check turn green.
17. Review and merge the pull request.

## Core message
Local testing catches problems before push. CI repeats those checks in a clean shared environment and makes the result visible to the entire team.
