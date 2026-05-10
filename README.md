
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Mom ❤️</title>

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&display=swap" rel="stylesheet">

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    font-family:'Inter',sans-serif;
    background:#050505;
    overflow:hidden;
    color:white;
}

/* Background */

.bg{
    position:fixed;
    inset:0;
    background:
    radial-gradient(circle at top left, rgba(255,0,120,0.18), transparent 35%),
    radial-gradient(circle at bottom right, rgba(0,150,255,0.18), transparent 35%),
    linear-gradient(to bottom,#050505,#000000);
    z-index:-5;
}

#particles{
    position:fixed;
    inset:0;
    z-index:-4;
}

.cursorGlow{
    position:fixed;
    width:300px;
    height:300px;
    border-radius:50%;
    background:radial-gradient(circle, rgba(255,0,120,0.18), transparent 70%);
    pointer-events:none;
    transform:translate(-50%,-50%);
    z-index:-3;
}

/* Layout */

.container{
    min-height:100vh;
    padding:40px;
    display:flex;
    justify-content:center;
    align-items:center;
}

.card{
    width:min(1150px,100%);
    min-height:700px;
    border-radius:36px;
    background:rgba(255,255,255,0.06);
    border:1px solid rgba(255,255,255,0.1);
    backdrop-filter:blur(18px);
    overflow:hidden;
    position:relative;
    box-shadow:
    0 0 80px rgba(255,0,120,0.12),
    0 0 120px rgba(0,120,255,0.08);
}

/* Sidebar */

.sidebar{
    position:absolute;
    left:0;
    top:0;
    bottom:0;
    width:240px;
    background:rgba(255,255,255,0.03);
    border-right:1px solid rgba(255,255,255,0.08);
    padding:30px 20px;
}

.logo{
    font-size:28px;
    font-weight:800;
    margin-bottom:40px;
}

.logo span{
    color:#ff5ca8;
}

.navBtn{
    width:100%;
    border:none;
    background:transparent;
    color:#cfcfcf;
    text-align:left;
    padding:18px;
    border-radius:16px;
    margin-bottom:12px;
    cursor:pointer;
    transition:0.3s;
    font-size:16px;
}

.navBtn:hover,
.active{
    background:rgba(255,255,255,0.08);
    color:white;
    transform:translateX(4px);
}

/* Main */

.main{
    margin-left:240px;
    padding:50px;
    min-height:700px;
    position:relative;
}

.page{
    display:none;
    animation:fade 0.5s ease;
}

.page.activePage{
    display:block;
}

@keyframes fade{
    from{
        opacity:0;
        transform:translateY(10px);
    }
    to{
        opacity:1;
        transform:translateY(0);
    }
}

.title{
    font-size:72px;
    line-height:0.95;
    font-weight:800;
    margin-bottom:30px;
}

.gradient{
    background:linear-gradient(90deg,#ffffff,#ff70b8);
    -webkit-background-clip:text;
    -webkit-text-fill-color:transparent;
}

.text{
    color:#d2d2d2;
    line-height:1.9;
    font-size:19px;
    max-width:650px;
}

.hero{
    display:flex;
    justify-content:space-between;
    align-items:center;
    gap:40px;
    flex-wrap:wrap;
}

.photo{
    width:320px;
    height:430px;
    object-fit:cover;
    border-radius:28px;
    border:1px solid rgba(255,255,255,0.12);
    box-shadow:0 0 50px rgba(255,0,120,0.25);
    transition:0.5s;
}

.photo:hover{
    transform:scale(1.03) rotate(-1deg);
}

/* Cards */

.grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
    gap:20px;
    margin-top:30px;
}

.box{
    background:rgba(255,255,255,0.05);
    border:1px solid rgba(255,255,255,0.08);
    border-radius:24px;
    padding:25px;
    transition:0.3s;
    cursor:pointer;
}

.box:hover{
    transform:translateY(-6px);
    background:rgba(255,255,255,0.08);
}

.box h3{
    margin-bottom:14px;
    font-size:22px;
}

.box p{
    color:#cfcfcf;
    line-height:1.7;
}

/* Secret button */

.secretBtn{
    margin-top:40px;
    border:none;
    padding:18px 30px;
    border-radius:999px;
    background:linear-gradient(90deg,#ff2d75,#ff7eb3);
    color:white;
    font-size:16px;
    font-weight:700;
    cursor:pointer;
    transition:0.3s;
    box-shadow:0 0 30px rgba(255,0,120,0.25);
}

.secretBtn:hover{
    transform:scale(1.05);
}

.popup{
    position:fixed;
    inset:0;
    background:rgba(0,0,0,0.7);
    display:none;
    justify-content:center;
    align-items:center;
    z-index:50;
}

.popupCard{
    width:min(600px,90%);
    background:#111;
    border-radius:30px;
    padding:40px;
    border:1px solid rgba(255,255,255,0.08);
    text-align:center;
    animation:pop 0.4s ease;
}

@keyframes pop{
    from{
        opacity:0;
        transform:scale(0.8);
    }
    to{
        opacity:1;
        transform:scale(1);
    }
}

.popupCard h2{
    font-size:42px;
    margin-bottom:20px;
}

.popupCard p{
    color:#d2d2d2;
    line-height:1.9;
    font-size:18px;
}

.close{
    margin-top:30px;
    border:none;
    background:#ff2d75;
    color:white;
    padding:14px 26px;
    border-radius:999px;
    cursor:pointer;
}

/* Responsive */

@media(max-width:900px){

body{
    overflow:auto;
}

.sidebar{
    position:relative;
    width:100%;
    border-right:none;
    border-bottom:1px solid rgba(255,255,255,0.08);
}

.main{
    margin-left:0;
    padding:30px;
}

.title{
    font-size:52px;
}

.hero{
    justify-content:center;
}

.photo{
    width:100%;
    max-width:320px;
}

}

</style>
</head>
<body>

<div class="bg"></div>
<canvas id="particles"></canvas>
<div class="cursorGlow"></div>

<div class="container">

<div class="card">

<div class="sidebar">

<div class="logo">
MOM<span>.EXE</span>
</div>

<button class="navBtn active" onclick="showPage(0,this)">
🏠 Home
</button>

<button class="navBtn" onclick="showPage(1,this)">
💖 Memories
</button>

<button class="navBtn" onclick="showPage(2,this)">
⚡ Mom Powers
</button>

<button class="navBtn" onclick="showPage(3,this)">
🌌 Final Message
</button>

</div>

<div class="main">

<!-- PAGE 1 -->
<div class="page activePage">

<div class="hero">

<div>

<div class="title">
For The <span class="gradient">Strongest</span><br>
Person I Know.
</div>

<div class="text">
You loved me from the start

<br><br>

You always supported me.You helped me when no one did and you made me feel happy.Youre the best


<br><br>

I don't say enough,
but a huge part of who I am exists because of you.
</div>

<button class="secretBtn" onclick="openPopup()">
Open Hidden Message
</button>

</div>



</div>

</div>

<!-- PAGE 2 -->
<div class="page">

<div class="title">
Favorite <span class="gradient">Memories</span>
</div>

<div class="grid">

<div class="box">
<h3>THE LOVE YOU GAVE ME</h3>
<p>
You supported me everytime.I love you
</p>
</div>

<div class="box">
<h3>Family Trips</h3>
<p>
We went on trips together but when we were having fun you were working for it
</p>
</div>

<div class="box">
<h3>Childhood</h3>
<p>
You fed me when when i irritated.you helped me in loose and tight..
</p>
</div>

</div>

</div>

<!-- PAGE 3 -->
<div class="page">

<div class="title">
Mom <span class="gradient">Abilities</span>
</div>

<div class="grid">

<div class="box">
<h3>🧠 Mind Reading</h3>
<p>
Knows something is wrong before anyone speaks.
</p>
</div>

<div class="box">
<h3>⚡ Infinite Energy</h3>
<p>
Runs the entire family with zero rest.
</p>
</div>



<div class="box">
<h3>sorry for fighting with kittu</h3>
<p>
I understand it now and i wont irritate her and even if she does I will ignore
</p>
</div>

</div>

</div>

<!-- PAGE 4 -->
<div class="page">

<div class="title">
No Universe Gets A Better <span class="gradient">Mom</span>.
</div>

<div class="text">
Thank you for every sacrifice I was too young to understand.

<br><br>

For every late night.
Every worry.
Every small thing nobody thanked you for.

<br><br>

You are the heart of this family.

<br><br>

Happy Mother's Day ❤️
</div>

</div>

</div>

</div>

</div>

<!-- POPUP -->

<div class="popup" id="popup">

<div class="popupCard">

<h2>Secret Message</h2>

<p>
You spent years making life easier for everyone else.

<br><br>

This page is small compared to everything you've done,
but I hope it reminds you how important you are.
</p>

<button class="close" onclick="closePopup()">
Close
</button>

</div>

</div>

<script>

/* PAGE SWITCHING */

const pages = document.querySelectorAll('.page');
const navBtns = document.querySelectorAll('.navBtn');

function showPage(index,btn){

pages.forEach(p=>p.classList.remove('activePage'));
navBtns.forEach(b=>b.classList.remove('active'));

pages[index].classList.add('activePage');
btn.classList.add('active');

}

/* POPUP */

function openPopup(){
    document.getElementById('popup').style.display='flex';
}

function closePopup(){
    document.getElementById('popup').style.display='none';
}

/* PARTICLES */

const canvas = document.getElementById('particles');
const ctx = canvas.getContext('2d');

canvas.width = window.innerWidth;
canvas.height = window.innerHeight;

const particles=[];

for(let i=0;i<100;i++){

particles.push({
    x:Math.random()*canvas.width,
    y:Math.random()*canvas.height,
    r:Math.random()*2,
    dx:(Math.random()-0.5)*0.5,
    dy:(Math.random()-0.5)*0.5
});

}

function animate(){

ctx.clearRect(0,0,canvas.width,canvas.height);

ctx.fillStyle='rgba(255,255,255,0.7)';

particles.forEach(p=>{

ctx.beginPath();
ctx.arc(p.x,p.y,p.r,0,Math.PI*2);
ctx.fill();

p.x += p.dx;
p.y += p.dy;

if(p.x<0 || p.x>canvas.width) p.dx*=-1;
if(p.y<0 || p.y>canvas.height) p.dy*=-1;

});

requestAnimationFrame(animate);

}

animate();

/* CURSOR GLOW */

const glow = document.querySelector('.cursorGlow');

window.addEventListener('mousemove',(e)=>{

    glow.style.left = e.clientX + 'px';
    glow.style.top = e.clientY + 'px';

});

</script>

</body>
</html>
```

