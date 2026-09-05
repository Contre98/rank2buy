# Rank2Buy

A tiny web app for listing things you want to buy and ranking them by what
matters: **urgency**, **need**, and **impact**.

## Use it

Open `index.html` in a browser. That's it — no build step, no server, no
dependencies. Everything is one self-contained HTML file, and your list is
saved in the browser's `localStorage`.

To host it, drop `index.html` on any static host (GitHub Pages, Netlify, etc.).

## How ranking works

Each item gets three scores from 1–10:

| Factor  | Question it answers            |
| ------- | ------------------------------ |
| Urgency | How soon do I need it?         |
| Need    | Necessity vs. nice-to-have     |
| Impact  | How much will it change things?|

The list is sorted by a weighted average of the three, shown out of 10. The
**Weighting** panel lets you change how much each factor counts — set need to 0
and impact to 3, say, and the list re-ranks instantly.

## Features

- Add items with an optional price
- Adjust any item's scores inline; the ranking updates as you go
- Mark items bought (and show/hide them)
- Export the ranked list as plain text to the clipboard
- Works offline, adapts to your system's light/dark theme
