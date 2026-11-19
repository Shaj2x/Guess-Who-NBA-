# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack

Static HTML/CSS/JS in a single `index.html`, no build step. Hosted from the GitHub repo (works on GitHub Pages or opened as a file).

## Users

NBA fans playing a quick deduction game, either one person against the CPU or two people passing one device back and forth (inferred from the modes the owner asked for; not separately confirmed). Sessions are short and casual, on a phone or a laptop.

## Product Purpose

Who's That Baller? is a two-sided deduction game: each side hides one of 24 NBA greats and races to name the other side's player by asking yes/no questions and flipping down the players each answer rules out. Success is a game that starts in one tap, is understandable without instructions elsewhere, and makes the CPU's reasoning visible as it plays.

## Positioning

The CPU plays in the open: it lights up which players its question would keep, types the question, gets the answer, and flips its own board live. Questions are real NBA knowledge (honors, draft, era, teams) about real players with real headshots.

## Operating Context

- Modes: vs CPU (Rookie, All-Star, MVP difficulty) and 2 Players pass-and-play with a hand-off screen between turns.
- Talk mode: players ask and answer out loud; the game only holds each board and secret player and tracks turns. One phone (passed between turns, guesses checked automatically) or each on their own phone (the player taps End turn / Their turn is done, and confirms what the other side answered to a guess).
- 16 fixed yes/no questions in six groups (position, size and number, honors, path to the league, era, teams). Answers are filled in automatically from the secret player.
- Each human picks their own secret player at the start (or takes a random pick); the CPU's is dealt and never matches yours. On a shared device both players pick, privately, before the first question. The pick sits face down and is shown only while its Show button is pressed (it hides again after 4 seconds and after every hand-off).
- Nobody asks until every player on the device has locked in; a tip-off screen confirms it and says who goes first. Whose turn it is is shown by a full-width turn banner, a name splash on every change, the lit side of the score strip, and a dimmed board while the other side plays.
- A wrong guess ends the game. Auto-flip is an optional helper.
- Players can type their own yes/no question. The game reads it against a per-player fact sheet (teams, draft pick, birthplace, debut and last season, height, jersey number, honors, name initials) and shows how it read the question before it is asked. Naming a player is refused (that is a guess). In 2 Players, a question the game cannot read is answered by the other player by hand.

## Capabilities and Constraints

- Roster of 24 players with facts as of the 2025–26 season, defined in `index.html`.
- Headshots load from NBA.com's headshot server by NBA player ID (IDs checked against nba_api's offline player list). Patrick Ewing uses a Wikimedia Commons photo (CC BY-SA 2.0, credit required). Images fall back to the jersey number when they fail to load.
- Win counts and settings persist in localStorage only.
- Fan-made; not affiliated with the NBA. No NBA or team logos.

## Brand Commitments

- Name: "Who's That Baller?" (the owner's chosen name, kept across redesigns).
- Team colours appear on player cards (owner decision, 2026-11-18).

## Evidence on Hand

- Player facts table in-game (`scoutTable`), headshots via NBA.com and one Wikimedia photo.
- No testimonials, stats about players of the game, or claims; none may be invented.

## Product Principles

1. One tap from opening to playing.
2. The rules are never more than one tap away, and a game-ending action always says so before it happens.
3. Show the opponent's thinking, never just its result.
4. The player's own board is the most important thing on screen.
5. A refresh or an interrupted phone session must not lose the game.
