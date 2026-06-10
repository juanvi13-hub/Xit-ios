# Xit-ios
Xit funcional iPhones 14 a 15<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>👹xit iOS 14💀</title>

<style>
body {
  margin: 0;
  height: 100vh;
  background: linear-gradient(120deg, #1e1e2f, #2b2b45);
  overflow: hidden;
  font-family: Arial;
}

/* PANEL */
#panel {
  width: 240px;
  position: absolute;
  top: 100px;
  left: 100px;
  background: rgba(255,255,255,0.1);
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255,255,255,0.2);
  border-radius: 12px;
  color: white;
  box-shadow: 0 10px 30px rgba(0,0,0,0.4);
}

/* HEADER */
#header {
  padding: 10px;
  background: rgba(255,255,255,0.15);
  cursor: grab;
  font-weight: bold;
  text-align: center;
  border-top-left-radius: 12px;
  border-top-right-radius: 12px;
}

/* BOTONES */
button {
  width: 90%;
  margin: 8px 10px;
  padding: 8px;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  background: #4a90e2;
  color: white;
  transition: 0.2s;
}

button:hover {
  background: #2d6cdf;
}
</style>
</head>

<body>

<div id="panel">
  <div id="header">👹xit iOS 14💀</div>

  <button onclick="openApp()">Open Free Fire</button>
  <button onclick="brightness()">Brillo Máximo</button>
  <button onclick="gamingMode()">Modo Gaming</button>
  <button onclick="voice()">Voz Activada</button>
</div>

<script>
let panel = document.getElementById("panel");
let header = document.getElementById("header");

let isDragging = false;
let offsetX, offsetY;

/* DRAG */
header.addEventListener("mousedown", (e) => {
  isDragging = true;
  offsetX = e.clientX - panel.offsetLeft;
  offsetY = e.clientY - panel.offsetTop;
  header.style.cursor = "grabbing";
});

document.addEventListener("mousemove", (e) => {
  if (isDragging) {
    panel.style.left = (e.clientX - offsetX) + "px";
    panel.style.top = (e.clientY - offsetY) + "px";
  }
});

document.addEventListener("mouseup", () => {
  isDragging = false;
  header.style.cursor = "grab";
});

/* FUNCIONES */

function openApp() {
  window.location.href = "intent://com.dts.freefireth#Intent;package=com.dts.freefireth;end";
}

function brightness() {
  document.body.style.filter = "brightness(200%)";
  alert("Brillo máximo activado");
}

function gamingMode() {
  document.body.style.filter = "contrast(130%) saturate(150%)";
  alert("Modo gaming activado");
}

function voice() {
  let msg = new SpeechSynthesisUtterance("opción activada, listo para jugar");
  speechSynthesis.speak(msg);
}
</script>

</body>
</html>
