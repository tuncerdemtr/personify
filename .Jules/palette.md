## 2024-05-22 - Focus Management in Vanilla JS SPA
**Learning:** Relying on `innerHTML` for rendering wipes the DOM and resets focus to `body`. This disorients screen reader users and breaks keyboard navigation flows, especially in quiz interfaces.
**Action:** Implement a `manageFocus` post-render hook that tracks state changes. If the screen changes, focus the main heading/input. If the content updates (like selecting an item), restore focus to the active element using a stable identifier (index/ID).
