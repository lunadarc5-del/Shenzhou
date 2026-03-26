
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Chronicles of the Ninth Circle</title>
<style>
body { margin:0; font-family: Georgia, serif; background:#0f0f12; color:#d6d8e0; line-height:1.9; padding-bottom:50px; }
section { display:none; padding:40px 20px; max-width:800px; margin:auto; }
.hero { display:flex; flex-direction:column; justify-content:center; align-items:center; height:100vh; text-align:center; background:linear-gradient(#0f0f12,#1a1c22); }
.hero h1 { font-size:48px; letter-spacing:4px; margin:0; color:#c9ccd6; }
.hero h2 { margin-top:10px; font-size:22px; color:#8a8fa3; }
.hero p { margin-top:25px; font-style:italic; opacity:0.8; max-width:700px; }
.btn { margin-top:20px; padding:10px 24px; background:#2a1f3a; color:white; cursor:pointer; text-decoration:none; border-radius:5px; }
.btn:hover { background:#3a2a55; }
.chapter-list a, .chapter-sublist a { display:block; margin:8px 0; text-decoration:none; color:#d6d8e0; border-bottom:1px solid #333; padding-bottom:5px; cursor:pointer; }
.chapter-list a:hover, .chapter-sublist a:hover { color:white; border-color:#6d5cae; }
h1,h2 { text-align:center; }
.back, .next { margin-top:30px; text-align:center; opacity:0.7; cursor:pointer; display:inline-block; padding:5px 10px; }
.back:hover, .next:hover { opacity:1; color:#6d5cae; }
.progress { position:fixed; top:0; left:0; height:3px; background:#6d5cae; width:0%; z-index:100; }
.comment-section { margin-top:20px; border-top:1px solid #444; padding-top:15px; }
.comment-section input, .comment-section textarea { width:100%; margin:5px 0; padding:8px; background:#1a1c22; border:1px solid #555; color:#d6d8e0; }
.comment-section button { padding:6px 14px; margin-top:5px; background:#2a1f3a; color:white; border:none; cursor:pointer; border-radius:4px; }
.comment-section button:hover { background:#3a2a55; }
.like-btn { margin-top:10px; cursor:pointer; font-size:16px; display:inline-block; }
.author { margin-top:10px; font-style:italic; opacity:0.7; }
p strong.character { color:white; font-weight:bold; }
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
const totalBab = 10;
const chaptersPerBab = [3,4,3,2,3,3,2,2,3,3]; 

function highlightCharacters(text){
  return text.replace(/\*(.*?)\*/g,'<strong class="character">$1</strong>');
}

for(let i=1;i<=totalBab;i++){
  document.write(`<section id="bab${i}"><h1>Bab ${i}</h1><div class="chapter-sublist">`);
  for(let j=1;j<=chaptersPerBab[i-1];j++){
    document.write(`<a onclick="openChapter('bab${i}','bab${i}-ch${j}')">Chapter ${j}</a>`);
  }
  document.write(`</div><div class="back" onclick="openSection('arsip')">← Kembali ke Arsip Bab</div></section>`);

  for(let j=1;j<=chaptersPerBab[i-1];j++){
    document.write(`<section id="bab${i}-ch${j}">
      <h2>Bab ${i} — Chapter ${j}</h2>
      <p>`);

    if(i===1 && j===1){
      document.write(highlightCharacters(`Langit pecah dalam satu kilatan cahaya.

Logam saling menghantam. Orang-orang berteriak. Lalu semuanya gelap.

*Lucien* tidak merasakan sakit. Hanya rasa jatuh yang panjang, seolah tubuhnya terlepas dari dunia.

Ia ingin membuka mata. Namun tidak ada cahaya. Tidak ada suara. Tidak ada apa-apa.

.....

Sebuah dentang terdengar pelan.

Ia membuka mata. Langit-langit kamar berwarna putih pucat. Lampu gantung kecil menyala redup. Udara terasa dingin dan bersih—berbeda dari kabin pesawat yang sesak dan penuh bau logam terbakar.

Ia menarik napas dalam. Tidak ada asap. Tidak ada kepanikan.

Ia bangkit perlahan dari tempat tidur besar. Jemarinya menyentuh seprai yang rapi dan halus.

Ia melihat tangannya sendiri. Kulitnya lebih pucat. Jarinya lebih panjang. Urat-uratnya tipis dan teratur.

Bukan tangannya.

Ia turun dari tempat tidur. Kakinya menyentuh lantai marmer. Tidak ada suara. Ia melangkah sekali lagi. Tetap sunyi.

Bukan karena ruangan itu hening—melainkan karena dunia tidak memberi gema atas langkahnya.

*Lucien* berjalan ke arah cermin.

Seorang pemuda menatapnya dari balik kaca. Rambut hitam tersisir rapi. Wajah muda dengan garis lembut bangsawan. Mata abu-abu yang terlalu tenang untuk seseorang yang baru saja mati.

Sebuah nama muncul perlahan di benaknya.

*Lucien:* “Aku mati… dan bangun di sini.”

Ia meraih gelas kecil di atas meja, lalu menjatuhkannya dengan sengaja. Gelas itu menyentuh lantai marmer. Tanpa denting.

Hening yang sama seperti saat ia membuka mata.

Sebuah pemahaman muncul.

*Circle 9 – Jalur Malam (Silent).*

Tingkatan kekuatan bagi para Arkanis. Setiap manusia yang menjalani ritual hanya dapat menerima satu jalur. Semakin tinggi tingkatnya, semakin besar tekanan pada pikiran.

Jika gagal—mereka kehilangan kewarasan.

Tubuh ini berhasil. *Circle 9 – Jalur Malam (Silent).*

Kemampuannya sederhana. Meredam suara. Menghapus gema.

Ia memusatkan pikiran. Radius sunyi itu melebar tipis di sekelilingnya. Ia mencoba menariknya kembali. Sunyi itu menyusut. Stabil. Terkendali.

Namun—

Bayangannya di cermin bergerak sepersekian detik lebih lambat.

*Lucien* membeku. Ia mengangkat tangan. Bayangan mengikuti. Tepat. Seolah tidak pernah ada keterlambatan.

Hening. Ia menatap matanya sendiri. Ada sesuatu yang tidak berasal dari Jalur Malam (Silent). Sesuatu yang tidak tercatat dalam sistem Circle.

.....

Ketukan terdengar di pintu.

*Lucien:*“Tuan muda.”

*Lucien:*“Masuk.”

Dua orang dari Gereja Malam Tanpa Bintang memasuki ruangan.

Uskup Aldric Mourne berdiri tegak dalam jubah hitam tanpa ornamen. Tatapannya tajam dan penuh pengukuran.

Di sampingnya, Sister Mirella Vance membuka buku catatan kecil.

*Aldric:* “Ritual berjalan lancar. Namun stabilitas tetap harus diperiksa. Bagaimana perasaanmu, *Lucien*?”

*Lucien:* “Tubuh saya… stabil. Tidak ada distorsi.”

*Mirella:* “Resonansi juga stabil, Tuan muda. Tapi jalur ini… bisa rapuh. Anda harus berhati-hati.”

*Lucien:* “Aku mengerti. Tapi aku merasa… ada sesuatu yang lain.”

*Aldric:* (menatap tajam) “Hati-hati dengan perasaan itu. Jalur Malam (Silent) menuntut kesabaran. Terlalu cepat menafsirkan bisa berbahaya.”

Sebelum pergi, Aldric berhenti sejenak.

*Aldric:* “Gereja selalu mengawasi mereka yang bangun dari malam. Ingat itu.”

Pintu tertutup.

Sore itu, teriakan terdengar dari arah pelabuhan.

Seorang Arkanis muda terjatuh di jalan berbatu.

*Arkanis muda:* “Aku bisa… aku bisa…”

Lingkaran samar menyala di bawah kakinya. Udara di sekelilingnya bergetar. Bayangannya memanjang tidak wajar.

Orang-orang mundur.

*Orang-orang:*“Dissonan!”

*Lucien* berdiri tidak jauh dari sana. Mengamati. Menghitung risiko.

Tubuh Arkanis itu bergetar hebat. Lingkaran cahaya di bawahnya retak. Dan untuk satu detik—suara di seluruh pelabuhan lenyap.

Bukan karena kemampuan *Lucien*. Lebih luas dari itu. Seolah dunia sendiri berhenti bernapas.

*Lucien* merasakannya. Di dalam dirinya, sesuatu menjawab. Bukan Jalur Malam (Silent). Lebih dalam. Lebih tua.

Lingkaran di kaki Arkanis itu padam. Ia ambruk. Suara kembali. Orang-orang berteriak. Gereja datang.

*Lucien* tetap berdiri. Wajahnya tenang.

Namun untuk pertama kalinya sejak ia bangun—ia tahu.
Ia tidak hanya membawa *Circle 9 – Jalur Malam (Silent)*.
Dan sesuatu di dalam dirinya telah bangkit bersamaan dengan dirinya.`));
    } else if(i===1 && j===2){
      document.write(highlightCharacters(`Malam jatuh di Funia. Lampu gas dan obor pelabuhan berkelip di kejauhan.

Dari balkon kamarnya, *Lucien* menatap jalan-jalan kota yang sepi.

*Lucien:* “Tenang… terlalu tenang.”

Funia selalu terlihat damai malam hari. Tapi di bawah kedamaian itu, ada keseimbangan rapuh—bangsawan, Gereja, Arkanis. Setiap langkah salah, bisa memicu Dissonan.

*Lucien* menutup mata. Ia memusatkan pikiran.
Sunyi menyebar dari dirinya, seperti biasa. Tapi ada sesuatu… ada getaran halus di bawah sunyi itu.
Seolah dunia di sekelilingnya menahan napas.

Ia membuka mata dan menatap meja kerja. Sebuah kotak kayu kecil tersimpan rapi—relik keluarga D’Armont, Circle 9.

*Lucien* melangkah mendekat. Jari-jari tangannya terulur.

*Lucien:* “Apa ini…?”

Begitu jarinya hampir menyentuh kotak, tubuhnya bereaksi. Getaran halus merambat, menilai.
*Lucien* mundur satu langkah.

*Lucien:* “Menilai aku?”
(dengan nada setengah tersenyum)

Ia duduk, menatap kotak dari dekat.
Sunyi mengalir di sekelilingnya. Tapi di dalamnya, sesuatu lain juga bergerak. Sesuatu yang lebih tua, lebih tua dari Circle, lebih tua dari Gereja.

*Lucien* menepuk meja.

*Lucien:* “Baik… mari kita lihat seberapa jauh kau bisa bawa aku.”

Kotak bergetar sedikit. Cahaya samar memantul di dinding. *Lucien* menahan napas.

*Suara:* “Bangkit.”

*Lucien* menatap kotak, menatap mata yang seakan hidup di kayu itu.

*Lucien:* “Bangkit… oke. Aku lihat dulu.”

Ia menempatkan kedua tangan di atas kotak. Sunyi mengalir keluar, menenangkan. Tapi di dalam ketenangan itu, sesuatu lain juga bangkit. Lebih tua, lebih besar dari Circle.

Lampu di balkon bergetar sebentar. Riak energi muncul di udara. *Lucien* menunduk, fokus.

*Lucien:* “Diam… tunggu… jangan salah langkah.”

Ia menarik napas panjang.

*Lucien:* “Biar kubuat percobaan kecil.”

*Lucien* memutar relik perlahan, jari-jarinya menyentuh ukiran halus.

*Lucien:* “Kalau aku cuma sentuh ringan, apa yang terjadi?”

Cahaya samar muncul di permukaan relik. Tangannya sedikit panas.

*Lucien:* “Ah… iya, ada respon.”

Ia mencoba menarik sunyi sedikit lebih jauh, memperluas radiusnya.
Lingkungan di kamar tetap diam, tapi kotak bergetar lagi. Cahaya memantul lebih terang.

*Lucien:* “Ini… menyenangkan. Aku bisa… merasakan lebih banyak.”

Ia menatap kotak dengan mata setengah berbinar, setengah khawatir.

*Lucien:* “Kalau Gereja tahu… mereka pasti tidak akan senang.”

Malam semakin dalam. Semua orang di Funia tidur. Tapi *Lucien* tidak.
Ia menyesuaikan ritme tangannya dengan relik, merasakan sunyi dan getaran aneh itu bersatu.

*Suara:* “Lebih jauh…”

*Lucien* menatap sekeliling.

*Lucien:* “Lebih jauh… oke.”
Ia mencondongkan tubuh, menekan tangan ke relik. Sunyi meluas. Ruangan terasa lebih berat. Kotak bergetar lebih kuat. Riak cahaya memantul ke dinding.

Ia tersenyum lagi, kali ini sedikit kagum.

*Lucien:* “Jadi, ini… bukan hanya Circle 9-ku. Ada sesuatu di sini. Sesuatu yang… lain.”

Hening malam itu pecah oleh langkah kaki di koridor. *Lucien* menoleh.

*Lucien:* “Siapa?”

Tidak ada siapa-siapa. Hanya bayangan lampu yang bergerak. Tapi ia bisa merasakan sesuatu—sesuatu mengamati, menunggu.

*Lucien* menarik napas, menepuk meja.

*Lucien:* “Diam… tunggu. Aku masih belajar.”

Ia menatap kotak lagi.

*Lucien:* “Ini baru permulaan. Aku harus tahu… seberapa jauh kau bisa bawa aku.”

Dan di balik sunyi, sesuatu mulai merespons. Tidak tergesa. Tidak menakutkan. Tetapi sadar. Lebih tua dari Circle. Lebih tua dari Gereja.

Malam itu, *Lucien* memahami:

*Lucien:* “Silent bukan hanya diam. Silent adalah memilih kapan dunia harus berhenti meresponsnya.”

Dan sesuatu di dalam dirinya… perlahan, mulai bangkit.`));
    } else {
      document.write(`Isi cerita Bab ${i}, Chapter ${j}...`);
    }

    document.write(`</p>
      <div class="like-btn" onclick="toggleLike('bab${i}-ch${j}')">❤️ <span id="like-bab${i}-ch${j}">0</span></div>
      <div class="comment-section">
        <h3>Komentar:</h3>
        <textarea id="comment-bab${i}-ch${j}" placeholder="Tulis komentar..."></textarea>
        <button onclick="addComment('bab${i}-ch${j}')">Kirim</button>
        <div id="comments-list-bab${i}-ch${j}"></div>
      </div>
      <div style="text-align:center; margin-top:20px;">
        <span class="back" onclick="backChapter(${i},${j})">← Previous</span> |
        <span class="next" onclick="nextChapter(${i},${j})">Next →</span>
      </div>
      <div class="back" onclick="openSection('arsip')">← Kembali ke Arsip Bab</div>
    </section>`);
  }
}

function openSection(id){
  document.querySelectorAll('section').forEach(s=>s.style.display='none');
  document.getElementById(id).style.display='block';
  window.scrollTo({top:0, behavior:'smooth'});
}

function openChapter(bab,ch){
  openSection(ch);
}

function backChapter(bab,chapter){
  if(chapter>1){
    openChapter(`bab${bab}`,`bab${bab}-ch${chapter-1}`);
  } else {
    openChapter(`bab${bab}`,`bab${bab}-ch1`);
  }
}

function nextChapter(bab,chapter){
  const maxChapters = [3,4,3,2,3,3,2,2,3,3];
  if(chapter<maxChapters[bab-1]){
    openChapter(`bab${bab}`,`bab${bab}-ch${chapter+1}`);
  }
}

function toggleLike(id){
  const el = document.getElementById('like-'+id);
  let count = parseInt(el.textContent);
  count++;
  el.textContent=count;
}

function addComment(id){
  const input = document.getElementById('comment-'+id);
  const list = document.getElementById('comments-list-'+id);
  if(input.value.trim()!==''){
    const div = document.createElement('div');
    div.textContent = input.value;
    div.style.borderTop='1px solid #555';
    div.style.padding='4px 0';
    list.appendChild(div);
    input.value='';
  }
}

window.addEventListener('scroll',function(){
  const winScroll=document.body.scrollTop || document.documentElement.scrollTop;
  const height=document.documentElement.scrollHeight - document.documentElement.clientHeight;
  const scrolled=(winScroll/height)*100;
  document.getElementById('progressBar').style.width=scrolled+'%';
});
</script>

</body>
</html>
