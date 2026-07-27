# French Tracker

A small collection of browser-based tools for tracking daily French study habits and TCF practice progress.

Everything runs locally in the browser. There is no framework, build process, account, or backend required. Progress and preferences are saved on the device using `localStorage`.

## Trackers

### French Daily

`daily-tracker.html` is a daily checklist for keeping a consistent French-learning routine.

Features:

- Daily study checklist
- Completion percentage and animated progress ring
- Completed tasks automatically move to the bottom
- Study streak tracking
- Light and dark modes
- Saved theme preference
- Confetti after completing every task
- Mobile-friendly layout and haptic feedback on supported devices

Use **New Day Reset** to clear the checklist. If every task was completed before the reset, the streak increases by one day.

### TCF Master Tracker

`comprehension.html` is the recommended TCF tracker. It tracks repeated practice across 40 reading exercises and 40 listening exercises.

Features:

- Separate reading (CE) and listening (CO) sections
- Configurable 3, 5, or 10 attempts per exercise
- Exercise and overall completion tracking
- Search exercises by number
- Hide completed exercises
- Reset individual exercise rows
- Manual light and dark modes
- JSON backup and restore
- Confetti when all attempts for an exercise are complete
- Progress saved locally in the browser

### TCF Practice Tracker (v1)

`comprehension-v1.html` is the original, simpler TCF tracker. It provides separate CE and CO sections, question-level completion tracking, progress statistics, and automatic device-based theming.

## Getting Started

1. Download or clone this repository.
2. Open the tracker you want in a modern browser:
   - `daily-tracker.html`
   - `comprehension.html` (recommended for TCF practice)
   - `comprehension-v1.html`
3. Start marking tasks or practice questions as complete.

No installation is necessary.

## Project Structure

```text
french-tracker/
├── daily-tracker.html
├── comprehension.html
├── comprehension-v1.html
└── README.md
```

## Data Storage

The trackers store progress in the browser's `localStorage`. This means:

- Progress remains available after refreshing or closing the page.
- Data is specific to the browser and device being used.
- Clearing browser site data will remove saved progress.
- No study data is sent to a server.

The main TCF tracker can export its progress to a `tcf_backup.json` file. Use **Restore** to import that file later or move progress to another browser or device.

The pages load the Canvas Confetti library from a CDN, so confetti effects require an internet connection. Core tracking features continue to work without it once the page is available locally.

## Customization

The project uses plain HTML, CSS, and JavaScript. To change the daily routine, edit the `tasks` array inside `daily-tracker.html`:

```js
const tasks = ["writing", "speaking", "listening"];
```

You can also adjust the colors in the CSS variables near the top of each HTML file.

## Browser Support

Use a current version of Chrome, Edge, Firefox, or Safari. `localStorage` must be enabled for progress to persist.
