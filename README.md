# Birthday-wish-<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy Birthday Ivana ❤️</title>

<style>
body {
    margin: 0;
    height: 100vh;
    background: linear-gradient(135deg, #ff9a9e, #fad0c4);
    font-family: 'Segoe UI', sans-serif;
    overflow: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
}

/* Card */
.card {
    background: white;
    padding: 40px 60px;
    border-radius: 20px;
    text-align: center;
    box-shadow: 0 0 25px rgba(255, 77, 109, 0.6);
    z-index: 2;
    max-width: 500px;
}

h1 {
    color: #ff4d6d;
    font-size: 2.5em;
}

.message {
    font-size: 1.2em;
    color: #555;
    margin-top: 20px;
    min-height: 80px;
}

/* Falling hearts */
.heart {
    position: absolute;
    color: #ff4d6d;
    font-size: 20px;
    animation: fall linear infinite;
}

@keyframes fall {
    from { transform: translateY(-10vh); opacity: 1; }
    to { transform: translateY(110vh); opacity: 0; }
}

/* Pulse heart */
.big-heart {
    font-size: 50px;
    animation: beat 1s infinite;
}

@keyframes beat {
    0% { transform: scale(1); }
    50% { transform: scale(1.2); }
    100% { transform: scale(1); }
}
</style>
</head>

<body>

<!-- Background Music -->
<audio autoplay loop>
  <source src="song.mp3" type="audio/mpeg">
</audio>

<div class="card">
    <div class="big-heart">❤️</div>
    <h1>Happy Birthday Ivana Chakraborty 💖</h1>
    <div class="message" id="typeText"></div>
    <p style="margin-top:20px;color:#ff4d6d;font-weight:bold;">
        Forever yours,<br>
        Sayan Kumar Bhukta ❤️
    </p>
</div>

<script>
/* Typewriter Love Message */
const text = "To my gorgeous sweetheart Ivana, you are the most beautiful part of my life. Like the song says — you live in my heart every moment. May your birthday be as magical as your smile. I love you endlessly ❤️";
let i = 0;

function typeWriter() {
    if (i < text.length) {
        document.getElementById("typeText").innerHTML += text.charAt(i);
        i++;
        setTimeout(typeWriter, 50);
    }
}
typeWriter();

/* Falling Hearts */
function createHeart() {
    const heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerHTML = "❤";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.animationDuration = (Math.random() * 3 + 2) + "s";
    heart.style.fontSize = (Math.random() * 20 + 10) + "px";
    document.body.appendChild(heart);
    setTimeout(() => heart.remove(), 5000);
}
setInterval(createHeart, 300);
</script>

</body>
</html>
