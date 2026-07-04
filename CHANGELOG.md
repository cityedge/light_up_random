# Changelog

## v1.0.0

### Added

- Initial public release candidate.
- Added local single-file HTML Light Up puzzle app.
- Added Japanese / English UI switching.
- Added dark theme UI.
- Added four board sizes:
  - 10 x 10 / Easy
  - 10 x 18 / Normal
  - 14 x 18 / Intermediate
  - 14 x 24 / Hard
- Added random puzzle generation.
- Added complete solver-based unique-solution checking.
- Added no-guess generation option based on the internal logical solver.
- Added clue-removal mode selector:
  - Unique-solution limit
  - Capped clue removal
- Added automatic forced capped clue removal for 14 x 24 boards.
- Added automatic board scaling so larger boards fit without board-level scrollbars.
- Added left-click light placement and right-click X mark memo placement.
- Added real-time lit-cell display.
- Added real-time light-conflict display.
- Added real-time clue satisfaction and clue-overflow display.
- Added reset and show-answer controls.
- Added seed input.
- Added detailed puzzle data dialog.
- Added internal quality score and difficulty estimate.
- Added detailed user guide.
- Added README, CHANGELOG, RELEASE_REVIEW, and MIT LICENSE files.

### Notes

- The app is designed around random generation rather than a fixed built-in puzzle book.
- Quality score and difficulty estimate are internal heuristic values, not official ratings.
- Larger boards and stricter generation settings can take longer to generate.
- Save data and achievements are planned as future extensions, but are not included in v1.0.0.
