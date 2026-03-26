<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Chronicles - Web Novel</title>
<style>
body { margin:0; font-family:'Arial', sans-serif; background:#f5f5f5; color:#222; }
header { text-align:center; padding:20px; background:#1b1b1b; color:#fff; }
h1, h2 { margin:10px 0; }
.chapter-list ul { list-style:none; padding:0; display:flex; flex-wrap:wrap; justify-content:center; }
.chapter-list li { margin:10px; }
.chapter-list a { text-decoration:none; color:#1b1b1b; background:#ffc107; padding:10px 20px; border-radius:5px; font-weight:bold; }
.chapter-list a:hover { background:#ffb300; }
.chapter-container { max-width:600px; margin:20px auto; }
.chapter-container img, .chapter-container p { width:100%; display:block; margin-bottom:15px; border-radius:5px; }
.chapter-nav { display:flex; justify-content:space-between; padding:10px 20px; background:#1b1b1b; }
.chapter-nav a, .chapter-nav button { color:#fff; background:#ff5722; border:none; padding:8px 15px; border-radius:5px; text-decoration:none; font-weight:bold; cursor:pointer; }
.chapter-nav a:hover, .chapter-nav button:hover { background:#e64a19; }
@media(max-width:700px){ .chapter-nav { flex-direction:column; gap:10px; } }
</style>
</head>
<body>

<header>
<h1>Chronicles</h1>
<p>Penulis: Ade Angga Pratama (Shenzhou)</p>
</header>

<section class="chapter-list">
<h2>Daftar Chapter</h2>
<ul>
<li><a href="#chapter1">Chapter 1</a></li>
<li><a href="#chapter2">Chapter 2</a></li>
<li><a href="#chapter3">Chapter 3</a></li>
<li><a href="#chapter4">Chapter 4</a></li>
<li><a href="#chapter5">Chapter 5</a></li>
<li><a href="#chapter6">Chapter 6</a></li>
<li><a href="#chapter7">Chapter 7</a></li>
<li><a href="#chapter8">Chapter 8</a></li>
<li><a href="#chapter9">Chapter 9</a></li>
<li><a href="#chapter10">Chapter 10</a></li>
</ul>
</section>

<!-- ===== Chapter Containers ===== -->
<div id="chapter1" class="chapter-container">
<div class="chapter-nav"><button onclick="scrollToPrevChapter(1)">⬅ Kembali</button><button onclick="scrollToNextChapter(1)">Next ➡</button></div>
<p>Ini adalah isi Chapter 1. Tambahkan teks atau gambar di sini.</p>
<div class="chapter-nav"><button onclick="scrollToPrevChapter(1)">⬅ Kembali</button><button onclick="scrollToNextChapter(1)">Next ➡</button></div>
</div>

<div id="chapter2" class="chapter-container">
<div class="chapter-nav"><button onclick="scrollToPrevChapter(2)">⬅ Kembali</button><button onclick="scrollToNextChapter(2)">Next ➡</button></div>
<p>Ini adalah isi Chapter 2. Tambahkan teks atau gambar di sini.</p>
<div class="chapter-nav"><button onclick="scrollToPrevChapter(2)">⬅ Kembali</button><button onclick="scrollToNextChapter(2)">Next ➡</button></div>
</div>

<div id="chapter3" class="chapter-container">
<div class="chapter-nav"><button onclick="scrollToPrevChapter(3)">⬅ Kembali</button><button onclick="scrollToNextChapter(3)">Next ➡</button></div>
<p>Ini adalah isi Chapter 3. Tambahkan teks atau gambar di sini.</p>
<div class="chapter-nav"><button onclick="scrollToPrevChapter(3)">⬅ Kembali</button><button onclick="scrollToNextChapter(3)">Next ➡</button></div>
</div>

<!-- Tambahkan chapter 4–10 dengan pola yang sama -->

<script>
const totalChapters = 10;

function scrollToNextChapter(current){
  let next = current + 1;
  if(next > totalChapters) next = totalChapters;
  document.getElementById(`chapter${next}`).scrollIntoView({behavior:'smooth'});
}

function scrollToPrevChapter(current){
  let prev = current - 1;
  if(prev < 1) prev = 1;
  document.getElementById(`chapter${prev}`).scrollIntoView({behavior:'smooth'});
}
</script>

</body>
</html>
