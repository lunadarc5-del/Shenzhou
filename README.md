<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Circle IX — Jalur Malam</title>

<style>
body{
  margin:0;
  background:#0f0f12;
  color:#d6d8e0;
  font-family:Georgia, serif;
  line-height:1.9;
}

section{
  display:none;
  padding:60px 20px;
  max-width:750px;
  margin:auto;
}

.hero{
  height:100vh;
  display:flex;
  flex-direction:column;
  justify-content:center;
  align-items:center;
  text-align:center;
  background:linear-gradient(#0f0f12,#1a1c22);
}

.hero h1{
  font-size:48px;
  letter-spacing:6px;
  margin:0;
  color:#c9ccd6;
}

.hero h2{
  margin-top:10px;
  font-size:22px;
  color:#8a8fa3;
}

.quote{
  margin-top:25px;
  font-style:italic;
  opacity:0.7;
}

.btn{
  margin-top:35px;
  padding:12px 28px;
  background:#2a1f3a;
  color:white;
  text-decoration:none;
  cursor:pointer;
  display:inline-block;
}

.btn:hover{
  background:#3a2a55;
}

.chapter-list a{
  display:block;
  margin:15px 0;
  text-decoration:none;
  color:#d6d8e0;
  border-bottom:1px solid #333;
  padding-bottom:8px;
}

.chapter-list a:hover{
  color:white;
  border-color:#6d5cae;
}

h1{
  text-align:center;
  margin-bottom:40px;
}

.back{
  margin-top:60px;
  text-align:center;
  opacity:0.6;
  cursor:pointer;
}

.progress{
  position:fixed;
  top:0;
  left:0;
  height:3px;
  background:#6d5cae;
  width:0%;
}
</style>
</head>

<body>

<div class="progress" id="progressBar"></div>

<!-- LANDING -->
<section id="landing" style="display:block;">
  <div class="hero">
    <h1>CIRCLE IX</h1>
    <h2>Jalur Malam</h2>
    <p class="quote">“Sunyi bukan ketiadaan suara.”</p>
    <div class="btn" onclick="openSection('arsip')">Mulai Membaca</div>
  </div>
</section>

<!-- ARSIP -->
<section id="arsip">
  <h1>BAB I — Circle 9: Jalur Malam</h1>

  <div class="chapter-list">
    <a onclick="openSection('ch1')">Chapter 1 — Dentang di Ruang Sunyi</a>
    <a onclick="openSection('ch2')">Chapter 2 — Retakan Stabilitas</a>
  </div>

  <div class="back" onclick="openSection('landing')">Kembali</div>
</section>

<!-- CHAPTER 1 -->
<section id="ch1">
  <h1>Chapter 1 — Dentang di Ruang Sunyi</h1>

  <p>Langit pecah dalam satu kilatan cahaya.</p>
  <p>Logam saling menghantam. Orang-orang berteriak.</p>
  <p>Lalu semuanya gelap.</p>

  <p>Lucien tidak merasakan sakit. Hanya rasa jatuh yang panjang.</p>

  <p>.....</p>

  <p>Ia membuka mata.</p>
  <p>Langit-langit kamar putih pucat menyambutnya.</p>

  <p>Lucien D’Armont.</p>
  <p>Circle 9. Jalur Malam.</p>

  <p>Namun bayangannya bergerak sepersekian detik lebih lambat.</p>

  <div class="back" onclick="openSection('arsip')">Kembali ke Arsip</div>
</section>

<!-- CHAPTER 2 -->
<section id="ch2">
  <h1>Chapter 2 — Retakan Stabilitas</h1>

  <p>Malam turun tanpa suara.</p>

  <p>Lucien berdiri di balkon kediaman D’Armont. Kota Funia tampak tenang, terlalu tenang.</p>

  <p>Ia mencoba memperluas radius sunyinya.</p>

  <p>Udara di sekelilingnya menekan. Tidak goyah. Stabil.</p>

  <p>Namun bayangan di kakinya—tidak mengikuti cahaya bulan.</p>

  <p>Untuk sesaat, bayangan itu memanjang ke arah yang berlawanan.</p>

  <p>Bukan efek Jalur Malam.</p>

  <p>Sesuatu yang lain.</p>

  <p>Lebih dalam dari Circle.</p>

  <div class="back" onclick="openSection('arsip')">Kembali ke Arsip</div>
</section>

<script>
function openSection(id){
  document.querySelectorAll("section").forEach(sec=>sec.style.display="none");
  document.getElementById(id).style.display="block";
  window.scrollTo(0,0);
}

window.onscroll=function(){
  let winScroll=document.body.scrollTop||document.documentElement.scrollTop;
  let height=document.documentElement.scrollHeight-document.documentElement.clientHeight;
  let scrolled=(winScroll/height)*100;
  document.getElementById("progressBar").style.width=scrolled+"%";
};
</script>

</body>
</html>
