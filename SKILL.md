---
name: toggle-dashboard-theme
description: Use when adding, moving, or refining a light and dark theme toggle in a dashboard, especially when the switch must persist user preference, live in a fixed corner, and render both themes correctly after refresh.
---

# Toggle Dashboard Theme

## Overview
A theme toggle should feel native to the dashboard, not bolted on. Keep a single source of truth for the current theme, persist it, and verify both themes after reload.

## Quick Reference
- Store the selected theme in local storage.
- Toggle the `dark` class on `document.documentElement`.
- Keep the control in a fixed, low-friction location such as the bottom-left corner.
- Re-render and verify both light and dark themes after refresh.

## Workflow
1. Introduce one reactive theme state.
2. Read the stored preference on mount and apply it immediately.
3. Toggle the root `dark` class when the button is clicked.
4. Persist the next theme value.
5. Verify the button location, icon, and copy in both modes.

## Common Mistakes
- Creating multiple theme states across components.
- Updating the button label without updating the actual root class.
- Forgetting persistence, so the page resets on reload.
- Placing the button where it collides with drawers, modals, or mobile safe areas.

## Example
Use when the user says: ?????????????????, ????????????, or ????????????????.
