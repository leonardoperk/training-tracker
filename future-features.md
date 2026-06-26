# Future Features — PPL Tracker

---

## Entry Gamification

**Idea:** Give the user positive and engaging feedback when entering sets and kg values during a workout.

**Examples:**
- Confetti effect when a new PR (personal record) is hit on weight or reps
- Subtle haptic + visual flash when a set is marked done
- "All sets done" celebration animation when an exercise is completed
- End-of-workout summary highlights PRs ("3 neue Bestleistungen heute 🏆")

**Implementation notes:**
- PR detection: compare current set's weight/reps against all-time max for that exercise from history
- Confetti: lightweight canvas-based library (e.g. canvas-confetti, ~3KB) or CSS-only particle burst
- Keep it subtle — fires max once per exercise per session, not on every set
- Must not interfere with the core input UX (no blocking overlays)
