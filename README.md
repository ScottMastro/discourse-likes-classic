# Discourse Likes Classic

A Discourse theme component that restores the pre-#39283 likes UI for forums that use likes only (no multi-reaction setup).

## What it does

Discourse PR [#39283](https://github.com/discourse/discourse/pull/39283) split the like-count into its own post-menu slot (rendered on the left) and replaced the liked-users popup with a filterable list that shows avatars, names, and per-user reaction icons. This component reverts that UI to something closer to the classic look:

- **Position**: moves the like-count button back to the right, next to the like heart, matching the old "double-button" layout.
- **No duplicate heart**: hides the heart icon on the count trigger so the adjacent like toggle isn't duplicated.
- **Popup as avatar grid**: replaces the stacked list with a compact grid of avatars (no names, no trailing heart icon).
- **Fit-to-content popup**: the popup shrinks to the grid size when there are only a few likers; wraps to a new row after 8 avatars.

## When to use

This is intended for forums where users only leave likes (no custom reactions). If you have multiple reaction types enabled, the filter UI this component hides is useful and you probably don't want this.

## Install

Admin → Customize → Themes → Install → *From a git repository*:

```
https://github.com/ScottMastro/discourse-likes-classic
```

Then add it as a component to your active theme.
