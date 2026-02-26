<!DOCTYPE html>
<html>
<head>
  <title>Mountain Climb Game</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background-color: #87CEEB;
      overflow: hidden;
    }

    #game {
      margin-top: 50px;
    }

    #mountain {
      height: 300px;
      width: 120px;
      background: linear-gradient(to top, #654321, #aaaaaa);
      margin: 20px auto;
      position: relative;
      border: 2px solid black;
      overflow: hidden;
    }

    #player {
      width: 20px;
      height: 20px;
      background: red;
      position: absolute;
      bottom: 0;
      left: 50px;
    }

    .stone {
      width: 20px;
      height: 20px;
      background: gray;
      border-radius: 50%;
      position: absolute;
      top: 0;
    }

    #info {
      margin-top: 15px;
      font-size: 18px;
    }
  </style>
</head>
<body>

<h1>Climb the Mountain!</h1>
<p>Press SPACE to climb.</p>

<div id="game">
  <div id="mountain">
    <div id="player"></div>
  </div>

  <div id="info">
    <p id="status">Start climbing!</p>
    <p>Score: <span id="score">0</span></p>
    <p>Speed: <span id="speed">0</span> climbs/sec</p>
  </div>
</div>
<script>
  const player = document.getElementById("player");
  const mountain = document.getElementById("mountain");
  const statusText = document.getElementById("status");
  const scoreText = document.getElementById("score");
  const speedText = document.getElementById("speed");

  let positionY = 0;
  let positionX = 50;
  let score = 0;
  let gameOver = false;
  let startTime = Date.now();
  let climbs = 0;

  const maxHeight = 280;
  const maxWidth = 100;

  // Create stone enemy
  const stone = document.createElement("div");
  stone.classList.add("stone");
  mountain.appendChild(stone);

  let stoneTop = 0;
  let stoneLeft = Math.random() * 100;
  stone.style.left = stoneLeft + "px";

  function updateSpeed() {
    const timeElapsed = (Date.now() - startTime) / 1000;
    const speed = (climbs / timeElapsed).toFixed(2);
    speedText.textContent = speed;
  }

  function endGame(message) {
    gameOver = true;
    statusText.textContent = message;
    document.removeEventListener("keydown", moveHandler);
  }

  function moveHandler(event) {
    if (gameOver) return;

    // UP (Space)
    if (event.code === "Space") {
      climbs++;
      positionY += 20;
      score += 10;
      statusText.textContent = "⬆ You climbed!";
    }

    // LEFT
    if (event.code === "ArrowLeft") {
      positionX -= 10;
    }

    // RIGHT
    if (event.code === "ArrowRight") {
      positionX += 10;
    }

    // DOWN
    if (event.code === "ArrowDown") {
      positionY -= 20;
      score -= 5;
      statusText.textContent = "⬇ You moved down!";
    }

    // Boundaries
    if (positionY < 0) positionY = 0;
    if (positionY > maxHeight) positionY = maxHeight;
    if (positionX < 0) positionX = 0;
    if (positionX > maxWidth) positionX = maxWidth;

    player.style.bottom = positionY + "px";
    player.style.left = positionX + "px";
    scoreText.textContent = score;

    updateSpeed();

    if (positionY >= maxHeight) {
      endGame("🏔 You reached the summit! YOU WIN!");
    }

    if (score < -20) {
      endGame("❌ Too weak! GAME OVER!");
    }
  }

  document.addEventListener("keydown", moveHandler);

  // Move stone
  function moveStone() {
    if (gameOver) return;

    stoneTop += 3;
    stone.style.top = stoneTop + "px";

    if (stoneTop > 300) {
      stoneTop = 0;
      stoneLeft = Math.random() * 100;
      stone.style.left = stoneLeft + "px";
    }

    checkCollision();
    requestAnimationFrame(moveStone);
  }

  function checkCollision() {
    const playerRect = player.getBoundingClientRect();
    const stoneRect = stone.getBoundingClientRect();

    if (
      playerRect.left < stoneRect.right &&
      playerRect.right > stoneRect.left &&
      playerRect.top < stoneRect.bottom &&
      playerRect.bottom > stoneRect.top
    ) {
      endGame("💥 A stone hit you! GAME OVER!");
    }
  }

  moveStone();
</script>
</body>
</html>
