# GitHub Workflow Demo

A one-page website used to practice the GitHub workflow: **Issues → Forks → Pull Requests → CI/CD**.

## How to contribute

1. Find an open issue in the **Issues** tab.
2. **Fork** this repository.
3. Edit `index.html` in your fork and commit.
4. Open a **Pull Request** and write `Closes #<issue number>` in the description.
5. Wait for the automated check to pass ✅, then it can be merged.

## How it works

`.github/workflows/main.yml` runs one job:

- **CI:** on every pull request, it checks that `index.html` is not empty.
- **CD:** after a merge into `main`, it runs the "Deploy to Production" step (a simulated deploy).
