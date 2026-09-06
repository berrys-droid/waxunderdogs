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
| `art/*` | covers, wordmark, portrait, `record-label.png` |
| `art/occasions/*` | 15 photographic occasion tiles on `/` |
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


## Homepage redesign — 6 Sep 2026

Two changes to `index.html`, both additive:

1. **The record is the play button.** `.play-btn`, `.tplay` and `.album-play`
   all render as a vinyl disc — grooves in CSS, the Wax Underdogs badge as the
   centre label, a paper-coloured spindle hole. It spins while audio plays and
   stops when it pauses; the icon counter-rotates so it stays upright. Wiring
   is a single delegated script at the end of the file that patches
   `HTMLMediaElement.play/pause`, so it works for every player on the page
   without touching the existing playback code.
2. **Occasions are photographs, not emoji.** The eight emoji cards became 15
   photo tiles (`art/occasions/`), each with a gradient veil, a corner tag and
   white type over the image. Added: Mother's Day, Father's Day, graduation,
   missing someone, thank you, apology, I love you.

Backup of the previous homepage: `/tmp/index.backup.html` on the Mac (not in git;
the previous version is in the history as of commit `02dc9d5`).
