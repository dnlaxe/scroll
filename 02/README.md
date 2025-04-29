# Scroll & Animation: 02-Intersection Observer + Parallax

# Features

- Full-screen sections (`100vh`) with scroll snapping for smooth page flow.
- Background images that fade in as the section becomes visible.
- Headings (`<h1>`) that fade in and drop down into view.
- Animated underline beneath each heading that draws from center on scroll.
- Smooth parallax effect where the heading moves slightly differently than the background image for a dynamic depth feeling.
- Responsive design using CSS variables for easy color and theme control.

# Methods and Techniques Used

- **Viewport Units (`vh`)** to create full-page scrollable sections.
- **Scroll Snap (`scroll-snap-type: y mandatory`)** to align sections perfectly while scrolling.
- **IntersectionObserver API** to detect when elements enter the viewport without expensive scroll event listeners.
- **Class Toggling** (`.classList.add()` / `.remove()`) to trigger CSS animations on scroll.
- **Opacity Transitions** for images (`img`) for smooth fade-in effects.
- **Drop-In Animation** for headings (`transform: translate()`) synchronized with opacity.
- **Underline Drawing Animation** using `::after` pseudo-elements with animated `width` transitions.
- **CSS Variables** (`--fg`, `--bg`, `--neon`) for scalable, easily adjustable themes.
- **Relative and Absolute Positioning** to layer text correctly over images.
- **Controlled Transition Timing** to sequence image fade-in, text drop, and underline drawing.
- **Parallax-Like Effect** by independently animating the heading position to add depth on scroll.
