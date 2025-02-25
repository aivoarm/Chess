    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Advanced Chess Game with Adaptive AI</title>
        <style>
            /* General Styling */
            body {
                display: flex;
                flex-direction: column;
                justify-content: center;
                align-items: center;
                height: 100vh;
                margin: 0;
                background: linear-gradient(135deg, #2e2e2e, #5e2e8e);
                font-family: 'Arial', sans-serif;
                overflow: hidden;
            }
        
            /* Make canvas responsive */
            canvas {
                border: 2px solid #fff;
                box-shadow: 0 0 20px rgba(255, 255, 255, 0.5);
                border-radius: 10px;
                width: 90vw;  /* Make it fit within screen */
                height: auto;
                max-width: 640px;
            }
        
            /* Info Panel (Turn Indicator & Difficulty Settings) */
            #infoPanel {
                display: flex;
                justify-content: space-between;
                width: 90vw;
                max-width: 640px;
                flex-wrap: wrap; /* Ensures it fits smaller screens */
                margin-bottom: 20px;
            }
        
            #turnInfo {
                color: #fff;
                font-size: 24px;
                text-shadow: 0 0 10px #00ffcc;
                text-align: center;
            }
        
            #difficultyControls {
                display: flex;
                align-items: center;
                justify-content: center;
                flex-wrap: wrap;
            }
        
            #difficultyControls label {
                color: #fff;
                margin-right: 10px;
                text-shadow: 0 0 10px #00ffcc;
            }
        
            #difficultySelect {
                background: rgba(255, 255, 255, 0.2);
                color: #fff;
                border: 1px solid #00ffcc;
                border-radius: 5px;
                padding: 5px;
            }
        
            /* Captured Pieces Display */
            #capturedPieces {
                display: flex;
                justify-content: space-between;
                width: 90vw;
                max-width: 640px;
                margin-top: 10px;
            }
        
            .capturedContainer {
                background: rgba(0, 0, 0, 0.3);
                border-radius: 5px;
                padding: 5px;
                min-height: 40px;
                width: 48%;
                text-align: center;
                font-size: 20px;
                color: #fff;
            }
        
            /* Move History Section */
            #moveHistory {
                max-height: 150px;
                overflow-y: auto;
                margin-top: 10px;
                background: rgba(0, 0, 0, 0.3);
                border-radius: 5px;
                padding: 10px;
                width: 90vw;
                max-width: 640px;
                color: #fff;
            }
        
            #movesList {
                display: flex;
                flex-wrap: wrap;
                gap: 5px;
            }
        
            .moveRecord {
                background: rgba(255, 255, 255, 0.1);
                padding: 3px 6px;
                border-radius: 3px;
                cursor: pointer;
            }
        
            .moveRecord:hover {
                background: rgba(255, 255, 255, 0.3);
            }
        
            /* Buttons Styling */
            .buttonContainer {
                display: flex;
                flex-wrap: wrap;
                justify-content: center;
                width: 90vw;
                max-width: 640px;
                gap: 10px;
                margin-top: 20px;
            }
        
            .gameButton {
                padding: 14px 20px;
                font-size: 18px;
                color: #fff;
                background: linear-gradient(45deg, #ff00cc, #00ffcc);
                border: none;
                border-radius: 12px;
                cursor: pointer;
                text-shadow: 0 0 10px #fff;
                box-shadow: 0 0 20px rgba(255, 255, 255, 0.3);
                transition: all 0.3s ease;
                width: 100%;
                max-width: 200px;
            }
        
            .gameButton:hover {
                background: linear-gradient(45deg, #00ffcc, #ff00cc);
                transform: scale(1.05);
            }
        
            /* Game Over Modal */
            #gameOverModal {
                display: none;
                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
                background: rgba(0, 0, 0, 0.9);
                padding: 30px;
                border-radius: 15px;
                text-align: center;
                z-index: 10;
                color: #fff;
                box-shadow: 0 0 30px rgba(0, 255, 204, 0.7);
                width: 90vw;
                max-width: 400px;
            }
        
            #gameOverModal h2 {
                margin-top: 0;
                color: #00ffcc;
                text-shadow: 0 0 10px #00ffcc;
            }
        
            /* Responsive Adjustments */
            @media (max-width: 768px) {
                #infoPanel {
                    flex-direction: column;
                    align-items: center;
                    text-align: center;
                }
        
                #difficultyControls {
                    margin-top: 10px;
                }
        
                canvas {
                    width: 100vw; /* Make canvas full width on small screens */
                    max-width: 480px;
                }
        
                .buttonContainer {
                    flex-direction: column;
                    align-items: center;
                }
        
                .gameButton {
                    max-width: 100%; /* Buttons stretch on small screens */
                }
            }
        </style>
        
    </head>
    <body>
        <div id="infoPanel">
            <div id="turnInfo">Turn: White (You)</div>
            <div id="difficultyControls">
                <label for="difficultySelect">AI Level:</label>
                <select id="difficultySelect">
                    <option value="1">Beginner</option>
                    <option value="2">Casual</option>
                    <option value="3" selected>Intermediate</option>
                    <option value="4">Advanced</option>
                    <option value="5">Master</option>
                </select>
            </div>
        </div>
        
        <canvas id="gameCanvas" width="640" height="640"></canvas>
        
        <div id="capturedPieces">
            <div class="capturedContainer"><div id="capturedWhite"></div></div>
            <div class="capturedContainer"><div id="capturedBlack"></div></div>
        </div>
        
        <div id="moveHistory">
            <h3>Move History</h3>
            <div id="movesList"></div>
        </div>
        
        <div class="buttonContainer">
            <button id="undoButton" class="gameButton">Undo Move</button>
            <button id="resetButton" class="gameButton">New Game</button>
            <button id="hintButton" class="gameButton">Hint</button>
        </div>
        
        <div id="gameOverModal">
            <h2 id="gameResult">Game Over</h2>
            <p id="gameOverMessage"></p>
            <button id="newGameButton" class="gameButton">Play Again</button>
        </div>

        <script>


            const canvas = document.getElementById('gameCanvas');
            const ctx = canvas.getContext('2d');
            const turnInfo = document.getElementById('turnInfo');
            const resetButton = document.getElementById('resetButton');
            const undoButton = document.getElementById('undoButton');
            const hintButton = document.getElementById('hintButton');
            const difficultySelect = document.getElementById('difficultySelect');
            const capturedWhite = document.getElementById('capturedWhite');
            const capturedBlack = document.getElementById('capturedBlack');
            const movesList = document.getElementById('movesList');
            const gameOverModal = document.getElementById('gameOverModal');
            const gameResult = document.getElementById('gameResult');
            const gameOverMessage = document.getElementById('gameOverMessage');
            const newGameButton = document.getElementById('newGameButton');

            const squareSize = 80;
            let currentTurn = 'white';
            let selectedPiece = null;
            let offsetX = 0, offsetY = 0;
            let gameHistory = [];
            let moveHistory = [];
            let capturedPiecesWhite = [];
            let capturedPiecesBlack = [];
            let lastMove = null;
            let validMoves = [];
            let inCheck = false;
            let gameOver = false;
            let aiThinking = false;
            let castlingRights = { whiteKingSide: true, whiteQueenSide: true, blackKingSide: true, blackQueenSide: true };
            let halfMoveClock = 0;
            let fullMoveNumber = 1;

            const pieceBaseValues = {
                'p': 100, 'n': 320, 'b': 330, 'r': 500, 'q': 900, 'k': 20000,
                'P': 100, 'N': 320, 'B': 330, 'R': 500, 'Q': 900, 'K': 20000
            };

            const pawnTable = [
                [ 0,  0,  0,  0,  0,  0,  0,  0], [50, 50, 50, 50, 50, 50, 50, 50],
                [10, 10, 20, 30, 30, 20, 10, 10], [ 5,  5, 10, 25, 25, 10,  5,  5],
                [ 0,  0,  0, 20, 20,  0,  0,  0], [ 5, -5,-10,  0,  0,-10, -5,  5],
                [ 5, 10, 10,-20,-20, 10, 10,  5], [ 0,  0,  0,  0,  0,  0,  0,  0]
            ];
            const knightTable = [
                [-50,-40,-30,-30,-30,-30,-40,-50], [-40,-20,  0,  0,  0,  0,-20,-40],
                [-30,  0, 10, 15, 15, 10,  0,-30], [-30,  5, 15, 20, 20, 15,  5,-30],
                [-30,  0, 15, 20, 20, 15,  0,-30], [-30,  5, 10, 15, 15, 10,  5,-30],
                [-40,-20,  0,  5,  5,  0,-20,-40], [-50,-40,-30,-30,-30,-30,-40,-50]
            ];
            const bishopTable = [
                [-20,-10,-10,-10,-10,-10,-10,-20], [-10,  0,  0,  0,  0,  0,  0,-10],
                [-10,  0, 10, 10, 10, 10,  0,-10], [-10,  5,  5, 10, 10,  5,  5,-10],
                [-10,  0,  5, 10, 10,  5,  0,-10], [-10,  5,  5,  5,  5,  5,  5,-10],
                [-10,  0,  5,  0,  0,  5,  0,-10], [-20,-10,-10,-10,-10,-10,-10,-20]
            ];
            const rookTable = [
                [ 0,  0,  0,  0,  0,  0,  0,  0], [ 5, 10, 10, 10, 10, 10, 10,  5],
                [-5,  0,  0,  0,  0,  0,  0, -5], [-5,  0,  0,  0,  0,  0,  0, -5],
                [-5,  0,  0,  0,  0,  0,  0, -5], [-5,  0,  0,  0,  0,  0,  0, -5],
                [-5,  0,  0,  0,  0,  0,  0, -5], [ 0,  0,  0,  5,  5,  0,  0,  0]
            ];
            const queenTable = [
                [-20,-10,-10, -5, -5,-10,-10,-20], [-10,  0,  0,  0,  0,  0,  0,-10],
                [-10,  0,  5,  5,  5,  5,  0,-10], [ -5,  0,  5,  5,  5,  5,  0, -5],
                [  0,  0,  5,  5,  5,  5,  0, -5], [-10,  5,  5,  5,  5,  5,  0,-10],
                [-10,  0,  5,  0,  0,  0,  0,-10], [-20,-10,-10, -5, -5,-10,-10,-20]
            ];
            const kingMiddleTable = [
                [-30,-40,-40,-50,-50,-40,-40,-30], [-30,-40,-40,-50,-50,-40,-40,-30],
                [-30,-40,-40,-50,-50,-40,-40,-30], [-30,-40,-40,-50,-50,-40,-40,-30],
                [-20,-30,-30,-40,-40,-30,-30,-20], [-10,-20,-20,-20,-20,-20,-20,-10],
                [ 20, 20,  0,  0,  0,  0, 20, 20], [ 20, 30, 10,  0,  0, 10, 30, 20]
            ];
            const kingEndgameTable = [
                [-50,-40,-30,-20,-20,-30,-40,-50], [-30,-20,-10,  0,  0,-10,-20,-30],
                [-30,-10, 20, 30, 30, 20,-10,-30], [-30,-10, 30, 40, 40, 30,-10,-30],
                [-30,-10, 30, 40, 40, 30,-10,-30], [-30,-10, 20, 30, 30, 20,-10,-30],
                [-30,-30,  0,  0,  0,  0,-30,-30], [-50,-30,-30,-30,-30,-30,-30,-50]
            ];

            const pieceSymbols = {
                'P': '♙', 'N': '♘', 'B': '♗', 'R': '♖', 'Q': '♕', 'K': '♔',
                'p': '♟', 'n': '♞', 'b': '♝', 'r': '♜', 'q': '♛', 'k': '♚'
            };

            const initialBoard = [
                ['r', 'n', 'b', 'q', 'k', 'b', 'n', 'r'],
                ['p', 'p', 'p', 'p', 'p', 'p', 'p', 'p'],
                ['', '', '', '', '', '', '', ''],
                ['', '', '', '', '', '', '', ''],
                ['', '', '', '', '', '', '', ''],
                ['', '', '', '', '', '', '', ''],
                ['P', 'P', 'P', 'P', 'P', 'P', 'P', 'P'],
                ['R', 'N', 'B', 'Q', 'K', 'B', 'N', 'R']
            ];
            let board = JSON.parse(JSON.stringify(initialBoard));
            const pieceColors = { 'white': '#fff', 'black': '#000' };

            const historyTable = Array(8).fill().map(() => Array(8).fill().map(() => 
                Array(8).fill().map(() => Array(8).fill(0))));
            const killerMoves = Array(10).fill().map(() => ({ move: null, score: 0 }));

            function drawBoard() {
                for (let row = 0; row < 8; row++) {
                    for (let col = 0; col < 8; col++) {
                        ctx.fillStyle = (row + col) % 2 === 0 ? '#f0d9b5' : '#b58863';
                        ctx.fillRect(col * squareSize, row * squareSize, squareSize, squareSize);
                    }
                }
                if (lastMove) {
                    ctx.fillStyle = 'rgba(255, 255, 0, 0.3)';
                    ctx.fillRect(lastMove.fromCol * squareSize, lastMove.fromRow * squareSize, squareSize, squareSize);
                    ctx.fillRect(lastMove.toCol * squareSize, lastMove.toRow * squareSize, squareSize, squareSize);
                }
                if (inCheck) {
                    const kingPos = findKing(currentTurn);
                    if (kingPos) {
                        ctx.fillStyle = 'rgba(255, 0, 0, 0.4)';
                        ctx.fillRect(kingPos.col * squareSize, kingPos.row * squareSize, squareSize, squareSize);
                    }
                }
                ctx.font = '14px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                for (let i = 0; i < 8; i++) {
                    ctx.fillStyle = (i % 2 === 0) ? '#b58863' : '#f0d9b5';
                    ctx.fillText(8 - i, squareSize / 8, i * squareSize + squareSize / 2);
                    ctx.fillStyle = (i % 2 === 1) ? '#b58863' : '#f0d9b5';
                    ctx.fillText(String.fromCharCode(97 + i), i * squareSize + squareSize / 2, 8 * squareSize - squareSize / 8);
                }
            }

            function drawPieces() {
                for (let row = 0; row < 8; row++) {
                    for (let col = 0; col < 8; col++) {
                        const piece = board[row][col];
                        if (piece && (!selectedPiece || selectedPiece.row !== row || selectedPiece.col !== col)) {
                            ctx.font = '60px Arial';
                            ctx.fillStyle = piece === piece.toUpperCase() ? pieceColors.white : pieceColors.black;
                            ctx.textAlign = 'center';
                            ctx.textBaseline = 'middle';
                            ctx.fillText(pieceSymbols[piece], col * squareSize + squareSize / 2, row * squareSize + squareSize / 2);
                        }
                    }
                }
            }

            function drawValidMoves() {
                ctx.globalAlpha = 0.6;
                for (const move of validMoves) {
                    ctx.fillStyle = board[move.toRow][move.toCol] ? 'rgba(255, 0, 0, 0.5)' : 'rgba(0, 255, 0, 0.5)';
                    ctx.beginPath();
                    ctx.arc(move.toCol * squareSize + squareSize / 2, move.toRow * squareSize + squareSize / 2, 
                            squareSize / 4, 0, Math.PI * 2);
                    ctx.fill();
                }
                ctx.globalAlpha = 1.0;
            }

            function updateCapturedPieces() {
                capturedWhite.innerHTML = capturedPiecesWhite.map(p => pieceSymbols[p]).join(' ');
                capturedBlack.innerHTML = capturedPiecesBlack.map(p => pieceSymbols[p]).join(' ');
            }

            function updateMoveHistory() {
                movesList.innerHTML = '';
                moveHistory.forEach((move, index) => {
                    const moveElement = document.createElement('div');
                    moveElement.className = 'moveRecord';
                    moveElement.textContent = move;
                    moveElement.onclick = () => revertToMove(index);
                    movesList.appendChild(moveElement);
                });
            }

            function revertToMove(index) {
                if (aiThinking || gameOver) return;
                board = JSON.parse(JSON.stringify(gameHistory[index].board));
                currentTurn = gameHistory[index].turn;
                castlingRights = gameHistory[index].castlingRights;
                lastMove = gameHistory[index].lastMove;
                capturedPiecesWhite = gameHistory[index].capturedWhite.slice();
                capturedPiecesBlack = gameHistory[index].capturedBlack.slice();
                gameHistory = gameHistory.slice(0, index + 1);
                moveHistory = moveHistory.slice(0, index + 1);
                halfMoveClock = gameHistory[index].halfMoveClock;
                fullMoveNumber = gameHistory[index].fullMoveNumber;
                inCheck = isKingInCheck(currentTurn);
                update();
                turnInfo.textContent = `Turn: ${currentTurn === 'white' ? 'White (You)' : 'Black (AI)'}`;
                checkGameState();
            }


            function getTouchPosition(event) {
    let rect = canvas.getBoundingClientRect();
    let touch = event.touches[0] || event.changedTouches[0];
    return {
        x: touch.clientX - rect.left,
        y: touch.clientY - rect.top
    };
}

canvas.addEventListener('mousedown', handleStart);
canvas.addEventListener('mousemove', handleMove);
canvas.addEventListener('mouseup', handleEnd);

// Touch events for mobile
canvas.addEventListener('touchstart', (event) => {
    event.preventDefault();
    handleStart(getTouchPosition(event));
});
canvas.addEventListener('touchmove', (event) => {
    event.preventDefault();
    handleMove(getTouchPosition(event));
});
canvas.addEventListener('touchend', (event) => {
    event.preventDefault();
    handleEnd();
});

function handleStart(position) {
    if (gameOver || currentTurn !== 'white' || aiThinking) return;
    const col = Math.floor(position.x / squareSize);
    const row = Math.floor(position.y / squareSize);
    if (board[row][col] && board[row][col] === board[row][col].toUpperCase()) {
        selectedPiece = { row, col, x: position.x, y: position.y };
        validMoves = getAllMoves('white').filter(m => m.fromRow === row && m.fromCol === col);
        update();
    }
}

function handleMove(position) {
    if (!selectedPiece) return;
    selectedPiece.x = position.x;
    selectedPiece.y = position.y;
    update();
}

function handleEnd() {
    if (!selectedPiece) return;
    const col = Math.floor(selectedPiece.x / squareSize);
    const row = Math.floor(selectedPiece.y / squareSize);
    const move = { fromRow: selectedPiece.row, fromCol: selectedPiece.col, toRow: row, toCol: col };

    if (isValidMove(move.fromRow, move.fromCol, row, col)) {
        makeMove(move);
        update();
        turnInfo.textContent = 'Turn: Black (AI)';
        checkGameState();
        if (!gameOver) setTimeout(aiMove, 500);
    }
    selectedPiece = null;
    validMoves = [];
    update();
}




            function isValidMove(fromRow, fromCol, toRow, toCol, checkForCheck = true) {
                if (toRow < 0 || toRow > 7 || toCol < 0 || toCol > 7) return false;
                const piece = board[fromRow][fromCol];
                if (!piece || (piece === piece.toUpperCase() ? 'white' : 'black') !== currentTurn) return false;

                const target = board[toRow][toCol];
                if (target && (target === target.toUpperCase()) === (piece === piece.toUpperCase())) return false;
                if (target && target.toLowerCase() === 'k') return false;

                const dx = toCol - fromCol;
                const dy = toRow - fromRow;
                let isValid = false;

                switch (piece.toLowerCase()) {
                    case 'p':
                        isValid = isValidPawnMove(fromRow, fromCol, toRow, toCol, piece === piece.toUpperCase() ? 'white' : 'black');
                        break;
                    case 'r':
                        isValid = (dx === 0 || dy === 0) && isPathClear(fromRow, fromCol, toRow, toCol);
                        break;
                    case 'n':
                        isValid = (Math.abs(dx) === 1 && Math.abs(dy) === 2) || (Math.abs(dx) === 2 && Math.abs(dy) === 1);
                        break;
                    case 'b':
                        isValid = Math.abs(dx) === Math.abs(dy) && isPathClear(fromRow, fromCol, toRow, toCol);
                        break;
                    case 'q':
                        isValid = (dx === 0 || dy === 0 || Math.abs(dx) === Math.abs(dy)) && isPathClear(fromRow, fromCol, toRow, toCol);
                        break;
                    case 'k':
                        isValid = Math.abs(dx) <= 1 && Math.abs(dy) <= 1 || 
                                (Math.abs(dx) === 2 && dy === 0 && isValidCastling(fromRow, fromCol, toRow, toCol));
                        break;
                }

                if (isValid && checkForCheck) {
                    const tempBoard = JSON.parse(JSON.stringify(board));
                    tempBoard[toRow][toCol] = piece;
                    tempBoard[fromRow][fromCol] = '';
                    if (isKingInCheck(currentTurn, tempBoard)) return false;
                    const opponentColor = currentTurn === 'white' ? 'black' : 'white';
                    if (!findKing(opponentColor, tempBoard)) return false;
                }
                return isValid;
            }

            function isValidPawnMove(fromRow, fromCol, toRow, toCol, color) {
                const dy = color === 'white' ? fromRow - toRow : toRow - fromRow;
                const dx = toCol - fromCol;
                const target = board[toRow][toCol];
                if (dx === 0 && dy === 1 && !target) return true;
                if (dx === 0 && dy === 2 && !target && !board[color === 'white' ? fromRow - 1 : fromRow + 1][fromCol] && 
                    ((color === 'white' && fromRow === 6) || (color === 'black' && fromRow === 1))) return true;
                if (Math.abs(dx) === 1 && dy === 1 && target && ((target === target.toUpperCase()) !== (color === 'white'))) return true;
                if (Math.abs(dx) === 1 && dy === 1 && !target && ((color === 'white' && fromRow === 3) || (color === 'black' && fromRow === 4)) && 
                    lastMove && Math.abs(lastMove.fromRow - lastMove.toRow) === 2 && lastMove.toCol === toCol && lastMove.toRow === fromRow && 
                    board[lastMove.toRow][lastMove.toCol].toLowerCase() === 'p') return true;
                return false;
            }

            function isValidCastling(fromRow, fromCol, toRow, toCol) {
                if (inCheck) return false;
                const isKingSide = toCol > fromCol;
                const rookCol = isKingSide ? 7 : 0;
                const row = currentTurn === 'white' ? 7 : 0;
                const rights = currentTurn === 'white' ? 
                    (isKingSide ? castlingRights.whiteKingSide : castlingRights.whiteQueenSide) : 
                    (isKingSide ? castlingRights.blackKingSide : castlingRights.blackQueenSide);
                if (!rights || board[row][rookCol].toLowerCase() !== 'r') return false;
                const step = isKingSide ? 1 : -1;
                for (let col = fromCol + step; col !== rookCol; col += step) {
                    if (board[row][col] || isSquareAttacked(row, col, currentTurn)) return false;
                }
                if (isSquareAttacked(row, fromCol, currentTurn)) return false;
                return true;
            }

            function isPathClear(fromRow, fromCol, toRow, toCol) {
                const dx = Math.sign(toCol - fromCol);
                const dy = Math.sign(toRow - fromRow);
                let row = fromRow + dy;
                let col = fromCol + dx;
                while (row !== toRow || col !== toCol) {
                    if (board[row][col]) return false;
                    row += dy;
                    col += dx;
                }
                return true;
            }

            function isSquareAttacked(row, col, color) {
                const enemyColor = color === 'white' ? 'black' : 'white';
                for (let r = 0; r < 8; r++) {
                    for (let c = 0; c < 8; c++) {
                        const piece = board[r][c];
                        if (piece && (piece === piece.toUpperCase() ? 'white' : 'black') === enemyColor) {
                            if (isValidMove(r, c, row, col, false)) return true;
                        }
                    }
                }
                return false;
            }

            function isKingInCheck(color, testBoard = board) {
                const kingPos = findKing(color, testBoard);
                return kingPos && isSquareAttacked(kingPos.row, kingPos.col, color);
            }

            function findKing(color, testBoard = board) {
                const king = color === 'white' ? 'K' : 'k';
                for (let row = 0; row < 8; row++) {
                    for (let col = 0; col < 8; col++) {
                        if (testBoard[row][col] === king) return { row, col };
                    }
                }
                return null;
            }

            function getAllMoves(color) {
                const moves = [];
                for (let fromRow = 0; fromRow < 8; fromRow++) {
                    for (let fromCol = 0; fromCol < 8; fromCol++) {
                        const piece = board[fromRow][fromCol];
                        if (piece && (piece === piece.toUpperCase() ? 'white' : 'black') === color) {
                            for (let toRow = 0; toRow < 8; toRow++) {
                                for (let toCol = 0; toCol < 8; toCol++) {
                                    if (isValidMove(fromRow, fromCol, toRow, toCol)) {
                                        moves.push({ fromRow, fromCol, toRow, toCol });
                                    }
                                }
                            }
                        }
                    }
                }
                return moves;
            }

            function evaluateBoard() {
                let score = 0;
                let pieceCount = 0;
                let whiteMaterial = 0;
                let blackMaterial = 0;
                const kingPos = findKing('black');
                const whiteKingPos = findKing('white');
                const gamePhase = pieceCount > 16 ? 'middle' : 'endgame';

                for (let row = 0; row < 8; row++) {
                    for (let col = 0; col < 8; col++) {
                        const piece = board[row][col];
                        if (piece) {
                            pieceCount++;
                            const isWhite = piece === piece.toUpperCase();
                            const baseValue = pieceBaseValues[piece];
                            const evalRow = isWhite ? row : 7 - row;
                            
                            const tableValue = piece.toLowerCase() === 'p' ? pawnTable[evalRow][col] :
                                piece.toLowerCase() === 'n' ? knightTable[evalRow][col] :
                                piece.toLowerCase() === 'b' ? bishopTable[evalRow][col] :
                                piece.toLowerCase() === 'r' ? rookTable[evalRow][col] :
                                piece.toLowerCase() === 'q' ? queenTable[evalRow][col] :
                                piece.toLowerCase() === 'k' ? (gamePhase === 'endgame' ? 
                                    kingEndgameTable[evalRow][col] : kingMiddleTable[evalRow][col]) : 0;

                            let pieceScore = baseValue + tableValue;
                            
                            if (piece.toLowerCase() === 'b') {
                                pieceScore += evaluateBishopPair(isWhite) * 50;
                            }
                            if (piece.toLowerCase() === 'r') {
                                pieceScore += (row === (isWhite ? 1 : 6) ? 25 : 0);
                            }
                            if (piece.toLowerCase() === 'p') {
                                pieceScore += evaluatePawnStructure(row, col, isWhite);
                            }

                            score += (isWhite ? 1 : -1) * pieceScore;
                            if (isWhite) whiteMaterial += baseValue; else blackMaterial += baseValue;

                            if (piece.toLowerCase() === 'k') {
                                const safetyScore = evaluateKingSafety(isWhite ? whiteKingPos : kingPos, isWhite ? 'white' : 'black');
                                score += (isWhite ? 1 : -1) * safetyScore;
                            }
                        }
                    }
                }

                score += evaluateMobility('black') - evaluateMobility('white');
                score += evaluateCenterControl('black') - evaluateCenterControl('white');
                score += evaluateDevelopment('black') - evaluateDevelopment('white');
                score += currentTurn === 'black' ? 10 : -10;
                const materialDiff = blackMaterial - whiteMaterial;
                score += materialDiff * 0.1;
                
                // Stronger king safety and checkmate threat detection
                if (isKingInCheck('black')) score -= 2000;
                if (isKingInCheck('white')) score += 2000;
                score -= evaluateKingExposure('black') * 100;
                score += evaluateKingExposure('white') * 100;

                return score;
            }

            function evaluateBishopPair(isWhite) {
                let bishopCount = 0;
                for (let row = 0; row < 8; row++) {
                    for (let col = 0; col < 8; col++) {
                        if (board[row][col] === (isWhite ? 'B' : 'b')) bishopCount++;
                    }
                }
                return bishopCount === 2 ? 1 : 0;
            }

            function evaluatePawnStructure(row, col, isWhite) {
                let score = 0;
                const pawn = isWhite ? 'P' : 'p';
                
                for (let r = 0; r < 8; r++) {
                    if (r !== row && board[r][col] === pawn) score -= 20;
                }
                
                let isolated = true;
                for (let c = Math.max(0, col - 1); c <= Math.min(7, col + 1); c++) {
                    if (c !== col) {
                        for (let r = 0; r < 8; r++) {
                            if (board[r][c] === pawn) {
                                isolated = false;
                                break;
                            }
                        }
                    }
                }
                if (isolated) score -= 25;

                if (isPassedPawn(row, col, isWhite)) score += 50 + (isWhite ? row : 7 - row) * 10;

                return score;
            }

            function isPassedPawn(row, col, isWhite) {
                const direction = isWhite ? -1 : 1;
                const enemyPawn = isWhite ? 'p' : 'P';
                for (let r = row + direction; r >= 0 && r < 8; r += direction) {
                    for (let c = Math.max(0, col - 1); c <= Math.min(7, col + 1); c++) {
                        if (board[r][c] === enemyPawn) return false;
                    }
                }
                return true;
            }

            function evaluateKingSafety(kingPos, color) {
                let score = evaluatePawnShield(kingPos, color);
                const enemyColor = color === 'white' ? 'black' : 'white';
                
                for (let col = Math.max(0, kingPos.col - 1); col <= Math.min(7, kingPos.col + 1); col++) {
                    let pawnCount = 0;
                    for (let row = 0; row < 8; row++) {
                        if (board[row][col] === (color === 'white' ? 'P' : 'p')) pawnCount++;
                    }
                    if (pawnCount === 0) score -= 30;
                }

                for (let r = Math.max(0, kingPos.row - 2); r <= Math.min(7, kingPos.row + 2); r++) {
                    for (let c = Math.max(0, kingPos.col - 2); c <= Math.min(7, kingPos.col + 2); c++) {
                        const piece = board[r][c];
                        if (piece && (piece === piece.toUpperCase() ? 'white' : 'black') === enemyColor) {
                            score -= pieceBaseValues[piece] * 0.1; // Increased penalty for nearby threats
                        }
                    }
                }

                return score;
            }

            function evaluateKingExposure(color) {
                const kingPos = findKing(color);
                if (!kingPos) return 0;
                let exposure = 0;
                
                // Check key defensive squares (like f7 for Black)
                const criticalSquares = color === 'black' ? [[1,5], [1,6]] : [[6,5], [6,6]];
                for (const [row, col] of criticalSquares) {
                    if (isSquareAttacked(row, col, color)) {
                        exposure += 1; // Penalty for each attacked square near king
                    }
                }
                return exposure;
            }

            function evaluatePawnShield(kingPos, color) {
                let shieldBonus = 0;
                const direction = color === 'white' ? -1 : 1;
                const row = kingPos.row + direction;
                if (row >= 0 && row < 8) {
                    for (let col = Math.max(0, kingPos.col - 1); col <= Math.min(7, kingPos.col + 1); col++) {
                        if (board[row][col] === (color === 'white' ? 'P' : 'p')) shieldBonus += 30; // Increased bonus
                    }
                }
                return shieldBonus;
            }

            function evaluateMobility(color) {
                return getAllMoves(color).length * 5;
            }

            function evaluateCenterControl(color) {
                let score = 0;
                const centerSquares = [[3, 3], [3, 4], [4, 3], [4, 4]];
                centerSquares.forEach(([row, col]) => {
                    const piece = board[row][col];
                    if (piece && (piece === piece.toUpperCase() ? 'white' : 'black') === color) {
                        score += piece.toLowerCase() === 'p' ? 10 : 20;
                    }
                });
                return score;
            }

            function evaluateDevelopment(color) {
                let score = 0;
                const isWhite = color === 'white';
                const pieces = isWhite ? ['N', 'B', 'Q'] : ['n', 'b', 'q'];
                const backRank = isWhite ? 7 : 0;
                
                for (let col = 0; col < 8; col++) {
                    for (const piece of pieces) {
                        if (board[backRank][col] === piece) score -= 20; // Increased penalty
                    }
                }
                return score;
            }

            function orderMoves(moves) {
                return moves.sort((a, b) => {
                    let aScore = scoreMove(a);
                    let bScore = scoreMove(b);
                    aScore += getHistoryScore(a);
                    bScore += getHistoryScore(b);
                    return bScore - aScore;
                });
            }

            function scoreMove(move) {
                let score = 0;
                const piece = board[move.fromRow][move.fromCol];
                const captured = board[move.toRow][move.toCol];
                if (captured) score += pieceBaseValues[captured] - pieceBaseValues[piece] * 0.1;
                if (piece.toLowerCase() === 'p' && (move.toRow === 0 || move.toRow === 7)) score += 800;
                if (isSquareAttacked(move.toRow, move.toCol, currentTurn === 'white' ? 'black' : 'white')) score += 100; // Increased check bonus
                // Bonus for defending f7/f2
                if (move.toRow === (piece === piece.toUpperCase() ? 6 : 1) && move.toCol === 5) score += 50;
                return score;
            }

            function getHistoryScore(move) {
                return historyTable[move.fromRow][move.fromCol][move.toRow][move.toCol];
            }

            function updateHistory(move, depth) {
                historyTable[move.fromRow][move.fromCol][move.toRow][move.toCol] += depth * depth;
            }

            function quiescence(alpha, beta, color) {
                const standPat = evaluateBoard();
                if (standPat >= beta) return beta;
                let newAlpha = Math.max(alpha, standPat);

                const moves = getAllMoves(color).filter(move => board[move.toRow][move.toCol] || 
                    (move.toRow === (color === 'white' ? 1 : 6) && move.toCol === 5)); // Include f7/f2 attacks
                const orderedMoves = orderMoves(moves);

                for (const move of orderedMoves) {
                    makeMove(move, true);
                    const score = -quiescence(-beta, -newAlpha, color === 'white' ? 'black' : 'white');
                    undoMove();
                    if (score >= beta) return beta;
                    newAlpha = Math.max(newAlpha, score);
                }
                return newAlpha;
            }

            function minimax(depth, alpha, beta, maximizingPlayer, ply = 0) {
                if (depth === 0) return quiescence(alpha, beta, maximizingPlayer ? 'black' : 'white');

                const moves = orderMoves(getAllMoves(maximizingPlayer ? 'black' : 'white'));
                if (moves.length === 0) return isKingInCheck(maximizingPlayer ? 'black' : 'white') ? 
                    (maximizingPlayer ? -1000000 - depth : 1000000 + depth) : 0;

                if (depth > 3 && !inCheck && ply > 0) {
                    currentTurn = maximizingPlayer ? 'white' : 'black';
                    const nullScore = -minimax(depth - 3, -beta, -beta + 1, !maximizingPlayer, ply + 1);
                    currentTurn = maximizingPlayer ? 'black' : 'white';
                    if (nullScore >= beta) return beta;
                }

                let bestMove = null;
                if (maximizingPlayer) {
                    let maxEval = -Infinity;
                    for (const move of moves) {
                        makeMove(move, true);
                        const eval = minimax(depth - 1, alpha, beta, false, ply + 1);
                        undoMove();
                        
                        if (eval > maxEval) {
                            maxEval = eval;
                            bestMove = move;
                        }
                        alpha = Math.max(alpha, eval);
                        if (beta <= alpha) break;
                    }
                    if (bestMove && depth > 2) {
                        updateHistory(bestMove, depth);
                        killerMoves[ply] = { move: bestMove, score: maxEval };
                    }
                    return maxEval;
                } else {
                    let minEval = Infinity;
                    for (const move of moves) {
                        makeMove(move, true);
                        const eval = minimax(depth - 1, alpha, beta, true, ply + 1);
                        undoMove();
                        
                        if (eval < minEval) {
                            minEval = eval;
                            bestMove = move;
                        }
                        beta = Math.min(beta, eval);
                        if (beta <= alpha) break;
                    }
                    if (bestMove && depth > 2) {
                        updateHistory(bestMove, depth);
                        killerMoves[ply] = { move: bestMove, score: minEval };
                    }
                    return minEval;
                }
            }
async function getBestMoveFromStockfish(fen) {
    try {
        const response = await fetch(`https://lichess.org/api/cloud-eval?fen=${encodeURIComponent(fen)}&multiPv=3&depth=18`);
        const data = await response.json();

        if (data.pvs && data.pvs.length > 0) {
            console.log("Stockfish Best Move:", data.pvs[0].moves);
            return data.pvs[0].moves.split(" ")[0]; // Best move in UCI notation
        }
    } catch (error) {
        console.error("Error fetching Stockfish move:", error);
    }
    return null;
}



function getFEN() {
    let fen = "";
    for (let row = 0; row < 8; row++) {
        let empty = 0;
        for (let col = 0; col < 8; col++) {
            const piece = board[row][col];
            if (piece === "") {
                empty++;
            } else {
                if (empty > 0) {
                    fen += empty;
                    empty = 0;
                }
                fen += piece;
            }
        }
        if (empty > 0) fen += empty;
        if (row < 7) fen += "/";
    }

    // Append turn info
    fen += ` ${currentTurn === 'white' ? 'w' : 'b'} `;

    // Castling rights
    let castling = "";
    if (castlingRights.whiteKingSide) castling += "K";
    if (castlingRights.whiteQueenSide) castling += "Q";
    if (castlingRights.blackKingSide) castling += "k";
    if (castlingRights.blackQueenSide) castling += "q";
    fen += castling || "-";

    // En passant target square (if applicable)
    let enPassant = "-";
    if (lastMove && board[lastMove.toRow][lastMove.toCol].toLowerCase() === "p" && Math.abs(lastMove.toRow - lastMove.fromRow) === 2) {
        enPassant = `${String.fromCharCode(97 + lastMove.toCol)}${8 - ((lastMove.fromRow + lastMove.toRow) / 2)}`;
    }
    fen += ` ${enPassant}`;

    // Half-move clock and full-move number
    fen += ` ${halfMoveClock} ${fullMoveNumber}`;

    console.log("FEN Sent to Stockfish:", fen); // Debugging output
    return fen;
}

function uciToMove(uci) {
    if (!uci || uci.length < 4) return null; // Ensure valid move string

    const fromCol = uci.charCodeAt(0) - 97; // 'a' -> 0
    const fromRow = 8 - parseInt(uci[1]); // '8' -> 0
    const toCol = uci.charCodeAt(2) - 97;
    const toRow = 8 - parseInt(uci[3]);

    // Handle pawn promotion
    let promotion = null;
    if (uci.length === 5) {
        promotion = uci[4].toUpperCase();
    }

    return { fromRow, fromCol, toRow, toCol, promotion };
}


async function aiMove() {
    if (gameOver || currentTurn !== 'black') return;
    aiThinking = true;

    const fen = getFEN(); // Convert board to FEN notation
    const bestMoveUCI = await getBestMoveFromStockfish(fen);

    if (bestMoveUCI) {
        const moveObj = uciToMove(bestMoveUCI); // Convert UCI move to board move format

        if (isValidMove(moveObj.fromRow, moveObj.fromCol, moveObj.toRow, moveObj.toCol)) {
            makeMove(moveObj);
            update();
            turnInfo.textContent = 'Turn: White (You)';
            checkGameState();
        } else {
            console.error("Invalid AI Move:", bestMoveUCI, moveObj);
        }
    } else {
        console.error("Stockfish returned no move.");
    }

    aiThinking = false;
}



 function makeMove(move, isAI = false) {
                const piece = board[move.fromRow][move.fromCol];
                const captured = board[move.toRow][move.toCol];
                const isPawnMove = piece.toLowerCase() === 'p';
                const isCapture = !!captured;
                let enPassantCapture = false;
                let promotionPiece = null;

                if (isPawnMove && Math.abs(move.toRow - move.fromRow) === 1 && Math.abs(move.toCol - move.fromCol) === 1 && !captured) {
                    enPassantCapture = true;
                    const capturedRow = move.fromRow;
                    const capturedCol = move.toCol;
                    capturedPiecesWhite.push(board[capturedRow][capturedCol]);
                    board[capturedRow][capturedCol] = '';
                } else if (captured) {
                    (piece === piece.toUpperCase() ? capturedPiecesBlack : capturedPiecesWhite).push(captured);
                }

                if (isPawnMove && (move.toRow === 0 || move.toRow === 7)) {
                    promotionPiece = piece === 'P' ? 'Q' : 'q';
                    board[move.toRow][move.toCol] = promotionPiece;
                } else {
                    board[move.toRow][move.toCol] = piece;
                }
                board[move.fromRow][move.fromCol] = '';

                if (piece.toLowerCase() === 'k' && Math.abs(move.toCol - move.fromCol) === 2) {
                    const rookFromCol = move.toCol > move.fromCol ? 7 : 0;
                    const rookToCol = move.toCol > move.fromCol ? 5 : 3;
                    board[move.fromRow][rookToCol] = board[move.fromRow][rookFromCol];
                    board[move.fromRow][rookFromCol] = '';
                }

                halfMoveClock = (isPawnMove || isCapture) ? 0 : halfMoveClock + 1;
                if (currentTurn === 'black') fullMoveNumber++;

                if (piece === 'K') {
                    castlingRights.whiteKingSide = castlingRights.whiteQueenSide = false;
                } else if (piece === 'k') {
                    castlingRights.blackKingSide = castlingRights.blackQueenSide = false;
                } else if (piece === 'R' && move.fromRow === 7) {
                    if (move.fromCol === 0) castlingRights.whiteQueenSide = false;
                    else if (move.fromCol === 7) castlingRights.whiteKingSide = false;
                } else if (piece === 'r' && move.fromRow === 0) {
                    if (move.fromCol === 0) castlingRights.blackQueenSide = false;
                    else if (move.fromCol === 7) castlingRights.blackKingSide = false;
                }

                lastMove = { ...move };
                currentTurn = currentTurn === 'white' ? 'black' : 'white';
                inCheck = isKingInCheck(currentTurn);
                const notation = getMoveNotation(move, piece, captured, enPassantCapture, promotionPiece);
                moveHistory.push(notation);
                gameHistory.push({
                    board: JSON.parse(JSON.stringify(board)),
                    turn: currentTurn,
                    castlingRights: { ...castlingRights },
                    lastMove: { ...lastMove },
                    capturedWhite: capturedPiecesWhite.slice(),
                    capturedBlack: capturedPiecesBlack.slice(),
                    halfMoveClock,
                    fullMoveNumber
                });
            }

            function getMoveNotation(move, piece, captured, enPassant, promotion) {
                const fromFile = String.fromCharCode(97 + move.fromCol);
                const fromRank = 8 - move.fromRow;
                const toFile = String.fromCharCode(97 + move.toCol);
                const toRank = 8 - move.toRow;
                let notation = '';
                if (piece.toLowerCase() === 'k' && Math.abs(move.toCol - move.fromCol) === 2) {
                    notation = move.toCol > move.fromCol ? 'O-O' : 'O-O-O';
                } else {
                    notation = piece.toLowerCase() === 'p' ? '' : piece.toUpperCase();
                    if (captured || enPassant) notation += piece.toLowerCase() === 'p' ? fromFile : 'x';
                    notation += toFile + toRank;
                    if (promotion) notation += '=' + promotion.toUpperCase();
                }
                if (inCheck) notation += isCheckmate() ? '#' : '+';
                return notation;
            }

            function undoMove() {
                if (gameHistory.length <= 1) return;
                gameHistory.pop();
                const state = gameHistory[gameHistory.length - 1];
                board = JSON.parse(JSON.stringify(state.board));
                currentTurn = state.turn;
                castlingRights = { ...state.castlingRights };
                lastMove = state.lastMove ? { ...state.lastMove } : null;
                capturedPiecesWhite = state.capturedWhite.slice();
                capturedPiecesBlack = state.capturedBlack.slice();
                halfMoveClock = state.halfMoveClock;
                fullMoveNumber = state.fullMoveNumber;
                moveHistory.pop();
                inCheck = isKingInCheck(currentTurn);
            }

            function isCheckmate() {
                return inCheck && getAllMoves(currentTurn).length === 0;
            }

            function isStalemate() {
                return !inCheck && getAllMoves(currentTurn).length === 0;
            }

            function checkGameState() {
                if (!findKing(currentTurn)) {
                    endGame(`${currentTurn === 'white' ? 'Black (AI)' : 'White (You)'} wins!`);
                    return;
                }
                if (isCheckmate()) {
                    endGame(`${currentTurn === 'white' ? 'Black (AI)' : 'White (You)'} wins by checkmate!`);
                } else if (isStalemate()) {
                    endGame('Stalemate! The game is a draw.');
                } else if (halfMoveClock >= 50) {
                    endGame('Draw by 50-move rule!');
                }
            }

            function endGame(message) {
                gameOver = true;
                gameResult.textContent = 'Game Over';
                gameOverMessage.textContent = message;
                gameOverModal.style.display = 'block';
            }

            function update() {
                drawBoard();
                drawPieces();
                if (selectedPiece) {
                    drawValidMoves();
                    const piece = board[selectedPiece.row][selectedPiece.col];
                    ctx.font = '60px Arial';
                    ctx.fillStyle = piece === piece.toUpperCase() ? pieceColors.white : pieceColors.black;
                    ctx.fillText(pieceSymbols[piece], selectedPiece.x, selectedPiece.y);
                }
                updateCapturedPieces();
                updateMoveHistory();
            }

            canvas.addEventListener('mousedown', (event) => {
                if (gameOver || currentTurn !== 'white' || aiThinking) return;
                const rect = canvas.getBoundingClientRect();
                const x = event.clientX - rect.left;
                const y = event.clientY - rect.top;
                const col = Math.floor(x / squareSize);
                const row = Math.floor(y / squareSize);
                if (board[row][col] && board[row][col] === board[row][col].toUpperCase()) {
                    selectedPiece = { row, col, x, y };
                    validMoves = getAllMoves('white').filter(m => m.fromRow === row && m.fromCol === col);
                    offsetX = x - col * squareSize;
                    offsetY = y - row * squareSize;
                    update();
                }
            });

            canvas.addEventListener('mousemove', (event) => {
                if (!selectedPiece) return;
                const rect = canvas.getBoundingClientRect();
                selectedPiece.x = event.clientX - rect.left;
                selectedPiece.y = event.clientY - rect.top;
                update();
            });

            canvas.addEventListener('mouseup', (event) => {
                if (!selectedPiece) return;
                const rect = canvas.getBoundingClientRect();
                const x = event.clientX - rect.left;
                const y = event.clientY - rect.top;
                const toCol = Math.floor(x / squareSize);
                const toRow = Math.floor(y / squareSize);
                const move = { fromRow: selectedPiece.row, fromCol: selectedPiece.col, toRow, toCol };

                if (isValidMove(move.fromRow, move.fromCol, toRow, toCol)) {
                    makeMove(move);
                    update();
                    turnInfo.textContent = 'Turn: Black (AI)';
                    checkGameState();
                    if (!gameOver) setTimeout(aiMove, 500);
                }
                selectedPiece = null;
                validMoves = [];
                update();
            });

            resetButton.addEventListener('click', resetGame);
            newGameButton.addEventListener('click', resetGame);

            function resetGame() {
                board = JSON.parse(JSON.stringify(initialBoard));
                currentTurn = 'white';
                gameHistory = [{ board: JSON.parse(JSON.stringify(initialBoard)), turn: 'white', castlingRights: { whiteKingSide: true, whiteQueenSide: true, blackKingSide: true, blackQueenSide: true }, lastMove: null, capturedWhite: [], capturedBlack: [], halfMoveClock: 0, fullMoveNumber: 1 }];
                moveHistory = [];
                capturedPiecesWhite = [];
                capturedPiecesBlack = [];
                lastMove = null;
                inCheck = false;
                gameOver = false;
                aiThinking = false;
                halfMoveClock = 0;
                fullMoveNumber = 1;
                turnInfo.textContent = 'Turn: White (You)';
                gameOverModal.style.display = 'none';
                update();
            }

            undoButton.addEventListener('click', () => {
                if (gameOver || aiThinking || gameHistory.length <= 1) return;
                undoMove();
                if (currentTurn === 'black') undoMove();
                update();
                turnInfo.textContent = `Turn: ${currentTurn === 'white' ? 'White (You)' : 'Black (AI)'}`;
                checkGameState();
            });

            hintButton.addEventListener('click', () => {
                if (gameOver || currentTurn !== 'white' || aiThinking) return;
                const moves = getAllMoves('white');
                if (moves.length === 0) return;
                const hintMove = moves[Math.floor(Math.random() * Math.min(3, moves.length))];
                lastMove = hintMove;
                update();
                setTimeout(() => {
                    lastMove = null;
                    update();
                }, 2000);
            });

            update();
        </script>
    </body>
    </html>
