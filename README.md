# Palette Studio

A designer tool for building color systems on a perceptually uniform **OKLCH** foundation — so saturation and luminosity behave the way your eye expects, not the way HSL mangles them.

**Live:** _(Vercel URL)_

## What it does

- **Matrix generator** — declare a system once (N evenly-spaced hues × a tone ramp × saturation sets) and the whole board builds itself. Change the base hex and every hue rotates together.
- **Base color** as the theme anchor — edit hex or drag L / C / H.
- **Tone ramps** with darkest/lightest lightness, hue drift, chroma taper, and luminosity snapping (shared tonal grid).
- **Hue spectrum** rows and a **full spectrum atlas** (all hues × lightness tiers), with vivid gamut-max chroma.
- **Neutrals** — near-gray ramps tinted across the spectrum, with their own saturation control, below a divider.
- **Two backgrounds** — the board color (exports) and the workspace behind (tool only).
- **Exports** — SVG, PNG (2×), CSS variables, and design tokens. The board is WYSIWYG: what you see is what exports.

## Running locally

It's a single static file. Open `index.html`, or serve it:

```bash
python3 -m http.server 4201
```

Then visit `http://localhost:4201`.

## Stack

No build, no dependencies — vanilla HTML/CSS/JS in one file. Color math is a from-scratch sRGB ↔ OKLab/OKLCH implementation with binary-search gamut fitting.
