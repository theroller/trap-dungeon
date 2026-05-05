# Trap Dungeon — AI Conventions

Inherits from `../../AGENTS.md` and `../AGENTS.md`. Architecture pattern is shared with `../lava-rise/` — fix sync/control bugs in both projects together when they recur.

## Game Overview

Single-arena stick-fighter. Two players over PeerJS. Switches scattered around the arena, each randomly mapped to a trap effect each round. Last alive wins.

## Architecture

- **Single file:** all logic in `index.html`. No build step, no module imports. PeerJS via unpkg CDN.
- **Logical canvas:** `cv.width=800, cv.height=1200` on every device. CSS scales canvas to fill viewport. Both host and guest run identical coordinate space.
- **Multiplayer:** host runs all physics + trap logic + RNG. Sends full state to guest each tick. Guest sends only its input. JSON serialization on PeerJS to avoid BinaryPack issues.
- **Per-device camera:** each iPad runs its own `updateCamera()` and follows `players[myIdx]`. Static arena means cameras barely move, but the pattern stays consistent with lava-rise.
- **State machine:** `lobby` → `playing` → `gameover` → restart.

## Game Objects

- **Players** — same shape as lava-rise: 20×50 stickfigure, hp, vx/vy, jumpsLeft, atkCd, dead.
- **Switches** — fixed positions, color-coded. `{ x, y, w, h, color, effect, used }`. `effect` is randomized per round from `EFFECTS`.
- **Active traps** — short-lived game objects: boulders falling, spike patches active, walls sliding in. Each has `type, x, y, vy, ttl` and an `update`/`draw` pair.

## Adding a Trap Effect

1. Add an entry to `EFFECTS` with a unique key.
2. In `triggerEffect(key, hitterIdx)`, push a new active trap onto `traps`.
3. Add a `case` in the trap update loop and a draw function.
4. Sync via `hostSend()`'s `traps:` array.

## Ford-Specific Rules

Same as lava-rise. Tap-only. Big visible feedback. No reading required for play.

## Known Issues To Inherit From Lava-Rise

When debugging cross-device sync, also check lava-rise — the multiplayer plumbing is identical and any fix likely applies to both.
