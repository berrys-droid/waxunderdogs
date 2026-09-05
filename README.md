# waxunderdogs.com

## current/
The site as it is live today, recovered from ~/Downloads (saved 2026-08-10).
- index.html  <- was waxunderdogs-index_2.html (the newest of three)
- intake.html <- was waxunderdogs-intake_3.html (the newest of four)
The internal link was rewritten from "waxunderdogs-intake.html" to "intake.html".
These are single-file pages: all CSS, JS and images are inline. No build step.

## proposed/
The rewrite drafted 2026-09-04 - label positioning, the disclosure standard,
the artist roster door, the studio, and a press kit page.
- index.html
- press.html
Placeholder links to fill in: /services and /intake.

Nothing here has been deployed. Deploy is manual.

## Where this came from
The live pages were recovered from ~/Downloads, where they had been saved as
browser downloads on 2026-08-10 - there was no project folder and no git repo.
Originals remain in ~/Downloads untouched.

## Suggested next step
    cd ~/waxunderdogs && git init && git add -A && git commit -m "Recover live site; add proposed rewrite"
Then connect it to the Vercel project so the next deploy has a history.
