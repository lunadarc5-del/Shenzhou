<!DOCTYPE html>
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
.btn { margin-top:35px; padding:12px 28px; background:#2a1f3a; color:white; cursor:pointer; text-decoration:none; }
.btn:hover { background:#3a2a55; }
.chapter-list a { display:block; margin:15px 0; text-decoration:none; color:#d6d8e0; border-bottom:1px solid #333; padding-bottom:8px; cursor:pointer; }
.chapter-list a:hover { color:white; border-color:#6d5cae; }
h1,h2 { text-align:center; }
.back { margin-top:50px; text-align:center; opacity:0.6; cursor:pointer; }
.progress { position:fixed; top:0; left:0; height:3px; background:#6d5cae; width:0%; z-index:100; }
.comment-section { margin-top:30px; border-top:1px solid #444; padding-top:20px; }
.comment-section input, .comment-section textarea { width:100%; margin:5px 0; padding:10px; background:#1a1c22; border:1px solid #555; color:#d6d8e0; }
.comment-section button { padding:8px 16px; margin-top:5px; background:#2a1f3a; color:white; border:none; cursor:pointer; }
.comment-section button:hover { background:#3a2a55; }
.like-btn { margin-top:20px; cursor:pointer; font-size:18px; }
</style>
</head>
<body>

<div class="progress" id="progressBar"></div>

<!-- LANDING PAGE -->
<section id="landing" style="display:block;">
  <div class="hero">
    <h1>Chronicles of the Ninth Circle</h1>
    <h2>A Victorian Gothic Occult Romance</h2>
    <p><strong>Genre:</strong> Victorian Gothic • Occult • Mystery • Aristocratic Romance • Dark Fantasy</p>
    <p><strong>Sinopsis (ID):</strong><br>
      Lucien tidak pernah percaya pada takdir. Hingga sebuah dentang logam dan kilatan cahaya mengakhiri hidupnya di dunia yang ia kenal.<br>
      Ia terbangun dalam tubuh bangsawan muda, menerima Lingkaran Kesembilan—Jalur Malam yang menguasai kesunyian.<br>
      Namun sesuatu lebih tua dari doktrin itu sendiri telah bangkit. Di balik intrik aristokrat dan pengawasan Gereja, sebuah rahasia menunggu untuk diungkap.
    </p>
    <p><strong>Synopsis (EN):</strong><br>
      Lucien never believed in destiny—until the sound of shattering metal and a flash of light ended his life.<br>
      He awakens in the body of a young aristocrat, receiving the Ninth Circle—The Path of Silence.<br>
      Yet something older than doctrine itself stirs. Beneath aristocratic intrigue and the Church's watch, a secret waits to be unveiled.
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
    <a onclick="openSection('bab4')">Bab 4 — Malam Tanpa Bintang</a>
    <a onclick="openSection('bab5')">Bab 5 — Resonansi Lama</a>
    <a onclick="openSection('bab6')">Bab 6 — Suara yang Hilang</a>
    <a onclick="openSection('bab7')">Bab 7 — Keheningan Memanggil</a>
    <a onclick="openSection('bab8')">Bab 8 — Retak Aristokrat</a>
    <a onclick="openSection('bab9')">Bab 9 — Lingkaran Terakhir</a>
    <a onclick="openSection('bab10')">Bab 10 — Kembali dari Malam</a>
  </div>
  <div class="back" onclick="openSection('landing')">Kembali ke Landing</div>
</section>

<!-- CHAPTERS -->
<section id="bab1">
  <h1>Bab 1 — Circle 9: Jalur Malam</h1>
  <p>Langit pecah dalam satu kilatan cahaya. Logam saling menghantam. Orang-orang berteriak. Lalu semuanya gelap...</p>
  <div class="like-btn" onclick="toggleLike('bab1')">❤️ <span id="like-bab1">0</span></div>
  <div class="comment-section">
    <h3>Komentar:</h3>
    <textarea id="comment-bab1" placeholder="Tulis komentar..."></textarea>
    <button onclick="addComment('bab1')">Kirim</button>
    <div id="comments-list-bab1"></div>
  </div>
  <div style="display:flex; justify-content:space-between; margin-top:30px;">
    <div class="btn" onclick="openSection('arsip')">Back to Arsip</div>
    <div class="btn" onclick="openSection('bab2')">Next Chapter →</div>
  </div>
</section>

<section id="bab2">
  <h1>Bab 2 — Retakan Stabilitas</h1>
  <p>Malam turun tanpa suara. Lucien berdiri di balkon kediaman D’Armont...</p>
  <div class="like-btn" onclick="toggleLike('bab2')">❤️ <span id="like-bab2">0</span></div>
  <div class="comment-section">
    <h3>Komentar:</h3>
    <textarea id="comment-bab2" placeholder="Tulis komentar..."></textarea>
    <button onclick="addComment('bab2')">Kirim</button>
    <div id="comments-list-bab2"></div>
  </div>
  <div style="display:flex; justify-content:space-between; margin-top:30px;">
    <div class="btn" onclick="openSection('bab1')">← Previous Chapter</div>
    <div class="btn" onclick="openSection('bab3')">Next Chapter →</div>
  </div>
</section>

<section id="bab3">
  <h1>Bab 3 — Bayangan Terlarang</h1>
  <p>Lucien mulai menyadari rahasia yang tersembunyi di balik Jalur Malam. Intrik aristokrat muncul...</p>
  <div class="like-btn" onclick="toggleLike('bab3')">❤️ <span id="like-bab3">0</span></div>
  <div class="comment-section">
    <h3>Komentar:</h3>
    <textarea id="comment-bab3" placeholder="Tulis komentar..."></textarea>
    <button onclick="addComment('bab3')">Kirim</button>
    <div id="comments-list-bab3"></div>
  </div>
  <div style="display:flex; justify-content:space-between; margin-top:30px;">
    <div class="btn" onclick="openSection('bab2')">← Previous Chapter</div>
    <div class="btn" onclick="openSection('bab4')">Next Chapter →</div>
  </div>
</section>

<section id="bab4">
  <h1>Bab 4 — Malam Tanpa Bintang</h1>
  <p>Gereja memonitor setiap gerakannya. Bayangan yang terlambat bergerak membuatnya semakin penasaran...</p>
  <div class="like-btn" onclick="toggleLike('bab4')">❤️ <span id="like-bab4">0</span></div>
  <div class="comment-section">
    <h3>Komentar:</h3>
    <textarea id="comment-bab4" placeholder="Tulis komentar..."></textarea>
    <button onclick="addComment('bab4')">Kirim</button>
    <div id="comments-list-bab4"></div>
  </div>
  <div style="display:flex; justify-content:space-between; margin-top:30px;">
    <div class="btn" onclick="openSection('bab3')">← Previous Chapter</div>
    <div class="btn" onclick="openSection('bab5')">Next Chapter →</div>
  </div>
</section>

<section id="bab5">
  <h1>Bab 5 — Resonansi Lama</h1>
  <p>Misteri yang lebih tua dari Circle mulai muncul. Sebuah ikatan perlahan tumbuh di antara keheningan...</p>
  <div class="like-btn" onclick="toggleLike('bab5')">❤️ <span id="like-bab5">0</span></div>
  <div class="comment-section">
    <h3>Komentar:</h3>
    <textarea id="comment-bab5" placeholder="Tulis komentar..."></textarea>
    <button onclick="addComment('bab5')">Kirim</button>
    <div id="comments-list-bab5"></div>
  </div>
  <div style="display:flex; justify-content:space-between; margin-top:30px;">
    <div class="btn" onclick="openSection('bab4')">← Previous Chapter</div>
    <div class="btn" onclick="openSection('bab6')">Next Chapter →</div>
  </div>
</section>

<section id="bab6">
  <h1>Bab 6 — Suara yang Hilang</h1>
  <p>Kemampuan Lucien menguak hal-hal yang tidak tercatat dalam doktrin. Ancaman mulai muncul...</p>
  <div class="like-btn" onclick="toggleLike('bab6')">❤️ <span id="like-bab6">0</span></div>
  <div class="comment-section">
    <h3>Komentar:</h3>
    <textarea id="comment-bab6" placeholder="Tulis komentar..."></textarea>
    <button onclick="addComment('bab6')">Kirim</button>
    <div id="comments-list-bab6"></div>
  </div>
  <div style="display:flex; justify-content:space-between; margin-top:30px;">
    <div class="btn" onclick="openSection('bab5')">← Previous Chapter</div>
    <div class="btn" onclick="openSection('bab7')">Next Chapter →</div>
  </div>
</section>

<section id="bab7">
  <h1>Bab 7 — Keheningan Memanggil</h1>
  <p>Romance mulai berisiko, pilihan moral muncul, ketegangan dengan Gereja meningkat...</p>
  <div class="like-btn" onclick="toggleLike('bab7')">❤️ <span id="like-bab7">0</span></div>
  <div class="comment-section">
    <h3>Komentar:</h3>
    <textarea id="comment-bab7" placeholder="Tulis komentar..."></textarea>
    <button onclick="addComment('bab7')">Kirim</button>
    <div id="comments-list-bab7"></div>
  </div>
  <div style="display:flex; justify-content:space-between; margin-top:30px;">
    <div class="btn" onclick="openSection('bab6')">← Previous Chapter</div>
    <div class="btn" onclick="openSection('bab8')">Next Chapter →</div>
  </div>
</section>

<section id="bab8">
  <h1>Bab 8 — Retak Aristokrat</h1>
  <p>Intrik keluarga dan politik muncul, Gereja mulai curiga, rahasia sedikit terbuka...</p>
  <div class="like-btn" onclick="toggleLike('bab8')">❤️ <span id="like-bab8">0</span></div>
  <div class="comment-section">
    <h3>Komentar:</h3>
    <textarea id="comment-bab8" placeholder="Tulis komentar..."></textarea>
    <button onclick="addComment('bab8')">Kirim</button>
    <div id="comments-list-bab8"></div>
  </div>
  <div style="display:flex; justify-content:space-between; margin-top:30px;">
    <div class="btn" onclick="openSection('bab7')">← Previous Chapter</div>
    <div class="btn" onclick="openSection('bab9')">Next Chapter →</div>
  </div>
</section>

<section id="bab9">
  <h1>Bab 9 — Lingkaran Terakhir</h1>
  <p>Climax cerita, pertaruhan tinggi, misteri besar terungkap, romance mencapai puncak...</p>
  <div class="like-btn" onclick="toggleLike('bab9')">❤️ <span id="like-bab9">0</span></div>
  <div class="comment-section">
    <h3>Komentar:</h3>
    <textarea id="comment-bab9" placeholder="Tulis komentar..."></textarea>
    <button onclick="addComment('bab9')">Kirim</button>
    <div id="comments-list-bab9"></div>
  </div>
  <div style="display:flex; justify-content:space-between; margin-top:30px;">
    <div class="btn" onclick="openSection('bab8')">← Previous Chapter</div>
    <div class="btn" onclick="openSection('bab10')">Next Chapter →</div>
  </div>
</section>

<section id="bab10">
  <h1>Bab 10 — Kembali dari Malam</h1>
  <p>Epilog: konsekuensi, penutupan romance, dunia, Circle, dan Gereja...</p>
  <div class="like-btn" onclick="toggleLike('bab10')">❤️ <span id="like-bab10">0</span></div>
  <div class="comment-section">
    <h3>Komentar:</h3>
    <textarea id="comment-bab10" placeholder="Tulis komentar..."></textarea>
    <button onclick="addComment('bab10')">Kirim</button>
    <div id="comments-list-bab10"></div>
  </div>
  <div style="display:flex; justify-content:space-between; margin-top:30px;">
    <div class="btn" onclick="openSection('bab9')">← Previous Chapter</div>
    <div class="btn" onclick="openSection('arsip')">Back to Arsip</div>
  </div>
</section>

<script>
// NAVIGATION
function openSection(id){
  document.querySelectorAll("section").forEach(sec=>sec.style.display="none");
  document.getElementById(id).style.display="block";
  window.scrollTo(0,0);
}

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
