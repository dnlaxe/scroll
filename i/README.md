# Microproject I – Sticky Panels, Progress Bar & Scroll-Triggered Animations

# Features

- Scrollable landing page composed of full-screen sticky `.panel` sections.
- Smooth progress bar at the top that:
  - Fills as the user scrolls down the page.
  - Updates in real time using `window.scrollY` and `document.documentElement.scrollHeight`.
- Scroll-triggered text animation:
  - Headings and paragraphs in each panel fade in and slide upward when the section enters view.
  - Resets on scroll out to enable replay on re-entry.
- Section 3 includes two animated `.square` cards that:
  - Scale up and fade in when visible (`IntersectionObserver` with `threshold: 0.5`).
  - Reset when scrolled out for reusability.
- Sticky behavior using `position: sticky` on panels for immersive transitions.
- Mobile-friendly `vh` unit fix for mobile browsers (like iOS Safari and Chrome):
  - Uses `visualViewport` and custom `--vh` CSS variable to calculate height correctly.
- Responsive design with `clamp()` font scaling and column-to-stack flex layout on smaller screens.

# Methods and Techniques Used

- **Sticky Positioning** (`position: sticky`) for panels that stay fixed during scroll until pushed by the next section.
- **IntersectionObserver API** to detect when panels and `.square` cards enter and exit the viewport.
- **Scroll Progress Tracking** using `scrollY / scrollable height` to calculate scroll percentage.
- **CSS Transitions** (`opacity`, `transform`, `scale`) to animate reveal and scale-up effects.
- **Viewport Height Correction** using `--vh` CSS variable and `visualViewport.height` to ensure 100% height on mobile devices.
- **Media Queries** for responsive design and layout shifts on smaller screens.
- **CSS Variables** (`--fg`, `--bg`, `--neon`, `--gray`) for consistent theming.