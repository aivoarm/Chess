♟️ Advanced Chess Game with Stockfish AI

📌 Overview

This is an interactive chess game featuring a smart AI opponent powered by Stockfish API. The game includes mobile-friendly touch controls, an adaptive AI difficulty system, and a move history tracker.

✨ Features

🎮 Interactive Chessboard – Click or tap to move pieces.

🤖 AI-Powered Opponent – Uses Stockfish API for strong chess moves.

📱 Mobile-Friendly – Supports touch gestures.

📜 Move History & Undo – View and revert moves.

🔥 Hints & Difficulty Levels – Get move suggestions and adjust AI strength.

🔍 En Passant, Castling & Pawn Promotion – Supports full chess rules.

📊 Beautiful UI – Clean and modern design.

🚀 How to Run

1️⃣ Clone the Repository

git clone https://github.com/your-repo/chess-game.git
cd chess-game

2️⃣ Open in Browser

Simply open Chess.html in your browser.

3️⃣ Play the Game

Move pieces by clicking/tapping.

AI plays as Black.

Use the Undo button to revert moves.

🔧 How It Works

🎯 AI Integration with Stockfish API

FEN Board Representation is sent to the Lichess Stockfish Cloud API.

API returns the best move, which is then applied to the game.

📜 Move Handling

The board is updated dynamically using JavaScript and the HTML5 Canvas API.

AI moves are validated before execution.

🛠️ Technologies Used

JavaScript (ES6+) – Game logic & AI handling

Stockfish API – AI move calculation

HTML5 & Canvas API – Chessboard rendering

CSS3 – Responsive UI design

🎮 Controls

Click/Tap on a piece to select it, then click/tap on a destination square.

Undo Move with the Undo Button.

Restart Game with the New Game Button.

Change AI Difficulty from the dropdown menu.

🐞 Debugging & Logs

If AI moves seem incorrect, check the console logs in DevTools (F12 > Console):

console.log("FEN Sent to Stockfish:", getFEN());
console.log("AI Move (UCI):", bestMoveUCI);
console.log("AI Move (Converted):", moveObj);

🤝 Contributing

Fork the repository

Create a new branch

git checkout -b feature-branch

Commit your changes

git commit -m "Add new feature"

Push to GitHub

git push origin feature-branch

Open a Pull Request 🚀

📜 License

This project is open-source under the MIT License.

💡 Built with passion for chess! 🏆♟️
