# AI Tools Mastery — One Product, One Story

Landing pages for BlockseBlock's 4-week live AI cohort for non-coders.

## Pages

| File | What it is |
| --- | --- |
| `docs/index.html` | Responsive / desktop-first landing page (1280px canvas, folds to mobile below 920px) |
| `docs/mobile.html` | Original mobile-first landing page (480px column) |

Both are **single self-contained HTML files** — no build step, no dependencies to install. Open them directly in a browser, or serve the `docs/` folder.

## Publish with GitHub Pages

Already enabled: Settings → Pages → Source *Deploy from a branch*, branch `main`, folder `/docs`.
The desktop page is served at the root URL; the mobile version at `/mobile.html`.

Pages only serves from `/` or `/docs` on a branch — hence `docs/` rather than `site/`.

`.nojekyll` is included so Pages serves the files as-is.

## Editing

The pages are built from Design Component sources in the design project:

- `AI Tools Mastery Landing Desktop.dc.html` → `docs/index.html`
- `AI Tools Mastery Landing.dc.html` → `docs/mobile.html`

Edit the source, re-bundle, and commit the regenerated files in `docs/`. Editing the bundled HTML by hand is possible but will be overwritten on the next export.

## Before going live

- Replace the price placeholder `₹[X,XXX]` in the Offer section.
- Point the "Book my free seat" links at the real registration URL (currently anchors to `#offer`).
- Confirm the cohort dates in the header ("Cohort 01 · Aug").

## Stack

Plain HTML with inline styles, anime.js 3.2.1 for motion, Google Fonts (Bricolage Grotesque + Inter). CSS 3D instead of WebGL for the hero, so it stays smooth on mid-range Android. `prefers-reduced-motion` is respected — animation collapses to a static, fully readable page.
