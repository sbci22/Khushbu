<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Car Racing Game</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    background: linear-gradient(135deg, #111, #252525);
    font-family: Arial, sans-serif;
    overflow: hidden;
    user-select: none;
}

.game {
    width: 400px;
    height: 100vh;
    max-height: 750px;
    margin: auto;
    position: relative;
    overflow: hidden;
    background: #333;
    border-left: 8px solid #777;
    border-right: 8px solid #777;
}

/* Road */
.road {
    position: absolute;
    width: 100%;
    height: 200%;
    top: -100%;
    background:
        repeating-linear-gradient(
            to bottom,
            #333 0px,
            #333 45px,
            #444 45px,
            #444 90px
        );
    animation: roadMove 0.5s linear infinite;
}

@keyframes roadMove {
    from {
        transform: translateY(0);
    }
    to {
        transform: translateY(90px);
    }
}

/* Lane lines */
.lane {
    position: absolute;
    width: 8px;
    height: 100%;
    left: 33.33%;
    background: repeating-linear-gradient(
        to bottom,
        white 0px,
        white 60px,
        transparent 60px,
        transparent 120px
    );
    animation: laneMove 0.6s linear infinite;
}

.lane2 {
    left: 66.66%;
}

@keyframes laneMove {
    from {
        background-position: 0 0;
    }
    to {
        background-position: 0 120px;
    }
}

/* Player Car */
.car {
    position: absolute;
    width: 60px;
    height: 105px;
    bottom: 30px;
    left: 170px;
    background: linear-gradient(90deg, #e00000, #ff4444, #b00000);
    border-radius: 14px 14px 8px 8px;
    z-index: 5;
    box-shadow: 0 5px 15px #000;
}

/* Windows */
.car::before {
    content: "";
    position: absolute;
    width: 42px;
    height: 35px;
    left: 9px;
    top: 12px;
    background: #111;
    border-radius: 10px 10px 5px 5px;
    border: 3px solid #777;
}

.car::after {
    content: "";
    position: absolute;
    width: 42px;
    height: 25px;
    left: 9px;
    bottom: 10px;
    background: #111;
    border-radius: 5px;
}

/* Wheels */
.wheel {
    position: absolute;
    width: 12px;
    height: 25px;
    background: #111;
    border-radius: 5px;
    top: 20px;
}

.w1 { left: -7px; }
.w2 { right: -7px; }
.w3 { left: -7px; bottom: 18px; top: auto; }
.w4 { right: -7px; bottom: 18px; top: auto; }

/* Enemy */
.enemy {
    position: absolute;
    width: 60px;
    height: 105px;
    background: linear-gradient(90deg, #0055ff, #4488ff, #003399);
    border-radius: 14px 14px 8px 8px;
    z-index: 4;
    box-shadow: 0 5px 15px #000;
}

.enemy::before {
    content: "";
    position: absolute;
    width: 42px;
    height: 35px;
    left: 9px;
    top: 12px;
    background: #111;
    border-radius: 10px 10px 5px 5px;
    border: 3px solid #777;
}

.enemy::after {
    content: "";
    position: absolute;
    width: 42px;
    height: 25px;
    left: 9px;
    bottom: 10px;
    background: #111;
    border-radius: 5px;
}

/* HUD */
.hud {
    position: absolute;
    top: 15px;
    left: 15px;
    right: 15px;
    z-index: 10;
    display: flex;
    justify-content: space-between;
}

.score, .speed {
    background: rgba(0,0,0,0.75);
    color: white;
    padding: 10px 15px;
    border-radius: 10px;
    font-weight: bold;
}

/* Game Over */
.gameover {
    position: absolute;
    inset: 0;
    background: rgba(0,0,0,0.8);
    z-index: 20;
    display: none;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    color: white;
}

.gameover h1 {
    color: #ff3333;
    font-size: 45px;
    margin-bottom: 15px;
}

.gameover p {
    font-size: 20px;
    margin-bottom: 20px;
}

button {
    padding: 14px 30px;
    border: none;
    border-radius: 10px;
    background: #ff2222;
    color: white;
    font-size: 18px;
    font-weight: bold;
    cursor: pointer;
}

button:hover {
    background: #cc0000;
}

/* Mobile Controls */
.controls {
    position: absolute;
    bottom: 15px;
    left: 0;
    right: 0;
    z-index: 15;
    display: flex;
    justify-content: space-around;
}

.control {
    width: 70px;
    height: 55px;
    border: none;
    background: rgba(255,255,255,0.2);
    color: white;
    font-size: 30px;
    border-radius: 15px;
}
</style>
</head>

<body>

<div class="game" id="game">

    <div class="road">
        <div class="lane"></div>
        <div class="lane lane2"></div>
    </div>

    <div class="hud">
        <div class="score">🏆 Score: <span id="score">0</span></div>
        <div class="speed">⚡ Speed: <span id="speed">5</span></div>
    </div>

    <!-- Player -->
    <div class="car" id="player">
        <div class="wheel w1"></div>
        <div class="wheel w2"></div>
        <div class="wheel w3"></div>
        <div class="wheel w4"></div>
    </div>

    <!-- Controls -->
    <div class="controls">
        <button class="control" id="left">⬅️</button>
        <button class="control" id="right">➡️</button>
    </div>

    <!-- Game Over -->
    <div class="gameover" id="gameover">
        <h1>GAME OVER</h1>
        <p>Your Score: <span id="finalScore">0</span></p>
        <button onclick="restartGame()">PLAY AGAIN</button>
    </div>

</div>

<script>

const game = document.getElementById("game");
const player = document.getElementById("player");
const scoreText = document.getElementById("score");
const finalScore = document.getElementById("finalScore");
const gameover = document.getElementById("gameover");
const speedText = document.getElementById("speed");

let playerX = 170;
let score = 0;
let speed = 5;
let gameRunning = true;
let enemies = [];

const lanes = [55, 170, 285];

/* Keyboard */
document.addEventListener("keydown", function(e) {

    if (!gameRunning) return;

    if (e.key === "ArrowLeft" || e.key.toLowerCase() === "a") {
        moveLeft();
    }

    if (e.key === "ArrowRight" || e.key.toLowerCase() === "d") {
        moveRight();
    }
});

/* Move Left */
function moveLeft() {
    if (playerX > 20) {
        playerX -= 115;
        if (playerX < 20) playerX = 20;
        player.style.left = playerX + "px";
    }
}

/* Move Right */
function moveRight() {
    if (playerX < 310) {
        playerX += 115;
        if (playerX > 310) playerX = 310;
        player.style.left = playerX + "px";
    }
}

/* Mobile buttons */
document.getElementById("left").addEventListener("touchstart", function(e) {
    e.preventDefault();
    moveLeft();
});

document.getElementById("right").addEventListener("touchstart", function(e) {
    e.preventDefault();
    moveRight();
});

document.getElementById("left").addEventListener("click", moveLeft);
document.getElementById("right").addEventListener("click", moveRight);


/* Create Enemy */
function createEnemy() {

    if (!gameRunning) return;

    const enemy = document.createElement("div");
    enemy.classList.add("enemy");

    let lane = lanes[Math.floor(Math.random() * lanes.length)];

    enemy.style.left = lane + "px";
    enemy.style.top = "-120px";

    game.appendChild(enemy);
    enemies.push(enemy);
}


/* Game Loop */
function gameLoop() {

    if (!gameRunning) return;

    enemies.forEach((enemy, index) => {

        let top = parseInt(enemy.style.top);

        top += speed;
        enemy.style.top = top + "px";

        /* Collision */
        let playerRect = player.getBoundingClientRect();
        let enemyRect = enemy.getBoundingClientRect();

        if (
            playerRect.left < enemyRect.right &&
            playerRect.right > enemyRect.left &&
            playerRect.top < enemyRect.bottom &&
            playerRect.bottom > enemyRect.top
        ) {
            endGame();
        }

        /* Remove enemy */
        if (top > game.clientHeight) {

            enemy.remove();
            enemies.splice(index, 1);

            score++;
            scoreText.textContent = score;

            /* Increase speed */
            if (score % 10 === 0) {
                speed++;
                speedText.textContent = speed;
            }
        }

    });

    requestAnimationFrame(gameLoop);
}


/* Spawn enemies */
setInterval(function() {

    if (gameRunning) {
        createEnemy();
    }

}, 1000);


/* Game Over */
function endGame() {

    gameRunning = false;

    finalScore.textContent = score;
    gameover.style.display = "flex";
}


/* Restart */
function restartGame() {

    enemies.forEach(enemy => enemy.remove());

    enemies = [];
    score = 0;
    speed = 5;
    playerX = 170;

    scoreText.textContent = "0";
    speedText.textContent = "5";

    player.style.left = playerX + "px";

    gameover.style.display = "none";

    gameRunning = true;

    requestAnimationFrame(gameLoop);
}


/* Start */
gameLoop();

</script>

</body>
</html>
