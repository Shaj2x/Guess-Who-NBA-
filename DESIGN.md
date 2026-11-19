---
name: Who's That Baller?
description: A one-on-one NBA deduction game dressed as a TV broadcast graphics package.
colors:
  network-navy: "#0a1a4a"
  network-navy-deep: "#061136"
  graphic-panel: "#12286a"
  graphic-panel-raised: "#1b3584"
  broadcast-yellow: "#ffc928"
  score-white: "#ffffff"
  ink-secondary: "#ccd6f5"
  ink-muted: "#97a7d8"
  plate-ink-muted: "#4a5683"
  answer-yes: "#2fd17c"
  answer-no: "#e0303c"
typography:
  call:
    fontFamily: "Sofia Sans Extra Condensed, Arial Narrow, system-ui, sans-serif"
    fontSize: "3.25rem"
    fontWeight: 800
    lineHeight: 0.95
    letterSpacing: "0.005em"
  headline:
    fontFamily: "Sofia Sans Extra Condensed, Arial Narrow, system-ui, sans-serif"
    fontSize: "2.25rem"
    fontWeight: 900
    lineHeight: 0.95
  score:
    fontFamily: "Sofia Sans Extra Condensed, Arial Narrow, system-ui, sans-serif"
    fontSize: "2.25rem"
    fontWeight: 900
    lineHeight: 0.9
    fontFeature: "tnum"
  body:
    fontFamily: "Sofia Sans, system-ui, sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.45
  label:
    fontFamily: "Sofia Sans, system-ui, sans-serif"
    fontSize: "0.75rem"
    fontWeight: 700
    letterSpacing: "0.08em"
rounded:
  xs: "3px"
  sm: "4px"
  md: "6px"
  lg: "8px"
spacing:
  s1: "4px"
  s2: "8px"
  s3: "12px"
  s4: "16px"
  s5: "24px"
  s6: "32px"
  s7: "48px"
components:
  button-primary:
    backgroundColor: "{colors.broadcast-yellow}"
    textColor: "{colors.network-navy}"
    rounded: "{rounded.sm}"
    height: "44px"
    padding: "0 24px"
  button-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.score-white}"
    rounded: "{rounded.sm}"
    height: "44px"
    padding: "0 24px"
  button-danger:
    backgroundColor: "{colors.answer-no}"
    textColor: "{colors.score-white}"
    rounded: "{rounded.sm}"
    height: "44px"
  score-box:
    backgroundColor: "{colors.score-white}"
    textColor: "{colors.network-navy}"
    typography: "{typography.score}"
    rounded: "{rounded.sm}"
  live-call:
    backgroundColor: "{colors.graphic-panel}"
    textColor: "{colors.score-white}"
    typography: "{typography.call}"
    padding: "16px 42px 16px 24px"
  chip:
    backgroundColor: "{colors.network-navy-deep}"
    textColor: "{colors.score-white}"
    rounded: "{rounded.sm}"
    height: "44px"
  chip-selected:
    backgroundColor: "{colors.broadcast-yellow}"
    textColor: "{colors.network-navy}"
---

# Design System: Who's That Baller?

## Overview

**Creative North Star: "Courtside Broadcast"**

The game is a TV broadcast of a one-on-one matchup. The screen is a graphics package over the arena: a score bug across the top, a lower-third that carries the live call, and player graphics for the cards. It is built for a fan on the couch at night with a game on, so the world is dark, saturated network navy with a single broadcast-yellow accent, the way a network's on-air package reads against the court.

Colour is spent where it carries meaning. Team colours live only on the player cards; the CPU's board is one colour that shows state; yellow marks whose turn it is, what the CPU is considering, and the one primary action.

**Key Characteristics:**
- A score bug with white score boxes and a yellow question clock
- A sheared lower-third that types each question and stamps YES or NO
- Player graphics: team-colour plate, headshot, white name bar with the jersey number
- One extra-condensed superfamily for every call, number and headline
- Flat navy depth with soft offset shadows; nothing glows

## Colors

### Primary
- **Broadcast yellow** (`#ffc928`): the accent. The primary button, the active-turn bar, the question clock, the speaker tag, selected chips, and the tiles the CPU is weighing. Navy text on it (11:1).

### Neutral
- **Network navy** (`#0a1a4a`): the ground. **Navy deep** (`#061136`) for the score bug, CPU board and dock. **Graphic panel** (`#12286a`) and **raised panel** (`#1b3584`) for lower-thirds, menus, dialogs and CPU tiles.
- **Score white** (`#ffffff`): primary text, score boxes and card name bars. **Secondary** `#ccd6f5` (11:1 on ground), **muted** `#97a7d8` (6.4:1 on ground) for meta only.

### Semantic
- **Yes** `#2fd17c` with dark text, **No** `#e0303c` with white text (4.6:1). Always paired with a check or cross icon, never colour alone.

### Named Rules
**The Cards Carry the Colour Rule.** Team colours appear only on player cards (plate and name-bar edge) and the "your player" chip. Every other surface is navy, white or yellow.

**The One Yellow Rule.** Yellow marks the single thing that matters now: the turn, the clock, the speaker, the primary action or the CPU's live consideration. Two yellow buttons never sit side by side.

## Typography

**Calls and numbers:** Sofia Sans Extra Condensed, 800–900, uppercase.
**Interface:** Sofia Sans, 400–700.

### Hierarchy
- **Call** (800, up to 3.25rem, 0.95): the live question in the lower-third.
- **Headline** (900, 2.25rem): "Your 24 players", dialog titles.
- **Score** (900, tabular): score boxes, question clock, card numbers, CPU tiles.
- **Body** (400, 1rem, 1.45): rules, help, play-by-play.
- **Label** (700, 0.75rem, tracked 0.08em, uppercase): small headings like "CPU level". The 11px floor holds for every functional label.

### Named Rules
**The Tabular Score Rule.** Every number that can change (counts, question clock, wins, jersey numbers in tables) uses tabular figures so nothing shifts as it ticks.

## Layout

The board is the work surface and fills the width below the broadcast block. Desktop: the stage (score bug and live call) sits beside a 336px CPU board. Below 860px the stage pins to the top of the screen while the board scrolls under it, and the CPU board collapses behind a Show toggle. The board runs 6 columns, 4 below 1000px and 3 below 480px. The page reserves bottom space equal to the dock so no card hides beneath it. Spacing steps on a 4px base: 4–8 inside a group, 12–24 between groups, 32+ between sections.

## Elevation & Depth

Depth comes from navy steps (deep, ground, panel, raised) and one soft offset shadow, `0 6px 18px rgba(2,6,24,.45)`, on floating graphics: the score bug, cards, dock, menus and dialogs. One floor-light radial falloff sits behind the page top, like arena lighting on the court.

### Named Rules
**The No Glow Rule.** Shadows always have an offset and blur; no zero-offset coloured halos, no neon edges.

## Shapes

Broadcast graphics are sharp: radii 3–8px only. The signature edge is a 12° shear: the lower-third's right end, the speaker tag, and the Play vs CPU button end in a slanted cut. A 4px yellow bar marks the leading edge of the live call and the top of dialogs.

## Components

### Buttons
- **Primary:** yellow fill, navy text, 44px (48px in the dock). Only one primary is visible at a time: Ask, then End turn.
- **Secondary:** transparent with a white 14% outline; hover lightens the fill.
- **Danger:** red fill for "Lock in guess" only.
- **Text button:** yellow underlined text for low-weight actions (Reset board, Player names, How to play). Reset board needs a second tap within 3 seconds.

### Chips
Question chips in the menu: navy-deep with an outline, 44px tall, yellow fill when selected. Once asked, a chip shows a YES or NO tag and is disabled.

### Cards / Containers
**Player card:** a team-colour plate with the NBA.com headshot standing on it, and a white name bar with a 3px team-colour top edge, the uppercase name, position and height, and the jersey number. Flipped cards turn to a navy back marked "Out". Hover lifts the card 3px; press scales to 0.98.

### Score bug
Navy-deep strip: each side shows the name, wins and a white score box reading "N LEFT". The active side gets a 4px yellow bar. The centre is the yellow question clock ("Q3") over the turn label.

### Live call (lower-third)
Graphic-panel block with a yellow leading bar and a sheared right end. A yellow speaker tag ("CPU ASKS") sits above the question in Call type, then a YES or NO stamp and a one-line explanation. Each new call wipes in from the left in 220ms.

### CPU board
Monochrome raised-navy tiles with jersey numbers; ruled-out tiles become outlines. While the CPU lines up a question, the tiles it would keep turn yellow and the rest dim.

## Do's and Don'ts

### Do:
- Do keep team colour on the cards and nowhere else.
- Do show one yellow primary action at a time.
- Do label every count with what it counts ("24 LEFT").
- Do keep the rules one tap away, and say "a miss costs your turn" whenever a guess is being picked.

### Don't:
- Don't add glows, gradients on surfaces, or glass.
- Don't put text under 11px, even in labels.
- Don't use a second display face; the call, score and headline voices are all Sofia Sans Extra Condensed.
- Don't add eyebrow labels above headings.
