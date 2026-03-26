
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Chronicles of the Ninth Circle</title>
<style>
body { margin:0; font-family: Georgia, serif; background:#0f0f12; color:#d6d8e0; line-height:1.8; }
section { display:none; padding:60px 20px; max-width:800px; margin:auto; }
.hero { display:flex; flex-direction:column; justify-content:center; align-items:center; height:100vh; text-align:center; background:linear-gradient(#0f0f12,#1a1c22); }
.hero h1 { font-size:48px; letter-spacing:4px; margin:0; color:#c9ccd6; }
.hero h2 { margin-top:10px; font-size:22px; color:#8a8fa3; }
.hero p { margin-top:25px; font-style:italic; opacity:0.8; max-width:700px; }
.btn { margin-top:20px; padding:10px 24px; background:#2a1f3a; color:white; cursor:pointer; text-decoration:none; border-radius:5px; }
.btn:hover { background:#3a2a55; }
.chapter-list a, .chapter-sublist a { display:block; margin:8px 0; text-decoration:none; color:#d6d8e0; border-bottom:1px solid #333; padding-bottom:5px; cursor:pointer; }
.chapter-list a:hover, .chapter-sublist a:hover { color:white; border-color:#6d5cae; }
h1,h2 { text-align:center; }
.back { margin-top:30px; text-align:center; opacity:0.6; cursor:pointer; }
.progress { position:fixed; top:0; left:0; height:3px; background:#6d5cae; width:0%; z-index:100; }
.comment-section { margin-top:20px; border-top:1px solid #444; padding-top:15px; }
.comment-section input, .comment-section textarea { width:100%; margin:5px 0; padding:8px; background:#1a1c22; border:1px solid #555; color:#d6d8e0; }
.comment-section button { padding:6px 14px; margin-top:5px; background:#2a1f3a; color:white; border:none; cursor:pointer; border-radius:4px; }
.comment-section button:hover { background:#3a2a55; }
.like-btn { margin-top:10px; cursor:pointer; font-size:16px; display:inline-block; }
.author { margin-top:10px; font-style:italic; opacity:0.7; }
</style>
</head>
<body>

<div class="progress" id="progressBar"></div>

<!-- LANDING PAGE -->
<section id="landing" style="display:block;">
  <div class="hero">
    <h1>Chronicles of the Ninth Circle</h1>
    <h2>A Victorian Gothic Occult Romance</h2>
    <p class="author">Penulis: Ade Angga Pratama (Shenzhou)</p>
    <p><strong>Genre:</strong> Victorian Gothic • Occult • Mystery • Romance</p>
    <p><strong>Sinopsis (ID):</strong><br>
      Lucien, seorang pemuda biasa, hidupnya berakhir tiba-tiba dalam sebuah kecelakaan. Ia terbangun di dunia baru, dalam tubuh bangsawan muda dan menerima Circle 9 — Jalur Malam yang menguasai kesunyian. Bersamaan dengan kebangkitan jalur ini, sesuatu yang lebih tua dan lebih berbahaya juga bangkit. Di tengah intrik aristokrat, pengawasan Gereja, dan misteri yang menanti untuk dipecahkan, Lucien harus menemukan jalan hidup barunya—sementara hati dan romansa mulai tumbuh perlahan.
    </p>
    <p><strong>Synopsis (EN):</strong><br>
      Lucien, an ordinary young man, suddenly meets his end in a tragic accident. He awakens in a new world, in the body of a young aristocrat, receiving Circle 9 — the Path of Night, mastering silence. Alongside this awakening, something older and more dangerous stirs. Amid aristocratic intrigue, Church surveillance, and mysteries waiting to be unraveled, Lucien must find his new path—while romance begins to bloom slowly.
    </p>
    <div class="btn" onclick="openSection('arsip')">Begin the Chronicle</div>
  </div>
</section>

<!-- ARSIP BABS -->
<section id="arsip">
  <h1>Arsip Bab</h1>
  <div class="chapter-list">
    <a onclick="openSection('bab1')">Bab 1 — Circle 9: Jalur Malam</a>
    <a onclick="openSection('bab2')">Bab 2 — Retakan Stabilitas</a>
    <a onclick="openSection('bab3')">Bab 3 — Bayangan Terlarang</a>
    <a onclick="openSection('bab4')">Bab 4 — Gereja Memantau</a>
    <a onclick="openSection('bab5')">Bab 5 — Intrik Aristokrat</a>
    <a onclick="openSection('bab6')">Bab 6 — Resonansi Gelap</a>
    <a onclick="openSection('bab7')">Bab 7 — Rahasia Masa Lalu</a>
    <a onclick="openSection('bab8')">Bab 8 — Romance yang Perlahan</a>
    <a onclick="openSection('bab9')">Bab 9 — Teror dan Kebenaran</a>
    <a onclick="openSection('bab10')">Bab 10 — Kebangkitan Penuh</a>
  </div>
  <div class="back" onclick="openSection('landing')">Kembali ke Landing</div>
</section>

<!-- GENERATE BAB & CHAPTER -->
<script>
const totalBab=10;
const chaptersPerBab=[3,4,3,2,3,3,2,2,3,3]; // jumlah chapter tiap bab

for(let i=1;i<=totalBab;i++){
  document.write(`<section id="bab${i}"><h1>Bab ${i}</h1><div class="chapter-sublist">`);
  for(let j=1;j<=chaptersPerBab[i-1];j++){
    document.write(`<a onclick="openChapter('bab${i}','bab${i}-ch${j}')">Chapter ${j}</a>`);
  }
  document.write(`</div><div class="back" onclick="openSection('arsip')">← Kembali ke Arsip Bab</div></section>`);

  for(let j=1;j<=chaptersPerBab[i-1];j++){
    document.write(`
    <section id="bab${i}-ch${j}">
      <h2>Bab ${i} — Chapter ${j}</h2>
      <p>Isi cerita Bab ${i}, Chapter ${j}...</p>
      <div class="like-btn" onclick="toggleLike('bab${i}-ch${j}')">❤️ <span id="like-bab${i}-ch${j}">0</span></div>
      <div class="comment-section">
        <h3>Komentar:</h3>
        <textarea id="comment-bab${i}-ch${j}" placeholder="Tulis komentar..."></textarea>
        <button onclick="addComment('bab${i}-ch${j}')">Kirim</button>
        <div id="comments-list-bab${i}-ch${j}"></div>
      </div>
      <div style="display:flex; justify-content:space-between; margin-top:20px;">
        <div class="btn" onclick="openChapter('bab${i}','bab${i}-ch${j-1>0?j-1:'arsip'}')">← Previous Chapter</div>
        <div class="btn" onclick="openChapter('bab${i}','bab${i}-ch${j+1<=chaptersPerBab[i-1]?j+1:'arsip'}')">Next Chapter →</div>
      </div>
    </section>
    `);
  }
}
</script>

<script>
// NAVIGATION
function openSection(id){
  document.querySelectorAll("section").forEach(sec=>sec.style.display="none");
  document.getElementById(id).style.display="block";
  window.scrollTo(0,0);
}
function openChapter(bab,chapter){ openSection(chapter); }

// PROGRESS BAR
window.onscroll=function(){
  let winScroll=document.body.scrollTop||document.documentElement.scrollTop;
  let height=document.documentElement.scrollHeight-document.documentElement.clientHeight;
  let scrolled=(winScroll/height)*100;
  document.getElementById("progressBar").style.width=scrolled+"%";
};

// LIKE SYSTEM
function toggleLike(id){
  let key='like-'+id;
  let current=localStorage.getItem(key) || 0;
  current=parseInt(current)+1;
  localStorage.setItem(key,current);
  document.getElementById('like-'+id).innerText=current;
}

// Load likes & comments on page load
window.onload=function(){
  document.querySelectorAll('.like-btn span').forEach(el=>{
    let key='like-'+el.id.replace('like-','');
    let val=localStorage.getItem(key) || 0;
    el.innerText=val;
  });
  document.querySelectorAll('[id^=comments-list-]').forEach(el=>{
    let key=el.id.replace('comments-list-','');
    let stored=localStorage.getItem('comments-'+key);
    if(stored) el.innerHTML=stored;
  });
};

// COMMENT SYSTEM
function addComment(id){
  let textarea=document.getElementById('comment-'+id);
  let comment=textarea.value.trim();
  if(comment==='') return;
  let container=document.getElementById('comments-list-'+id);
  let p=document.createElement('p'); 
  p.innerText=comment; 
  p.style.borderBottom='1px solid #444'; 
  p.style.padding='5px 0';
  container.appendChild(p);
  textarea.value='';
  localStorage.setItem('comments-'+id, container.innerHTML);
}
</script>

</body>
</html>
