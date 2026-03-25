<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Web Novelku</title>
<style>
body {
    font-family: 'Georgia', serif;
    background-color: #fdf6e3;
    color: #333;
    margin: 0;
    padding: 0;
    transition: background-color 0.3s, color 0.3s;
}
body.dark {
    background-color: #1e1e1e;
    color: #ddd;
}
header {
    text-align: center;
    padding: 2rem;
    background-color: #eee8d5;
    transition: background-color 0.3s;
}
body.dark header { background-color: #2c2c2c; }
main { max-width: 600px; margin: 2rem auto; padding: 1rem; }
.chapter { display: none; opacity: 0; transition: opacity 0.5s; }
.chapter.active { display: block; opacity: 1; }
.navigation { margin-top: 2rem; display: flex; justify-content: space-between; }
.navigation button { padding: 0.5rem 1rem; font-size: 1rem; cursor: pointer; background-color: #2a7ae2; color: white; border: none; border-radius: 5px; transition: background-color 0.3s; }
.navigation button:hover { background-color: #1f5bb5; }
.bookmark { margin-top: 1rem; display: flex; justify-content: space-between; align-items: center; }
.bookmark button { padding: 0.3rem 0.8rem; font-size: 0.9rem; cursor: pointer; background-color: #e27a2a; color: white; border: none; border-radius: 5px; transition: background-color 0.3s; }
.bookmark button:hover { background-color: #b55f20; }
.chapter-list { margin: 1rem 0; }
.chapter-list button { display: block; width: 100%; padding: 0.5rem; margin: 0.2rem 0; text-align: left; cursor: pointer; border: 1px solid #ccc; border-radius: 5px; background-color: #fff; transition: background-color 0.3s; }
.chapter-list button:hover { background-color: #eee; }
body.dark .chapter-list button { background-color: #333; color: #ddd; border-color: #555; }
body.dark .chapter-list button:hover { background-color: #444; }
.feedback { margin-top: 2rem; border-top: 1px solid #ccc; padding-top: 1rem; }
.feedback textarea { width: 100%; height: 60px; padding: 0.5rem; font-size: 1rem; border-radius: 5px; border: 1px solid #ccc; }
.feedback button { margin-top: 0.5rem; padding: 0.5rem 1rem; font-size: 1rem; cursor: pointer; background-color: #2a7ae2; color: white; border: none; border-radius: 5px; transition: background-color 0.3s; }
.feedback button:hover { background-color: #1f5bb5; }
</style>
</head>
<body>
<header>
<h1>Judul Novelku</h1>
<p>Baca bab demi bab di sini</p>
<button id="toggleDark">🌙 Mode Malam</button>
</header>
<main>
<!-- Daftar Bab -->
<div class="chapter-list">
    <button onclick="goChapter(0)">Bab 1: Awal Cerita</button>
    <button onclick="goChapter(1)">Bab 2: Konflik</button>
    <button onclick="goChapter(2)">Bab 3: Puncak Cerita</button>
</div>

<!-- Bab 1 -->
<div class="chapter active" id="chapter1">
<h2>Bab 1: Awal Cerita</h2>
<p>Ini adalah awal ceritaku. Tulis ceritamu di sini...</p>
</div>

<!-- Bab 2 -->
<div class="chapter" id="chapter2">
<h2>Bab 2: Konflik</h2>
<p>Bab kedua mulai menampilkan konflik cerita...</p>
</div>

<!-- Bab 3 -->
<div class="chapter" id="chapter3">
<h2>Bab 3: Puncak Cerita</h2>
<p>Di bab ini, cerita mencapai puncaknya...</p>
</div>

<!-- Navigasi dan Bookmark -->
<div class="navigation">
    <button id="prevBtn">← Sebelumnya</button>
    <button id="nextBtn">Selanjutnya →</button>
</div>
<div class="bookmark">
    <span id="bookmarkStatus">Tidak ada bookmark</span>
    <button id="bookmarkBtn">⭐ Bookmark Bab Ini</button>
</div>

<!-- Feedback Form -->
<div class="feedback">
<h3>Kirim Komentar / Saran</h3>
<textarea id="feedbackText" placeholder="Tulis komentarmu..."></textarea>
<button id="sendFeedback">Kirim</button>
</div>
</main>

<script>
const chapters = ["chapter1","chapter2","chapter3"];
let current = 0;

const showChapter = index=>{
    chapters.forEach((id,i)=>{
        const el = document.getElementById(id);
        if(i===index){
            el.classList.add("active");
            setTimeout(()=>el.style.opacity="1",50);
        } else {
            el.style.opacity="0";
            setTimeout(()=>el.classList.remove("active"),500);
        }
    });
    updateBookmarkStatus();
    localStorage.setItem("lastChapter",index);
};

// Navigasi tombol
document.getElementById("prevBtn").addEventListener("click",()=>{
    if(current>0){ current--; showChapter(current); }
});
document.getElementById("nextBtn").addEventListener("click",()=>{
    if(current<chapters.length-1){ current++; showChapter(current); }
});

// Lompat bab
function goChapter(index){ current=index; showChapter(current); }

// Mode Malam
const body=document.body;
document.getElementById("toggleDark").addEventListener("click",()=>body.classList.toggle("dark"));

// Bookmark
const bookmarkBtn=document.getElementById("bookmarkBtn");
const bookmarkStatus=document.getElementById("bookmarkStatus");
function updateBookmarkStatus(){
    const saved=localStorage.getItem("bookmark");
    bookmarkStatus.textContent=(saved==current)?"Bab ini di-bookmark ⭐":"Tidak ada bookmark";
}
bookmarkBtn.addEventListener("click",()=>{
    localStorage.setItem("bookmark",current);
    updateBookmarkStatus();
});

// Muat bab terakhir
window.addEventListener("load",()=>{
    const last=localStorage.getItem("lastChapter");
    if(last!==null){ current=parseInt(last); showChapter(current); }
});

// Feedback
const feedbackText=document.getElementById("feedbackText");
document.getElementById("sendFeedback").addEventListener("click",()=>{
    if(feedbackText.value.trim()!==""){
        alert("Terima kasih atas komentarmu!");
        feedbackText.value="";
    }else{
        alert("Tulis komentar terlebih dahulu!");
    }
});
</script>
</body>
</html>
