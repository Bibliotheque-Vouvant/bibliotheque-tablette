<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<title>Tablette Bibliothèque</title>

<style>

body{
font-family: Arial;
background:#eef2f7;
margin:0;
text-align:center;
}

header{
background:#2c5aa0;
color:white;
padding:30px;
font-size:32px;
}

.grid{
display:grid;
grid-template-columns: repeat(3, 1fr);
gap:30px;
padding:40px;
max-width:900px;
margin:auto;
}

.card{
background:white;
padding:40px;
border-radius:18px;
box-shadow:0 6px 14px rgba(0,0,0,0.2);
text-decoration:none;
color:#333;
font-size:24px;
transition:transform 0.2s;
}

.card:active{
transform:scale(0.96);
}

.icon{
font-size:70px;
margin-bottom:15px;
}

footer{
margin-top:20px;
padding:20px;
color:#666;
font-size:18px;
}

</style>

<script>

var inactivityTime = function () {
    var time;

    function goHome() {
        location.reload();
    }

    function resetTimer() {
        clearTimeout(time);
        time = setTimeout(goHome, 300000);
    }

    document.onload = resetTimer;
    document.onmousemove = resetTimer;
    document.onkeypress = resetTimer;
    document.onclick = resetTimer;
    document.ontouchstart = resetTimer;
};

function adminAccess(){
var code = prompt("Code administrateur");
if(code=="85120"){
alert("Mode administrateur");
}
}

window.onload = inactivityTime;

</script>

</head>

<body>

<header onclick="adminAccess()">
📚 Bibliothèque  
<br>Tablette en accès public
</header>

<div class="grid">

<a class="card" href="https://emedia.vendee.fr/" target="_self">
<div class="icon">📖</div>
Plateforme e-media
</a>

<a class="card" href="intent:#Intent;action=android.intent.action.MAIN;package=com.toutapprendre;end">
<div class="icon">📰</div>
Accès à la presse
</a>

<a class="card" href="https://www.google.fr" target="_self">
<div class="icon">🌐</div>
Internet
</a>

<a class="card" href="https://www.youtube.com" target="_self">
<div class="icon">▶</div>
YouTube
</a>

<a class="card" href="https://read.bookcreator.com/D3NbA00iL9SuPzJ020XG8IXbMKD3/vnYH2uOARBqjIJ_kAVmC3Q/TdowKg0PTGem7uWyfPBESQ" target="_self">
<div class="icon">📚</div>
Les Juifs en Vendée
</a>

</div>

<footer>
Merci de respecter le matériel de la bibliothèque
</footer>

</body>
</html>
