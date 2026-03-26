

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

<!-- BAB 1 -->
<section id="bab1">
  <h1>Bab 1 — Circle 9: Jalur Malam</h1>
  <div class="chapter-sublist">
    <a onclick="openChapter('bab1','bab1-ch1')">Chapter 1</a>
    <a onclick="openChapter('bab1','bab1-ch2')">Chapter 2</a>
    <a onclick="openChapter('bab1','bab1-ch3')">Chapter 3</a>
  </div>
  <div class="back" onclick="openSection('arsip')">← Kembali ke Arsip Bab</div>
</section>

<!-- BAB 1 CHAPTER 1 -->
<section id="bab1-ch1">
  <h2>Bab 1 — Chapter 1</h2>
  <p>
Langit pecah dalam satu kilatan cahaya.<br><br>

Logam saling menghantam. Orang-orang berteriak. Lalu semuanya gelap.<br><br>

Lucien tidak merasakan sakit. Hanya rasa jatuh yang panjang, seolah tubuhnya terlepas dari dunia.<br><br>

Ia ingin membuka mata. Namun tidak ada cahaya. Tidak ada suara. Tidak ada apa-apa.<br><br>

.....<br><br>

Sebuah dentang terdengar pelan.<br><br>

Ia membuka mata. Langit-langit kamar berwarna putih pucat. Lampu gantung kecil menyala redup. Udara terasa dingin dan bersih—berbeda dari kabin pesawat yang sesak dan penuh bau logam terbakar.<br><br>

Ia menarik napas dalam. Tidak ada asap. Tidak ada kepanikan.<br><br>

Ia bangkit perlahan dari tempat tidur besar. Jemarinya menyentuh seprai yang rapi dan halus.<br><br>

Ia melihat tangannya sendiri. Kulitnya lebih pucat. Jarinya lebih panjang. Urat-uratnya tipis dan teratur.<br><br>

Bukan tangannya.<br><br>

Ia turun dari tempat tidur. Kakinya menyentuh lantai marmer. Tidak ada suara. Ia melangkah sekali lagi. Tetap sunyi.<br><br>

Bukan karena ruangan itu hening—<br>
melainkan karena dunia tidak memberi gema atas langkahnya.<br><br>

Lucien berjalan ke arah cermin.<br><br>

Seorang pemuda menatapnya dari balik kaca. Rambut hitam tersisir rapi. Wajah muda dengan garis lembut bangsawan. Mata abu-abu yang terlalu tenang untuk seseorang yang baru saja mati.<br><br>

Sebuah nama muncul perlahan di benaknya.<br><br>

<em>Lucien D’Armont.</em><br><br>

Ingatan yang bukan miliknya mengalir, rapi dan tertata. Putra kedua keluarga D’Armont. Kota Funia. Baru saja menjalani ritual penerimaan Circle.<br><br>

Ia terdiam cukup lama.<br><br>

<em>Lucien:</em> “Aku mati… dan bangun di sini.”<br><br>

Ia meraih gelas kecil di atas meja, lalu menjatuhkannya dengan sengaja. Gelas itu menyentuh lantai marmer. Tanpa denting.<br><br>

Hening yang sama seperti saat ia membuka mata.<br><br>

Sebuah pemahaman muncul.<br><br>

<em>Circle 9 – Jalur Malam (Silent).</em><br><br>

Tingkatan kekuatan bagi para Arkanis. Setiap manusia yang menjalani ritual hanya dapat menerima satu jalur. Semakin tinggi tingkatnya, semakin besar tekanan pada pikiran.<br><br>

Jika gagal—mereka kehilangan kewarasan.<br><br>

Tubuh ini berhasil. Circle 9 – Jalur Malam (Silent).<br><br>

Kemampuannya sederhana. Meredam suara. Menghapus gema.<br><br>

Ia memusatkan pikiran. Radius sunyi itu melebar tipis di sekelilingnya. Ia mencoba menariknya kembali. Sunyi itu menyusut. Stabil. Terkendali.<br><br>

Namun—<br><br>

Bayangannya di cermin bergerak sepersekian detik lebih lambat.<br><br>

Lucien membeku. Ia mengangkat tangan. Bayangan mengikuti. Tepat. Seolah tidak pernah ada keterlambatan.<br><br>

Hening. Ia menatap matanya sendiri. Ada sesuatu yang tidak berasal dari Jalur Malam (Silent). Sesuatu yang tidak tercatat dalam sistem Circle.<br><br>

.....<br><br>

Ketukan terdengar di pintu.<br><br>

<em>Lucien:</em>“Tuan muda.”<br><br>

<em>Lucien:</em>“Masuk.”<br><br>

Dua orang dari Gereja Malam Tanpa Bintang memasuki ruangan.<br><br>

Uskup Aldric Mourne berdiri tegak dalam jubah hitam tanpa ornamen. Tatapannya tajam dan penuh pengukuran.<br><br>

Di sampingnya, Sister Mirella Vance membuka buku catatan kecil.<br><br>

<em>Aldric:</em> “Ritual berjalan lancar. Namun stabilitas tetap harus diperiksa. Bagaimana perasaanmu, Lucien?”<br><br>

<em>Lucien:</em> “Tubuh saya… stabil. Tidak ada distorsi.”<br><br>

<em>Mirella:</em> “Resonansi juga stabil, Tuan muda. Tapi jalur ini… bisa rapuh. Anda harus berhati-hati.”<br><br>

<em>Lucien:</em> “Aku mengerti. Tapi aku merasa… ada sesuatu yang lain.”<br><br>

<em>Aldric:</em> (menatap tajam) “Hati-hati dengan perasaan itu. Jalur Malam (Silent) menuntut kesabaran. Terlalu cepat menafsirkan bisa berbahaya.”<br><br>

Sebelum pergi, Aldric berhenti sejenak.<br><br>

<em>Aldric:</em> “Gereja selalu mengawasi mereka yang bangun dari malam. Ingat itu.”<br><br>

Pintu tertutup.<br><br>

Sore itu, teriakan terdengar dari arah pelabuhan.<br><br>

Seorang Arkanis muda terjatuh di jalan berbatu.<br><br>

<em>Arkanis muda:</em> “Aku bisa… aku bisa…”<br><br>

Lingkaran samar menyala di bawah kakinya. Udara di sekelilingnya bergetar. Bayangannya memanjang tidak wajar.<br><br>

Orang-orang mundur.<br><br>

<em>Orang-orang:</em>“Dissonan!”<br><br>

Lucien berdiri tidak jauh dari sana. Mengamati. Menghitung risiko.<br><br>

Tubuh Arkanis itu bergetar hebat. Lingkaran cahaya di bawahnya retak. Dan untuk satu detik—suara di seluruh pelabuhan lenyap.<br><br>

Bukan karena kemampuan Lucien. Lebih luas dari itu. Seolah dunia sendiri berhenti bernapas.<br><br>

Lucien merasakannya. Di dalam dirinya, sesuatu menjawab. Bukan Jalur Malam (Silent). Lebih dalam. Lebih tua.<br><br>

Lingkaran di kaki Arkanis itu padam. Ia ambruk. Suara kembali. Orang-orang berteriak. Gereja datang.<br><br>

Lucien tetap berdiri. Wajahnya tenang.<br><br>

Namun untuk pertama kalinya sejak ia bangun—ia tahu.<br><br>
Ia tidak hanya membawa Circle 9 – Jalur Malam (Silent).<br>
Dan sesuatu di dalam dirinya telah bangkit bersamaan dengan dirinya.
  </p>
  <div class="like-btn" onclick="toggleLike('bab1-ch1')">❤️ <span id="like-bab1-ch1">0</span></div>
  <div class="comment  <h3>Komentar:</h3>
    <textarea id="comment-bab1-ch1" placeholder="Tulis komentar..."></textarea>
    <button onclick="addComment('bab1-ch1')">Kirim</button>
    <div id="comments-list-bab1-ch1"></div>
  </div>
  <div style="display:flex; justify-content:space-between; margin-top:20px;">
    <div class="btn" onclick="openChapter('bab1','arsip')">← Previous Chapter</div>
    <div class="btn" onclick="openChapter('bab1','bab1-ch2')">Next Chapter →</div>
  </div>
</section>

<!-- BAB 1 CHAPTER 2 -->
<section id="bab1-ch2">
  <h2>Bab 1 — Chapter 2</h2>
  <p>
Malam jatuh di Funia. Lampu gas dan obor pelabuhan berkelip di kejauhan.<br><br>

Dari balkon kamarnya, Lucien menatap jalan-jalan kota yang sepi.<br><br>

<em>Lucien:</em> “Tenang… terlalu tenang.”<br><br>

Funia selalu terlihat damai malam hari. Tapi di bawah kedamaian itu, ada keseimbangan rapuh—bangsawan, Gereja, Arkanis. Setiap langkah salah, bisa memicu Dissonan.<br><br>

Lucien menutup mata. Ia memusatkan pikiran.<br>
Sunyi menyebar dari dirinya, seperti biasa. Tapi ada sesuatu… ada getaran halus di bawah sunyi itu.<br>
Seolah dunia di sekelilingnya menahan napas.<br><br>

Ia membuka mata dan menatap meja kerja. Sebuah kotak kayu kecil tersimpan rapi—relik keluarga D’Armont, Circle 9.<br><br>

<em>Lucien:</em> “Apa ini…?”<br><br>

Begitu jarinya hampir menyentuh kotak, tubuhnya bereaksi. Getaran halus merambat, menilai.<br>
Lucien mundur satu langkah.<br><br>

<em>Lucien:</em> “Menilai aku?”<br>
(dengan nada setengah tersenyum)<br><br>

Ia duduk, menatap kotak dari dekat.<br>
Sunyi mengalir di sekelilingnya. Tapi di dalamnya, sesuatu lain juga bergerak. Sesuatu yang lebih tua, lebih tua dari Circle, lebih tua dari Gereja.<br><br>

Lucien menepuk meja.<br><br>

<em>Lucien:</em> “Baik… mari kita lihat seberapa jauh kau bisa bawa aku.”<br><br>

Kotak bergetar sedikit. Cahaya samar memantul di dinding. Lucien menahan napas.<br><br>

<em>Suara:</em> “Bangkit.”<br><br>

Lucien menatap kotak, menatap mata yang seakan hidup di kayu itu.<br><br>

<em>Lucien:</em> “Bangkit… oke. Aku lihat dulu.”<br><br>

Ia menempatkan kedua tangan di atas kotak. Sunyi mengalir keluar, menenangkan. Tapi di dalam ketenangan itu, sesuatu lain juga bangkit. Lebih tua, lebih besar dari Circle.<br><br>

Lampu di balkon bergetar sebentar. Riak energi muncul di udara. Lucien menunduk, fokus.<br><br>

<em>Lucien:</em> “Diam… tunggu… jangan salah langkah.”<br><br>

Ia menarik napas panjang.<br><br>

<em>Lucien:</em> “Biar kubuat percobaan kecil.”<br><br>

Lucien memutar relik perlahan, jari-jarinya menyentuh ukiran halus.<br><br>

<em>Lucien:</em> “Kalau aku cuma sentuh ringan, apa yang terjadi?”<br><br>

Cahaya samar muncul di permukaan relik. Tangannya sedikit panas.<br><br>

<em>Lucien:</em> “Ah… iya, ada respon.”<br><br>

Ia mencoba menarik sunyi sedikit lebih jauh, memperluas radiusnya.<br>
Lingkungan di kamar tetap diam. Tapi kotak bergetar lebih kuat.<br><br>

<em>Lucien:</em> “Ini… bukan sekadar jalur Malam (Silent). Ini sesuatu… lain.”<br><br>

Ia menutup mata, menenangkan pikiran. Detak jantungnya perlahan. Ia merasakan ritme yang stabil—aneh, tapi stabil.<br><br>

<em>Lucien:</em> “Stabilitas aneh… tapi sesuai.”<br><br>

Ia membuka mata. Lampu di kamar kembali normal. Relik tetap di sana, sunyi. Tapi ada sesuatu di dalam dirinya… perlahan, mulai bangkit.
  </p>
  <div class="like-btn" onclick="toggleLike('bab1-ch2')">❤️ <span id="like-bab1-ch2">0</span></div>
  <div class="comment-section">
    <h3>Komentar:</h3>
    <textarea id="comment-bab1-ch2" placeholder="Tulis komentar..."></textarea>
    <button onclick="addComment('bab1-ch2')">Kirim</button>
    <div id="comments-list-bab1-ch2"></div>
  </div>
  <div style="display:flex; justify-content:space-between; margin-top:20px;">
    <div class="btn" onclick="openChapter('bab1','bab1-ch1')">← Previous Chapter</div>
    <div class="btn" onclick="openChapter('bab1','bab1-ch3')">Next Chapter →</div>
  </div>
</section>

<!-- BAB 1 CHAPTER 3 Placeholder -->
<section id="bab1-ch3">
  <h2>Bab 1 — Chapter 3</h2>
  <p>Chapter 3 akan segera hadir.</p>
</section>

<!-- Script -->
<script>
function openSection(id){
  document.querySelectorAll('section').forEach(s=>s.style.display='none');
  document.getElementById(id).style.display='block';
}

function openChapter(bab, chapter){
  openSection(chapter);
}

function toggleLike(chapterId){
  const span = document.getElementById('like-'+chapterId);
  span.textContent = parseInt(span.textContent)+1;
}

function addComment(chapterId){
  const textarea = document.getElementById('comment-'+chapterId);
  const list = document.getElementById('comments-list-'+chapterId);
  if(textarea.value.trim()==='') return;
  const div = document.createElement('div');
  div.textContent = textarea.value;
  div.style.borderBottom='1px solid #444';
  div.style.padding='4px 0';
  list.appendChild(div);
  textarea.value='';
}

window.addEventListener('scroll',()=>{
  const winScroll = document.body.scrollTop || document.documentElement.scrollTop;
  const height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
  const scrolled = (winScroll / height) * 100;
  document.getElementById('progressBar').style.width = scrolled+'%';
});
</script>
</body>
</html>
