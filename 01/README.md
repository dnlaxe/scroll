# Scroll & Animation: 01-Scroll Basics + Back to Top Button

# Features

- Sticky navigation bar that stays pinned to the top while scrolling.
- Full-screen sections using `100vh` for modern scroll-based layout.
- Floating "Back to Top" button that:
  - Starts hidden off-screen below the viewport.
  - Slides up into view once the user scrolls past 200px.
  - Smoothly scrolls the page back to the top when clicked.
- Large, minimal arrow button with fixed positioning in the bottom-right corner.
- Clean structure and responsive behavior with basic CSS variables for easy styling.

# Methods and Techniques Used

- **Viewport Units (`vh`)** to create full-height hero and content sections.
- **Sticky Positioning** using `position: sticky` to keep the navbar visible.
- **Fixed Positioning** for the back-to-top button anchored to the screen.
- **Scroll Detection** via `window.scrollY` to track user scroll position.
- **Class Toggling** (`.classList.add()` / `.remove()`) to control the visibility of the scroll button.
- **Smooth Scrolling** with `window.scrollTo({ top: 0, behavior: 'smooth' })`.
- **Slide-In Animation** using a `transition` on the `bottom` property (`-150px` → `20px`).
- **Responsive UI Enhancements** with flexible positioning (`right: 10px`).
- **CSS Variables** (`--fg`, `--bg`, `--neon`) for scalable theme customization.

