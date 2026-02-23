<!DOCTYPE html>
<html lang="ro">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>one-mc.ro</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
<style>
*{margin:0;padding:0;box-sizing:border-box;}
body{font-family:'Poppins',sans-serif;background:linear-gradient(135deg,#050505,#120000,#1a0000);color:white;overflow-x:hidden;}
body::before{content:"";position:fixed;width:500px;height:500px;background:red;filter:blur(150px);opacity:0.15;top:-150px;left:-150px;animation:moveGlow 10s infinite alternate ease-in-out;}
@keyframes moveGlow{from{transform:translate(0,0);}to{transform:translate(300px,200px);}}
header{text-align:center;padding:30px;font-size:32px;font-family:'Orbitron',sans-serif;font-weight:700;letter-spacing:3px;background:rgba(0,0,0,0.7);backdrop-filter:blur(10px);border-bottom:1px solid rgba(255,0,0,0.3);animation:fadeDown 1s ease;}
@keyframes fadeDown{from{opacity:0; transform:translateY(-30px);}to{opacity:1; transform:translateY(0);}}
nav{display:flex;justify-content:center;gap:60px;padding:20px;background:rgba(0,0,0,0.6);}
nav a{position:relative;cursor:pointer;font-weight:600;transition:0.3s;}
nav a::after{content:"";position:absolute;left:0;bottom:-5px;width:0%;height:2px;background:red;transition:0.4s;}
nav a:hover{color:red;}
nav a:hover::after{width:100%;}
section{display:none;padding:80px 10%;animation:fadeIn 0.6s ease forwards;}
section.active{display:block;}
@keyframes fadeIn{from{opacity:0; transform:translateY(20px);}to{opacity:1; transform:translateY(0);}}
h2{font-size:28px;margin-bottom:30px;animation:pulseText 2s infinite alternate;}
@keyframes pulseText{from{color:white;}to{color:red;}}
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:30px;}
.card{background:rgba(0,0,0,0.7);border:1px solid rgba(255,0,0,0.2);padding:25px;border-radius:15px;transition:0.4s;position:relative;overflow:hidden;}
.card::before{content:"";position:absolute;width:100%;height:100%;top:0;left:-100%;background:linear-gradient(120deg,transparent,rgba(255,0,0,0.3),transparent);transition:0.6s;}
.card:hover::before{left:100%;}
.card:hover{transform:translateY(-10px) scale(1.03);box-shadow:0 0 25px rgba(255,0,0,0.6);}
button{margin-top:15px;padding:10px 20px;border:none;border-radius:8px;background:red;color:white;font-weight:600;cursor:pointer;transition:0.3s;}
button:hover{background:darkred;transform:scale(1.1);}
footer{text-align:center;padding:25px;background:rgba(0,0,0,0.8);border-top:1px solid rgba(255,0,0,0.3);margin-top:60px;font-size:14px;}
</style>
</head>
<body>
<header>one-mc.ro</header>
<nav>
<a onclick="showSection('store')">Store</a>
<a onclick="showSection('info')">Informatii</a>
</nav>
<section id="store" class="active">
<h2>Sa donati cate 10 euro de persoana sa o aducem pe bunica la viata</h2>
<div class="grid">
<div class="card">
<h3>Premium Package</h3>
<p>Donati 50 euro si sunteti stapanii nostri</p>
<button onclick="window.open('https://discord.gg/onemc','_blank')">Doneaza</button>
</div>
<div class="card">
<h3>VIP Access</h3>
<p>Beneficii speciale disponibile.</p>
<button onclick="window.open('https://discord.gg/onemc','_blank')">Doneaza</button>
</div>
</div>
</section>
<section id="info">
<h2>MarioNac ne este dor de bunica ta</h2>
</section>
<footer>© 2026 one-mc.ro - Toate drepturile rezervate</footer>
<script>
function showSection(id){
    document.querySelectorAll("section").forEach(sec=>sec.classList.remove("active"));
    document.getElementById(id).classList.add("active");
}
</script>
</body>
</html>
