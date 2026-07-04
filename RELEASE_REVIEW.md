# Release Review: Light Up Random v1.0.0

This document summarizes the review performed before packaging Light Up Random v1.0.0.

## Scope

v1.0.0 is the first public release candidate. It provides a browser-only random Light Up puzzle app with local puzzle generation, unique-solution checking, no-guess filtering, clue reduction, quality scoring, and difficulty estimation.

## Reviewed areas

### Application versioning

- Updated browser title to `Light Up Random v1.0.0`.
- Added visible `v1.0.0` version badge in the app header.
- Added app version display in the detailed puzzle data dialog.
- Prepared GitHub-facing release package with `index.html`.

### User interface

- Confirmed compact two-row generation UI:
  - board size
  - guessing option
  - clue-removal option
  - New Puzzle / Reset / Show Answer buttons
- Moved seed input near the detailed puzzle data button.
- Moved debug-heavy metrics into the Detailed Puzzle Data dialog.
- Kept normal screen focused on puzzle play and achievement-relevant metrics.
- Added browser-native tooltips for major controls and detailed data labels.

### Board sizes and scaling

- Replaced square experimental board set with four release-facing sizes:
  - 10 x 10
  - 10 x 18
  - 14 x 18
  - 14 x 24
- Confirmed automatic board scaling is used to avoid board-level scrollbars.
- Confirmed 14 x 24 forces capped clue removal to avoid excessive generation time and overly sparse clue layouts.

### Puzzle generation

- Random generator creates a full candidate solution first.
- Clues are derived from adjacent lights around black cells.
- Complete solver is used to confirm unique solution.
- No-guess mode uses logical solver completion as an acceptance condition.
- Generation continues until a puzzle matching the selected conditions is found.
- UI enters a waiting state during generation.

### Solvers and evaluation

- Complete solver checks solution uniqueness.
- Logical solver estimates whether a puzzle can be solved without guessing.
- Quality score and difficulty score are displayed as heuristic internal estimates.
- Heavy only-cover patterns are tracked and reflected in quality scoring.
- Detailed metrics are available in the Detailed Puzzle Data dialog.

### Documentation

- Added `README.md`.
- Added detailed `USER_GUIDE.md`.
- Added `CHANGELOG.md`.
- Added this release review.
- Added MIT `LICENSE`.

## Technical checks

- Extracted embedded JavaScript from `index.html` and ran `node --check` successfully.
- Confirmed package includes:
  - `index.html`
  - `README.md`
  - `USER_GUIDE.md`
  - `CHANGELOG.md`
  - `RELEASE_REVIEW.md`
  - `LICENSE`

## Known limitations

- Save data is not implemented in v1.0.0.
- Achievements are not implemented in v1.0.0.
- Puzzle-book mode is not implemented in v1.0.0.
- The seed is useful for reproduction within the same version and settings, but is not a permanent compatibility guarantee.
- Quality score and difficulty score are heuristic values.
- The logical solver does not represent every possible human solving technique.
- Generation runs on the main thread in v1.0.0, so the UI may temporarily pause during heavy generation.

## Release assessment

The package is suitable for the v1.0.0 GitHub release and GitHub Pages publication.
