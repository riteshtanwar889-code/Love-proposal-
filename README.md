<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For My Rabbit ❤️</title>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial,sans-serif;
}

body{
height:100vh;
display:flex;
justify-content:center;
align-items:center;
background:linear-gradient(135deg,#ff6ec7,#7873f5);
overflow:hidden;
}

.container{
text-align:center;
background:white;
padding:30px;
border-radius:20px;
box-shadow:0 0 20px rgba(0,0,0,0.2);
position:relative;
width:90%;
max-width:450px;
}

h1{
color:#ff1493;
margin-bottom:15px;
}

p{
font-size:20px;
margin-bottom:25px;
}

button{
padding:12px 25px;
font-size:18px;
border:none;
border-radius:25px;
cursor:pointer;
margin:10px;
transition:0.3s;
}

#yesBtn{
background:#28a745;
color:white;
}

#yesBtn:hover{
transform:scale(1.1);
}

#noBtn{
background:#dc3545;
color:white;
position:absolute;
}

.heart{
position:absolute;
font-size:25px;
animation:float 5s linear infinite;
opacity:0.8;
}

@keyframes float{
0%{
transform:translateY(100vh);
opacity:0;
}
100%{
transform:translateY(-100px);
opacity:1;
}
}
</style>
</head>

<body>

<div class="container" id="proposalBox">
<h1>💍 Will You Marry Me? 💍</h1>

<p>
Meri Jaan 😘,<br><br>
You are the most beautiful part of my life ❤️<br>
Will you be mine forever? 🥺💍
</p>

<button id="yesBtn" onclick="accepted()">Yes ❤️</button>
<button id="noBtn">No 😅</button>

</div>

<script>

const noBtn=document.getElementById("noBtn");

noBtn.addEventListener("mouseover",function(){

let x=Math.random()*(window.innerWidth-120);
let y=Math.random()*(window.innerHeight-120);

noBtn.style.left=x+"px";
noBtn.style.top=y+"px";

});

function accepted(){

document.body.innerHTML=`

<div style="
height:100vh;
display:flex;
justify-content:center;
align-items:center;
text-align:center;
background:linear-gradient(135deg,#ff6ec7,#7873f5);
color:white;
padding:20px;
">

<div>

<h1 style="font-size:3rem;">💍 You Are Married, Meri Jaan 😘 💍</h1>

<h2 style="margin-top:20px;">
I Love You My Rabbit 💗🐰
</h2>

<h2 style="margin-top:15px;">
I Will Always Love You ❤️
</h2>

<h3 style="margin-top:20px;">
Forever & Ever ✨💕
</h3>

<h1 style="margin-top:30px;">🎉❤️🎊</h1>

</div>

</div>
`;

for(let i=0;i<80;i++){

let heart=document.createElement("div");

heart.innerHTML="💖";

heart.style.position="absolute";
heart.style.left=Math.random()*100+"vw";
heart.style.top=Math.random()*100+"vh";
heart.style.fontSize=(20+Math.random()*30)+"px";

heart.style.animation="float 5s linear infinite";

document.body.appendChild(heart);
}
}

function createHeart(){

let heart=document.createElement("div");

heart.classList.add("heart");

heart.innerHTML="💖";

heart.style.left=Math.random()*100+"vw";

heart.style.animationDuration=
(3+Math.random()*4)+"s";

document.body.appendChild(heart);

setTimeout(()=>{
heart.remove();
},5000);
}

setInterval(createHeart,500);

</script>

</body>
</html>
