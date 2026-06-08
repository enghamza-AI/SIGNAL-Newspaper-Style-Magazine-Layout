# 🗞️ SIGNAL — Newspaper-Style Magazine Layout

Week 1 project from the Diamond Fullstack Roadmap.

https://signal-newspaper-style-magazine-lay.vercel.app/

## Folder Structure

```
magazine-layout/
├── index.html        ← All HTML (semantic structure)
├── css/
│   └── style.css     ← All styles (variables, grid, flexbox, responsive)
├── assets/           ← Empty for now; add images here later
└── README.md         ← This file
```

## What This Project Demonstrates

| Concept | Where |
|---|---|
| Semantic HTML5 (`nav`, `header`, `main`, `aside`, `article`, `footer`) | `index.html` |
| CSS Grid (3-column page layout) | `.page-grid` in style.css |
| CSS Grid (hero layout with named areas) | `.hero` in style.css |
| Flexbox (card rows, sidebar, footer) | `.cards-row`, `.sidebar`, `.footer__inner` |
| CSS Variables (design tokens) | `:root` in style.css |
| CSS-only dark/light toggle | `:has()` selector + hidden checkbox |
| Sticky nav | `position: sticky` on `.nav` |
| Sticky sidebar | `position: sticky` on `.sidebar` |
| Responsive design (320px → 1440px) | Media queries at bottom of style.css |
| Hover micro-interactions | `.card:hover`, `.tag:hover`, `.card__link:hover` |
| `clamp()` fluid typography | `font-size: clamp(...)` in hero + card titles |
| BEM naming convention | `.card__body`, `.nav__links`, `.sidebar__heading` |

## Key CSS Concepts Used

### CSS Grid Named Areas
```css
.hero {
  grid-template-areas:
    "kicker  kicker"
    "title   subtitle"
    "title   meta";
}
```

### CSS :has() for Dark Mode (no JS!)
```css
body:has(#theme-toggle:checked) {
  --color-bg: #f5f2eb;  /* All variables switch at once */
}
```

### Fluid Typography with clamp()
```css
font-size: clamp(3.5rem, 7vw, 7rem);
/* min: 3.5rem | preferred: 7% viewport width | max: 7rem */
```

