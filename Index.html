<!DOCTYPE html>    
<html lang="it">    
<head>    
<meta charset="UTF-8">    
<meta name="viewport" content="width=device-width, initial-scale=1.0">  
<title>regalo del mio mori mori</title>    
    
<style>    
@import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&display=swap');    
    
body{    
    margin:0;    
    background:radial-gradient(circle,#0b1d17,#000);    
    font-family:'Orbitron',sans-serif;    
    color:#fff;    
    display:flex;    
    justify-content:center;    
    align-items:center;    
    min-height:100vh;    
    touch-action: none; /* Fondamentale per grattare da mobile */  
}    
    
.container{    
    width:90%;    
    max-width:650px;    
    background:rgba(0,0,0,0.9);    
    border:2px solid #ff0055;    
    border-radius:15px;    
    padding:25px;    
    box-shadow:0 0 30px #ff0055;    
}    
    
h1,h2{text-align:center;color:#ff0055;}    
    
.timer{    
    text-align:center;    
    font-size:22px;    
    margin-bottom:15px;    
    color:#00ffcc;    
}    
    
input,button{    
    width:100%;    
    padding:12px;    
    margin:10px 0;    
    border-radius:6px;    
    border:none;    
    font-family:'Orbitron',sans-serif;    
    box-sizing: border-box;   
}    
    
input{    
    background:#111;    
    color:#fff;    
    border:1px solid #ff0055;    
}    
    
button{    
    background:#ff0055;    
    color:#fff;    
    cursor:pointer;    
    font-weight: bold;    
    font-size: 16px;  
}    
    
.answer{    
    background:#111;    
    padding:12px;    
    margin:8px 0;    
    border-radius:6px;    
    cursor:pointer;    
    border:1px solid #333;    
}    
    
.answer.selected{    
    background:#0f8a3a;    
    box-shadow:0 0 10px #0f8a3a;    
}    
    
.hidden{display:none;}    
    
/* STILE GRATTA E VINCI */  
.scratch-container {  
    position: relative;  
    width: 300px;  
    height: 350px;  
    margin: 20px auto;  
    border: 4px solid #fff;  
    border-radius: 10px;  
    overflow: hidden;  
    user-select: none;  
}  
  
.result-layer {  
    width: 100%;  
    height: 100%;  
    background: #222;  
    display: flex;  
    flex-direction: column;  
    align-items: center;  
    justify-content: center;  
    text-align: center;  
    padding: 10px;  
    box-sizing: border-box;  
}  
  
.result-layer img {  
    max-width: 90%;  
    max-height: 200px;  
    object-fit: contain;  
    margin-bottom: 10px;  
    border-radius: 8px;  
    box-shadow: 0 0 15px rgba(255, 255, 255, 0.5);  
}  
  
canvas {  
    position: absolute;  
    top: 0;  
    left: 0;  
    cursor: crosshair;  
}  
</style>    
</head>    
    
<body>    
    
<div class="container">    
    
<div id="login">    
    <h1>ACCESSO RISERVATO</h1>    
    <input id="user" placeholder="Email" type="text">    
    <input id="pass" type="password" placeholder="Password">    
    <button onclick="checkLogin()">ENTRA NEL GIOCO</button>    
</div>    
    
<div id="rules" class="hidden">    
    <p>    
    Buongiorno concorrente numero 010 le regole del seguente gioco sono molto semplici.<br><br>    
    Verrà sottoposta a un quiz su delle semplicissime domande di cultura generale.<br>    
    Se le risposte corrette saranno 6 su 10 avrà accesso al suo regalo.<br><br>    
    In caso contrario visto che c’è stato da poco il suo compleanno può scegliere se vedere per l’ultima volta un quadrato un triangolo o un cerchio.<br><br>    
    Se ha capito la citazione può proseguire col quiz cliccando sul tasto start altrimenti può chiudere tutto qui e andare a casa.<br><br>    
    (Prima però accompagni il suo fantastico magnifico e inimitabile fidanzato ettore dall’avvocato grazie )    
    </p>    
    <button onclick="startQuiz()">START</button>    
</div>    
    
<div id="quiz" class="hidden">    
    <div class="timer" id="timerDisplay">05:00</div>    
    <div id="quizContent"></div>  
</div>    
    
<div id="final" class="hidden">    
    <h2>GRATTA E VINCI</h2>    
    <p style="text-align:center; font-size:14px; color:#aaa;">Passa il dito per scoprire il premio</p>  
      
    <div class="scratch-container">  
        <div id="resultLayer" class="result-layer"></div>  
        <canvas id="scratchCanvas" width="300" height="350"></canvas>  
    </div>  
</div>    
    
</div>    
    
<script>    
const questions=[    
{q:"Quante sono le Sfere del Drago (quelle classiche)?",a:["7 quelle della Terra + 8 quelle di Namek","1","4","7"],c:3},    
{q:"Qual è il sogno di Luffy?",a:["Trovare tutti i frutti","Diventare il Re dei Pirati","Diventare famoso","Pirata più forte"],c:1},    
{q:"Takemichi può tornare nel passato grazie a:",a:["Un sogno","Un telefono","Una stretta di mano","Un pugno"],c:2},    
{q:"Chi è il fratello di Goku?",a:["Bardack","Gohan","Raditz","Vegeta"],c:2},    
{q:"Chi usa principalmente le spade?",a:["Usopp","Zoro","Sanji","Luffy"],c:1},    
{q:"Chi è Mikey?",a:["Il protagonista","Il più alto","Il leader della Tokyo Manji Gang","Il più intelligente"],c:2},    
{q:"Come si chiama l’attacco più famoso di Goku?",a:["Final Flash","Genkidama","Big Bang","Kamehameha"],c:3},    
{q:"Che tipo di pirata è Luffy?",a:["Solitario","Ex marinaio","Capitano Cappello di Paglia","Grande nave"],c:2},    
{q:"Cosa vuole fare Takemichi tornando nel passato?",a:["Vendicarsi","Salvare Hinata","Cambiare scuola","Capo gang"],c:1},    
{q:"Quale NON è un anime?",a:["Naruto Shippuden: Il videogioco","One Piece","Dragon Ball","Tokyo Revengers"],c:0}    
];    
    
let score=0,current=0,time=300,timerInterval;    
    
function checkLogin(){    
    const userInput = document.getElementById("user").value.trim();  
    const passInput = document.getElementById("pass").value.trim();  
      
    if(userInput === "regalotardi" && passInput === "shein"){    
        document.getElementById("login").classList.add("hidden");    
        document.getElementById("rules").classList.remove("hidden");    
    } else {  
        alert("ACCESSO NEGATO");    
    }  
}    
    
function startQuiz(){    
    document.getElementById("rules").classList.add("hidden");    
    document.getElementById("quiz").classList.remove("hidden");    
    startTimer();    
    loadQuestion();    
}    
    
function startTimer(){    
    const timerDisplay = document.getElementById("timerDisplay");  
    timerInterval=setInterval(()=>{    
        time--;    
        let m=String(Math.floor(time/60)).padStart(2,'0');    
        let s=String(time%60).padStart(2,'0');    
        timerDisplay.innerText=`${m}:${s}`;    
        if(time<=0){    
            clearInterval(timerInterval);    
            endQuiz();    
        }    
    },1000);    
}    
    
function loadQuestion(){    
    if(current>=questions.length){endQuiz();return;}    
    const q=questions[current];    
    const quizDiv = document.getElementById("quiz");  
      
    const timerHTML = document.getElementById("timerDisplay").outerHTML;  
    quizDiv.innerHTML = timerHTML + `<h2>${current+1}) ${q.q}</h2>`;  
      
    q.a.forEach((ans,i)=>{    
        let d=document.createElement("div");    
        d.className="answer";    
        d.innerText=ans;    
        d.onclick=()=>selectAnswer(d,i);    
        quizDiv.appendChild(d);    
    });    
}    
    
function selectAnswer(el,i){    
    el.classList.add("selected");    
    const allAnswers = document.querySelectorAll('.answer');  
    allAnswers.forEach(a => a.style.pointerEvents = 'none');  
  
    if(i===questions[current].c) score++;    
      
    setTimeout(()=>{  
        current++;  
        loadQuestion();  
    },600);    
}    
    
function endQuiz(){    
    clearInterval(timerInterval);    
    document.getElementById("quiz").classList.add("hidden");    
    document.getElementById("final").classList.remove("hidden");    
    initScratchCard(); // Inizia il gratta e vinci  
}    
    
function initScratchCard() {  
    const resultLayer = document.getElementById("resultLayer");  
    const canvas = document.getElementById("scratchCanvas");  
    const ctx = canvas.getContext("2d");  
      
    // --- LINK IMMAGINI INSERITI QUI ---  
    // Vittoria: iPad Rosa (Link Ufficiale Apple)  
    const linkVittoria = "https://store.storeimages.cdn-apple.com/4668/as-images.apple.com/is/ipad-10th-gen-pink-select-202210";   
    // Sconfitta: Guardie Squid Game (Thumbnail YouTube HD)  
    const linkSconfitta = "https://img.youtube.com/vi/PBwTk38yYUA/maxresdefault.jpg";   
      
    if(score >= 6){  
        // VINTO  
        resultLayer.innerHTML = `  
            <h3 style="color:#0f8a3a">ACCESSO CONSENTITO</h3>  
            <img src="${linkVittoria}" alt="iPad Rosa">  
            <p style="font-size:18px; margin-top:5px;">iPad A16 rosa</p>  
        `;  
    } else {  
        // PERSO  
        resultLayer.innerHTML = `  
            <h3 style="color:#ff0000">ELIMINATO</h3>  
            <img src="${linkSconfitta}" alt="Squid Game">  
            <p style="font-size:18px; margin-top:5px;">Riprova sarai più fortunata</p>  
        `;  
    }  
  
    // Disegna la copertura argentata  
    ctx.fillStyle = "#C0C0C0";   
    ctx.fillRect(0, 0, canvas.width, canvas.height);  
      
    // Testo sopra la copertura  
    ctx.fillStyle = "#000";  
    ctx.font = "24px Orbitron";  
    ctx.textAlign = "center";  
    ctx.fillText("GRATTA QUI", canvas.width/2, canvas.height/2);  
  
    let isDrawing = false;  
  
    function scratch(x, y) {  
        ctx.globalCompositeOperation = "destination-out";  
        ctx.beginPath();  
        ctx.arc(x, y, 25, 0, Math.PI * 2);  
        ctx.fill();  
    }  
  
    // Eventi Mouse (PC)  
    canvas.addEventListener("mousedown", (e) => { isDrawing = true; });  
    canvas.addEventListener("mouseup", () => { isDrawing = false; });  
    canvas.addEventListener("mousemove", (e) => {  
        if (!isDrawing) return;  
        const rect = canvas.getBoundingClientRect();  
        scratch(e.clientX - rect.left, e.clientY - rect.top);  
    });  
  
    // Eventi Touch (Cellulare)  
    canvas.addEventListener("touchstart", (e) => {  
        isDrawing = true;  
        e.preventDefault();   
    }, {passive: false});  
      
    canvas.addEventListener("touchend", () => { isDrawing = false; });  
      
    canvas.addEventListener("touchmove", (e) => {  
        if (!isDrawing) return;  
        e.preventDefault();   
        const rect = canvas.getBoundingClientRect();  
        const touch = e.touches[0];  
        scratch(touch.clientX - rect.left, touch.clientY - rect.top);  
    }, {passive: false});  
}  
</script>    
    
</body>    
</html>  
