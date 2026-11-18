# AI: Your Move

A facilitated discussion game for business leaders, adapted from the supplied AI: Your Move presentation. The original seven dilemmas and A/B/C choices are retained. New fictional pressure events and commitment prompts add interaction. This is a static game with no AI service or backend.

## Play

Open `dist/index.html` in a modern browser, or open the separately supplied single-file `AI-Your-Move.html`. For reliable browser storage, serve over HTTP. For example, from this folder run `python3 -m http.server 8000 --directory dist`, then open http://localhost:8000.

Use one shared device for a team of 3–6. Players pass the device to vote privately, then reveal the vote counts together. This version does not synchronize separate devices or maintain a cross-team leaderboard.

## 38-minute run of show

- Briefing and team setup: 2 minutes.
- Seven rounds: 4 minutes each (28 total).
- Select three priorities and complete commitments: 6 minutes.
- Closing pitch: 2 minutes.

The clock starts after setup; the briefing allocation therefore provides a small practical buffer. Timers are advisory, can pause, and never auto-submit or discard work. Difficulty changes discussion pressure, not the time allowance. Real workshop pacing should be piloted.

Within each round: 45 seconds for reading and voting, 75 seconds for the reveal and debate, 60 seconds for the constraint/challenge, and 60 seconds to commit. Standard mode can spend the constraint time examining its decision challenge.

## Difficulty

- Standard: original dilemma and a concrete leadership challenge.
- Stretch: one additional constraint.
- Boardroom: a second pressure event plus a required mitigation.

No universal correct answers or artificial business performance scores. Progress counts recorded decisions. PROTECT explicitly requires attention to all three review areas. Facilitators should ask for evidence, assumptions and trade-offs.

## Outputs and storage

Each decision captures direction, action/reason, accountable owner, and evidence/review. Three selected priorities add a first step, day-90 evidence and review date. Export produces a plain-text report. A report can be exported during an unfinished session.

Submitted decisions and final-priority fields persist in localStorage when available. Unsubmitted round forms and private votes do not survive navigation or refresh. Use Export before leaving a shared device, then Reset in the facilitator guide to clear the saved session. Google Fonts is the only external runtime request; system fonts provide a fallback without connectivity. There is no analytics or server-side participant-data collection.

## Publish later to GitHub Pages

Source and a GitHub Actions deployment workflow are ready. Nothing is published by this package.

1. Choose/create the public repository and upload this folder's contents, including `.github/workflows/pages.yml`, to its `main` branch. Do not upload participant reports or the source presentation.
2. In repository Settings > Pages, select GitHub Actions as the build/deployment source.
3. Run the Publish game to GitHub Pages workflow, or push to main.
4. Use the Pages URL reported by the deployment.

No installation or build is required. Relative asset paths support a repository subpath. If the repository uses another default branch, adjust the workflow's branch setting.

## Editing

- `dist/rounds.js`: dilemmas, options, pressure events and challenges.
- `dist/app.js`: game flow and browser storage.
- `dist/style.css`: typography, colours and responsive layout.
- `dist/index.html`: shell and facilitator guide.

The standalone HTML is a convenience snapshot. After editing source, regenerate it by inlining the stylesheet and the two JavaScript files in their existing order.

## Validation

JavaScript syntax checked. Browser walkthrough completed for all seven rounds in Boardroom mode with three players, including concealed votes, vote counts, final unlock, the three-priority limit, required commitment fields, report download, storage reload and reset. Board checked at 390px and desktop widths. Standard/Stretch and every 4–6-player combination have not received separate full walkthroughs. Workshop duration remains a facilitation estimate.
