# Development Flow

## Purpose
Create and iterate on the ZoneMinder modern userstyle CSS with Stylus-friendly configuration and responsive/mobile tuning.

## Workflow Summary
1. Open the ZoneMinder UI in Playwriter at `https://your-zoneminder-domain/index.php?view=event&eid=33`.
2. Inspect page structure with `getCleanHTML` and targeted `page.evaluate` to locate selectors.
3. Edit `zoneminder-modern.user.css` to apply style changes.
4. Refresh and inject the CSS into the Playwriter page for validation.
5. Capture screenshots with `screenshotWithAccessibilityLabels` to verify layout changes.
6. Iterate on layout, typography, and responsive breakpoints based on screenshots.

## Playwriter Loop
1. `page.goto` target view URL.
2. `page.waitForLoadState('load')` before inspection.
3. Use `getCleanHTML` or `page.evaluate` for selectors.
4. Inject CSS via `page.addStyleTag`.
5. Validate using `screenshotWithAccessibilityLabels`.

## Style Targets
- Consistent dark surfaces, borders, and accent colors.
- Tables, forms, and navigation elements share the same visual system.
- Mobile-first adjustments at `max-width: 767px`.
- Minimal, compact controls and status rows to conserve vertical space.

## Notes
- Use the Stylus `@var` domain field for user-specific hosts.
- Avoid hiding the video element at mobile breakpoints.
