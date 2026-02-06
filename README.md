# Valentine
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Valentine 💖</title>

<style>
body {
  margin: 0;
  height: 100vh;
  background: linear-gradient(135deg, #ff758c, #ff7eb3);
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: Arial, sans-serif;
  overflow: hidden;
}

.container {
  text-align: center;
  color: white;
}

h1 {
  font-size: 1.9rem;
  margin-bottom: 30px;
}

button {
  padding: 15px 32px;
  font-size: 18px;
  border: none;
  border-radius: 12px;
  cursor: pointer;
}

#yes {
  background: #28a745;
  color: white;
}

#no {
  background: #dc3545;
  color: white;
  position: absolute;
}

/* floating hearts */
.heart {
  position: fixed;
  bottom: -20px;
  font-size: 22px;
  animation: float 5s linear forwards;
}

@keyframes float {
  0% { transform: translateY(0); opacity: 1; }
  100% { transform: translateY(-100vh); opacity: 0; }
}
</style>
</head>

<body onclick="playMusic()">

<audio id="song" loop>
  <source src="burmese-love-song.mp3" type="audio/mpeg">
</audio>

<div class="container">
  <h1>
    Will you be my Valentine,<br>
    Lay Lay Myint? 💖
  </h1>

  <button id="yes" onclick="goLove()">Yes 💕</button>
  <button id="no" onmouseover="moveNo()">No 💔</button>
</div>

<script>
const noBtn = document.getElementById("no");

function moveNo() {
  const x = Math.random() * (window.innerWidth - 100);
  const y = Math.random() * (window.innerHeight - 60);
  noBtn.style.left = x + "px";
  noBtn.style.top = y + "px";
}

function goLove() {
  window.location.href = "love.html";
}

function playMusic() {
  document.getElementById("song").play();
}

setInterval(() => {
  const heart = document.createElement("div");
  heart.className = "heart";
  heart.innerHTML = "💗";
  heart.style.left = Math.random() * 100 + "vw";
  document.body.appendChild(heart);
  setTimeout(() => heart.remove(), 5000);
}, 400);
</script>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>I Love You ❤️</title>

<style>
body {
  margin: 0;
  height: 100vh;
  background: radial-gradient(circle, #ff4d6d, #c9184a);
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: Arial, sans-serif;
  color: white;
  overflow: hidden;
}

h1 {
  font-size: 2.6rem;
  animation: pulse 1.4s infinite;
  text-align: center;
}

@keyframes pulse {
  0% { transform: scale(1); }
  50% { transform: scale(1.12); }
  100% { transform: scale(1); }
}

.heart {
  position: fixed;
  font-size: 24px;
  animation: fall 4s linear forwards;
}

@keyframes fall {
  0% { transform: translateY(-10vh); opacity: 1; }
  100% { transform: translateY(110vh); opacity: 0; }
}
</style>
</head>

<body>

<h1>❤️ I love you ❤️<br>ချစ်တယ် ❤️</h1>

<script>
setInterval(() => {
  const heart = document.createElement("div");
  heart.className = "heart";
  heart.innerHTML = "💖";
  heart.style.left = Math.random() * 100 + "vw";
  document.body.appendChild(heart);
  setTimeout(() => heart.remove(), 4000);
}, 300);
</script>

</body>
</html>
