# Workout Tracker Changelog

## v3.0.1 — 2026-05-03
- **iPhone safe area fix**: Added `viewport-fit=cover` to viewport meta tag so `env(safe-area-inset-bottom)` actually applies — prevents START NEW WEEK button from being clipped by iPhone curved edges

## v3.0 — 2026-05-03
- **Upper Body**: Renamed "Full Body" workout type to "Upper Body" (internal key unchanged)
- **Full Body (combined)**: New workout type that renders both Upper Body + Legs & Core sections in one view
- **Streak badge**: 🔥 N streak counter in app header showing consecutive completed workout days
- **Stats card**: Weekly stats (This Week, Avg Done, Streak) shown as a compact 3-cell card
- **Stats display modes**: Off / After Finish / Always — persisted in `wl26_prefs` localStorage key
- **Settings popup sections**: Reorganized into labeled sections — 📅 Workout Schedule, 📊 Weekly Stats, 🛠 Tools
- **Schedule grid**: Days now show 4 options (Upper Body, Legs & Core, Full Body, Rest) in a 2×2 grid
- **Save button**: Renamed from "Save Schedule" to "Save"

## v2.9 — 2026-05-03
- **START NEW WEEK** button replaces "NEW WEEK — CLEAR ALL" (↻ icon, no trash)
- **Two-step confirmation**: Step 1 explains the archive + clear action with week dates; Step 2 "Are You Sure?" safety net with Go Back option
- **Archive before clear**: tapping Archive & Start Fresh saves the week's per-day stats (date, type, done/total, completed flag) to localStorage (`wl26_history`) before wiping checked state
- **📋 History button** added to gear/settings modal — shows all archived weeks grouped by date range with per-day stats and completion checkmarks
- **doReset** no longer destroys data — it archives first, then clears

## v2.8 — 2026-05-03
- **Finish/Complete button**: Orange `☐ Finish` button when workout not yet marked done; tapping it marks the day complete, saves to localStorage (`wl26_done`), and shows a workout summary modal with kudos. Green `☑ Complete` button when already marked done (opens summary for review).
- **Edit button moved to settings gear popup** (done in prior session).
- **Section counts turn green** as soon as any exercises in that section are checked (previously only turned green when the full section was done).
- **doReset (New Week)** now also clears `completedDays` for the current week.
