# waxunderdogs.com

Static site. No build step — every page is a single self-contained HTML file
with its CSS, JS and images inline.

## Deployed

| File | URL |
|---|---|
| `index.html` | `/` — the storefront, live since 10 Aug 2026 |
| `intake.html` | `/intake` — the commission intake flow |
| `press.html`  | `/press` — press kit (added 4 Sep 2026) |

`vercel.json` sets `cleanUrls`, so `/press` serves `press.html` without the
extension.

## Not deployed

`drafts/home.html` — the proposed rewrite of the home page (label positioning,
disclosure standard, artist roster, studio). Excluded from deployment by
`.vercelignore`, so it is not reachable on the live site. Two placeholder links
inside it still need real targets: `/services` and `/intake`.

## History

The live pages had no repository. They were recovered on 5 Sep 2026 from
browser downloads in `~/Downloads` dated 10 Aug 2026, and committed as
`current/` and `proposed/` in commit `fad9e0f`. That commit is still the
archive — those folders were flattened to the root afterwards, so the originals
are recoverable with `git show fad9e0f:current/index.html`.

⚠️ The recovered pages are an August snapshot. If the live site was edited on
Vercel after 10 Aug, this repo is behind it — diff before overwriting.
