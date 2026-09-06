# waxunderdogs.com

Static site. No build step — every page is a single self-contained HTML file
with its CSS, JS and images inline.

## Deployed

| File | URL |
|---|---|
| `index.html` | `/` — the commission storefront (live, unchanged) |
| `label.html` | `/label` — the label home page, rebuilt 6 Sep in the storefront's own design system |
| `intake.html` | `/intake` — the commission brief form |
| `press.html`  | `/press` — press kit |
| `art/*` | covers, wordmark, portrait |
| `audio/*.mp3` | 7 commission examples for `/studio`, plus `hold.mp3` for the label page |

### The label page

Rebuilt 6 Sep 2026 after an advisory board rejected the first attempt. That
version was typographic — no art, no audio, a different palette — and the
Listener seat put it best: *"a record store where all the sleeves are empty."*

The rebuild uses the storefront's own tokens (Fraunces + Space Grotesk, paper
`#faf7f2`, amber `#d98a2b`, plum `#3a2a3f`), leads with a working player for
Hold, and shows the four singles with real cover art. Disclosure moved from a
boxed rules list at the top to a credit line under each release — demonstrated
per record rather than declared up front.

Unreleased singles carry a date and no audio. Anam's credits read "final at
release" while its vocal provenance is unresolved.

**To make the label the home page:** `git mv index.html studio.html && git mv
label.html index.html`, then fix the two internal links (`/label` → `/studio`
in the label page; the storefront's `/intake` stays).

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
