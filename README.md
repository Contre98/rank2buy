# Rank2Buy

A tiny web app for listing things you want to buy and ranking them by what
matters: **urgency**, **need**, **impact**, **want**, and **cost**.

## Use it

Open `index.html` in a browser. That's it — no build step, no server, no
dependencies. Everything is one self-contained HTML file, and your list is
saved in the browser's `localStorage`.

To host it, drop `index.html` on any static host (GitHub Pages, Netlify, etc.).

## How ranking works

Each item gets five scores from 1–10:

| Factor  | Question it answers             | Direction        |
| ------- | ------------------------------- | ---------------- |
| Urgency | How soon do I need it?          | higher = sooner  |
| Need    | Necessity vs. nice-to-have      | higher = sooner  |
| Impact  | How much will it change things? | higher = sooner  |
| Want    | How much do I just want it?     | higher = sooner  |
| Cost    | 1 = cheap, 10 = expensive       | higher = *later* |

**Cost runs backwards on purpose.** An expensive thing should be harder to
justify, so cost enters the ranking flipped (a 10 counts as a 1). It's the amber
slider, so you can see at a glance which factor is arguing against the purchase.

The list is sorted by a weighted average of the five, shown out of 10. The
**Weighting** panel lets you change how much each factor counts — drop cost to 0
to ignore price entirely, or push it to 3 to let cheap wins rise — and the list
re-ranks instantly. **Reset** puts every weight back to 1.

## Features

- Add items with an optional price
- Adjust any item's scores inline; the ranking updates as you go
- Mark items bought (and show/hide them)
- Export the ranked list as plain text to the clipboard
- Works offline, adapts to your system's light/dark theme
