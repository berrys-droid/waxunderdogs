# waxunderdogs.com

Static site. No build step — every page is a single self-contained HTML file
with its CSS, JS and images inline.

## Deployed

| File | URL |
|---|---|
| `index.html` | `/` — **the label**: positioning, disclosure standard, artist door, studio section |
| `studio.html` | `/studio` — the commission storefront, with the catalogue players |
| `intake.html` | `/intake` — the commission brief form |
| `press.html`  | `/press` — press kit |
| `audio/*.mp3` | seven tracks the `/studio` catalogue players load |

The label page leads as of 5 Sep 2026. The storefront it replaced at `/` is
unchanged apart from its intake link and a back-link to `/`.

`vercel.json` sets `cleanUrls`, so `/press` serves `press.html` without the
extension.

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
