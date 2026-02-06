<!DOCTYPE html>  
<html lang="en">  
<head>  
<meta charset="UTF-8">  
<meta name="viewport" content="width=device-width, initial-scale=1.0">  
<title>Asif Mustaffa ❤️</title>  
  
<style>  
body {  
  margin: 0;  
  height: 100vh;  
  background: radial-gradient(circle at top, #ff9aa2, #ff4d6d);  
  display: flex;  
  align-items: center;  
  justify-content: center;  
  font-family: 'Georgia', serif;  
  color: white;  
  text-align: center;  
  overflow: hidden;  
}  
  
.card {  
  background: rgba(255,255,255,0.2);  
  padding: 45px;  
  border-radius: 25px;  
  max-width: 460px;  
  box-shadow: 0 25px 60px rgba(0,0,0,0.35);  
  backdrop-filter: blur(8px);  
  animation: fadeIn 2s ease;  
}  
  
h1 {  
  font-size: 2.4rem;  
}  
  
p {  
  font-size: 1.15rem;  
  line-height: 1.7;  
}  
  
button {  
  padding: 14px 32px;  
  border-radius: 30px;  
  border: none;  
  cursor: pointer;  
  font-size: 1rem;  
  margin: 10px;  
  transition: 0.3s;  
}  
  
button:hover {  
  transform: scale(1.15);  
}  
  
.yes {  
  background: white;  
  color: #ff4d6d;  
  font-weight: bold;  
}  
  
.no {  
  background: transparent;  
  border: 2px solid white;  
  color: white;  
}  
  
.hearts span {  
  position: absolute;  
  font-size: 22px;  
  animation: float 8s infinite ease-in;  
}  
  
@keyframes fadeIn {  
  from { opacity: 0; transform: translateY(40px); }  
  to { opacity: 1; transform: translateY(0); }  
}  
  
@keyframes float {  
  0% { transform: translateY(110vh); opacity: 0; }  
  50% { opacity: 1; }  
  100% { transform: translateY(-10vh); opacity: 0; }  
}  
  
/* HEART MERGE */  
.heart-merge {  
  position: relative;  
  width: 120px;  
  height: 60px;  
  margin: 30px auto 10px;  
}  
  
.heart {  
  position: absolute;  
  font-size: 45px;  
  opacity: 0;  
}  
  
.heart.left {  
  left: 0;  
  animation: moveLeft 4s forwards;  
}  
  
.heart.right {  
  right: 0;  
  animation: moveRight 4s forwards;  
}  
  
@keyframes moveLeft {  
  0% { opacity: 0; transform: translateX(0); }  
  100% { opacity: 1; transform: translateX(35px) scale(1.2); }  
}  
  
@keyframes moveRight {  
  0% { opacity: 0; transform: translateX(0); }  
  100% { opacity: 1; transform: translateX(-35px) scale(1.2); }  
}  
  
/* MERGED HEART GLOW */  
.merged-heart {  
  font-size: 55px;  
  opacity: 0;  
  animation: pulseGlow 2.5s forwards 4s;  
}  
  
@keyframes pulseGlow {  
  0% {  
    opacity: 0;  
    transform: scale(0.6);  
    text-shadow: 0 0 0 rgba(255,255,255,0);  
  }  
  60% {  
    opacity: 1;  
    transform: scale(1.3);  
    text-shadow: 0 0 20px rgba(255,255,255,0.8);  
  }  
  100% {  
    opacity: 1;  
    transform: scale(1);  
    text-shadow: 0 0 35px rgba(255,255,255,0.9);  
  }  
}  
  
.final-line {  
  margin-top: 10px;  
  font-style: italic;  
  opacity: 0;  
  animation: fadeText 2s forwards 6s;  
}  
  
@keyframes fadeText {  
  to { opacity: 0.9; }  
}  
  
/* HIDDEN YOUTUBE PLAYER */  
#player {  
  width: 0;  
  height: 0;  
  opacity: 0;  
  pointer-events: none;  
}  
</style>  
</head>  
  
<body>  
  
<div id="player"></div>  
  
<div class="card" id="card">  
  <h1>Asif Mustaffa 💕</h1>  
  <p>  
    Between late-night calls,<br>  
    quiet longing,<br>  
    and all the miles between us…<br><br>  
    I found something rare.<br>  
    I found you.  
  </p>  
  
  <h1>Will you be my Valentine? 💌</h1>  
  
  <button class="yes" onclick="sayYes()">Yes ❤️</button>  
  <button class="no" onclick="moveNo()">No 😅</button>  
</div>  
  
<div class="hearts"></div>  
  
<script>  
function sayYes() {  
  // Play YouTube song after click  
  document.getElementById("player").innerHTML = `  
    <iframe  
      src="https://www.youtube.com/embed/GX9x62kFsVU?autoplay=1&controls=0&loop=1&playlist=GX9x62kFsVU"  
      frameborder="0"  
      allow="autoplay"  
    ></iframe>  
  `;  
  
  document.getElementById("card").innerHTML = `  
    <h1>Gehra hua… ❤️</h1>  
  
    <p style="font-style: italic;">  
      “Asif, hazaar meel ka safar bhi chhota lagta hai,<br>  
      Jab dil har pal tum tak pahunch jaata hai.<br>  
      Tumhara naam hi kaafi hai meri har kahani ke liye,<br>  
      Har khamoshi mein bhi tum hi nazar aate ho.<br><br>  
  
      Hum door sahi, par dil ek hi dhadkan mein bandhe hain,<br>  
      Yeh ishq waqt aur faaslon se kabhi nahi darta.<br>  
      Mera har aaj, har kal tumse hi roshan hai,<br>  
      Aur meri sabse khoobsurat mohabbat… tum ho.”  
    </p>  
  
    <p style="font-style: italic; opacity: 0.85;">  
      “Agar mohabbat ko ek awaaz milti,<br>  
      toh woh sirf tumhara naam hota, Asif…<br>  
      aur main tumhari hoon — aaj bhi, aur hamesha.”  
    </p>  
  
    <div class="heart-merge">  
      <div class="heart left">❤️</div>  
      <div class="heart right">❤️</div>  
    </div>  
  
    <div class="merged-heart">❤️</div>  
    <div class="final-line">Two hearts. One us.</div>  
  
    <p style="margin-top: 15px; font-weight: bold;">  
      — Nafisa  
    </p>  
  `;  
}  
  
function moveNo() {  
  const btn = document.querySelector(".no");  
  btn.style.position = "absolute";  
  btn.style.left = Math.random() * window.innerWidth + "px";  
  btn.style.top = Math.random() * window.innerHeight + "px";  
}  
  
const heartsContainer = document.querySelector(".hearts");  
setInterval(() => {  
  const h = document.createElement("span");  
  h.innerHTML = "❤️";  
  h.style.left = Math.random() * 100 + "vw";  
  h.style.animationDuration = (Math.random() * 4 + 5) + "s";  
  heartsContainer.appendChild(h);  
  setTimeout(() => h.remove(), 8000);  
}, 250);  
</script>  
  
</body>  
</html>  
