# HCI Study Notes

A small one-page website with simple notes on Human–Computer Interaction (HCI). It also has a tracking panel at the bottom that shows how a visitor uses the page.

This is an HCI course project.

## How to open

1. Keep everything in one folder (only `index.html` is needed).
2. Double-click `index.html`. It opens in your browser.

No installation, no internet, no server needed.

## What is on the page

- **Introduction** – what HCI is
- **Heuristics** – the usability principles, shown as cards
- **Diagrams** – design process, gulfs of execution and evaluation, Fitts's law
- **Laws** – short notes on the main laws

There is also a **Dark / Light** button at the top to change the theme.

## Tracking panel

Tracking starts automatically when the page opens. Nothing is asked.

The panel at the bottom shows:

- Time spent on the page
- Number of clicks
- Number of key presses
- How far the page was scrolled (%)
- How much the mouse moved (px)

### Buttons

| Button | What it does |
|---|---|
| ▼ Hide / ▲ Tracking | Hides or shows the panel. Tracking keeps running while it is hidden. |
| 🔴 Show click dots | Shows a numbered red dot on every place you clicked. |
| ⏸ Pause / ▶ Resume | Stops or continues tracking. |
| 📋 Log | Opens a list of the latest 40 events (click, key press, time, position). |
| ⬇ Export | Downloads all the data as `interaction-data.json`. |
| 🗑 Clear | Deletes all recorded data (it asks first, and you can Undo right after). |

### Keyboard shortcuts

- `Alt + D` – dark / light mode
- `Alt + T` – show / hide click dots
- `Alt + P` – pause / resume tracking
- `Alt + H` – hide / show the panel

## What is saved

- Clicks (what was clicked and where)
- Key presses (only that a key was pressed, **never what was typed**)
- Scroll depth, mouse distance, and time spent in each section
- The last 500 events are kept. Older ones are dropped.

## Privacy

All data stays in the browser. Nothing is sent to any server. If you refresh or close the page, the data is gone, so use **Export** before leaving if you want to keep it.

## Exported file

`interaction-data.json` has two parts:

- `summary` – total time, clicks, key presses, mouse distance, max scroll %, and seconds spent in each section
- `events` – the full list of events with time, type, target and position

If the download is blocked by the browser, the data opens in a new tab instead. You can copy or save it from there.

## Code and languages

All the code is inside one file: `index.html`. There are no other code files.

| Part | Language | Where in `index.html` | What it does |
|---|---|---|---|
| Page structure and text | HTML | Main part of the file (`<nav>`, `<main>`, `<footer>`, `<aside>`) | Headings, notes, buttons, the tracking panel layout |
| Diagrams | SVG (written inside HTML) | Inside the Diagrams section | Design process, gulfs and Fitts's law drawings |
| Look and design | CSS | Inside the `<style>` tag at the top | Colors, layout, cards, dark / light theme, the tracking panel and red dots |
| Behavior | JavaScript | Inside the `<script>` tag at the bottom | Tracking (clicks, keys, scroll, mouse), live counters, Log, Export, Clear / Undo, Pause, Hide panel, dark mode and keyboard shortcuts |

The heuristics cards are also created by JavaScript from a list in the script.

## Files

- `index.html` – the whole project (HTML, CSS and JavaScript in one file)
- `README.md` – this file
