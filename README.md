# Advanced Chess Game with Adaptive AI

Welcome to the **Advanced Chess Game with Adaptive AI**, a fully interactive, single-file HTML5 chess game built with JavaScript and Canvas. Play against an AI with adjustable difficulty levels, review move history, undo moves, and save the game locally to play offline—all from your browser!

Live demo: [https://aivoarm.github.io/Chess/](https://aivoarm.github.io/Chess/)

## Features

- **Adaptive AI**: Choose from five difficulty levels (Beginner to Master). The AI uses a local minimax algorithm with alpha-beta pruning and a Stockfish API fallback when online.
- **Interactive UI**: Drag pieces on a responsive chessboard, with visual highlights for valid moves and checks.
- **Move History**: Track and revert to any previous move.
- **Undo & Hint**: Undo your last move or get a hint for your next one.
- **Captured Pieces**: See captured pieces displayed for both sides.
- **Save Locally**: Download the game as a single `chess_game.html` file to play offline.
- **Responsive Design**: Works on desktop and mobile devices with touch support.
- **Social Media Ready**: Share the game with a custom chessboard preview (inline PNG).

## How to Play

1. **Online**: Visit [https://aivoarm.github.io/Chess/](https://aivoarm.github.io/Chess/) in your browser.
2. **Move Pieces**: Click and drag (or tap and drag on mobile) to move White pieces. The AI plays Black.
3. **Adjust Difficulty**: Use the "AI Level" dropdown to set the AI’s strength (1-5).
4. **Game Controls**:
   - **Undo Move**: Revert your last move.
   - **New Game**: Reset the board.
   - **Hint**: Highlight a suggested move.
   - **Save Game Locally**: Download `chess_game.html` to play offline.
5. **Offline**: Open the downloaded `chess_game.html` in a browser. The AI will use the local fallback without internet.

## Installation

No installation is required to play online! To host or modify the game yourself:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/aivoarm/Chess.git
   cd Chess
