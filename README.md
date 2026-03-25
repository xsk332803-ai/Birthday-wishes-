# Birthday-wishes-<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday Jiyabunnesha 💖</title>

<style>
body {
    margin: 0;
    font-family: 'Segoe UI', sans-serif;
    background: linear-gradient(to bottom, #ff9a9e, #fad0c4);
    text-align: center;
    overflow-x: hidden;
}

/* Header */
h1 {
    color: white;
    margin-top: 20px;
    font-size: 28px;
    animation: glow 2s infinite alternate;
}

@keyframes glow {
    from { text-shadow: 0 0 10px #fff; }
    to { text-shadow: 0 0 20px #ff4da6; }
}

/* Message box */
.message {
    background: white;
    margin: 20px;
    padding: 15px;
    border-radius: 15px;
    font-size: 16px;
}

/* Button */
button {
    background: #ff4da6;
    border: none;
    padding: 12px 20px;
    color: white;
    border-radius: 20px;
    font-size: 16px;
    cursor: pointer;
}

/* Cake */
.cake {
    font-size: 50px;
    margin: 20px;
    animation: bounce 1.5s infinite;
}

@keyframes bounce {
    0%,100% { transform: translateY(0); }
    50% { transform: translateY(-10px); }
}

/* Floating hearts */
.heart {
    position: fixed;
    color: pink;
    animation: floatUp 5s linear infinite;
}

@keyframes floatUp {
    0% { transform: translateY(100vh); opacity:1; }
    100% { transform: translateY(-10vh); opacity:0; }
}

/* Game */
#game {
    margin: 20px;
}

#tapBtn {
    font-size: 20px;
    padding: 15px;
    border-radius: 50%;
    background: #ff66b2;
}

</style>
</head>

<body>

<h1>Happy Birthday Jiyabunnesha 💖</h1>

<div class="cake">🎂</div>

<div class="message">
    Dear Jiyabunnesha 💕 <br><br>
    On your special day, I just want to say…<br>
    You are the most beautiful person in my life 🌸<br>
    Your smile makes everything brighter ✨<br><br>
    I wish you endless happiness and love 💖
</div>

<button onclick="showWish()">Tap for Surprise 🎁</button>

<div id="surprise" class="message" style="display:none;">
    I like you more than words can explain… 💗<br>
    Happy Birthday once again 🥰
</div>

<!-- Game -->
<div id="game">
    <h2>Tap Game 💕</h2>
    <p>Tap the heart 10 times!</p>
    <button id="tapBtn">💖</button>
    <p id="score">0 / 10</p>
</div>

<script>
// Surprise message
function showWish() {
    document.getElementById("surprise").style.display = "block";
}

// Floating hearts
function createHeart() {
    const heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerText = "💗";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.fontSize = Math.random() * 20 + 20 + "px";
    document.body.appendChild(heart);

    setTimeout(() => {
        heart.remove();
    }, 5000);
}

setInterval(createHeart, 500);

// Game logic
let count = 0;
document.getElementById("tapBtn").onclick = function() {
    count++;
    document.getElementById("score").innerText = count + " / 10";

    if(count == 10){
        alert("Yay! You unlocked a message 💖\nI really like you Jiyabunnesha 🥰");
    }
};
</script>

</body>
</html>
