# BIRTHDAY-WISHES-.-
BIRTHDAY WISHES TO MY SISTER !!
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>Rashi • Birthday Experience</title>

<style>
*{box-sizing:border-box;margin:0;padding:0}

html,body{
  width:100%;
  height:100%;
  overflow:hidden;
}

body{
  font-family:Arial,sans-serif;
  color:#fff;
  background:#03050d;
}

/* ---------- ANIMATED BACKGROUND ---------- */

#bg{
  position:fixed;
  inset:0;
  overflow:hidden;
  background:
    radial-gradient(circle at 15% 20%,#7117d8,transparent 30%),
    radial-gradient(circle at 85% 80%,#ff187f,transparent 28%),
    radial-gradient(circle at 50% 50%,#062b62,transparent 35%),
    #03050d;
  transition:background 1s ease;
}

.stars{
  position:absolute;
  inset:-50%;
  background-image:
    radial-gradient(#fff 1px,transparent 1px);
  background-size:42px 42px;
  opacity:.35;
  animation:stars 18s linear infinite;
}

@keyframes stars{
  to{transform:translate(80px,120px)}
}

/* QUESTION-SPECIFIC EFFECTS */

.wave{
  position:absolute;
  width:70vw;
  height:70vw;
  border-radius:50%;
  border:2px solid rgba(0,220,255,.18);
  left:15%;
  top:15%;
  animation:wave 5s infinite;
}

.wave:nth-child(2){
  animation-delay:1.5s;
}

.wave:nth-child(3){
  animation-delay:3s;
}

@keyframes wave{
  0%{transform:scale(.5);opacity:.7}
  100%{transform:scale(2.2);opacity:0}
}

.ring{
  position:absolute;
  width:280px;
  height:280px;
  border-radius:50%;
  border:3px solid #00eaff;
  box-shadow:
    0 0 20px #00eaff,
    inset 0 0 25px #7a3cff;
  left:50%;
  top:50%;
  transform:translate(-50%,-50%);
  animation:spin 5s linear infinite;
}

.ring:before,
.ring:after{
  content:"";
  position:absolute;
  inset:25px;
  border:2px solid #ff36a8;
  border-radius:50%;
}

.ring:after{
  inset:55px;
  border-color:#ffd45c;
}

@keyframes spin{
  to{transform:translate(-50%,-50%) rotate(360deg)}
}

.lightning{
  position:absolute;
  width:3px;
  height:100vh;
  background:linear-gradient(
    transparent,#fff,#00eaff,transparent
  );
  filter:drop-shadow(0 0 10px #00eaff);
  opacity:.25;
  animation:flashLightning 2s infinite;
}

.lightning:nth-child(1){left:20%;transform:rotate(20deg)}
.lightning:nth-child(2){left:70%;transform:rotate(-18deg);animation-delay:.7s}

@keyframes flashLightning{
  0%,85%,100%{opacity:0}
  88%{opacity:1}
  90%{opacity:.1}
  92%{opacity:1}
}

/* ---------- SCREEN ---------- */

.screen{
  position:fixed;
  inset:0;
  display:flex;
  align-items:center;
  justify-content:center;
  padding:14px;
  text-align:center;
  z-index:5;
}

.hidden{
  display:none!important;
}

.card{
  width:min(92vw,650px);
  max-height:92vh;
  overflow:auto;
  padding:clamp(22px,5vw,40px);
  border-radius:28px;

  background:rgba(5,5,20,.58);
  border:1px solid rgba(255,255,255,.22);
  backdrop-filter:blur(18px);

  box-shadow:
    0 0 30px rgba(0,220,255,.12),
    0 0 60px rgba(255,0,150,.14);

  animation:cardIn .8s ease;
}

.card::-webkit-scrollbar{
  display:none;
}

@keyframes cardIn{
  from{
    opacity:0;
    transform:scale(.8) translateY(25px);
  }
  to{
    opacity:1;
    transform:scale(1) translateY(0);
  }
}

.tag{
  font-size:11px;
  letter-spacing:4px;
  opacity:.65;
  margin-bottom:18px;
}

h1{
  font-size:clamp(30px,8vw,48px);
  line-height:1.15;
  text-shadow:
    0 0 12px #fff,
    0 0 35px #ff2d9d;
}

.rashi{
  font-size:clamp(48px,13vw,75px);
  font-weight:900;
  margin:18px 0;

  background:linear-gradient(
    90deg,
    #fff,
    #ff4eaf,
    #9f7cff,
    #00eaff,
    #ffd45c,
    #fff
  );

  background-size:400%;
  -webkit-background-clip:text;
  color:transparent;

  animation:gradient 4s linear infinite;
}

@keyframes gradient{
  to{background-position:400%}
}

.question{
  font-size:clamp(19px,5vw,27px);
  line-height:1.5;
  margin:24px auto 28px;
  max-width:570px;
}

button{
  border:0;
  border-radius:50px;
  padding:14px 25px;
  margin:6px;
  font-size:16px;
  font-weight:bold;
  cursor:pointer;
  touch-action:manipulation;
}

.yes{
  color:#6d0050;
  background:#fff;
  box-shadow:
    0 0 14px #fff,
    0 0 30px #ff35a8;
}

.no{
  color:#fff;
  background:#ff376d;
  position:relative;
  z-index:20;
}

.hint{
  font-size:12px;
  opacity:.5;
  margin-top:14px;
}

/* ---------- COUNTDOWN ---------- */

.count{
  font-size:clamp(80px,25vw,140px);
  font-weight:bold;
  margin:15px;
  text-shadow:
    0 0 20px #fff,
    0 0 70px #00eaff,
    0 0 100px #ff2da2;
  animation:count .8s ease;
}

@keyframes count{
  from{transform:scale(2);opacity:0}
  to{transform:scale(1);opacity:1}
}

/* ---------- PORTAL ---------- */

.portal{
  width:min(55vw,260px);
  aspect-ratio:1;
  margin:25px auto;
  border-radius:50%;

  background:
    radial-gradient(circle,
      #fff 0%,
      #ffd45c 5%,
      #ff2d9d 18%,
      #7c35ff 42%,
      #00eaff 62%,
      transparent 70%
    );

  box-shadow:
    0 0 25px #fff,
    0 0 60px #ff2d9d,
    0 0 100px #00eaff;

  animation:portal 1.5s infinite alternate;
}

@keyframes portal{
  from{transform:scale(.8) rotate(0)}
  to{transform:scale(1.08) rotate(180deg)}
}

/* ---------- CAKE ---------- */

.cake{
  font-size:clamp(70px,20vw,110px);
  margin:15px;
  animation:cake 1s infinite alternate;
}

@keyframes cake{
  from{transform:translateY(0) rotate(-3deg)}
  to{transform:translateY(-12px) rotate(3deg)}
}

/* ---------- ENVELOPE ---------- */

.envelopeWrap{
  margin:35px auto 20px;
  perspective:1000px;
}

.envelope{
  position:relative;
  width:min(78vw,330px);
  height:min(50vw,215px);
  margin:auto;
  cursor:pointer;

  background:linear-gradient(
    135deg,
    #7927ff,
    #ff2494,
    #00bfe9
  );

  border-radius:10px;

  box-shadow:
    0 0 25px #ff2b9d,
    0 0 55px rgba(0,220,255,.5);

  transition:1s;
}

.envelopeBack{
  position:absolute;
  inset:0;
  background:linear-gradient(
    135deg,#6420cc,#d61a83
  );
}

.flap{
  position:absolute;
  inset:0;
  background:linear-gradient(
    135deg,#ff69bd,#8238e9
  );
  clip-path:polygon(0 0,100% 0,50% 58%);
  transform-origin:top center;
  transition:1s;
  z-index:6;
}

.letter{
  position:absolute;
  left:8%;
  bottom:8px;
  width:84%;
  min-height:150px;

  background:#fff;
  color:#3d1639;

  border-radius:6px;
  padding:18px;

  transform:translateY(65px);
  transition:1.2s;

  z-index:4;
}

.envelope.open .flap{
  transform:rotateX(180deg);
}

.envelope.open .letter{
  transform:translateY(-105px);
}

.seal{
  position:absolute;
  width:54px;
  height:54px;
  border-radius:50%;
  background:#fff;
  color:#d50075;

  display:flex;
  align-items:center;
  justify-content:center;

  left:50%;
  top:50%;
  transform:translate(-50%,-50%);

  z-index:10;
  box-shadow:0 0 20px #fff;
  transition:.4s;
}

.envelope.open .seal{
  opacity:0;
}

/* ---------- CLEAN MESSAGE ---------- */

.messageScreen{
  position:fixed;
  inset:0;
  display:flex;
  align-items:center;
  justify-content:center;
  padding:18px;
  z-index:30;

  background:
    radial-gradient(circle at 50% 30%,
      #39116b,
      transparent 35%),
    #03050d;

  animation:messageIn 1s ease;
}

.messageBox{
  width:min(92vw,650px);
  max-height:90vh;
  overflow:auto;

  padding:28px 22px;

  background:rgba(255,255,255,.08);
  border:1px solid rgba(255,255,255,.25);
  border-radius:28px;

  box-shadow:
    0 0 35px rgba(255,45,160,.25),
    0 0 70px rgba(0,220,255,.12);
}

.messageBox::-webkit-scrollbar{
  display:none;
}

.messageTitle{
  font-size:clamp(32px,9vw,52px);
  font-weight:bold;

  background:linear-gradient(
    90deg,#ffd45c,#fff,#ff55b7,#00eaff
  );

  -webkit-background-clip:text;
  color:transparent;

  background-size:300%;
  animation:gradient 4s linear infinite;
}

.messageText{
  margin:25px auto;
  font-size:clamp(16px,4.5vw,20px);
  line-height:1.8;
  max-width:560px;
}

.signature{
  font-size:22px;
  margin-top:20px;
}

/* ---------- EFFECTS ---------- */

.particle{
  position:fixed;
  top:-40px;
  z-index:40;
  pointer-events:none;
  font-size:24px;
  animation:fall linear forwards;
}

.heart{
  position:fixed;
  bottom:-30px;
  z-index:40;
  pointer-events:none;
  animation:heart linear forwards;
}

.firework{
  position:fixed;
  z-index:40;
  pointer-events:none;
  font-size:42px;
  animation:firework 1.2s ease-out forwards;
}

@keyframes fall{
  to{
    transform:translateY(110vh) rotate(720deg);
    opacity:0;
  }
}

@keyframes heart{
  to{
    transform:translateY(-110vh);
    opacity:0;
  }
}

@keyframes firework{
  0%{
    transform:scale(.2);
    opacity:1;
  }
  100%{
    transform:scale(4);
    opacity:0;
  }
}

@keyframes messageIn{
  from{
    opacity:0;
    transform:scale(.8);
  }
  to{
    opacity:1;
    transform:scale(1);
  }
}

@media(max-height:600px){
  .card{
    padding:18px;
  }

  .question{
    margin:15px auto;
  }

  .cake{
    font-size:65px;
    margin:5px;
  }

  .tag{
    margin-bottom:10px;
  }
}
</style>
</head>

<body>

<div id="bg">
  <div class="stars"></div>
</div>


<!-- INTRO -->

<div class="screen" id="intro">

<div class="card">

<div class="tag">PRIVATE EXPERIENCE • 001</div>

<h1>
A message has been<br>
waiting for you...
</h1>

<div class="rashi">
RASHI ❤️
</div>

<p style="font-size:18px;line-height:1.7">
Four questions.<br>
One final surprise.<br>
Are you ready?
</p>

<br>

<button class="yes" onclick="startQuiz()">
BEGIN THE JOURNEY ✨
</button>

</div>

</div>


<!-- QUIZ -->

<div class="screen hidden" id="quiz">

<div class="card">

<div class="tag" id="number">
QUESTION 01 / 04
</div>

<div class="question" id="question"></div>

<div id="buttons">

<button class="yes" onclick="yesAnswer()">
YES ❤️
</button>

<button class="no" id="noButton" onclick="noAnswer()">
NO 😈
</button>

</div>

<div class="hint">
Choose carefully... your answer unlocks the next scene.
</div>

</div>

</div>


<!-- COUNTDOWN -->

<div class="screen hidden" id="countdown">

<div class="card">

<div class="tag">
FINAL ACCESS SEQUENCE
</div>

<div class="count" id="countNumber">
3
</div>

<p style="font-size:18px">
Preparing Rashi's surprise...
</p>

</div>

</div>


<!-- PORTAL -->

<div class="screen hidden" id="portalScreen">

<div class="card">

<div class="tag">
ACCESS GRANTED ✓
</div>

<h1>THE MOMENT HAS ARRIVED</h1>

<div class="portal"></div>

<p>
Opening the birthday dimension... ✨
</p>

</div>

</div>


<!-- BIRTHDAY -->

<div class="screen hidden" id="birthday">

<div class="card">

<div class="tag">
TODAY • A VERY SPECIAL DAY
</div>

<h1>
HAPPY BIRTHDAY
</h1>

<div class="rashi">
RASHI ❤️
</div>

<div class="cake">
🎂
</div>

<p style="font-size:18px;line-height:1.7">
Some days become memories.<br>
Some people make those memories special.
</p>

<br>

<button class="yes" onclick="showEnvelope()">
THERE'S ONE MORE THING 💌
</button>

</div>

</div>


<!-- ENVELOPE -->

<div class="screen hidden" id="envelopeScreen">

<div class="card">

<div class="tag">
A PRIVATE MESSAGE • FOR RASHI
</div>

<h1 style="font-size:30px">
Something was saved for you. 💌
</h1>

<div class="envelopeWrap">

<div class="envelope"
id="envelope"
onclick="openEnvelope()">

<div class="envelopeBack"></div>

<div class="letter">
<strong>For Rashi ❤️</strong>
<br>
<span style="font-size:13px">
A little message is waiting...
</span>
</div>

<div class="flap"></div>

<div class="seal">
❤️
</div>

</div>

</div>

<p id="hint" style="opacity:.65">
Tap the envelope to reveal your message ✨
</p>

</div>

</div>


<script>

/* ================= QUESTIONS ================= */

const questions=[

"If you could keep one beautiful moment from this year forever, would you? 🌙",

"What makes a moment truly unforgettable — the memory itself, or the people who make it special? ✨",

"If a mystery surprise was created especially for you, would curiosity make you open it? 🎁",

"One final choice, Rashi... are you ready to unlock the message waiting specifically for you? 🔐"

];

let current=0;


/* ================= START ================= */

function startQuiz(){

  document.getElementById("intro")
  .classList.add("hidden");

  document.getElementById("quiz")
  .classList.remove("hidden");

  setScene(0);

  showQuestion();

}


/* ================= SCENE ================= */

function setScene(n){

  const bg=document.getElementById("bg");

  if(n===0){

    bg.style.background=
    "radial-gradient(circle at 20% 20%,#7120d9,transparent 30%),"+
    "radial-gradient(circle at 80% 80%,#ff1880,transparent 28%),"+
    "#03050d";

  }

  if(n===1){

    bg.style.background=
    "radial-gradient(circle at 50% 20%,#006d9d,transparent 30%),"+
    "radial-gradient(circle at 80% 80%,#00d4ff,transparent 25%),"+
    "#020817";

  }

  if(n===2){

    bg.style.background=
    "radial-gradient(circle at 50% 50%,#4612a8,transparent 30%),"+
    "radial-gradient(circle at 20% 80%,#ff249b,transparent 25%),"+
    "#05000f";

  }

  if(n===3){

    bg.style.background=
    "radial-gradient(circle at 20% 20%,#005b9c,transparent 28%),"+
    "radial-gradient(circle at 80% 70%,#ff207e,transparent 28%),"+
    "radial-gradient(circle at 50% 50%,#3a006b,transparent 35%),"+
    "#02050d";

  }

}


/* ================= QUESTION ================= */

function showQuestion(){

  document.getElementById("question")
  .innerHTML=questions[current];

  document.getElementById("number")
  .innerHTML=
  "QUESTION 0"+(current+1)+" / 04";

  resetNo();

}


/* ================= YES ================= */

function yesAnswer(){

  current++;

  if(current>=4){

    startCountdown();

  }else{

    setScene(current);

    showQuestion();

  }

}


/* ================= NO ================= */

function noAnswer(){

  const btn=
  document.getElementById("noButton");

  const margin=12;

  const maxX=
  window.innerWidth-btn.offsetWidth-margin;

  const maxY=
  window.innerHeight-btn.offsetHeight-margin;

  const x=
  margin+
  Math.random()*Math.max(20,maxX-margin);

  const y=
  margin+
  Math.random()*Math.max(20,maxY-margin);

  btn.style.position="fixed";

  btn.style.left=x+"px";

  btn.style.top=y+"px";

  btn.style.transform=
  "rotate("+
  (Math.random()*35-17)+"deg)";

}


/* ================= RESET ================= */

function resetNo(){

  const btn=
  document.getElementById("noButton");

  btn.style.position="relative";
  btn.style.left="auto";
  btn.style.top="auto";
  btn.style.transform="none";

}


/* ================= COUNTDOWN ================= */

function startCountdown(){

  document.getElementById("quiz")
  .classList.add("hidden");

  document.getElementById("countdown")
  .classList.remove("hidden");

  let n=3;

  const display=
  document.getElementById("countNumber");

  display.innerHTML=n;

  const timer=setInterval(()=>{

    n--;

    if(n>0){

      display.innerHTML=n;

      display.style.animation="none";

      void display.offsetWidth;

      display.style.animation=
      "count .8s ease";

    }else{

      clearInterval(timer);

      display.innerHTML="✨";

      setTimeout(openPortal,700);

    }

  },1000);

}


/* ================= PORTAL ================= */

function openPortal(){

  document.getElementById("countdown")
  .classList.add("hidden");

  document.getElementById("portalScreen")
  .classList.remove("hidden");

  setTimeout(()=>{

    document.getElementById("portalScreen")
    .classList.add("hidden");

    document.getElementById("birthday")
    .classList.remove("hidden");

    celebration(35);

  },2600);

}


/* ================= BIRTHDAY -> ENVELOPE ================= */

function showEnvelope(){

  document.getElementById("birthday")
  .classList.add("hidden");

  document.getElementById("envelopeScreen")
  .classList.remove("hidden");

}


/* ================= OPEN ENVELOPE ================= */

function openEnvelope(){

  const envelope=
  document.getElementById("envelope");

  if(envelope.classList.contains("open"))
  return;

  envelope.classList.add("open");

  document.getElementById("hint")
  .innerHTML="Opening your message... 💖";

  setTimeout(showCleanMessage,1700);

}


/* ================= CLEAN MESSAGE ================= */

function showCleanMessage(){

  /* Envelope screen completely disappears */

  document.getElementById("envelopeScreen")
  .classList.add("hidden");


  const screen=
  document.createElement("div");

  screen.className="messageScreen";

  screen.innerHTML=`

    <div class="messageBox">

      <div class="tag">
        FROM A LITTLE CORNER OF THE HEART ❤️
      </div>

      <div class="messageTitle">
        HAPPY BIRTHDAY RASHI
      </div>

      <div class="messageText" id="typing"></div>

      <div class="signature">
        🎂✨ With lots of good wishes ✨🎂
      </div>

    </div>

  `;

  document.body.appendChild(screen);

  typeMessage();

  celebration(100);

}


/* ================= TYPING ================= */

function typeMessage(){

  const message=
  "Dear Rashi ❤️<br><br>"+
  "Some people make ordinary moments feel special without even trying. Today is your day, and I hope this new chapter brings you happiness that stays, dreams that come true, people who genuinely value you, and countless moments worth remembering. ✨<br><br>"+
  "Keep smiling, keep dreaming, and never forget how wonderfully unique you are. May this year give you more reasons to laugh, more memories to treasure, and many beautiful surprises along the way. 🌷<br><br>"+
  "<strong>Happy Birthday, Rashi! 🎂❤️</strong><br>"+
  "May your next chapter be your most beautiful one yet. ✨";

  const box=
  document.getElementById("typing");

  let i=0;

  function type(){

    if(i<message.length){

      box.innerHTML=message.slice(0,i+1);

      i++;

      setTimeout(type,18);

    }

  }

  type();

}


/* ================= CELEBRATION ================= */

function celebration(amount){

  /* CONFETTI */

  for(let i=0;i<amount;i++){

    const p=
    document.createElement("div");

    p.className="particle";

    p.innerHTML=[
      "🎉","🎊","✨","⭐",
      "💖","🎈","💫","🌟"
    ][Math.floor(Math.random()*8)];

    p.style.left=
    Math.random()*100+"vw";

    p.style.animationDuration=
    (2+Math.random()*4)+"s";

    document.body.appendChild(p);

    setTimeout(()=>p.remove(),7000);

  }


  /* HEARTS */

  for(let i=0;i<Math.floor(amount/2);i++){

    const h=
    document.createElement("div");

    h.className="heart";

    h.innerHTML=
    ["❤️","💖","💗","💜"]
    [Math.floor(Math.random()*4)];

    h.style.left=
    Math.random()*100+"vw";

    h.style.fontSize=
    (18+Math.random()*25)+"px";

    h.style.animationDuration=
    (3+Math.random()*4)+"s";

    document.body.appendChild(h);

    setTimeout(()=>h.remove(),8000);

  }


  /* FIREWORKS */

  if(amount>=80){

    for(let i=0;i<45;i++){

      setTimeout(()=>{

        const f=
        document.createElement("div");

        f.className="firework";

        f.innerHTML=
        ["✨","💥","⭐","💫"]
        [Math.floor(Math.random()*4)];

        f.style.left=
        (5+Math.random()*90)+"vw";

        f.style.top=
        (5+Math.random()*75)+"vh";

        document.body.appendChild(f);

        setTimeout(()=>f.remove(),1300);

      },i*90);

    }

  }

}

</script>

</body>
</html>
