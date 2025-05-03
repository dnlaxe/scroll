# Scroll & Animation: 04-Multi-Directional Staggered Reveals

# Features

- Full-screen sections using `100vh` and scroll snapping for a clean vertical scroll experience.
- Each section contains multiple elements (`<h1>`, `<p>`, `<button>`) that:
  - Fade in and slide into view from a chosen direction.
  - Animate one after another with a delay, creating a staggered cascade effect.
  - Reset when scrolled out, allowing the animation to replay on re-entry.
- Declarative control using `data-direction`:
  - `[data-direction="down"]` for bottom-to-top reveal.
  - `[data-direction="left"]` and `[data-direction="right"]` for horizontal motion.
- Responsive typography scaling with media queries.
- Reusable `.reveal` class for any scroll-activated animation element.
- Minimal, accessible design using CSS variables for clean theming.

# Methods and Techniques Used

- **Viewport Units (`vh`)** to create full-screen scrollable sections.
- **Scroll Snap (`scroll-snap-type: y mandatory`)** for snapping alignment.
- **IntersectionObserver API** to detect section entry and exit.
- **Staggered Animation** using `setTimeout(i * 500)` for sequential reveals.
- **Custom Directions via `data-direction`** to define animation origin (`X` or `Y` axis).
- **Reusable Class-Based Animation** for consistency across sections.
- **CSS Transitions** for `opacity` and `transform` for smooth entry effects.
- **Responsive Design** with scalable font sizes using media queries.
- **CSS Variables** (`--fg`, `--bg`, `--neon`) to manage colors and themes.

