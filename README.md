# GitHub Workflow Demo

A one-page website for practicing the GitHub workflow: **Issue → Branch → Pull Request → CI → Merge → CD**.

## The workflow

### 1. Issue: describe the problem
**Issues → New issue**, e.g. `Typo on homepage`. GitHub gives it a number, e.g. **#1**.

### 2. Branch: a safe place to work
**Code** tab → branch dropdown (`main`) → type `fix-typo` → **Create branch**.
`main` stays untouched while you work.

### 3. Pull Request: propose the change
On `fix-typo`, edit `index.html` and **Commit changes**.
Click **Compare & pull request** and write `Closes #1` in the description.

### 4. CI: the automatic check
GitHub Actions runs on the pull request and tests the result of merging it into `main`:
- ✅ **Check that index.html is not empty**
- ⏭️ **Deploy to Production** is skipped, because nothing deploys from a pull request.

If the check fails (❌), the change shouldn't be merged.

### 5. Merge and CD: ship it
Click **Merge pull request**. Issue #1 closes automatically.
A new run starts on `main`, and this time **Deploy to Production** runs.

## The workflow file

`.github/workflows/main.yml`:

| Trigger | What runs |
|---|---|
| `pull_request` | CI: check that `index.html` is not empty |
| `push` to `main` (a merge) | CI + CD: the check, then a simulated deploy |
