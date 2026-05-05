# Trap Dungeon

Two-player stick-fighter where the arena is a puzzle. Hit switches to trigger random traps — boulders, spikes, walls — and try not to be the one they hit.

**Players:** Ford (blue) vs Finn (red), one player per iPad over PeerJS.
**Platform:** iPad in landscape or portrait, touch only. Desktop keyboard fallback for testing.
**Deployed:** https://theroller.github.io/trap-dungeon

## How to Play

- Walk over a switch to trigger a trap. You don't know what each switch does until you hit it.
- Some traps hurt the other player. Some hurt YOU. Some hurt both.
- Bump into your opponent from above to deal damage (jump on their head).
- Last one alive wins the round.

## Controls

- Tap left/right of your character — move
- Tap bottom 28% of screen — jump (double jump available)
- Walk into a switch — trigger
- Walk into the other player from above — damage them
- Spacebar (desktop) — jump

## Running Locally

Open `index.html` in a browser. Tap **LOCAL TEST** for keyboard 2-player on one screen.

## Roadmap

- [ ] More trap types (floor drop, control reversal, heal, freeze)
- [ ] Round system (best-of-3) so memorising switches matters
- [ ] Visual hint showing what a switch did *after* it's triggered
- [ ] Cross-iPad sync polish (shared with lava-rise)
- [ ] Sound effects for each trap
