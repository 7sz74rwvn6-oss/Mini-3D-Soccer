<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<title>Mini Futbol 2D</title>
<style>
body { margin:0; padding:0; overflow:hidden; background:#27ae60; font-family:Arial; }
#score {
  position:absolute; top:20px; left:50%; transform:translateX(-50%);
  font-size:48px; color:white; z-index:2; transition: all 0.2s;
}
#gameArea {
  position:relative; width:100vw; height:100vh; overflow:hidden;
}
#ball, #keeper {
  position:absolute; border-radius:50%;
}
#ball { width:40px; height:40px; background:#f1c40f; }
#keeper { width:60px; height:60px; background:#e74c3c; top:50px; }
#joystickBase {
  position:absolute; bottom:20px; left:20px; width:140px; height:140px;
  background: rgba(255,255,255,0.2); border-radius:50%; touch-action:none; z-index:2;
}
#joystickStick {
  position:absolute; width:70px; height:70px; background: rgba(255,255,255,0.5);
  border-radius:50%; top:35px; left:35px; touch-action:none;
}
#shootBtn {
  position:absolute; bottom:30px; right:30px; width:100px; height:100px;
  background: rgba(255,0,0,0.5); border-radius:50%; font-size:24px; color:white; border:none; z-index:2;
}
</style>
</head>
<body>
<div id="score">Gol: 0</div>
<div id="gameArea">
  <div id="ball"></div>
  <div id="keeper"></div>
  <div id="joystickBase"><div id="joystickStick"></div></div>
  <button id="shootBtn">Şut</button>
</div>

<script>
const ball = document.getElementById('ball');
const keeper = document.getElementById('keeper');
const joystickBase = document.getElementById('joystickBase');
const stick = document.getElementById('joystickStick');
const shootBtn = document.getElementById('shootBtn');
const scoreEl = document.getElementById('score');

let score = 0;
let ballPos = {x:window.innerWidth/2-20, y:window.innerHeight-100};
let keeperPos = {x:window.innerWidth/2-30, y:50};
let joystick={x:0,y:0,active:false};
let shootSpeed = 0;

// Joystick
stick.addEventListener('touchstart', ()=>joystick.active=true);
stick.addEventListener('touchend', ()=>{
  joystick.active=false; joystick.x=0; joystick.y=0;
  stick.style.left='35px'; stick.style.top='35px';
});
stick.addEventListener('touchmove', e=>{
  if(!joystick.active) return;
  const touch=e.touches[0];
  const rect=joystickBase.getBoundingClientRect();
  let dx = touch.clientX-(rect.left+rect.width/2);
  let dy = touch.clientY-(rect.top+rect.height/2);
  const max=rect.width/2;
  if(dx>max) dx=max; if(dx<-max) dx=-max;
  if(dy>max) dy=max; if(dy<-max) dy=-max;
  joystick.x = dx/max;
  joystick.y = dy/max;
  // stick’i topun hareketine göre göster
  stick.style.left = (dx+35)+'px';
  stick.style.top = (dy+35)+'px';
  e.preventDefault();
},{passive:false});

// Şut tuşu
shootBtn.addEventListener('touchstart', ()=>{
  shootSpeed = 15; // px/frame ileri hız
});

// Güncelleme
function updatePositions(){
  ball.style.left = ballPos.x+'px';
  ball.style.top = ballPos.y+'px';
  keeper.style.left = keeperPos.x+'px';
  keeper.style.top = keeperPos.y+'px';
}

// Oyun döngüsü
function gameLoop(){
  // Joystick ile top hareketi
  ballPos.x += joystick.x*5;
  ballPos.y -= joystick.y*5;

  // Şut hareketi
  if(shootSpeed>0){
    ballPos.y -= shootSpeed;
    shootSpeed *= 0.9;
  }

  // Saha sınırları
  ballPos.x = Math.max(Math.min(ballPos.x, window.innerWidth-40),0);
  ballPos.y = Math.max(Math.min(ballPos.y, window.innerHeight-40),0);

  // Kaleci sola-sağa hareket
  keeperPos.x = window.innerWidth/2 + Math.sin(Date.now()*0.003)*200;

  // Gol kontrolü (kaleciyi geçerse)
  if(ballPos.y <= keeperPos.y + 60 && Math.abs(ballPos.x - (keeperPos.x+30))>30){
    score++;
    scoreEl.innerText = "Gol: "+score;
    scoreEl.style.transform='scale(1.5)';
    setTimeout(()=>scoreEl.style.transform='scale(1)',200);
    ballPos = {x:window.innerWidth/2-20, y:window.innerHeight-100};
    shootSpeed=0;
  }

  updatePositions();
  requestAnimationFrame(gameLoop);
}

// Başlangıç pozisyonu
updatePositions();
requestAnimationFrame(gameLoop);

</script>
</body>
</html>
