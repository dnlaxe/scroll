# Scroll & Animation: 05-Scroll-Based Step Reveal (Scroller Timeline)

## Features

- **Scroll-based storytelling layout** with synchronized **timeline navigation**, **media playback**, and **step content**.
- Multi-panel layout:
  - **Sticky timeline** on the left with clickable visual progression.
  - **Sticky media panel** in the center displaying contextual videos.
  - **Scrollable step content** on the right that:
    - Fades in on scroll.
    - Triggers media changes on entry.
    - Highlights the corresponding step in the timeline.
- **Smooth media transitions** using fade-out/fade-in animation when changing video sources.
- **Responsive step reveal** based on scroll position with subtle Y-axis motion.
- **Sticky layout logic** allows sections to remain visible while scrolling through content.
- Minimalist, accessible design with **CSS variables** for theming.

## Methods and Techniques Used

- **Sticky Layouts**  
  Persistent visibility of timeline and media elements using `position: sticky`.

- **Viewport Triggers**
  - Manual visibility check using `getBoundingClientRect()` and scroll thresholds.
  - Current step detection via midpoint check (`rect.top <= window.innerHeight / 2`).

- **Media Swapping Logic**
  - Detects if media source needs to change.
  - Uses `.fade-out` class and `setTimeout` to coordinate video source change with visual fading.

- **Timeline Highlighting**
  - Timeline list items gain an `.active` class based on the current scroll step.
  - Uses `data-step` attributes for declarative step mapping.

- **Smooth Entry Animation**
  - Each `.step` fades and slides upward into view (`opacity`, `translateY`).
  - Animation resets when scrolled out.

- **CSS Transitions**  
  Elegant fade and slide effects for steps and media.

- **CSS Variables**  
  Defined as `--fg`, `--bg`, `--neon` to maintain theme consistency.

- **Responsive Layout**  
  Layout divided into `20% / 30% / 50%` for timeline, media, and steps.