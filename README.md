# Free-Online-games-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Free Games Hub</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: #333;
        }
        header {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 1rem;
        }
        nav {
            background-color: #444;
            padding: 0.5rem;
            text-align: center;
        }
        nav a {
            color: white;
            margin: 0 1rem;
            text-decoration: none;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 1rem;
        }
        .game-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1rem;
        }
        .game-card {
            background: white;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            padding: 1rem;
            text-align: center;
        }
        .game-card h3 {
            margin-top: 0;
        }
        .game-embed {
            width: 100%;
            height: 400px;
            border: none;
        }
        footer {
            text-align: center;
            padding: 1rem;
            background-color: #333;
            color: white;
            margin-top: 2rem;
        }
    </style>
</head>
<body>
    <header>
        <h1>Free Games Hub</h1>
        <p>Play awesome games for free!</p>
    </header>
    <nav>
        <a href="#action">Action</a>
        <a href="#puzzle">Puzzle</a>
        <a href="#strategy">Strategy</a>
    </nav>
    <div class="container">
        <section id="action">
            <h2>Action Games</h2>
            <div class="game-grid">
                <div class="game-card">
                    <h3>Snake Game</h3>
                    <p>A classic snake game. Use arrow keys to play.</p>
                    <iframe class="game-embed" src="data:text/html,<html><body><canvas id='canvas' width='400' height='400'></canvas><script>const canvas = document.getElementById('canvas'); const ctx = canvas.getContext('2d'); let snake = [{x:200,y:200}]; let direction = {x:0,y:0}; let food = {x:Math.floor(Math.random()*20)*20, y:Math.floor(Math.random()*20)*20}; function draw() { ctx.clearRect(0,0,400,400); ctx.fillStyle='green'; snake.forEach(s => ctx.fillRect(s.x,s.y,20,20)); ctx.fillStyle='red'; ctx.fillRect(food.x,food.y,20,20); } function update() { const head = {x:snake[0].x + direction.x, y:snake[0].y + direction.y}; snake.unshift(head); if (head.x === food.x && head.y === food.y) { food = {x:Math.floor(Math.random()*20)*20, y:Math.floor(Math.random()*20)*20}; } else { snake.pop(); } } document.addEventListener('keydown', e => { if (e.key === 'ArrowUp') direction = {x:0,y:-20}; if (e.key === 'ArrowDown') direction = {x:0,y:20}; if (e.key === 'ArrowLeft') direction = {x:-20,y:0}; if (e.key === 'ArrowRight') direction = {x:20,y:0}; }); setInterval(() => { update(); draw(); }, 100);</script></body></html>"></iframe>
                </div>
            </div>
        </section>
        <section id="puzzle">
            <h2>Puzzle Games</h2>
            <div class="game-grid">
                <div class="game-card">
                    <h3>Tic-Tac-Toe</h3>
                    <p>Classic Tic-Tac-Toe. Click to play.</p>
                    <iframe class="game-embed" src="data:text/html,<html><body><div id='board' style='display:grid;grid-template-columns:repeat(3,50px);gap:5px;margin:20px;'></div><script>const board = document.getElementById('board'); let currentPlayer = 'X'; for (let i = 0; i < 9; i++) { const cell = document.createElement('div'); cell.style.width='50px'; cell.style.height='50px'; cell.style.border='1px solid black'; cell.style.display='flex'; cell.style.alignItems='center'; cell.style.justifyContent='center'; cell.addEventListener('click', () => { if (!cell.textContent) { cell.textContent = currentPlayer; currentPlayer = currentPlayer === 'X' ? 'O' : 'X'; } }); board.appendChild(cell); }</script></body></html>"></iframe>
                </div>
            </div>
        </section>
        <section id="strategy">
            <h2>Strategy Games</h2>
            <p>More games coming soon! Add your own by embedding HTML5 games.</p>
        </section>
    </div>
    <footer>
        <p>&copy; 2023 Free Games Hub. All games are free and open-source.</p>
    </footer>
</body>
</html>
