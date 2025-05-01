# Scroll & Animation: 03-Parallax Hero, Sticky Nav & Scroll Reveal

# Features

- Full-screen hero section with three parallax layers:
  - **Background** layer that scrolls the slowest.
  - **Midground** image that scrolls fastest for contrast.
  - **Foreground heading** with moderate motion.
- Smooth parallax effect using `transform: translateY(...)` and scroll position.
- Sticky navigation bar that stays fixed to the top of the screen.
- Navigation bar gains a subtle bottom border when scrolled below the hero.
- Hamburger menu design for mobile responsiveness.
- Centered downward arrow that:
  - Stays visually aligned on screen.
  - Smooth-scrolls to the content section when clicked.
- Scroll-triggered reveal animation for content:
  - `.content` fades in and slides upward when entering the viewport.
  - Effect resets on scroll-out, allowing repeated entry animations.
- Responsive design with layout and typography adjustments on smaller screens.

# Methods and Techniques Used

- **Parallax Effect** using `window.scrollY` and `transform: translateY(...)` on layered elements.
- **Fixed Navigation Bar** with `position: fixed`, `z-index`, and media queries.
- **Scroll Detection** to add `.scrolled` class using `window.scrollY` and a custom threshold.
- **IntersectionObserver API** to detect when `.content` enters or exits the viewport.
- **Class Toggling** for scroll-in/out animations (`.visible` class).
- **Smooth Scrolling** via `.scrollIntoView({ behavior: 'smooth' })`.
- **Responsive Design** using media queries for font sizes and mobile nav behavior.
- **CSS Variables** (`--fg`, `--bg`, `--neon`) for scalable, themeable color handling.
- **Will-change and layering strategies** for parallax performance and stacking context.