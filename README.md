# Light Up Random v1.0.0

Light Up Random は、ブラウザだけで動作する単体HTML版の Light Up パズルアプリです。固定問題集ではなく、ユーザーが選んだ盤面サイズと生成条件に応じて、その場でランダム問題を作成します。

This is a local browser-based random Light Up puzzle app. It generates uniquely solvable puzzles in the browser and lets you solve them with simple mouse operations.

## Main features

- Single-file local HTML app
- Japanese / English UI switch
- Dark theme interface
- Four board sizes:
  - 10 x 10 / Easy
  - 10 x 18 / Normal
  - 14 x 18 / Intermediate
  - 14 x 24 / Hard
- Random puzzle generation with unique-solution checking
- Optional no-guess puzzle generation
- Two clue-removal modes:
  - Unique-solution limit
  - Capped clue removal
- Automatic board scaling to avoid board scrollbars
- Left-click to place/remove a light
- Right-click to place/remove an X mark
- Real-time rule feedback for lit cells, light conflicts, satisfied clues, and clue overflow
- Show answer / reset
- Seed input for reproducibility within the same app version and generator behavior
- Detailed puzzle data dialog for generation metrics, quality score, difficulty estimate, solver stats, clue-removal stats, and board structure metrics

## Recommended environment

Recommended:

- Desktop Google Chrome or Microsoft Edge
- A reasonably modern PC for larger boards

The app may also run in other modern browsers. Large-board generation can take time, especially when no-guess generation and strong clue removal are selected.

## Privacy

Puzzle generation, solving, quality evaluation, and play state are processed locally in the browser. This app does not upload puzzle data or user operations to a server.

When published via GitHub Pages, GitHub only serves the static files. The actual puzzle generation runs in the user’s browser.

## Files in this repository

- `index.html` — application body
- `README.md` — project overview
- `USER_GUIDE.md` — detailed user guide
- `CHANGELOG.md` — version history
- `RELEASE_REVIEW.md` — release review notes
- `LICENSE` — MIT License

## Basic usage

1. Open `index.html` in a browser.
2. Select a board size.
3. Choose whether to allow guessing.
4. Choose a clue-removal mode.
5. Press **New Puzzle**.
6. Place lights with left click.
7. Place X marks with right click.
8. Solve the puzzle.

## GitHub Pages

For GitHub Pages publication, place `index.html` and the Markdown documents in the repository root. No build step is required.

## License

MIT License. See `LICENSE`.
