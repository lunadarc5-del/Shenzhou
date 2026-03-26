
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

<!-- BAB & CHAPTER -->
<script>
const totalBab=10;
const chaptersPerBab=[3,4,3,2,3,3,2,2,3,3];

// Chapter 1 & 2 full isi cerita sesuai kiriman user
const chapterContent = {
  "bab1-ch1": `
<p>Langit pecah dalam satu kilatan cahaya.</p>
<p>Logam saling menghantam. Orang-orang berteriak. Lalu semuanya gelap.</p>
<p>Lucien tidak merasakan sakit. Hanya rasa jatuh yang panjang, seolah tubuhnya terlepas dari dunia.</p>
<p>Ia ingin membuka mata. Namun tidak ada cahaya. Tidak ada suara. Tidak ada apa-apa.</p>
<p>.....</p>
<p>Sebuah dentang terdengar pelan.</p>
<p>Ia membuka mata. Langit-langit kamar berwarna putih pucat. Lampu gantung kecil menyala redup. Udara terasa dingin dan bersih—berbeda dari kabin pesawat yang sesak dan penuh bau logam terbakar.</p>
<p>Ia menarik napas dalam. Tidak ada asap. Tidak ada kepanikan.</p>
<p>Ia bangkit perlahan dari tempat tidur besar. Jemarinya menyentuh seprai yang rapi dan halus.</p>
<p>Ia melihat tangannya sendiri. Kulitnya lebih pucat. Jarinya lebih panjang. Urat-uratnya tipis dan teratur.</p>
<p>Bukan tangannya.</p>
<p>Ia turun dari tempat tidur. Kakinya menyentuh lantai marmer. Tidak ada suara. Ia melangkah sekali lagi. Tetap sunyi.</p>
<p>Bukan karena ruangan itu hening—melainkan karena dunia tidak memberi gema atas langkahnya.</p>
<p>Lucien berjalan ke arah cermin.</p>
<p>Seorang pemuda menatapnya dari balik kaca. Rambut hitam tersisir rapi. Wajah muda dengan garis lembut bangsawan. Mata abu-abu yang terlalu tenang untuk seseorang yang baru saja mati.</p>
<p>Sebuah nama muncul perlahan di benaknya.</p>
<p><em>Lucien D’Armont.</em></p>
<p>Ingatan yang bukan miliknya mengalir, rapi dan tertata. Putra kedua keluarga D’Armont. Kota Funia. Baru saja menjalani ritual penerimaan Circle.</p>
<p>Ia terdiam cukup lama.</p>
<p><strong>Lucien:</strong> “Aku mati… dan bangun di sini.”</p>
<p>Ia meraih gelas kecil di atas meja, lalu menjatuhkannya dengan sengaja. Gelas itu menyentuh lantai marmer. Tanpa denting.</p>
<p>Hening yang sama seperti saat ia membuka mata.</p>
<p>Sebuah pemahaman muncul.</p>
<p><strong>Circle 9 – Jalur Malam (Silent).</strong></p>
<p>Tingkatan kekuatan bagi para Arkanis. Setiap manusia yang menjalani ritual hanya dapat menerima satu jalur. Semakin tinggi tingkatnya, semakin besar tekanan pada pikiran.</p>
<p>Jika gagal—mereka kehilangan kewarasan.</p>
<p>Tubuh ini berhasil. Circle 9 – Jalur Malam (Silent).</p>
<p>Kemampuannya sederhana. Meredam suara. Menghapus gema.</p>
<p>Ia memusatkan pikiran. Radius sunyi itu melebar tipis di sekelilingnya. Ia mencoba menariknya kembali. Sunyi itu menyusut. Stabil. Terkendali.</p>
<p>Namun—</p>
<p>Bayangannya di cermin bergerak sepersekian detik lebih lambat.</p>
<p>Lucien membeku. Ia mengangkat tangan. Bayangan mengikuti. Tepat. Seolah tidak pernah ada keterlambatan.</p>
<p>Hening. Ia menatap matanya sendiri. Ada sesuatu yang tidak berasal dari Jalur Malam (Silent). Sesuatu yang tidak tercatat dalam sistem Circle.</p>
<p>.....</p>
<p>Ketukan terdengar di pintu.</p>
<p><strong>Lucien:</strong>“Tuan muda.”</p>
<p><strong>Lucien:</strong>“Masuk.”</p>
<p>Dua orang dari Gereja Malam Tanpa Bintang memasuki ruangan.</p>
<p>Uskup Aldric Mourne berdiri tegak dalam jubah hitam tanpa ornamen. Tatapannya tajam dan penuh pengukuran.</p>
<p>Di sampingnya, Sister Mirella Vance membuka buku catatan kecil.</p>
<p><strong>Aldric:</strong> “Ritual berjalan lancar. Namun stabilitas tetap harus diperiksa. Bagaimana perasaanmu, Lucien?”</p>
<p><strong>Lucien:</strong> “Tubuh saya… stabil. Tidak ada distorsi.”</p>
<p><strong>Mirella:</strong> “Resonansi juga stabil, Tuan muda. Tapi jalur ini… bisa rapuh. Anda harus berhati-hati.”</p>
<p><strong>Lucien:</strong> “Aku mengerti. Tapi aku merasa… ada sesuatu yang lain.”</p>
<p><strong>Aldric:</strong> (menatap tajam) “Hati-hati dengan perasaan itu. Jalur Malam (Silent) menuntut kesabaran. Terlalu cepat menafsirkan bisa berbahaya.”</p>
<p>Sebelum pergi, Aldric berhenti sejenak.</p>
<p><strong>Aldric:</strong> “Gereja selalu mengawasi mereka yang bangun dari malam. Ingat itu.”</p>
<p>Pintu tertutup.</p>
<p>Sore itu, teriakan terdengar dari arah pelabuhan.</p>
<p>Seorang Arkanis muda terjatuh di jalan berbatu.</p>
<p><strong>Arkanis muda:</strong> “Aku bisa… aku bisa…”</p>
<p>Lingkaran samar menyala di bawah kakinya. Udara di sekelilingnya bergetar. Bayangannya memanjang tidak wajar.</p>
<p>Orang-orang mundur.</p>
<p><strong>Orang-orang:</strong>“Dissonan!”</p>
<p>Lucien berdiri tidak jauh dari sana. Mengamati. Menghitung risiko.</p>
<p>Tubuh Arkanis itu bergetar hebat. Lingkaran cahaya di bawahnya retak. Dan untuk satu detik—suara di seluruh pelabuhan lenyap.</p>
<p>Bukan karena kemampuan Lucien. Lebih luas dari itu. Seolah dunia sendiri berhenti bernapas.</p>
<p>Lucien merasakannya. Di dalam dirinya, sesuatu menjawab. Bukan Jalur Malam (Silent). Lebih dalam. Lebih tua.</p>
<p>Lingkaran di kaki Arkanis itu padam. Ia ambruk. Suara kembali. Orang-orang berteriak. Gereja datang.</p>
<p>Lucien tetap berdiri. Wajahnya tenang.</p>
<p>Namun untuk pertama kalinya sejak ia bangun—ia tahu.<br>
Ia tidak hanya membawa Circle 9 – Jalur Malam (Silent).<br>
Dan sesuatu di dalam dirinya telah bangun bersamaan dengan dirinya.</p>
  `,
  "bab1-ch2": `
<p>Malam jatuh di Funia. Lampu gas dan obor pelabuhan berkelip di kejauhan.</p>
<p>Dari balkon kamarnya, Lucien menatap jalan-jalan kota yang sepi.</p>
<p><strong>Lucien:</strong> “Tenang… terlalu tenang.”</p>
<p>Funia selalu terlihat damai malam hari. Tapi di bawah kedamaian itu, ada keseimbangan rapuh—bangsawan, Gereja, Arkanis. Setiap langkah salah, bisa memicu Dissonan.</p>
<p>Lucien menutup mata. Ia memusatkan pikiran. Sunyi menyebar dari dirinya, seperti biasa. Tapi ada sesuatu… ada getaran halus di bawah sunyi itu. Seolah dunia di sekelilingnya menahan napas.</p>
<p>Ia membuka mata dan menatap meja kerja. Sebuah kotak kayu kecil tersimpan rapi—relik keluarga D’Armont, Circle 9.</p>
<p>Lucien melangkah mendekat. Jari-jari tangannya terulur.</p>
<p><strong>Lucien:</strong> “Apa ini…?”</p>
<p>Begitu jarinya hampir menyentuh kotak, tubuhnya bereaksi. Getaran halus merambat, menilai. Lucien mundur satu langkah.</p>
<p><strong>Lucien:</strong> “Menilai aku?” (dengan nada setengah tersenyum)</p>
<p>Ia duduk, menatap kotak dari dekat. Sunyi mengalir di sekelilingnya. Tapi di dalamnya, sesuatu lain juga bergerak. Sesuatu yang lebih tua, lebih tua dari Circle, lebih tua dari Gereja.</p>
<p>Lucien menepuk meja.</p>
<p><strong>Lucien:</strong> “Baik… mari kita lihat seberapa jauh kau bisa bawa aku.”</p>
<p>Kotak bergetar sedikit. Cahaya samar memantul di dinding. Lucien menahan napas.</p>
<p><strong>Suara:</strong> “Bangkit.”</p>
<p>Lucien menatap kotak, menatap mata yang seakan hidup di kayu itu.</p>
<p><strong>Lucien:</strong> “Bangkit… oke. Aku lihat dulu.”</p>
<p>Ia menempatkan kedua tangan di atas kotak. Sunyi mengalir keluar, menenangkan. Tapi di dalam ketenangan itu, sesuatu lain juga bangkit. Lebih tua, lebih besar dari Circle.</p>
<p>Lampu di balkon bergetar sebentar. Riak energi muncul di udara. Lucien menunduk, fokus.</p>
<p><strong>Lucien:</strong> “Diam… tunggu… jangan salah langkah.”</p>
<p>Ia menarik napas panjang.</p>
<p><strong>Lucien:</strong> “Biar kubuat percobaan kecil.”</p>
<p>Lucien memutar relik perlahan, jari-jarinya menyentuh ukiran halus.</p>
<p><strong>Lucien:</strong> “Kalau aku cuma sentuh ringan, apa yang terjadi?”</p>
<p>Cahaya samar muncul di permukaan relik. Tangannya sedikit panas.</p>
<p><strong>Lucien:</strong> “Ah… iya, ada respon.”</p>
<p>Ia mencoba menarik sunyi sedikit lebih jauh, memperluas radiusnya. Lingkungan di kamar tetap diam, tapi kotak bergetar lagi. Cahaya memantul lebih terang.</p>
<p><strong>Lucien:</strong> “Ini… menyenangkan. Aku bisa… merasakan lebih banyak.”</p>
<p>Ia menatap kotak dengan mata setengah berbinar, setengah khawatir.</p>
<p><strong>Lucien:</strong> “Kalau Gereja tahu… mereka pasti tidak akan senang.”</p>
<p>Malam semakin dalam. Semua orang di Funia tidur. Tapi Lucien tidak. Ia menyesuaikan ritme tangannya dengan relik, merasakan sunyi dan getaran aneh itu bersatu.</p>
<p><strong>Suara:</strong> “Lebih jauh…”</p>
<p>Lucien menatap sekeliling.</p>
<p><strong>Lucien:</strong> “Lebih jauh… oke.”</p>
<p>Ia mencondongkan tubuh, menekan tangan ke relik. Sunyi meluas. Ruangan terasa lebih berat. Kotak bergetar lebih kuat. Riak cahaya memantul ke dinding.</p>
<p>Ia tersenyum lagi, kali ini sedikit kagum.</p>
<p><strong>Lucien:</strong> “Jadi, ini… bukan hanya Circle 9-ku. Ada sesuatu di sini. Sesuatu yang… lain.”</p>
<p>Hening malam itu pecah oleh langkah kaki di koridor. Lucien menoleh.</p>
<p><strong>Lucien:</strong> “Siapa?”</p>
<p>Tidak ada siapa-siapa. Hanya bayangan lampu yang bergerak. Tapi ia tahu, sesuatu mengawasinya, sesuatu yang sama tua dengan jalur yang ia terima—atau lebih tua.</p>
<p>Lucien menarik napas dalam-dalam. Malam itu, ia sadar: Circle 9 – Jalur Malam (Silent) hanyalah permulaan. Dan dunia barunya tidak akan pernah tenang lagi.</p>
  `
};
</script>

<div id="chapter-container" style="display:none;">
  <h1 id="chapter-title"></h1>
  <div id="chapter-content"></div>
  <div>
    <span class="like-btn" id="likeBtn">👍 <span id="likeCount">0</span></span>
  </div>
  <div class="comment-section">
    <h3>Komentar</h3>
    <textarea id="commentText" rows="3" placeholder="Tulis komentar..."></textarea>
    <button onclick="addComment()">Kirim</button>
    <div id="commentList"></div>
  </div>
  <div style="margin-top:20px; text-align:center;">
    <span class="btn" onclick="prevChapter()">Previous Chapter</span>
    <span class="btn" onclick="nextChapter()">Next Chapter</span>
  </div>
  <div class="back" onclick="openSection('arsip')">Kembali ke Arsip Bab</div>
</div>

<script>
// Navigation
let currentBab=1;
let currentCh=1;

function openSection(sectionId) {
  document.querySelectorAll("section").forEach(s=>s.style.display="none");
  document.getElementById(sectionId).style.display="block";
  if(sectionId.startsWith("bab")){
    currentBab=parseInt(sectionId.replace("bab",""));
    currentCh=1;
    loadChapter(currentBab,currentCh);
  }
}

// Load chapter
function loadChapter(bab,ch){
  const container=document.getElementById("chapter-container");
  const title=`Bab ${bab} — Chapter ${ch}`;
  document.getElementById("chapter-title").innerHTML=title;
  const key=`bab${bab}-ch${ch}`;
  document.getElementById("chapter-content").innerHTML=chapterContent[key] || "<p>Chapter ini masih belum tersedia.</p>";
  container.style.display="block";

  // Like
  const likeKey=`like-${key}`;
  const likeCount=localStorage.getItem(likeKey)||0;
  document.getElementById("likeCount").innerText=likeCount;
  document.getElementById("likeBtn").onclick=()=>{
    let count=parseInt(localStorage.getItem(likeKey)||0)+1;
    localStorage.setItem(likeKey,count);
    document.getElementById("likeCount").innerText=count;
  }

  // Comments
  const commentKey=`comment-${key}`;
  const comments=JSON.parse(localStorage.getItem(commentKey)||"[]");
  const list=document.getElementById("commentList");
  list.innerHTML="";
  comments.forEach(c=>{
    const p=document.createElement("p");
    p.innerText=c;
    list.appendChild(p);
  });
}

function addComment(){
  const key=`bab${currentBab}-ch${currentCh}`;
  const commentKey=`comment-${key}`;
  const text=document.getElementById("commentText").value.trim();
  if(text==="") return;
  const comments=JSON.parse(localStorage.getItem(commentKey)||"[]");
  comments.push(text);
  localStorage.setItem(commentKey,JSON.stringify(comments));
  document.getElementById("commentText").value="";
  loadChapter(currentBab,currentCh);
}

function nextChapter(){
  if(currentCh<chaptersPerBab[currentBab-1]){
    currentCh++;
  }else if(currentBab<totalBab){
    currentBab++;
    currentCh=1;
  }else return;
  loadChapter(currentBab,currentCh);
}

function prevChapter(){
  if(currentCh>1){
    currentCh--;
  }else if(currentBab>1){
    currentBab--;
    currentCh=chaptersPerBab[currentBab-1];
  }else return;
  loadChapter(currentBab,currentCh);
}

// Progress bar
window.onscroll=function(){
  const winScroll=document.body.scrollTop || document.documentElement.scrollTop;
  const height=document.documentElement.scrollHeight - document.documentElement.clientHeight;
  const scrolled=(winScroll/height)*100;
  document.getElementById("progressBar").style.width=scrolled+"%";
};
</script>

</body>
</html>
