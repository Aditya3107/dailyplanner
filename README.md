# Daily Planner Widget

A compact daily planning and task-management widget. Set goals each morning, break them into tasks and micro-steps, check them off through the day, and keep a streak alive by hitting your daily target.

Made with Claude 

**Live app:** [importantdailyplanner.netlify.app](https://importantdailyplanner.netlify.app)

---

## Features

- **Plan your day** — add goals, break each into tasks and micro-steps. Entries save on Enter or simply by tapping away (mobile-friendly).
- **Today view** — progress ring, three-level checklist. Checking a parent checks all its children; parents auto-complete when all children are done.
- **Celebrations** — ribbons fly when you complete a goal or hit your daily target (paw prints in the Kitty theme).
- **Streak counter** — counts consecutive days at or above the target (default 80%, adjustable).
- **Stats** — 14-day completion chart, planned vs. done (last 7 days), time-of-day productivity, and a 4-week streak calendar.
- **Review** — end-of-day summary per goal; "Close the day" logs it to history.
- **Settings (gear icon)** — text size (85–130%), 6 fonts (incl. Handwritten, Pixel, Groovy), 6 themes (Midnight, Daylight, Ocean, Synthwave, Bubblegum, Kitty), and a full reset with confirmation popup.

All data is stored locally in the browser (localStorage) — no account, no server. Data is tied to the browser and file location/URL it runs from.

## Files

- `github-pages/` — hosting package (`index.html` + `apple-touch-icon.png`)
- `icon/` — app icon as `.ico` (Windows shortcut) and `.png`
- `export/` — intermediate build sources

## Run it on Windows (as an app window)

1. Save the standalone file somewhere permanent, e.g. `C:\Apps\DailyPlannerWidget.html`
2. Create a desktop shortcut with target:
   ```
   "C:\Program Files\Google\Chrome\Application\chrome.exe" --app="file:///C:/Apps/DailyPlannerWidget.html" --window-size=440,760
   ```
3. Optional: Properties → Change Icon → browse to `icon/Daily Planner.ico`
4. Pin to taskbar. Don't move the file afterwards — your data is tied to its path.

## Run it on iPhone

The app is hosted on Netlify at **https://importantdailyplanner.netlify.app**.

1. Open that URL in Safari (to update the hosted version, drag a new `index.html` into the Netlify Deploys page)
2. Share → **Add to Home Screen**
3. It opens fullscreen with the planner icon, like a native app

Note: each device keeps its own data — there is no sync.

## How the streak works

A day counts toward the streak when its completion percentage (checked leaf items ÷ planned leaf items) meets the target when the day is closed or rolls over. Weekends are free: Saturdays and Sundays never break the streak and skipping them carries it from Friday to Monday, and hitting the target on a weekend still adds to it. Missing a weekday or finishing below target resets the streak.
