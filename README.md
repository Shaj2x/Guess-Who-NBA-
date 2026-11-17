# Who's That Baller?

An NBA-themed take on the classic "guess the mystery person" board game. Open `index.html` in any browser — no build step.

**Modes**
- **vs CPU**: watch the CPU's board flip and its questions type out live on the jumbotron. Three levels: Rookie, All-Star, MVP.
- **2 Players**: pass and play on one device, with a hand-off screen between turns so nobody sees the other secret.

**How to play**
- You and the CPU each get a secret player from the same 24 NBA greats.
- On your turn, ask a yes/no question (position, height, jersey number, championships, MVP, No. 1 pick, college, born abroad, era, Lakers/Celtics/Texas teams).
- Flip down every player the answer rules out (or tick **Auto-flip**), then end your turn.
- The CPU asks you a question back; your answers are filled in automatically.
- Think you know it? Hit **Make a guess** and click the player. Miss and you lose.

Player facts are as of the 2025–26 season; the full fact sheet is in the in-game **Scouting report**.

**Headshots** load from NBA.com's headshot server by NBA player ID (IDs checked against nba_api's offline player list). Patrick Ewing's photo comes from Wikimedia Commons (CC BY-SA 2.0, credited in the footer) because NBA.com has no headshot for him. Any image that fails to load falls back to the jersey number.
