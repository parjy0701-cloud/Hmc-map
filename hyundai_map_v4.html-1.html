<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>현대자동차 출고센터</title>
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css"/>
<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>
<style>
* { margin:0; padding:0; box-sizing:border-box; }
body { font-family:'Apple SD Gothic Neo','Noto Sans KR',sans-serif; background:#111; color:#fff; height:100vh; display:flex; flex-direction:column; overflow:hidden; }
.header { background:linear-gradient(135deg,#002c5f,#00428a); padding:10px 14px; display:flex; align-items:center; justify-content:space-between; box-shadow:0 2px 12px rgba(0,0,0,.5); z-index:1000; flex-shrink:0; }
.header-left { display:flex; align-items:center; gap:9px; }
.logo { background:#fff; color:#002c5f; font-weight:900; font-size:12px; padding:3px 7px; border-radius:3px; }
.h-title { font-size:14px; font-weight:700; }
.h-sub { font-size:10px; color:#8ab4e8; margin-top:1px; }
.btn-gps { background:#1e90ff; border:none; color:#fff; padding:7px 13px; border-radius:18px; font-size:12px; font-weight:700; cursor:pointer; transition:background .2s; white-space:nowrap; }
.top-bar { background:#0d1117; padding:7px 10px; display:flex; gap:5px; align-items:center; overflow-x:auto; border-bottom:1px solid #21262d; flex-shrink:0; scrollbar-width:none; }
.top-bar::-webkit-scrollbar { display:none; }
.fb { border:1.5px solid #30363d; background:#21262d; color:#8b949e; padding:4px 11px; border-radius:14px; font-size:11px; font-weight:600; cursor:pointer; white-space:nowrap; transition:all .15s; }
.fb.on { background:#1e90ff; border-color:#1e90ff; color:#fff; }
.fb.bae.on { background:#f39c12; border-color:#f39c12; }
.divider { width:1px; height:20px; background:#30363d; flex-shrink:0; margin:0 3px; }
.map-toggle { border:1.5px solid #3d7a2a; background:#2d4a1e; color:#6fcf47; padding:4px 10px; border-radius:14px; font-size:11px; font-weight:700; cursor:pointer; white-space:nowrap; }
.map-toggle.normal { border-color:#30363d; background:#21262d; color:#8b949e; }
#map { flex:1; }
.bs { position:fixed; bottom:0; left:0; right:0; background:#161b22; border-radius:18px 18px 0 0; z-index:2000; transform:translateY(100%); transition:transform .32s cubic-bezier(.4,0,.2,1); box-shadow:0 -4px 28px rgba(0,0,0,.7); max-height:75vh; overflow-y:auto; }
.bs.open { transform:translateY(0); }
.bs-handle { display:flex; justify-content:center; padding:10px; cursor:pointer; }
.bs-bar { width:36px; height:3px; background:#30363d; border-radius:2px; }
.bs-body { padding:0 15px 30px; }
.badge { display:inline-block; padding:2px 9px; border-radius:8px; font-size:10px; font-weight:700; margin-bottom:7px; }
.b-del { background:#1e3a5f; color:#58a6ff; }
.b-bae { background:#3a2010; color:#f0883e; }
.bs-name { font-size:19px; font-weight:800; margin-bottom:2px; }
.bs-code { font-size:11px; color:#8b949e; margin-bottom:11px; }
.bs-grid { display:grid; grid-template-columns:1fr 1fr; gap:7px; margin-bottom:13px; }
.bc { background:#21262d; border-radius:9px; padding:9px 11px; border:1px solid #30363d; }
.bc-full { grid-column:1/-1; background:#21262d; border-radius:9px; padding:9px 11px; border:1px solid #30363d; }
.bc label { font-size:9px; color:#8b949e; display:block; margin-bottom:3px; }
.bc-v { font-size:13px; font-weight:700; color:#e6edf3; }
.bc-v-sm { font-size:12px; font-weight:500; color:#e6edf3; line-height:1.5; }
.bs-btns { display:flex; gap:7px; flex-wrap:wrap; }
.btn-call { flex:1; min-width:80px; background:#238636; color:#fff; border:none; padding:11px 8px; border-radius:9px; font-size:12px; font-weight:700; cursor:pointer; }
.btn-mgr  { flex:1; min-width:80px; background:#6f42c1; color:#fff; border:none; padding:11px 8px; border-radius:9px; font-size:12px; font-weight:700; cursor:pointer; }
.btn-navi { flex:1; min-width:80px; background:#1e90ff; color:#fff; border:none; padding:11px 8px; border-radius:9px; font-size:12px; font-weight:700; cursor:pointer; }
.btn-x { width:38px; background:#21262d; color:#8b949e; border:1px solid #30363d; border-radius:9px; cursor:pointer; font-size:16px; flex-shrink:0; }
.ov { position:fixed; inset:0; z-index:1999; display:none; background:rgba(0,0,0,.3); }
.ov.on { display:block; }
.chip-box { position:absolute; top:112px; right:10px; z-index:999; }
.chip { background:rgba(13,17,23,.92); border:1px solid #30363d; border-radius:9px; padding:5px 9px; font-size:10px; text-align:center; backdrop-filter:blur(6px); }
.chip-n { font-size:17px; font-weight:800; color:#58a6ff; display:block; }
.near-box { position:absolute; top:112px; left:10px; z-index:999; background:rgba(13,17,23,.92); border:1px solid #1e90ff; border-radius:9px; padding:7px 11px; font-size:10px; backdrop-filter:blur(6px); display:none; max-width:160px; }
.near-box.on { display:block; }
.near-lbl { color:#8b949e; margin-bottom:1px; }
.near-nm { color:#58a6ff; font-weight:700; font-size:12px; }
.near-dist { color:#2ecc71; font-size:11px; }
.legend { position:absolute; bottom:14px; left:10px; z-index:999; background:rgba(13,17,23,.92); border:1px solid #30363d; border-radius:9px; padding:9px 11px; backdrop-filter:blur(6px); min-width:122px; }
.lg-t { font-size:9px; color:#8b949e; margin-bottom:5px; font-weight:700; }
.lg-i { display:flex; align-items:center; gap:5px; margin-bottom:4px; font-size:10px; }
.lg-dot { width:10px; height:10px; border-radius:50%; flex-shrink:0; }
.lg-box { width:10px; height:10px; border-radius:2px; flex-shrink:0; opacity:.65; }
.loading { position:fixed; inset:0; background:#0d1117; z-index:9999; display:flex; flex-direction:column; align-items:center; justify-content:center; gap:14px; }
.ld-logo { background:#002c5f; color:#fff; font-size:26px; font-weight:900; padding:14px 26px; border-radius:10px; letter-spacing:-1px; }
.ld-txt { color:#8b949e; font-size:13px; }
.ld-bar { width:180px; height:3px; background:#21262d; border-radius:2px; overflow:hidden; }
.ld-prog { height:100%; background:linear-gradient(90deg,#002c5f,#1e90ff); border-radius:2px; animation:ldanim 1.6s ease forwards; }
@keyframes ldanim { 0%{width:0} 100%{width:100%} }

/* ── 토스트 (alert 대체) ── */
.toast { position:fixed; bottom:90px; left:50%; transform:translateX(-50%) translateY(20px); background:#1e242c; border:1px solid #30363d; border-radius:12px; padding:11px 18px; font-size:12px; font-weight:600; z-index:3000; opacity:0; transition:all .3s; pointer-events:none; white-space:nowrap; box-shadow:0 4px 20px rgba(0,0,0,.6); max-width:90vw; text-align:center; }
.toast.show { opacity:1; transform:translateX(-50%) translateY(0); }
.toast.ok   { border-color:#2ecc71; color:#2ecc71; }
.toast.err  { border-color:#e74c3c; color:#f1948a; }
.toast.info { border-color:#1e90ff; color:#58a6ff; }
.toast.warn { border-color:#f39c12; color:#f39c12; }

.ztip { background:rgba(0,0,0,.75)!important; border:1px solid rgba(255,255,255,.2)!important; box-shadow:none!important; color:#fff!important; font-size:12px!important; font-weight:800!important; border-radius:6px!important; padding:2px 7px!important; pointer-events:none!important; white-space:nowrap!important; }
</style>
</head>
<body>

<div class="loading" id="ld">
  <div class="ld-logo">HYUNDAI</div>
  <div class="ld-txt">출고센터 현황지도 로딩중...</div>
  <div class="ld-bar"><div class="ld-prog"></div></div>
</div>

<div class="header">
  <div class="header-left">
    <div class="logo">HMC</div>
    <div>
      <div class="h-title">출고센터 현황지도</div>
      <div class="h-sub">전국 13개 거점 · 예시버전</div>
    </div>
  </div>
  <button class="btn-gps" id="gpsBtn" onclick="locateMe()">📍 내 위치</button>
</div>

<div class="top-bar">
  <button class="fb on" onclick="setFilter('all',this)">🗺️ 전체</button>
  <button class="fb"    onclick="setFilter('출고센터',this)">🏭 출고센터</button>
  <button class="fb bae" onclick="setFilter('배송센터',this)">🚚 배송센터</button>
  <div class="divider"></div>
  <button class="map-toggle" id="mapBtn" onclick="toggleMap()">🛰️ 위성ON</button>
</div>

<div id="map"></div>

<div class="chip-box">
  <div class="chip"><span class="chip-n" id="cnt">13</span>개소</div>
</div>
<div class="near-box" id="nearBox">
  <div class="near-lbl">🎯 가장 가까운 센터</div>
  <div class="near-nm" id="nearNm">-</div>
  <div class="near-dist" id="nearDist">-</div>
</div>
<div class="legend" id="legend">
  <div class="lg-t">범 례</div>
  <div class="lg-i"><div class="lg-dot" style="background:#1e90ff;border:2px solid rgba(255,255,255,.6);"></div>출고센터</div>
  <div class="lg-i"><div class="lg-dot" style="background:#f39c12;border:2px solid rgba(255,255,255,.6);"></div>배송센터</div>
  <div class="lg-i"><div class="lg-box" style="background:#1e90ff;"></div>출고센터 부지</div>
  <div class="lg-i"><div class="lg-box" style="background:#f39c12;"></div>배송센터 부지</div>
  <div class="lg-i"><div class="lg-dot" style="background:#00bfff;border:2px solid #1e90ff;"></div>내 위치</div>
</div>

<div class="toast" id="toast"></div>
<div class="ov" id="ov" onclick="closeBS()"></div>
<div class="bs" id="bs">
  <div class="bs-handle" onclick="closeBS()"><div class="bs-bar"></div></div>
  <div class="bs-body" id="bsBody"></div>
</div>

<script>
const CENTERS = [
  {name:"울산출고센터", code:"6600-2", address:"울산광역시 북구 염포로 700번지",             tel:"052-215-2401", lat:35.539828, lng:129.376840, type:"출고센터", manager:"윤영태", mobile:"010-5068-2425", staff:80},
  {name:"울산배송센터", code:"6666-2", address:"울산광역시 북구 염포로 700번지",             tel:"052-215-7800", lat:35.5405,   lng:129.3730,   type:"배송센터", manager:"이상섭", mobile:"010-2827-8946", staff:168},
  {name:"전주출고센터", code:"4659-3", address:"전라북도 완주군 봉동읍 완주산단5로 163",    tel:"063-260-5231", lat:35.953185, lng:127.135764, type:"출고센터", manager:"최영기", mobile:"010-3877-6953", staff:9},
  {name:"아산출고센터", code:"4665-4", address:"충청남도 아산시 인주면 현대로 1077",        tel:"041-530-5901", lat:36.888494, lng:126.888448, type:"출고센터", manager:"박상덕", mobile:"010-6740-0588", staff:10},
  {name:"옥천출고센터", code:"8300-1", address:"충청북도 옥천군 옥천읍 옥천동이로 387-32",  tel:"043-731-8472", lat:36.277874, lng:127.606275, type:"출고센터", manager:"이중재", mobile:"010-8801-5401", staff:5},
  {name:"시흥출고센터", code:"6500-1", address:"경기도 시흥시 정왕천로 279",                tel:"031-434-2414", lat:37.334413, lng:126.711466, type:"출고센터", manager:"이정일", mobile:"010-9114-4247", staff:15},
  {name:"신갈출고센터", code:"4469-1", address:"경기도 용인시 기흥구 중부대로 690",         tel:"031-281-3761", lat:37.259972, lng:127.142821, type:"출고센터", manager:"-",     mobile:"-",             staff:0},
  {name:"원주출고센터", code:"4586-1", address:"강원도 원주시 문막읍 원문로 2122",          tel:"033-731-4741", lat:37.336497, lng:127.848128, type:"출고센터", manager:"박경운", mobile:"010-3792-3788", staff:4},
  {name:"담양출고센터", code:"4597-1", address:"전라남도 담양군 봉산면 제월길 192",         tel:"061-381-1136", lat:35.253655, lng:126.964528, type:"출고센터", manager:"전석형", mobile:"010-8971-8374", staff:5},
  {name:"칠곡출고센터", code:"5600-1", address:"경상북도 칠곡군 왜관읍 현대로 177",        tel:"054-977-7982", lat:35.987748, lng:128.435044, type:"출고센터", manager:"-",     mobile:"-",             staff:0},
  {name:"함안출고센터", code:"4498-1", address:"경상남도 함안군 군북면 함마대로 290-14",    tel:"055-584-1270", lat:35.253665, lng:128.371344, type:"출고센터", manager:"유권준", mobile:"010-2571-5785", staff:5},
  {name:"남양출고센터", code:"7600-1", address:"경기도 화성시 장안면 매바위로366번길 55",    tel:"031-351-8602", lat:37.078877, lng:126.816307, type:"출고센터", manager:"-",     mobile:"-",             staff:0},
  {name:"영남출고센터", code:"5600-1", address:"경상북도 칠곡군 지천면 금호로 272",        tel:"054-977-7984", lat:35.918452, lng:128.484196, type:"출고센터", manager:"박순철", mobile:"010-3528-4752", staff:10},
];

// ── 타일 ────────────────────────────────────────
const tileSat    = L.tileLayer('https://server.arcgisonline.com/ArcGIS/rest/services/World_Imagery/MapServer/tile/{z}/{y}/{x}',{maxZoom:19,attribution:'© Esri'});
const tileKor    = L.tileLayer('https://xdworld.vworld.kr/2d/Hybrid/service/{z}/{x}/{y}.png',{maxZoom:19,attribution:'© VWorld'});
const tileStreet = L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png',{maxZoom:19,attribution:'© OpenStreetMap'});

const map = L.map('map',{center:[36.5,127.8],zoom:7,zoomControl:false,layers:[tileSat,tileKor]});
L.control.zoom({position:'bottomright'}).addTo(map);

let isSat=true;
function toggleMap(){
  const btn=document.getElementById('mapBtn');
  if(isSat){
    map.removeLayer(tileSat); map.removeLayer(tileKor); map.addLayer(tileStreet);
    btn.textContent='🛰️ 위성OFF'; btn.classList.add('normal'); isSat=false;
  } else {
    map.removeLayer(tileStreet); map.addLayer(tileSat); map.addLayer(tileKor);
    btn.textContent='🛰️ 위성ON'; btn.classList.remove('normal'); isSat=true;
  }
}

function makePoly(lat,lng,w=220,h=220){
  const hl=(h/2)/111000, hln=(w/2)/(111000*Math.cos(lat*Math.PI/180));
  return [[lat+hl,lng-hln],[lat+hl,lng+hln],[lat-hl,lng+hln],[lat-hl,lng-hln]];
}
function makeIcon(type){
  const bg=type==='출고센터'?'#1e90ff':'#f39c12', em=type==='출고센터'?'🏭':'🚚';
  return L.divIcon({className:'',html:`<div style="width:36px;height:36px;background:${bg};border-radius:50% 50% 50% 0;transform:rotate(-45deg);border:2.5px solid rgba(255,255,255,.85);box-shadow:0 3px 12px rgba(0,0,0,.7);display:flex;align-items:center;justify-content:center;"><span style="transform:rotate(45deg);font-size:16px;">${em}</span></div>`,iconSize:[36,36],iconAnchor:[18,36],popupAnchor:[0,-36]});
}

let mLayer=L.layerGroup().addTo(map), pLayer=L.layerGroup().addTo(map), curFilter='all';
function draw(){
  mLayer.clearLayers(); pLayer.clearLayers(); let cnt=0;
  CENTERS.forEach(c=>{
    if(curFilter!=='all'&&c.type!==curFilter)return;
    const pc=c.type==='출고센터'?'#1e90ff':'#f39c12';
    const poly=L.polygon(makePoly(c.lat,c.lng),{color:pc,fillColor:pc,fillOpacity:.25,weight:2.5,dashArray:'6,4'}).addTo(pLayer);
    poly.bindTooltip(c.name,{permanent:false,direction:'top',className:'ztip'});
    poly.on('click',()=>openBS(c));
    L.marker([c.lat,c.lng],{icon:makeIcon(c.type)}).on('click',()=>openBS(c)).addTo(mLayer);
    cnt++;
  });
  document.getElementById('cnt').textContent=cnt;
}
draw();

function setFilter(f,btn){
  curFilter=f;
  document.querySelectorAll('.fb').forEach(b=>b.classList.remove('on'));
  btn.classList.add('on'); draw();
}

function openBS(c){
  const bc=c.type==='출고센터'?'b-del':'b-bae', bl=c.type==='출고센터'?'🏭 출고센터':'🚚 배송센터';
  const hM=c.manager!=='-', hMb=c.mobile!=='-';
  document.getElementById('bsBody').innerHTML=`
    <span class="badge ${bc}">${bl}</span>
    <div class="bs-name">${c.name}</div>
    <div class="bs-code">부서코드 ${c.code}</div>
    <div class="bs-grid">
      ${hM?`<div class="bc"><label>👤 센터장</label><div class="bc-v">${c.manager}</div></div>`:''}
      ${c.staff>0?`<div class="bc"><label>👥 대상인원</label><div class="bc-v">${c.staff}명</div></div>`:''}
      <div class="bc"><label>📞 대표전화</label><div class="bc-v" style="font-size:12px;">${c.tel}</div></div>
      ${hMb?`<div class="bc"><label>📱 센터장 연락처</label><div class="bc-v" style="font-size:12px;">${c.mobile}</div></div>`:''}
      <div class="bc-full"><label>📍 주소</label><div class="bc-v-sm">${c.address}</div></div>
    </div>
    <div class="bs-btns">
      <button class="btn-call" onclick="call('${c.tel}')">📞 대표전화</button>
      ${hMb?`<button class="btn-mgr" onclick="call('${c.mobile}')">📱 센터장</button>`:''}
      <button class="btn-navi" onclick="navi(${c.lat},${c.lng},'${c.name}')">🧭 길찾기</button>
      <button class="btn-x" onclick="closeBS()">✕</button>
    </div>`;
  document.getElementById('bs').classList.add('open');
  document.getElementById('ov').classList.add('on');
  document.getElementById('legend').style.display='none';
  map.setView([c.lat,c.lng],16);
}
function closeBS(){
  document.getElementById('bs').classList.remove('open');
  document.getElementById('ov').classList.remove('on');
  document.getElementById('legend').style.display='block';
}
function call(tel){window.location.href='tel:'+tel;}
function navi(lat,lng,name){
  if(/iPhone|iPad/i.test(navigator.userAgent)) window.location.href=`maps://maps.apple.com/?daddr=${lat},${lng}`;
  else window.open(`https://map.kakao.com/link/to/${encodeURIComponent(name)},${lat},${lng}`,'_blank');
}

// ══════════════════════════════════════
//  토스트 (alert 완전 대체)
// ══════════════════════════════════════
let _tt=null;
function showToast(msg,type='info',ms=3500){
  const t=document.getElementById('toast');
  t.textContent=msg; t.className='toast show '+type;
  if(_tt)clearTimeout(_tt);
  _tt=setTimeout(()=>t.className='toast',ms);
}

// ══════════════════════════════════════
//  GPS — watchPosition + 오류코드별 처리
// ══════════════════════════════════════
let myMk=null, watchId=null, firstFix=true;

function locateMe(){
  const btn=document.getElementById('gpsBtn');

  if(!navigator.geolocation){
    showToast('❌ 이 브라우저는 GPS를 지원하지 않습니다','err');
    return;
  }

  // 이미 추적중 → 종료
  if(watchId!==null){
    navigator.geolocation.clearWatch(watchId);
    watchId=null; firstFix=true;
    if(myMk){map.removeLayer(myMk);myMk=null;}
    document.getElementById('nearBox').classList.remove('on');
    btn.textContent='📍 내 위치';
    btn.style.background='';
    showToast('📍 위치 추적 종료','info');
    return;
  }

  btn.textContent='⏳ 찾는중...';
  btn.style.background='#555';
  showToast('📡 GPS 신호 수신중...','info',15000);

  watchId = navigator.geolocation.watchPosition(
    // ── 성공 ──
    function(pos){
      const la=pos.coords.latitude, ln=pos.coords.longitude;
      const acc=Math.round(pos.coords.accuracy);

      btn.textContent='📍 추적중 ✕';
      btn.style.background='#2ecc71';

      if(myMk) map.removeLayer(myMk);
      myMk = L.circleMarker([la,ln],{
        radius:11, fillColor:'#00bfff', color:'#1e90ff', weight:3, fillOpacity:.95
      }).addTo(map).bindPopup(`📍 현재 내 위치<br><small>정확도 약 ${acc}m</small>`);

      if(firstFix){ map.setView([la,ln],14); firstFix=false; }

      let minD=Infinity, near=null;
      CENTERS.forEach(c=>{const d=Math.hypot(c.lat-la,c.lng-ln);if(d<minD){minD=d;near=c;}});
      document.getElementById('nearNm').textContent   = near.name;
      document.getElementById('nearDist').textContent = `📏 약 ${(minD*111).toFixed(1)}km`;
      document.getElementById('nearBox').classList.add('on');

      showToast(`✅ 위치 확인 (정확도 ${acc}m)`,'ok',3000);
    },

    // ── 실패 — 오류코드별 ──
    function(err){
      watchId=null; firstFix=true;
      btn.textContent='📍 내 위치';
      btn.style.background='';

      switch(err.code){
        case 1:
          showToast('❌ 위치 권한 거부 — 브라우저 주소창 자물쇠 > 위치 허용','err',6000);
          break;
        case 2:
          showToast('📡 GPS 신호 없음 — 실외 이동 후 재시도','err',5000);
          break;
        case 3:
          showToast('⏱ GPS 시간 초과 — 다시 눌러주세요','warn',4000);
          break;
      }
    },
    { enableHighAccuracy:true, timeout:15000, maximumAge:5000 }
  );
}

window.addEventListener('load',()=>{
  setTimeout(()=>{
    const ld=document.getElementById('ld');
    ld.style.transition='opacity .4s'; ld.style.opacity='0';
    setTimeout(()=>ld.style.display='none',420);
  },1600);
});
</script>
</body>
</html>
