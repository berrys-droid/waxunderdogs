# waxunderdogs.com

Static site. No build step — every page is a single self-contained HTML file
with its CSS, JS and images inline.

## Deployed

| File | URL |
|---|---|
| `index.html` | `/` — the storefront, live since 10 Aug 2026 |
| `intake.html` | `/intake` — the commission intake flow |
| `audio/*.mp3` | seven tracks the catalogue players load |
| `press.html`  | `/press` — press kit (added 4 Sep 2026) |

`vercel.json` sets `cleanUrls`, so `/press` serves `press.html` without the
extension.

## Not deployed

`drafts/home.html` — the proposed rewrite of the home page (label positioning,
disclosure standard, artist roster, studio). Excluded from deployment by
`.vercelignore`, so it is not reachable on the live site. Two placeholder links
inside it still need real targets: `/services` and `/intake`.

## History

The live pages had no repository. On 5 Sep 2026 they were first recovered from
loose downloads dated 10 Aug 20:23 — **the wrong version**, whose catalogue
players synthesised chords with the Web Audio API instead of playing the mp3s.
Deploying it regressed the live site.

The correct source is `~/Downloads/waxunderdogs-site/` (11 Aug 00:38): real
`index.html`, the intake page, an `audio/` folder of seven mp3s, a `.vercel`
project link and a `deploy.sh`. That is what this repo now holds.

Vercel project: `waxunderdogs-site` (`prj_hdO49OTMiM97uJivNCfvXtQQi2bf`).
Previously deployed by `vercel deploy --prod` from that folder; now deployed
from this repo on push.
