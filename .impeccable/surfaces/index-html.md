---
version: 1
slug: "index-html"
primary_target: "index.html"
related_targets: []
---

# Surface brief: game screen (index.html)

Scope: the whole game surface (home launcher, game screen, hand-off, result, help). Mode: Experience with Operate rules for the controls (a game people play, not a page they read).
Audience and task: NBA fans playing a short deduction game vs the CPU or pass-and-play. Task per turn: ask one question, flip down who does not fit, end turn or guess.
Constraints: keep all game behaviour, roster, questions, headshots and credits. Team colour only on player cards. Add: rules on the launcher and in-game help, guess-loses warning, labelled counts, phone layout with the board reachable and the dock not covering cards, game saved across refresh.
Memorable moment: the CPU's turn read like a live broadcast graphic.

## Direction contract

THESIS: The game is a TV broadcast of a one-on-one matchup. Refuses the floating-card dashboard and the luxury landing-page shell; the screen is a graphics package over the arena.

OWN-WORLD: Saturated network navy ground, a lighter navy for graphic panels, broadcast yellow as the one accent (score highlight, current turn, CPU highlight), white type. Panels end in sheared 12-degree cuts like lower-thirds; numbers sit in white score-bug boxes; tags are small yellow slabs. Sofia Sans superfamily: Extra Condensed for numbers and calls, Sans for UI. No glows, no gradients beyond one floor-light falloff behind the board.

STORY: The player sees the matchup at once (who is up, players left each side), understands the rules from one line, asks, watches the answer stamp in, flips, and watches the CPU work its board live.

FIRST VIEWPORT: Full-width score bug at top (You, players left, question clock, players left, CPU). Under it a lower-third live call bar spanning the board width: yellow tag naming the asker, the question in large extra-condensed type, YES/NO slab. CPU board as a compact monochrome strip at the right of the bar (collapsible on phones). The player's board fills everything below. Dock pinned bottom with the one primary action.

FORM: broadcast graphics package; seed: none (pinned)

SIGNATURE: the question clock (shot-clock box counting questions) and the lower-third live call that types the CPU's question and stamps YES or NO. Motion grammar: graphics wipe in from the left with a short clip-path reveal, 220ms ease-out; nothing loops.
