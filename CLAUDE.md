# learn-js — Claude Code Guide

## What This Is

A personal JavaScript learning lab. Each experiment is a single self-contained HTML file demonstrating one concept — DOM manipulation, event listeners, state machines, animation with `setTimeout`. No build step, hosted on GitHub Pages.

---

## Tech Stack

- Vanilla HTML5/CSS3/JavaScript — no frameworks, no build step
- Single-file architecture: each experiment is one complete HTML file (inline `<style>` + inline `<script>`)
- Google Fonts: Share Tech Mono, Press Start 2P, Lora
- GitHub Pages hosting

---

## File Structure

```
learn-js/
  learnjs.html                    — first experiment: DOM manipulation & state machine
  front-end-dev.html              — random ping animation (flashing light)
  html-inline-css-js-template.html — blank template for new experiments
  plant-grow/
    plant-grow.html               — 14-frame plant growth animation
    plant1.png … plant14.png      — sprite frames
  image0.png … image4.png         — assets for learnjs.html
  tech-light.png                  — assets for front-end-dev.html
  tech-dark.png
  tech-darker.png
  plant1.png                      — root-level copy (used by learnjs.html)
```

---

## Experiments

| File | Concept | Key Technique |
|------|---------|---------------|
| `learnjs.html` | DOM manipulation, state machine | `getElementById`, `innerHTML`, `addEventListener`, cycling through 3 states with a counter, background image swap |
| `front-end-dev.html` | Async timing, random delays | `setTimeout` with random delay (`Math.random()`), recursive self-scheduling, image swap sequence |
| `plant-grow/plant-grow.html` | Frame-by-frame animation | Nested `setTimeout` calls stepping through 14 sprite frames, recursive loop with random rest delay |
| `html-inline-css-js-template.html` | — | Blank starting point for new experiments |

---

## Visual Style

Warm, hand-crafted palette used across experiments:

- Background: `#8c968c` (sage green) or `#f3e8c8` (parchment)
- Panels/cards: `#f3e8c8` with `border: 2px solid #504d43`, `border-radius: 10px`
- Accent blue: `#4a6fa5` / `#7a9fd4`
- Font: Share Tech Mono (monospace, readable, slightly retro)
- Shadows: `box-shadow: 2px 5px 10px rgba(0,0,0,0.5)`

---

## Coding Conventions

- Single-file HTML: `<style>` in `<head>`, `<script>` at end of `<body>`
- No shared code between experiments — each file is fully self-contained
- `getElementById` + direct `style` property mutation for all DOM updates
- `setTimeout` (not `setInterval`) for animation timing — recursive self-call at end of sequence
- State tracked as a plain `let` counter or flag variable, not an object

---

## Key Constraints

- Each experiment is monolithic — all changes happen in one file
- No shared JavaScript or CSS between experiments
- Image paths are relative to the HTML file — keep assets in the same folder
- New experiments should start from `html-inline-css-js-template.html`
- Sub-experiments with their own assets get their own subfolder (see `plant-grow/`)
