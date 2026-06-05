# Day of the Tentacle Theatre Hub

A community hub for all things Day of the Tentacle — written in Markdown, published as a clean static site.

**Workflow:** edit `contents.md` → run `python build.py` → preview with `serve.bat` or open `index.html`.

## Repository layout

| Path | Purpose |
|------|---------|
| `contents.md` | Source of truth — edit this |
| `build.py` | Builds HTML from Markdown |
| `index.html` | Generated site (commit for GitHub Pages) |
| `assets/site.css` | Page styling |
| `serve.bat` | Build + local preview at http://localhost:8000/ |

## Build locally

Requires Python 3:

```powershell
pip install -r requirements.txt
python build.py
```

Double-click **`serve.bat`** to rebuild and open the site in your browser.

After editing Markdown, bump `version` and `date` in the YAML front matter when you want, run `python build.py`, then commit both the `.md` source and generated `index.html`.

## GitHub Pages

Push the repo with generated HTML at the root. No CI build step — regenerate locally before pushing.

Relative links work for a **project site** (`selloa.github.io/<repo-name>/`).

## Adding content

Edit `contents.md`:

- Top-level sections use `#` (Collections, Art, Technical, …)
- Subsections use `##` or `###`
- For links, put a title on one line and the URL on the next — the build script turns them into links automatically
- A title and description can be combined on one line (`Title - description`) before the URL
- `## Page build notes` at the bottom is author-only and stripped from the published page

## Status

Initial scaffold (v0.1.0). Grow incrementally.
