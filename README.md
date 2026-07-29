<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday Saloni ❤️</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Poppins',sans-serif;
}

body{

height:100vh;
overflow:hidden;
display:flex;
justify-content:center;
align-items:center;

background:linear-gradient(-45deg,
#ff9ecf,
#ffd6e7,
#fff3c4,
#d8f3ff);

background-size:400% 400%;

animation:bgMove 12s infinite alternate;

}

@keyframes bgMove{

0%{
background-position:left;
}

100%{
background-position:right;
}

}

.card{

width:90%;
max-width:760px;

background:rgba(255,255,255,.18);

backdrop-filter:blur(18px);

border:2px solid rgba(255,255,255,.3);

border-radius:30px;

padding:35px;

text-align:center;

box-shadow:0 20px 60px rgba(0,0,0,.25);

animation:cardIn 1.2s ease;

position:relative;

z-index:5;

}

@keyframes cardIn{

0%{

transform:scale(.6);

opacity:0;

}

100%{

transform:scale(1);

opacity:1;

}

}

.title{

font-size:48px;

font-weight:bold;

color:white;

text-shadow:

0 0 10px hotpink,

0 0 20px deeppink,

0 0 40px pink;

animation:glow 2s infinite alternate;

}

@keyframes glow{

from{

text-shadow:
0 0 10px hotpink,
0 0 20px deeppink;

}

to{

text-shadow:
0 0 25px hotpink,
0 0 50px deeppink,
0 0 70px white;

}

}

.subtitle{

margin-top:10px;

font-size:28px;

color:#fff;

}

.cat{

font-size:75px;

margin:20px;

animation:catJump 1.8s infinite;

}

@keyframes catJump{

50%{

transform:translateY(-18px) rotate(-5deg);

}

}

.cake{

font-size:90px;

margin:20px;

animation:cakeFloat 3s infinite;

}

@keyframes cakeFloat{

50%{

transform:translateY(-10px);

}

}

.message{

font-size:20px;

line-height:1.8;

color:white;

margin-top:15px;

}

button{

margin-top:30px;

padding:16px 45px;

font-size:20px;

border:none;

border-radius:50px;

background:#ff2d7a;

color:white;

cursor:pointer;

transition:.4s;

box-shadow:0 10px 25px rgba(255,20,147,.4);

}

button:hover{

transform:scale(1.08);

background:#ff006e;

}

.float{

position:absolute;

bottom:-100px;

font-size:35px;

animation:floatUp linear infinite;

opacity:.9;

}

@keyframes floatUp{

0%{

transform:translateY(0);

opacity:0;

}

15%{

opacity:1;

}

100%{

transform:translateY(-120vh);

opacity:0;

}

}

.footer{

margin-top:25px;

color:white;

font-size:18px;

}

</style>

</head>

<body>

<div class="card">

<div class="cat">🐱🎀🐱</div>

<div class="title">
🎉 Happy Birthday 🎉
</div>

<div class="subtitle">
💖 Dear Saloni 💖
</div>

<div class="cake">
🎂
</div>

<div class="message">

May your smile always shine brighter than the stars. ✨

<br><br>

May your dreams come true...

May happiness always stay with you...

May today become the most beautiful memory of your life.

💖🌸🎂

</div>

<button onclick="nextPart()">

🎁 Open Surprise

</button>

<div class="footer">

🐱 Stay Cute • 🌸 Stay Happy • ❤️ Keep Smiling

</div>

</div>

<script>

const emojis=["💖","🎈","✨","🐱","🌸","🎉","💕","🦋"];

for(let i=0;i<45;i++){

let e=document.createElement("div");

e.className="float";

e.innerHTML=emojis[Math.floor(Math.random()*emojis.length)];

e.style.left=Math.random()*100+"%";

e.style.animationDuration=(6+Math.random()*8)+"s";

e.style.animationDelay=Math.random()*6+"s";

e.style.fontSize=(20+Math.random()*30)+"px";

document.body.appendChild(e);

}

function nextPart() {

alert("🎂 Surprise is getting ready for Saloni! ❤️");

}/* ===========================
   PART 2 - Cake Cut Animation
   =========================== */

// 3D style cake replace
document.querySelector(".cake").innerHTML = `
<div id="cake3d">
    <div class="top"></div>
    <div class="cream"></div>
    <div class="bottom"></div>
    <div class="candle"></div>
    <div class="flame"></div>
</div>
`;

// Extra CSS
const style=document.createElement("style");

style.innerHTML=`

#cake3d{

width:220px;
height:180px;
margin:auto;
position:relative;
perspective:1000px;

}

.top{

width:220px;
height:70px;
background:#ff9ec4;
border-radius:50%;
position:absolute;
top:25px;

}

.cream{

width:220px;
height:30px;
background:white;
position:absolute;
top:60px;

}

.bottom{

width:220px;
height:80px;
background:#ff7aa8;
position:absolute;
top:85px;
border-radius:0 0 20px 20px;

}

.candle{

width:12px;
height:45px;
background:#ffffff;
position:absolute;
left:104px;
top:-10px;
border-radius:10px;

}

.flame{

width:18px;
height:18px;
background:gold;
border-radius:50%;
position:absolute;
left:101px;
top:-25px;
box-shadow:0 0 25px gold;
animation:flicker .4s infinite alternate;

}

@keyframes flicker{

from{
transform:scale(1);
}

to{
transform:scale(1.2);
}

}

.cut{

animation:cutCake 1.3s forwards;

}

@keyframes cutCake{

0%{

transform:rotate(0);

}

100%{

transform:rotate(-8deg)
translateX(-30px);

}

}

.rightHalf{

animation:rightCake 1.3s forwards;

}

@keyframes rightCake{

100%{

transform:
rotate(8deg)
translateX(30px);

}

}

`;

document.head.appendChild(style);


// Replace button function

function nextPart(){

let cake=document.getElementById("cake3d");

cake.classList.add("cut");

document.querySelector(".flame").style.display="none";

setTimeout(()=>{

alert("🎂 Cake Cut Successfully!\n\nHappy Birthday Saloni ❤️🥳");

},1300);

}/* ===========================
   PART 3 - Final Celebration
   =========================== */

// Fireworks + Confetti + Letter

function showCelebration(){

// Confetti
for(let i=0;i<180;i++){

let c=document.createElement("div");

c.style.position="fixed";
c.style.left=Math.random()*100+"vw";
c.style.top="-20px";
c.style.width="10px";
c.style.height="10px";
c.style.borderRadius="50%";
c.style.background=`hsl(${Math.random()*360},100%,60%)`;
c.style.pointerEvents="none";
c.style.zIndex="9999";

document.body.appendChild(c);

let y=0;

let fall=setInterval(()=>{

y+=6;

c.style.top=y+"px";
c.style.transform=`rotate(${y*4}deg)`;

if(y>window.innerHeight){

clearInterval(fall);

c.remove();

}

},20);

}

// Fireworks
for(let i=0;i<12;i++){

setTimeout(()=>{

let fw=document.createElement("div");

fw.innerHTML="🎆";

fw.style.position="fixed";

fw.style.left=Math.random()*80+10+"%";

fw.style.top=Math.random()*40+10+"%";

fw.style.fontSize="60px";

fw.style.zIndex="9999";

fw.style.animation="boom .8s ease";

document.body.appendChild(fw);

setTimeout(()=>fw.remove(),900);

},i*400);

}

// Birthday Letter
setTimeout(()=>{

let box=document.createElement("div");

box.innerHTML=`

<div style="
position:fixed;
top:50%;
left:50%;
transform:translate(-50%,-50%);
width:90%;
max-width:500px;
background:white;
padding:30px;
border-radius:25px;
box-shadow:0 0 40px hotpink;
text-align:center;
z-index:99999;
font-family:Poppins;
">

<h2 style="color:#ff1493;">
💖 Happy Birthday Saloni 💖
</h2>

<p style="font-size:18px;line-height:1.8;color:#444;">

May your smile always shine. ✨<br>

May every dream come true. 🌈<br>

May your life always be filled with happiness. ❤️<br><br>

Never stop smiling because your smile makes the world brighter. 😊<br><br>

🎂 Happy Birthday Saloni 🎂

</p>

<button onclick="this.parentElement.parentElement.remove()"
style="
padding:12px 30px;
border:none;
background:#ff1493;
color:white;
border-radius:30px;
cursor:pointer;
font-size:18px;
">

Thank You ❤️

</button>

</div>

`;

document.body.appendChild(box);

},1800);

}

// Firework animation

const style2=document.createElement("style");

style2.innerHTML=`

@keyframes boom{

0%{

transform:scale(.2);

opacity:0;

}

50%{

transform:scale(1.5);

opacity:1;

}

100%{

transform:scale(2);

opacity:0;

}

}

`;

document.head.appendChild(style2);


// Replace button function

nextPart=function(){

let cake=document.getElementById("cake3d");

if(cake){

cake.classList.add("cut");

}

let flame=document.querySelector(".flame");

if(flame){

flame.style.display="none";

}

setTimeout(()=>{

showCelebration();

},1000);

}

</script>

</body>
</html># Birthday-wishes-
