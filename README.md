# Research Methods in CEM — course website

Quarto site for the graduate seminar. The rendered site is the live syllabus; ETL links to it.

## One-time setup

```bash
# 1. install Quarto: https://quarto.org/docs/get-started/
# 2. create an empty GitHub repo named research-methods-cem (no README, no .gitignore), then:
git init
git add .
git commit -m "Initial course site"
git branch -M main
git remote add origin https://github.com/CBRyanAhn/research-methods-cem.git
git push -u origin main

# 3. first publish (creates the gh-pages branch and turns on Pages)
quarto publish gh-pages
```

The site then lives at <https://cbryanahn.github.io/research-methods-cem/> — already set as `site-url:` in `_quarto.yml`, so nothing to edit.

## Every time after that

```bash
quarto preview          # local check at localhost:4000
quarto publish gh-pages # build + push + deploy
```

Or let the GitHub Action in `.github/workflows/publish.yml` do it — push to `main` and it deploys.

## Structure

| File | Contents |
|---|---|
| `index.qmd` | Landing page |
| `calendar.qmd` | 15-week master calendar |
| `schedule.qmd` | Week-by-week readings and labs |
| `syllabus.qmd` | Outcomes, roles, assessment, rubrics |
| `methods.qmd` | Methodology inventory |
| `readings.qmd` | Core reference shelf |
| `handouts/` | Student handouts |
| `changelog.qmd` | Student-facing change log |
| `instructor/` | **Not rendered, not tracked.** Gitignored — lives only on your machine |
| `CLAUDE.md` | Editing conventions, read automatically by Claude Code |

## Working with Claude Code

Open this folder in Claude Code and describe the change in plain language. `CLAUDE.md` carries the conventions so you do not have to restate them.
