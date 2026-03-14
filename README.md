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
  height: 100%;
  width: 100%;
  overflow: hidden; /* Pour plein écran */
}

header{
  background:#2c5aa0;
  color:white;
  padding:30px;
  font-size:30px;
}

.grid{
  display:grid;
  grid-template-columns: repeat(2, 1fr);
  gap:30px;
  padding:40px;
  max-width:700px;
  margin:auto;
}

.card{
  background:white;
  padding:35px;
  border-radius:15px;
  box-shadow:0 4px 10px rgba(0,0,0,0.2);
  text-decoration:none;
  color:#333;
  font-size:22px;
}

.icon{
  font-size:60px;
  margin-bottom:10px;
}

footer{
  margin-top:20px;
  padding:20px;
  color:#666;
  font-size:16px;
}

/* Centrage total du body pour plein écran */
body > * {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  min-height: 100%;
}
</style>

<script>
var inactivityTime = function () {
    var time;
    window.onload = resetTimer;
    document.onmousemove = resetTimer;
    document.onkeypress = resetTimer;
    document.onclick = resetTimer;

    function goHome() {
        location.reload();
    }

    function resetTimer() {
        clearTimeout(time);
        time = setTimeout(goHome, 300000);
    }
};

window.onload = inactivityTime;

function adminAccess(){
  var code = prompt("Code administrateur");
  if(code=="85120"){
    window.location="about:blank";
  }
}
</script>

</head>

<body>

<header onclick="adminAccess()">
📚 Bibliothèque  
<br>Tablette en accès public
</header>

<div class="grid">

<a class="card" href="https://www.youtube.com" target="_blank">
<div class="icon">▶</div>
YouTube
</a>

<a class="card" href="https://VOTRE-PLATEFORME-EMEDIA.FR" target="_blank">
<div class="icon">📖</div>
Plateforme e-media
</a>

<a class="card" href="https://www.google.fr" target="_blank">
<div class="icon">🌐</div>
Internet
</a>

<a class="card" href="file:///storage/emulated/0/Documents/" target="_blank">
<div class="icon">📄</div>
Documents PDF
</a>

<a class="card" href="https://read.bookcreator.com/D3NbA00iL9SuPzJ020XG8IXbMKD3/vnYH2uOARBqjIJ_kAVmC3Q/TdowKg0PTGem7uWyfPBESQ" target="_blank">
<div class="icon">📚</div>
Les Juifs en Vendée<br>
Fanny et Cécile Rajngewic
</a>

</div>

<footer>
Merci de respecter le matériel de la bibliothèque
</footer>

<!-- Script plein écran -->
<script>
function goFullscreen() {
    const elem = document.documentElement;
    if (elem.requestFullscreen) {
        elem.requestFullscreen();
    } else if (elem.webkitRequestFullscreen) { // Android / Safari
        elem.webkitRequestFullscreen();
    } else if (elem.msRequestFullscreen) { // Edge / IE
        elem.msRequestFullscreen();
    }
    document.body.removeEventListener("click", goFullscreen);
}

// Écoute le premier tap n'importe où sur le body
document.body.addEventListener("click", goFullscreen);
</script>

</body>
</html>
