# Workout Log — Help & Reference

## What is this app?
A **Progressive Web App (PWA)** — a website that behaves like a native app. It is not in the App Store and does not require any download. It runs entirely on your device, works offline, and stores all data locally in your browser's storage.

---

## Installing the app

### iPhone / iPad (Safari)
1. Open Safari and go to `psgambat-oss.github.io/workout-tracker`
2. Tap the **Share** button → **Add to Home Screen**
3. Tap **Add** — the app icon appears on your home screen

### Android (Chrome)
1. Open Chrome and go to `psgambat-oss.github.io/workout-tracker`
2. Tap the three-dot menu → **Add to Home screen** (or look for the install prompt in the address bar)
3. Tap **Add** — the app icon appears on your home screen

### Desktop (Chrome / Edge / Safari)
1. Go to `psgambat-oss.github.io/workout-tracker`
2. Look for the install icon in the address bar, or use the browser menu → **Install app**
3. The app opens in its own window

---

## Updating the app
**You do NOT need to reinstall every time there's an update.**

- **Code-only updates** (new features, bug fixes, layout changes): Open Safari, visit `psgambat-oss.github.io/workout-tracker` once to refresh the cache, then close Safari and reopen the app from your home screen. Done.
- **Reinstall required only when**: the home screen icon or app title changes. You'll be told explicitly when this is needed.

> Reinstalling wipes all your localStorage data. Always export a backup first (Settings → Export Data Now) before reinstalling.

---

## Daily Use

### Selecting a Day
Tap any day tab at the top (M T W T F S S) to view that day's workout. The current day is highlighted in orange. The 3-letter month abbreviation appears above the M tab.

### Checking Off Exercises
Tap any exercise row to check it off. Tap again to uncheck. A green dot appears on the day tab once you have any progress.

### Finishing a Workout
When you're done, tap the orange **Finish** button in the top-right. This:
- Marks the day as complete
- Shows a summary of what you did
- Triggers an auto-export if that setting is on

Once finished, the button turns green — **✓ Complete** — and tapping it shows your summary again.

### Timed Exercises
Exercises with a ⏱ icon track time. After checking one, +/− buttons appear to log how many minutes you did. Timed exercises include all Warm Up / Cooldown, Cardio, and Yoga items.

---

## Workout Types
| Type | Description |
|------|-------------|
| Upper Body | Chest, Lats, Shoulders, Back, Biceps, Triceps, Forearms |
| Legs | Legs + Glutes |
| Full Body | Both Upper Body and Legs sections combined |
| Rest | No workout — day is skipped |

### Optional Sections
Any day can include any combination of these sections, configured per-day in Settings:

| Section | Description |
|---------|-------------|
| Warm Up/Cooldown | Cardio warm-up, Yoga (Dynamic/Static), Static Stretching — all timed |
| Cardio | Treadmill, Cycling, Rowing, Elliptical, Freestyle — all timed |
| Abs + Core | TRX, Crunches, Leg Raises, BOSU, Ab Machines |
| Yoga | Active Standing Poses, Core Work, Deep Stretches — all timed |

Warm Up appears first; Cardio, Abs + Core, and Yoga appear at the end of the workout.

---

## Settings (⚙︎ Gear Icon)

### 📅 Workout Mode
Settings opens with a **Schedule / Builder** toggle — you use one or the other, not both.

#### Schedule
The standard week schedule. Uses a two-column layout with a single **STRENGTH | EXERCISE** header. For each day:
- **Left column (Strength)** — choose Upper Body, Legs, Full Body, or Rest
- **Right column (Exercise)** — toggle optional sections: Warm Up/Cooldown, Abs + Core, Cardio, Yoga

Tap **Save** to apply.

#### Builder
Build a fully custom workout for each day of the week. When Builder is selected, the schedule is bypassed entirely — only your chosen exercises appear in the workout view.

- **✎ Customize Days →** — opens the builder to configure each day
- In the builder, tap day tabs (M–S) to switch days
- Check exercises to include them; uncheck to hide them
- Sections and subheaders with no checked items are hidden automatically
- **Select All / Clear All** — quickly check or uncheck all exercises for the current day
- **Copy to →** — copy the current day's selections to one or more other days
- The workout header shows **CUSTOM WORKOUT** and the progress count reflects only your selected exercises
- Builder selections are saved and carry forward to the next week automatically

### Weekly Stats
Controls the stats card (**This Week / Avg / Day / Streak**) displayed below the day tabs:
- **Off** — never shown
- **After Finish** — shown automatically after you tap Finish, until the next day
- **Always** — always visible

**Avg / Day** shows the average number of exercises you checked per workout day this week — not a percentage of all available exercises.

### Trainer Notes
Tap **✎ Manage Notes** to add personal reminders that appear on your workout screen. Toggle ON/OFF to show or hide them.

### Tools
| Button | What it does |
|--------|-------------|
| ✎ Edit Exercises | Add, rename, delete, reorder, or hide exercises, sections, and subheaders |
| 📋 History | View archived weeks with per-day completion stats |
| Auto-Export on Finish | Toggle ON/OFF — automatically saves a JSON backup after each Finish |
| ⬇ Export Data Now | Manually export all data to a JSON file (works on iOS, Android, and desktop) |
| 📂 Import Backup | Restore all data from a previously exported JSON file |

---

## Editing Exercises (Edit Mode)

Tap **✎ Edit Exercises** in Settings to enter edit mode.

| Control | What it does |
|---------|-------------|
| ≡ Drag handle | Reorder exercises, subheaders, or sections |
| ⇄ Move | Move an exercise to a different section or subheader |
| Hide | Hide a built-in exercise (it won't appear during workouts) |
| ✕ Delete | Remove a user-created exercise (with confirmation) |
| ✎ Pencil | Rename an exercise |
| + Add to [Section] | Add a new exercise to that section |
| + Add Subheader | Add a new subheader within a section |
| + Add Section | Add a new top-level section |

### Hidden exercises
Tapping **Hide** on a built-in exercise removes it from your workout view but does not delete it. To restore hidden exercises, look for the **Show hidden items** toggle at the top of each section in edit mode — hidden exercises appear dimmed with a **Show** button to restore them.

User-created exercises show a **✕** button instead of Hide — these are permanently deleted when removed.

### Rest Day
If today is scheduled as a rest day, the app shows a **Settings** link directly on screen — tap it to change today's workout type.

---

## Start New Week
The **↻ START NEW WEEK** button at the bottom of the screen:
1. Archives the current week's data to History
2. Clears all checked exercises so you start fresh
3. Requires two confirmations to prevent accidental resets

Your history is always viewable in Settings → 📋 History.

---

## Streak
The 🔥 streak count in the stats card shows consecutive days where you had a scheduled workout and tapped Finish. Rest days don't break the streak.

---

## Data Backup & Restore

### Exporting
Settings → **⬇ Export Data Now** saves a file named `workout-log-YYYY-MM-DD.json` to a location you choose. On iPhone/iPad this opens the Files app; on Android it saves to your Downloads folder; on desktop it saves wherever your browser downloads files.

### What's in the export
- Your workout schedule
- All checked exercises (current week)
- Completed day flags
- Full workout history
- Any custom exercises you've added
- App preferences (stats mode, auto-export setting)
- Hidden exercise list

### Auto-Export
When **Auto-Export on Finish** is ON, a JSON file is saved automatically every time you tap Finish. Recommended to keep this on so you always have a recent backup.

### Restoring after a reinstall
Since all data is stored on-device, reinstalling the app wipes it. To get back to where you were:

1. **Before reinstalling** — go to Settings → **⬇ Export Data Now** and save the file somewhere you can find it (a cloud folder, email to yourself, etc.)
2. **Reinstall the app** using the steps above for your device
3. **Open Settings** → **📂 Import Backup**
4. Your device's file picker opens — navigate to your saved JSON file and select it
5. A confirmation screen shows the date of the backup — tap **Restore**
6. All your data is back: schedule, history, exercises, and preferences

---

## Right Arm Note
Sections marked with a trainer note (Jim Delgado, CKTP) show a reminder to add an extra unilateral set on the right side.

---

## App Info
- **Hosted at**: `psgambat-oss.github.io/workout-tracker`
- **Works offline**: Yes — all data is stored on-device
- **Backup/sync**: Manual via JSON export — save to any location you choose
- **Version history**: See `CHANGELOG.md`
