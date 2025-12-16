<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>M S GAMER – User Panel</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;800&display=swap" rel="stylesheet">

<!-- Firebase -->
<script src="https://www.gstatic.com/firebasejs/8.10.0/firebase-app.js"></script>
<script src="https://www.gstatic.com/firebasejs/8.10.0/firebase-database.js"></script>

<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:Poppins}
body{
  background:radial-gradient(circle at top,#0f2027,#050511 70%);
  color:#fff;
  text-align:center;
}

/* LOGO */
.vip-logo{
  width:110px;
  margin:15px auto 5px;
  border-radius:50%;
  border:4px solid gold;
  box-shadow:0 0 25px gold,0 0 60px #ffcc00;
}

/* 3D NAME */
.game-name{
  font-size:38px;
  font-weight:800;
  color:#00ffd5;
  text-shadow:0 2px 0 #009f9f,0 4px 0 #007777,0 6px 0 #004f4f,0 10px 18px rgba(0,255,213,.9);
  margin-bottom:8px;
}

/* NOTICE */
.notice3d{
  margin:12px auto;
  font-size:18px;
  font-weight:700;
  color:#ffea00;
  text-shadow:0 2px 0 #bfa800,0 4px 0 #8f7f00,0 6px 12px rgba(255,234,0,.9);
  animation:pulse 2s infinite;
}
@keyframes pulse{0%{transform:scale(1)}50%{transform:scale(1.05)}100%{transform:scale(1)}}

/* SLIDER */
.slider{
  width:92%;
  max-width:420px;
  height:180px;
  margin:15px auto;
  border-radius:18px;
  overflow:hidden;
  box-shadow:0 0 25px rgba(0,255,213,.4);
}
.slider img{
  width:100%;
  height:100%;
  object-fit:cover;
}

/* APP CARD */
.app{
  background:#0b0b0b;
  margin:15px auto;
  width:92%;
  max-width:420px;
  border-radius:20px;
  padding:15px;
  box-shadow:0 0 25px rgba(0,255,213,.25);
}
.app img{
  width:100%;
  height:160px;
  object-fit:cover;
  border-radius:15px;
}
.app h3{margin:10px 0 5px}
.app p{font-size:13px;opacity:.7}
.app button{
  margin-top:10px;
  width:100%;
  padding:10px;
  border:none;
  border-radius:12px;
  background:linear-gradient(45deg,#00ffd5,#00a2ff);
  color:#000;
  font-weight:700;
  cursor:pointer;
}

/* FLOATING SOCIAL */
.floating-social{
  position:fixed;
  right:15px;
  bottom:20px;
  display:flex;
  flex-direction:column;
  gap:12px;
  z-index:9999;
}
.float-btn{
  width:55px;
  height:55px;
  border-radius:50%;
  display:flex;
  align-items:center;
  justify-content:center;
  font-size:26px;
  cursor:pointer;
  color:#fff;
  animation:float 2s infinite;
}
.float-btn.wa{
  background:#25D366;
  box-shadow:0 0 20px rgba(37,211,102,.9);
}
.float-btn.ig{
  background:linear-gradient(45deg,#f58529,#dd2a7b,#8134af);
  box-shadow:0 0 20px rgba(221,42,123,.9);
}
@keyframes float{0%{transform:translateY(0)}50%{transform:translateY(-6px)}100%{transform:translateY(0)}}
</style>
</head>

<body>

<img id="siteLogo" class="vip-logo" src="">
<div class="game-name" id="gameName">M S GAMER</div>
<div id="notice" class="notice3d"></div>

<div class="slider">
  <img id="sliderImg" src="">
</div>

<div id="apps"></div>

<!-- FLOATING ICONS -->
<div class="floating-social">
  <div id="floatWA" class="float-btn wa" onclick="openWA()">💬</div>
  <div id="floatIG" class="float-btn ig" onclick="openIG()">📸</div>
</div>

<script>
/* FIREBASE CONFIG */
const firebaseConfig = {
  apiKey: "AIzaSyD5D_QLvv0_QsXRIEIzBqYlYaaHE6NT_Wo",
  authDomain: "download-fba43.firebaseapp.com",
  databaseURL: "https://download-fba43-default-rtdb.firebaseio.com",
  projectId: "download-fba43",
  storageBucket: "download-fba43.firebasestorage.app",
  messagingSenderId: "995088630092",
  appId: "1:995088630092:web:9ad36c31437d7bad368fe9"
};
firebase.initializeApp(firebaseConfig);

var db = firebase.database();

/* REFS */
var logoRef   = db.ref("site/logo");
var nameRef   = db.ref("site/name");
var noticeRef = db.ref("notice");
var sliderRef = db.ref("sliders");
var appsRef   = db.ref("apps");
var waRef     = db.ref("site/whatsapp");
var igRef     = db.ref("site/instagram");

/* LOAD LOGO */
logoRef.on("value",s=>{ if(s.val()) siteLogo.src = s.val(); });

/* LOAD NAME */
nameRef.on("value",s=>{ if(s.val()) gameName.innerText = s.val(); });

/* LOAD NOTICE */
noticeRef.on("value",s=>{ notice.innerText = s.val() || ""; });

/* SLIDER */
let slides=[],i=0;
sliderRef.on("value",s=>{
  slides=[];
  let d=s.val()||{};
  for(let k in d) slides.push(d[k]);
  if(slides.length){
    sliderImg.src=slides[0];
    setInterval(()=>{
      i=(i+1)%slides.length;
      sliderImg.src=slides[i];
    },3000);
  }
});

/* APPS */
appsRef.on("value",s=>{
  apps.innerHTML="";
  let d=s.val()||{};
  for(let k in d){
    let a=d[k];
    apps.innerHTML+=`
      <div class="app">
        <img src="${a.image}">
        <h3>${a.name}</h3>
        <p>Downloads: ${a.downloads||0}</p>
        <button onclick="downloadApp('${k}','${a.apk}')">⬇️ Download</button>
      </div>`;
  }
});

/* DOWNLOAD */
function downloadApp(key,link){
  appsRef.child(key).child("downloads")
    .transaction(n=>(n||0)+1);
  window.open(link,"_blank");
}

/* SOCIAL */
let waLink="", igLink="";
waRef.on("value",s=>{ waLink=s.val(); if(!waLink) floatWA.style.display="none"; });
igRef.on("value",s=>{ igLink=s.val(); if(!igLink) floatIG.style.display="none"; });

function openWA(){ if(waLink) window.open(waLink,"_blank"); }
function openIG(){ if(igLink) window.open(igLink,"_blank"); }

</script>

</body>
</html>
