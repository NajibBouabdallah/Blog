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

## 2026-07-23 - CSS Specificity Overrides on the HTML Hidden Attribute
**Learning:** Adding custom display styles (e.g. `display: inline-block`) on components like loader spinners overrides the default browser display style for the HTML `hidden` attribute. This can result in elements remaining visible even when they are programmatically toggled with the `hidden` attribute.
**Action:** Always explicitly define style rules like `.spinner[hidden] { display: none; }` or a global `[hidden] { display: none !important; }` utility to ensure reliable visibility state changes for assistive technologies and users.

## 2026-07-27 - CSS Transforms on SVG Elements for Intuitive State Changes
**Learning:** An active dropdown toggle button benefits from an animated icon transition, such as translating and rotating hamburger lines into a close "X" symbol. This provides a direct, delightful, and highly visible indicator of state change.
**Action:** Implement `transform-origin: center` and transition the `transform` and `opacity` properties of SVG lines when `aria-expanded` toggles between true and false.

## 2026-07-28 - Explicit color-scheme Overrides for Manual Theme Toggle
**Learning:** Setting a custom HTML root theme attribute (e.g. `data-theme="dark"`) does not automatically adjust the browser's default system rendering unless `color-scheme` is explicitly configured. This can cause default form controls and background canvas elements to mismatch when manually toggled.
**Action:** Always pair custom theme attributes with explicit CSS `color-scheme: light` and `color-scheme: dark` rules, and ensure toggle icons represent the *target* transition state (e.g. show a moon icon in light mode to switch to dark) for intuitive, accessible navigation.

## 2026-07-29 - Asynchronous Form Processing Screen-Reader UX and Focus Routing
**Learning:** Asynchronous form submissions should immediately update polite aria-live regions with an active loading feedback text (e.g. "Subscribing...") rather than clearing them. This ensures screen readers announce the processing state instantly. Furthermore, keyboard-based bypass links (like skip-to-content) require the target landmark to possess `tabindex="-1"` and a custom outline reset to correctly shift programmatic focus across browsers without visual layout shifts.
**Action:** Always populate polite live regions with an active processing status on submit, and ensure any skip link target element includes `tabindex="-1"` and a focused style override.
