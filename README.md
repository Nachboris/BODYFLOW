# 💪 BodyFlow

**A minimalist progressive workout tracker for bodyweight + resistance band training — built as a single self-contained HTML file, installable as a PWA.**

🔗 **Live app:** [nachboris.github.io/BODYFLOW](https://nachboris.github.io/BODYFLOW/)

---

## What is BodyFlow?

BodyFlow is a personal workout tracker designed around one principle: **zero friction**. No account, no server, no install, no setup. Open it in your browser and start training.

It tracks two alternating full-body sessions (A & B), each ~30 min, using bodyweight + resistance bands. Every workout logs your reps, accumulates XP, maintains your streak, and pushes your progression automatically.

Everything is stored locally on your device (no account, no cloud).

---

## Features

### 🏋️ Workout Sessions
- **Session A** — Full Body Push/Glutes: Jumping Jacks, Squat, Push-Ups, Plank, Glute Bridge, Romanian Deadlift (band)
- **Session B** — Full Body Pull/Posture: Jumping Jacks, Bulgarian Squat, W-Raise, Side Plank, Overhead Press (band), Superman, Face Pull (band)
- Built-in rest timer, rep logging, and technique cues for every exercise
- YouTube demo links for each exercise (always accessible, no dead links)
- Resistance band indicators with color-coded levels (gray / dark-gray / black)

### 📈 Auto-Progression
- 5 progressive tiers per exercise (e.g. push-ups: 3×10 → 3×12 → 3×15 → 4×12 → 4×15)
- After 3 sessions at a tier, you automatically advance — and earn +50 XP
- Progression indicator on every exercise card

### 🎮 XP & Levels
- 100 levels with exponential XP curve (~4–6 months to max with consistency)
- Full session: +100 XP · Partial session (≥3 exercises): +50 XP · External activity: +100 XP
- **Streak multiplier**: 2 weeks ×1.2 · 3 weeks ×1.5 · 4+ weeks ×2.0
- XP penalty for missed sessions the previous week (−30 XP each, max −90)
- Milestone bonuses at levels 10, 25, 50, 75

### 🏃 External Activities
- Log any activity as a session: hiking, cycling, swimming, running, badminton, yoga, and more
- Counts toward XP, streak, and the 30-day challenge

### 🎯 30-Day Challenge
- Set a reward (if you succeed) and a stake (if you fail)
- Target: 3 sessions/week for 4 weeks
- Automatic result: +500 XP for success, −200 XP for failure

### 📊 Tracking Tab
- Reps chart per exercise (last 8 sessions)
- Sessions chart per week (last 8 weeks, with dates)
- XP history and level progress
- 12 unlockable badges
- Full session history

### ⚙️ No-Nonsense Tech
- Single HTML file, no dependencies, no build step
- Data stored in `localStorage` — 100% offline, 100% private
- Service Worker for full offline support
- Installable as a PWA (see below)

---

## Quick Start Guide

1. **Open the app** at [nachboris.github.io/BODYFLOW](https://nachboris.github.io/BODYFLOW/)
2. Go to **Settings** (⚙️ tab) → enter your name and preferred training days
3. On the **Today** screen, tap the session card (green = Session A, blue = Session B)
4. For each exercise: tap **▶ Start** to begin the rest timer, log your reps with the **+/−** buttons
5. Finish the session — confetti, XP, and level-up await
6. Check your progress anytime in the **Tracking** tab

**Tips:**
- Log every session, even partial ones (≥3 exercises still earns 50 XP and counts for your streak)
- Use **🏃 Log another activity** on rest days — it counts toward your streak and challenge
- Your streak is weekly, not daily — missing one day in a week is fine as long as you train that week

---

## Install on Your Phone (PWA)

BodyFlow works as a Progressive Web App — it runs like a native app, works offline, and lives on your home screen.

### iPhone / Safari
1. Open [nachboris.github.io/BODYFLOW](https://nachboris.github.io/BODYFLOW/) in **Safari** (must be Safari, not Chrome)
2. Tap the **Share** button (the square with an arrow pointing up)
3. Scroll down and tap **"Add to Home Screen"**
4. Name it `BodyFlow` and tap **Add**

### Android / Chrome
1. Open the app in **Chrome**
2. Tap the **three-dot menu** (⋮) in the top right
3. Tap **"Add to Home Screen"** (or "Install app" if prompted automatically)
4. Confirm — done

> Once installed, the app works fully offline. No internet required after the first load.

---

## FAQ

**Is my data backed up anywhere?**  
No — all data lives in your browser's `localStorage`. It stays on your device and is never sent anywhere. To back it up manually: Settings → **Export JSON**. Keep that file safe.

**I reinstalled the app / cleared my browser data and lost my sessions. Can I recover them?**  
If you exported a JSON backup, you can re-import it (Settings → Recover data). If you didn't export, the data is unfortunately gone — localStorage is wiped with browser data.

**Does it work without internet?**  
Yes, fully — once you've loaded the app at least once, the Service Worker caches everything. You can train in airplane mode.

**Can I use it on a desktop?**  
Yes, it works in any modern browser. The layout is optimized for mobile but perfectly functional on desktop.

**I updated the page and my data disappeared.**  
This shouldn't happen — data persists across updates. If it did, use Settings → **Recover lost data**, which tries to restore from previous app versions' keys.

**What resistance bands does this work with?**  
Any long-loop fabric resistance bands work. The app is calibrated for 3 resistance levels (light / medium / heavy). You don't need a specific brand.

**Can I add exercises or change the program?**  
Not from within the app — the program is intentionally fixed and curated. If you're comfortable with code, the program is defined in the `SESSIONS` object in `index.html`.

**Why is it a single HTML file?**  
Deliberate choice: zero build tools, zero dependencies, trivially hostable on GitHub Pages, easy to version and share. The entire app is ~140 KB.

---

## Tech Stack

| Layer | Choice |
|---|---|
| Framework | Vanilla JS (no dependencies) |
| Storage | `localStorage` |
| Offline | Service Worker (sw.js) |
| Fonts | Fraunces + Plus Jakarta Sans (Google Fonts) |
| Hosting | GitHub Pages |
| Build | None — single HTML file |

---

## License

Personal project — not open for contributions. Feel free to fork and adapt for your own use.
