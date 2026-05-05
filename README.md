# Trap Dungeon

Top-down two-player dungeon. Walk over colored switches to trigger random traps — spikes, swinging blades, sliding walls, dart volleys — and lure your opponent into them. Players cannot damage each other directly; the room is the weapon.

**Players:** Ford (blue) vs Finn (red), one player per iPad over PeerJS.
**Platform:** iPad portrait, touch only. Desktop keyboard fallback for testing.
**Deployed:** https://theroller.github.io/trap-dungeon

## How to Play

- Walk over a colored switch to trigger a trap. Each color does something different — and the colors are randomised every round.
- Traps hurt whoever they touch, including you. Push your opponent into the spikes!
- Some switches help you (heal). Some hurt both (shock). The trick is learning what each color does before your opponent does.
- Last one alive wins.

## Controls (Brawl Stars-style dual joystick)

- **Touch — left half of screen:** drag = move (blue joystick)
- **Touch — right half of screen:** drag = aim and fire continuously (orange joystick); just touch to fire forward
- **Bumping** the other player shoves them — push them onto a spike tile or into the blade!
- **Desktop:** WASD or arrows to move, F or Space to attack

## Match format

Best of 5 — first to 3 round wins takes the match. Round score shown as pips at the top of the screen.

## Running Locally

Open `index.html` in a browser. Tap **LOCAL TEST** for keyboard 2-player on one screen.

## Roadmap

- [ ] More trap types (floor drop, control reversal, heal, freeze)
- [ ] Round system (best-of-3) so memorising switches matters
- [ ] Visual hint showing what a switch did *after* it's triggered
- [ ] Cross-iPad sync polish (shared with lava-rise)
- [ ] Sound effects for each trap
