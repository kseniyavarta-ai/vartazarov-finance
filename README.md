# 🐈 Flerken — Vartazarov family finance

Household budget, retirement plan and mortgage tracker.

- **Live app:** https://kseniyavarta-ai.github.io/vartazarov-finance/
- **Previews:** https://kseniyavarta-ai.github.io/vartazarov-finance/previews/<file-name>

## File naming

| File | What it is |
|---|---|
| `index.html` | **The live app.** Never renamed — GitHub Pages only serves this name. |
| `previews/index_YYYY-MM-DD_what-changed.html` | A version to test before it goes live, e.g. `previews/index_2026-10-21_mortgage-tab.html`. Lowercase, words joined with `-`. |
| `CHANGELOG.md` | One line per version: date, label, what changed. |

Every version shows its label on the PIN screen (e.g. `v2026.10.21 · mortgage-tab`), so you can always tell which one you are looking at.

## How a change goes live

1. New version is added as `previews/index_<date>_<what-changed>.html` and pushed.
2. Test it at its preview link (it is a separate copy, but it does use the shared Google Sheet).
3. When approved, the same file is copied over `index.html` and pushed. Live in ~1 minute.
4. A line is added to `CHANGELOG.md`.

Commit messages follow the same idea: `<area>: <what changed>`, e.g. `mortgage: add house fill tab`.

## Structure

```
index.html                     live app (single file)
previews/                      versions waiting for approval
CHANGELOG.md                   history of versions
.github/workflows/main.yml     deploys to GitHub Pages on every push to main
```
