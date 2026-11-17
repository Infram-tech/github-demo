# GitHub Workflow Demo

A one-page website used to practice the GitHub workflow: **Issues → Forks → Pull Requests → CI/CD**.

🌐 Live site: https://infram-tech.github.io/github-demo/

## How to contribute

1. Find an open issue in the **Issues** tab.
2. **Fork** this repository.
3. Edit `index.html` in your fork and commit.
4. Open a **Pull Request** and write `Closes #<issue number>` in the description.
5. Wait for the automated check to pass ✅. Once it's merged, the site updates automatically.

## How it works

`.github/workflows/main.yml` runs two jobs:

- **test** (CI) runs on every pull request and makes sure `index.html` isn't empty and still has a heading.
- **deploy** (CD) runs after a merge into `main` and publishes the site to GitHub Pages.
