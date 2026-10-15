# Loopwork: case study

*Self-initiated concept. No client, no users, no shipped product, and no metrics. The people, pieces' practice data and numbers in the screens are fictional sample content; the pieces named are public-domain works.*

## Problem
Intermediate pianists tend to practise by playing a piece from the top. The easy 80% gets repeated and the few hard bars (the ones that actually cause stumbles) get a fraction of the time. Existing tools are either metronomes (no memory of where you struggle) or score players (built for listening, not drilling).

## User
An adult hobbyist or advanced student practising 30-40 minutes a day at an upright or digital piano, phone on the music desk, hands busy. They want to feel progress and are quietly frustrated that the same bars keep failing.

## Key decisions
1. **One numeral per practice screen.** Tempo is the thing the player is climbing, so it is the largest element (236px condensed) and readable from a piano bench. Everything else supports it.
2. **A "ladder" instead of a free tempo dial.** Tempo rises a fixed step only after N consecutive clean reps, and drops back after two slips. This removes the decision of "when am I ready?" and makes progress honest. Rules are editable per passage (screen 5).
3. **Self-rating with two big buttons.** Clean / Slipped, 68pt tall at thumb reach, with S / C / Space on desktop. Audio detection is used to suggest bars on a first run-through, but the player stays in charge of the verdict.
4. **Heat, not red/green.** Difficulty is a warm ramp (dark to amber to orange); mint is reserved for earned things. Slips are shown as data, and the slip animation avoids a failure flash.
5. **A skyline as the signature graphic.** A bar-by-bar silhouette of slips appears in onboarding, the library, the empty state and the desktop studio, so the product's whole idea (a few tall bars) is readable at a glance.
6. **Deliberate contrast with warm-paper/serif work.** Near-black canvas, condensed uppercase display type, and a single saturated accent, to suit a dim practice room and to feel more like an instrument panel than a dashboard.
7. **Empty state with a real obstacle.** The first-run library combines "nothing flagged yet" with a microphone-permission notice and a sample piece, so there is always a next action.

## System
- **Colour:** Ink 0-3 surfaces, Bone text (3 steps), Signal #FF5B21, Amber, Mint, and a 5-step heat ramp. Text pairs were computed against WCAG 2: body 17.2:1, secondary 9.6:1, labels 5.5:1 on cards, accent text 6.4:1, and dark text on heat cells at least 6.1:1. (Bone 3 is not used on Ink 3, where it falls to 4.4:1.)
- **Type:** Bahnschrift condensed (width axis 75) for display, Bahnschrift regular for text, Consolas for data and labels. Scale: 236 / 82 / 40 / 16-20 / 16 / 11.
- **Spacing and shape:** 4pt grid (4-48), radii 10 / 16 / 24 / pill, 20px mobile gutters.
- **Components:** primary/bone/ghost buttons, chips, segmented control, toggle, stepper, bar cell (upcoming / done / now / hard), rep pips, skyline, ladder rail, heat grid.
- **Motion:** loop fill is linear and tempo-locked; rung climb rolls the numeral 280ms with a single pulse; slips nudge a cell 2px twice; reduced motion falls back to cross-fades; haptics differ for clean, climb and drop-back. These are notes only; nothing is prototyped.

## What I would test next
- Does the ladder (3 clean reps to climb, drop back 8 after 2 slips) feel motivating or punishing? Try 2 vs 3 vs 5 reps with a handful of players.
- Can players self-rate reliably, or do they need audio confirmation? Compare self-rating with suggested ratings.
- Is the skyline understood without explanation by first-time users?
- Does the 236px numeral and 68pt button layout hold up at arm's length on a music desk, in dim light?
- Whether desktop is wanted at all for a practice session, or only for weekly review.

## Known limits
Static screens only, one piece of sample data, no accessibility audit beyond contrast, and no real audio detection behind the "run-through" idea.
