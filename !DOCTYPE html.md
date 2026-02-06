<!DOCTYPE html>  
<html lang="en">  
<head>  
<meta charset="UTF-8">  
<title>Will You Be My Valentine?</title>  
<meta name="viewport" content="width=device-width, initial-scale=1.0">  
  
<style>  
body {  
  margin: 0;  
  height: 100vh;  
  background: linear-gradient(135deg, #ffdde1, #ee9ca7);  
  display: flex;  
  justify-content: center;  
  align-items: center;  
  font-family: Georgia, serif;  
  color: #5a0c2d;  
  text-align: center;  
  transition: background 4s ease;  
}  
  
body.dim {  
  background: linear-gradient(135deg, #2b0a18, #000000);  
}  
  
#card {  
  background: rgba(255,255,255,0.92);  
  padding: 25px;  
  border-radius: 20px;  
  max-width: 360px;  
  box-shadow: 0 15px 40px rgba(0,0,0,0.3);  
}  
  
h1 {  
  font-size: 26px;  
}  
  
button {  
  margin: 12px;  
  padding: 10px 22px;  
  font-size: 16px;  
  border-radius: 20px;  
  border: none;  
  cursor: pointer;  
  background: #c2185b;  
  color: white;  
}  
  
#typedText {  
  font-size: 15px;  
  line-height: 1.8;  
  white-space: pre-line;  
}  
  
.cursor {  
  display: inline-block;  
  animation: blink 1s infinite;  
}  
  
@keyframes blink {  
  0%,50% {opacity:1;}  
  51%,100% {opacity:0;}  
}  
  
#finalQuestion {  
  display: none;  
  font-size: 18px;  
  font-weight: bold;  
  margin-top: 25px;  
}  
  
#whisper, #finalLine {  
  display: none;  
  margin-top: 12px;  
  font-style: italic;  
  opacity: 0.75;  
}  
  
/* Hearts */  
.heart-merge {  
  position: relative;  
  width: 120px;  
  height: 60px;  
  margin: 30px auto 10px;  
  display: none;  
}  
  
.heart {  
  position: absolute;  
  font-size: 42px;  
  opacity: 0;  
}  
  
.heart.left {  
  left: 0;  
  animation: leftMove 4s forwards;  
}  
  
.heart.right {  
  right: 0;  
  animation: rightMove 4s forwards;  
}  
  
@keyframes leftMove {  
  0% {transform: translateX(0); opacity:0;}  
  20% {opacity:1;}  
  100% {transform: translateX(36px) scale(1.2); opacity:1;}  
}  
  
@keyframes rightMove {  
  0% {transform: translateX(0); opacity:0;}  
  20% {opacity:1;}  
  100% {transform: translateX(-36px) scale(1.2); opacity:1;}  
}  
  
.merged-heart {  
  display: none;  
  font-size: 55px;  
  margin-top: 10px;  
  text-shadow:  
    0 0 10px rgba(255,80,120,0.8),  
    0 0 20px rgba(255,80,120,0.8),  
    0 0 30px rgba(255,80,120,0.8);  
}  
  
/* Real heartbeat (lub–dub) */  
.heartbeat {  
  animation: heartbeat 1.4s infinite;  
}  
  
@keyframes heartbeat {  
  0% {transform: scale(1);}  
  10% {transform: scale(1.18);}  
  20% {transform: scale(1);}  
  30% {transform: scale(1.12);}  
  40% {transform: scale(1);}  
  100% {transform: scale(1);}  
}  
</style>  
</head>  
  
<body>  
  
<div id="card">  
  <h1>Asif ❤️</h1>  
  <p>  
    Miles apart, yet my heart finds its way to you every day.<br>  
    So I have one question…  
  </p>  
  <h2>Will you be my Valentine?</h2>  
  <button onclick="sayYes()">Yes 💖</button>  
</div>  
  
<!-- Hidden YouTube player -->  
<iframe id="ytSong" width="0" height="0" frameborder="0" allow="autoplay"></iframe>  
  
<script>  
function sayYes() {  
  document.body.classList.add("dim");  
  
  document.getElementById("ytSong").src =  
    "https://www.youtube.com/embed/GX9x62kFsVU?autoplay=1";  
  
  if (navigator.vibrate) {  
    navigator.vibrate([200,100,200]);  
  }  
  
  document.getElementById("card").innerHTML = `  
    <h1>For You, Asif ❤️</h1>  
    <div id="typedText"></div><span class="cursor">▍</span>  
  
    <div id="finalQuestion">  
      Will you be my Valentine,<br>  
      and remain the one my heart aches for?  
    </div>  
  
    <div id="whisper">“I want you… even from afar.”</div>  
    <div id="finalLine">“Say yes… my heart already has.”</div>  
  
    <div class="heart-merge">  
      <div class="heart left">❤️</div>  
      <div class="heart right">❤️</div>  
    </div>  
  
    <div class="merged-heart">❤️</div>  
  
    <p id="signature" style="display:none; font-weight:bold; margin-top:15px;">  
      — Nafisa  
    </p>  
  `;  
  
  const text = `  
Asif,  
  
Loving you from a distance has made my feelings louder,  
deeper, and impossible to hide.  
The space between us doesn’t weaken what I feel —  
it sharpens it, intensifies it, makes it burn brighter.  
  
There are nights when I close my eyes  
and imagine your presence so vividly  
that my heart forgets we are miles apart.  
I miss you fiercely, endlessly, completely.  
  
You are not just someone I love,  
you are someone I long for.  
My heart chooses you without hesitation,  
and my soul recognizes you without doubt.  
  
Distance may keep our hands apart,  
but it has no power over my heart.  
It already belongs to you —  
completely, unapologetically, and endlessly.  
`;  
  
  let i = 0;  
  const speed = 60;  
  
  function typeWriter() {  
    if (i < text.length) {  
      document.getElementById("typedText").innerHTML += text.charAt(i);  
      i++;  
      setTimeout(typeWriter, speed);  
    } else {  
      document.querySelector(".cursor").style.display = "none";  
  
      setTimeout(()=>document.getElementById("finalQuestion").style.display="block",1200);  
      setTimeout(()=>document.getElementById("whisper").style.display="block",2200);  
      setTimeout(()=>document.getElementById("finalLine").style.display="block",3200);  
  
      setTimeout(()=>{  
        document.querySelector(".heart-merge").style.display="block";  
        const heart=document.querySelector(".merged-heart");  
        heart.style.display="block";  
        heart.classList.add("heartbeat");  
        document.getElementById("signature").style.display="block";  
  
        if (navigator.vibrate) {  
          setInterval(()=>navigator.vibrate([120,80,90]),1400);  
        }  
      },4500);  
    }  
  }  
  typeWriter();  
}  
</script>  
  
</body>  
</html>  
