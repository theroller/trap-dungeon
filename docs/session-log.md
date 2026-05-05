# Session Log

Running history of each weekend session: what was built, what Ford said, what to carry forward.

---

## Session 1 — 2026-05-04

**Version shipped:** v1.0

**What we built:**
- New project scaffolded after Ford asked to start the Traps level
- Single-arena 2-player fighter, no scrolling, fixed dungeon stage
- 6 colored switches in fixed positions (4 on floor, 2 on mid platforms, 1 on top platform)
- Switch → effect mapping is randomised every round (the "memorise" mechanic)
- 6 trap effects: boulder drop, spike patch, sliding wall, shock-both, heal, speed boost
- Auto-attack on player contact (jump-on-head dynamic from lava-rise carries over)
- PeerJS multiplayer (host/join/local-test) reusing the lava-rise lobby and sync pattern
- Per-device camera, fixed logical canvas (800×1200)
- HUD shows switch count and active trap count for sync diagnostics

**What Ford said:**

**What clicked:**

**What was confusing:**

**Bugs noticed:**
- Same family of cross-device sync issues expected as in lava-rise — defer until v1 is playable

**What to build next:**
- [ ] Best-of-3 round system (so memorising switch effects across rounds matters)
- [ ] Visual indicator on switches AFTER triggered, hinting what they did last time
- [ ] More trap variety: floor drop, ice patches, fireball spray
- [ ] Sound effects — each trap needs its own
- [ ] Shared multiplayer fix-up pass with lava-rise

---

## Session 2 — 2026-05-04 (same day)

**Version shipped:** v2.0 — full top-down redesign

**What we built:**
- Pivoted from vertical platformer to top-down dungeon based on Ford's idea
- Top-down arena, single screen, fixed 800x1200 logical canvas
- 5 interior pillars to navigate around
- 6 colored switches placed throughout the room
- Drag-anywhere virtual joystick (touch); WASD / arrows on desktop
- AABB collision against walls and pillars
- Trap-only damage model: players cannot damage each other directly — only traps hurt
- Spike patches drop under the OTHER player's position when triggered
- Swinging blade sweeps across the room
- Sliding wall closes in from one side
- Dart volleys fire from a random wall
- Shock damages both, heal restores hitter

**Open questions for Ford:**
- Should players be able to push each other into traps (bumper-style), or is "lure them in" enough?
- Does he want a way to block / dodge actively (roll, dash)?
- Best-of-N rounds, or single-life?

---

## Template for future sessions

```
## Session N — YYYY-MM-DD

**Version shipped:** vX.Y

**What we built:**

**What Ford said:**

**What clicked:**

**What was confusing:**

**Bugs noticed:**

**What to build next:**
```
