# Workout Tracker Changelog

## v3.6 — 2026-05-05
- **Workout Builder**: New per-day custom exercise builder — select any exercises from any section for each day of the week. When Builder is active, the schedule is bypassed entirely.
- **Workout Mode toggle**: Settings now shows a unified "📅 Workout Mode" section with a Schedule / Builder segmented control — one or the other, never both
- **Builder progress**: Done/total counts and section counts reflect only your builder-selected exercises when Builder is on
- **Customize Days**: Tap to open the builder — day tabs M–S, checkbox per exercise, sections/subheaders auto-hide when empty
- **Select All / Clear All**: Quickly select or clear all exercises for the current builder day
- **Copy to →**: Copy the current day's builder selections to one or more other days
- **Settings scroll**: Settings no longer jumps to top after each change — scroll position is preserved
- **Help updated**: In-app Help and HELP.md updated to document Workout Mode (Schedule / Builder)

## v3.5.4 — 2026-05-05
- **Delete protection**: ✕ delete button on sections and subheaders now only appears on user-created ones — built-in sections and subheaders can no longer be accidentally deleted
- **Custom flag**: Newly added sections and subheaders are marked `custom: true` so they remain deletable

## v3.5.3 — 2026-05-05
- **🎬 Video links**: Add a YouTube or web URL to any exercise via Edit mode — a 🎬 icon appears on the exercise row and taps open the video in the browser
- **Removed video sub-sections**: STRETCHING VIDEOS (Warm Up/Cooldown) and Core Videos (Abs + Core) removed from default exercises — add your own via the 🎬 URL field instead
- **Migration**: Existing users with STRETCHING VIDEOS or Core Videos sub-sections will have them automatically removed on next load

## v3.5.2 — 2026-05-05
- **⏱ Timed indicator**: Clock icon appears on all timed exercises (Warm Up, Cardio, Yoga) before checking — disappears once checked and time selector appears
- **AVG / DAY**: Replaced misleading "AVG DONE %" with average exercises checked per workout day this week
- **WARM UP / COOLDOWN**: "Cool Down" corrected to one word "Cooldown" throughout
- **Exercises**: Renamed "Mat side ankle touch" → "Mat heel touch"; added "Weighted side bend" to Crunches
- **Streak**: 🔥 badge removed from app title — still visible in stats card
- **Settings**: Schedule redesigned as two-column layout (STRENGTH | EXERCISE) with single header row
- **Trainer Notes**: "Tap to manage" replaced with visible "✎ Manage Notes" in orange
- **Migration**: Automatically upgrades old stored exercise data — removes stale Stretching section, adds missing STATIC STRETCHING / YOGA / STRETCHING VIDEOS groups to Warm Up, upgrades old Cardio to include Freestyle variants and Elliptical

## v3.5 — 2026-05-04
- **Optional Sections**: Warm Up / Cooldown, Cardio, Abs + Core, and Yoga can now be added to any workout day — toggled per-day in Settings via pill buttons
- **New schedule types**: Simplified to Upper Body, Legs, Full Body, and Rest (removed "Legs & Core" as a type)
- **Shared sections architecture**: Warm Up / Cooldown, Cardio, Abs + Core, and Yoga live in a shared pool — included in any day when toggled on
- **Warm Up / Cooldown expanded**: New sub-sections — YOGA (Dynamic Movement / Static Stretching), STATIC STRETCHING, and STRETCHING VIDEOS; all items timed
- **CARDIO expanded**: Added Freestyle variants (Run, Incline Hike, Walk, Cycle, Row) and new ELLIPTICAL sub-section (HIIT Glide, Freestyle Glide)
- **YOGA section**: New top-level workout section with Active Standing Poses, Core Work, Deep Stretches — available as an optional section on any day
- **Hide / Delete exercises**: Built-in exercises get a Hide button; user-created custom exercises get a ✕ Delete button. Hidden items are stored and can be shown/restored in edit mode via "Show hidden items" toggle
- **Month in header**: 3-letter month abbreviation (e.g. May) displayed above the M (Monday) day tab
- **Trainer Notes default blank**: New users start with no trainer notes pre-filled
- **Spelling fixes**: "HIT" → "HIIT" throughout; "Warmup" → "Warm Up" throughout
- **Stretching section removed**: Merged into Warm Up / Cooldown sub-sections
- **Schedule migration**: Old schedule format (strings) automatically upgraded to new object format on first load

## v3.4 — 2026-05-04
- **Edit mode overhaul**: Drag handles (≡) to reorder sections, subheaders, and exercises
- **Move exercise (⇄)**: Move any exercise to a different section or subheader via picker modal
- **Delete sections & subheaders**: ✕ button with confirmation on section headers and subheaders
- **Bug fix**: + Add Exercise button no longer breaks when group name contains quotes
- **Import Backup**: 📂 Import Backup button in Settings restores all data from a JSON file — works on iOS, Android, and desktop
- **Welcome popup**: Shows on first launch and after each update with version number and what's new
- **Rest day UX**: If today is a rest day, a Settings link appears on screen to change it
- **Sticky Settings buttons**: Cancel/Save always visible at bottom of Settings — no longer hidden by scrolling; transparent gap below buttons eliminated
- **Centered input modals**: Add/Edit/Subheader modals now centered so iOS keyboard doesn't cover buttons
- **Help updated**: New Editing Exercises section, device-agnostic install and backup instructions, PWA spelled out, Import Backup documented
- **Export**: Clarified as platform-agnostic (iOS, Android, desktop)

## v3.3.1 — 2026-05-04
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
