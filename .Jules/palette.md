# Palette's Journal 🎨

## 2025-07-08 - Zero-State Repository UX
**Learning:** The "empty repository" state is a missed UX opportunity.
**Action:** Initialize with a high-quality README to establish a positive UX foundation immediately.

## 2025-07-14 - Accessible Foundation & Dark Mode
**Learning:** A "Zero-State" project benefits greatly from early adoption of accessibility landmarks and system-aware dark mode, providing a robust template for future growth.
**Action:** Always include a skip-to-content link and `color-scheme: light dark` in the initial HTML boilerplate.

## 2026-07-19 - Interactive Navigation Micro-UX
**Learning:** Providing fully keyboard-accessible dropdown menus using `aria-expanded`, combined with subtle hover states, click toggles, and Escape-key dismissals, greatly improves interaction accessibility for assistive technologies and power users alike.
**Action:** Always map toggle buttons using `aria-expanded` and implement Escape-key listener to quickly dismiss dropdown components while returning focus back to the menu toggle.

## 2026-07-21 - Click-Outside and Selection Auto-Close in Nav Menus
**Learning:** Mobile and keyboard users expect responsive dropdown navigation to close automatically upon selecting a link to prevent overlay blocking, and pointer users expect intuitive click-outside dismissal.
**Action:** Always pair dropdown expansion with selection-based auto-closure and a global click-outside listener to ensure seamless flow and visibility.
