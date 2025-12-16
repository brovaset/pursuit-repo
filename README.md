# pursuit-repo

Practice repo

## Phase 1 scaffold (implemented)

This commit adds a mobile-first HTML/CSS scaffold for the tournament news site:

- `index.html` — header, breaking news banner, demo scoreboard, team news grid, organization spotlight, footer
- `styles/styles.css` — CSS variables and responsive component styles (host colors included)
- `assets/logo.svg`, `assets/placeholder.svg` — logo + placeholder images
- `scripts/main.js` — small JS (nav toggle, demo ticker)

Notes: content is placeholder/demo only. Editorial rules and full content pages will be added in subsequent phases.

## Phase 1 polishing

- Accessibility: Added a skip link and improved keyboard focus behavior for the mobile nav (Escape closes and focus returns to the toggle).
- Performance: Preloaded `styles.css` to reduce render blocking and added `decoding="async"` and `srcset` attributes to images.
- Favicons: Added `assets/favicon.svg`.
- Minor: improved ticker rotation logic and added meta `theme-color`.

## Phase 2 (initial)

- Added `schedule.html`: a schedule page stub with team/date client-side filtering (sample entries provided).
- Added a `Multimedia Highlights` gallery on the homepage with an accessible lightbox viewer.
- Refined news cards with subtle team color accents and improved gallery/thumb styles.
- Added lightbox keyboard handling (Esc to close) and ensured focus management when opening viewer.

### Responsive images / WebP guidance

- Replaced inline placeholders with responsive `srcset`/`sizes` variants (`assets/placeholder-320.svg`, `placeholder-640.svg`, `placeholder-1200.svg`) and updated markup to use them.
- Recommendation: convert placeholder SVGs to optimized photographic `WebP` images and place them under `assets/webp/`.
- Helper script: `./scripts/convert-to-webp.sh` (uses `cwebp` and `rsvg-convert` for SVG rasterization) — run locally if `cwebp` is installed.
- After adding real images, update the `srcset` entries to point at `assets/webp/<name>-320.webp` etc for best performance.
