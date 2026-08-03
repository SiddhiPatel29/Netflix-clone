**[Live Demo](https://siddhipatel29.github.io/Netflix-clone/)**

# Netflix Clone

A front-end clone of the Netflix landing page, built with plain **HTML and CSS only** (no JavaScript, no frameworks).

## Features

- **Hero section** with background image, gradient overlay, and an animated red curve dividing the hero from the content below
- **Trending Now** horizontally scrolling movie row
  - Left/right scroll arrows powered by CSS scroll-snap and anchor links (no JS)
  - Arrows crossfade in/out based on scroll position using CSS scroll-driven animations (`animation-timeline`), with a static fallback for browsers that don't support it yet
  - Large numbered overlays on each poster (Netflix-style ranking)
- **More reasons to join** section with custom inline SVG icons (TV cast icon, download icon, paper-plane icon, kids-profile icon) on gradient card backgrounds
- **Frequently Asked Questions** accordion-style rows (Font Awesome plus icons)
- **Footer** with:
  - Email signup CTA
  - 4-column link grid
  - Language selector
  - Region text and reCAPTCHA notice
- **Fully responsive** — fluid layout using `clamp()` and CSS Grid, with breakpoints at 1150px, 1024px, 768px, and 480px

## Tech Stack

- HTML5
- CSS3 (Flexbox, Grid, CSS custom properties, scroll-driven animations)
- [Font Awesome](https://fontawesome.com/) (via CDN) for icons
- No JavaScript, no build tools — open `index.html` directly or serve with any static server (e.g. Live Server)

## Project Structure

```
├── index.html
├── style.css
└── assets/
    ├── logo.svg
    ├── img2.jpg          # hero background
    └── movie1.webp ... movie10.webp   # trending row posters
```

## Running Locally

1. Clone the repo
2. Open `index.html` directly in a browser, **or** serve it with a local dev server (recommended, e.g. VS Code's Live Server extension) so relative asset paths resolve correctly
3. No install step, no dependencies to run

## Browser Support Notes

- The scroll-arrow crossfade animation relies on CSS scroll-driven animations (`animation-timeline`), currently supported in Chromium-based browsers (Chrome, Edge, Opera). Other browsers will still show the arrows, just without the scroll-linked fade — this is handled gracefully via `@supports`.

## Known Limitations

- This is a static front-end clone for learning/demo purposes — there is no backend, authentication, or video playback functionality
- Movie posters and logo are placeholder assets and must be supplied locally under `assets/`
- Footer and FAQ links are placeholders (`href="#"`)

## Acknowledgements

Built as a learning project to practice responsive layout, CSS-only interactivity, and recreating a real-world UI from scratch.