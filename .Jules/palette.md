## 2026-10-07 - Browser Chrome Theme-Color Synchronization
**Learning:** Mobile and desktop browsers format top browser chrome and address bars according to the `<meta name="theme-color">` HTML tag. Dynamically updating `meta[name="theme-color"]` when users toggle between light and dark themes ensures complete visual harmony between web app content and native browser chrome.
**Action:** Always include `<meta name="theme-color">` in `<head>` and update its `content` attribute synchronously inside theme toggle logic.
