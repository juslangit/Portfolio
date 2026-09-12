# Portfolio

Personal portfolio site for **Luqman Hakeem** — AI full stack developer, Cyberjaya, Malaysia.

**Live:** https://juslangit.github.io/Portfolio/

## What it is

A single self-contained `index.html`. No build step, no bundler, no framework,
no `node_modules`. Open the file in a browser and it works.

| Piece | How |
|---|---|
| Layout | Pastel bento grid, CSS Grid, 12 columns collapsing to 1 |
| Hero 3D | Three.js r128 (cdnjs UMD) — a flat-shaded icosahedron that leans toward the cursor |
| Cursor | Custom dot + lagging ring, disabled on touch and for reduced motion |
| Reveal | `IntersectionObserver`, staggered, with count-up numbers |
| Easter egg | *Kedai Runtuh* — a canvas mini stacker. Konami code, or the 🍜 in the footer |

## Design tokens

Warm paper background `#faf7f2`, ink `#2b2622`, six pastel card fills
(mint, peach, lilac, sky, butter, rose). 26px radius, soft two-layer shadows,
Plus Jakarta Sans.

## Accessibility & degradation

- Everything respects `prefers-reduced-motion` — reveals, tilt, cursor, confetti and the 3D scene all switch off.
- The 3D hero is wrapped in `try/catch`: no WebGL means the canvas is removed and the rest of the page is untouched.
- Skip link, visible focus rings, `Escape` closes the game, keyboard drop with `Space`.
- Works at 360px wide.

## Editing

Everything lives in `index.html`:

- **Content** — the `<main>` block, top to bottom: hero, stats, work, 3D & games, about, contact.
- **Colours** — the `:root` block at the top of `<style>`.
- **Behaviour** — the numbered sections in the final `<script>`.

## Deploy

Pushing to `main` publishes automatically via GitHub Pages.
