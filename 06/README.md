# Scroll & Animation: 06-Image Grid Reveal, Hover Zoom & Caption Fade

## Features

- **Masonry-style image grid** using CSS Grid with custom area placement for a dynamic layout.
- **Scroll-triggered reveal animation**:
  - Each `.photo` fades in and slides upward when entering the viewport.
  - Animation resets on scroll-out for repeated reveal on re-entry.
- **Hover effect** on images:
  - Slight zoom (`scale(1.05)`) for interactivity.
  - Caption slides in from below with a semi-transparent overlay.
- **Captions**:
  - Displayed on hover with smooth fade-in and translateY effect.
  - Positioned at the bottom of each image for clarity.
- **Responsive Design**:
  - Grid layout switches to a single-column stack on screens under 600px.
  - Maintains square aspect ratios using `aspect-ratio` and auto adjustments.

## Methods and Techniques Used

- **CSS Grid Layout** with manually assigned `grid-area` values for unique, artistic placement.
- **Scroll Reveal Animation** via `IntersectionObserver`:
  - Watches `.reveal-img` elements and toggles `.reveal` class based on visibility.
- **CSS Transitions** for smooth appearance and hover interactions:
  - `transform` and `opacity` transitions enhance both scroll-in and hover behaviors.
- **Hover Effects**:
  - Image scale and caption reveal using `:hover` selectors.
  - Maintains performance with GPU-accelerated transforms.
- **Lazy Loading** with `loading="lazy"` on images to optimize performance.
- **CSS Variables** (`--fg`, `--bg`, `--neon`) for easy theme control.
- **Mobile Optimization** using `@media` queries to adapt layout and grid behavior on small screens.

## Design Notes

- Minimalist typography with a monospace font for a clean, modern aesthetic.
- Balanced white space and consistent `gap` for an open visual feel.
- Use of `z-index` layering ensures hover effects display clearly without overlap.
