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
- [ ] More trap variety: floor drop, control reverse, freeze, fireball spray
- [ ] Sound effects — each trap needs its own
- [ ] Shared multiplayer fix-up pass with lava-rise

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
