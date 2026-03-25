<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Novelku Estetik</title>
  <style>
    body {
      font-family: 'Merriweather', serif;
      background-color: #fdf6e3;
      color: #333;
      line-height: 1.8;
      max-width: 800px;
      margin: 50px auto;
      padding: 20px 40px;
      box-shadow: 0 0 20px rgba(0,0,0,0.1);
      border-radius: 10px;
      scroll-behavior: smooth;
    }
    h1 {
      text-align: center;
      color: #b22222;
      margin-bottom: 10px;
    }
    h2 {
      color: #8b0000;
      margin-top: 40px;
      margin-bottom: 15px;
    }
    p {
      margin-bottom: 20px;
    }
    nav {
      text-align: center;
      margin: 30px 0;
    }
    nav button {
      background-color: #b22222;
      color: #fff;
      border: none;
      padding: 10px 20px;
      margin: 0 10px;
      border-radius: 5px;
      cursor: pointer;
      font-weight: bold;
      transition: 0.3s;
    }
    nav button:hover {
      background-color: #8b0000;
    }
    footer {
      text-align: center;
      margin-top: 50px;
      font-size: 0.9em;
      color: #666;
    }
  </style>
</head>
<body>

  <h1>Judul Novelku</h1>

  <nav>
    <button onclick="goTo('bab1')">Bab 1</button>
    <button onclick="goTo('bab2')">Bab 2</button>
    <button onclick="goTo('bab3')">Bab 3</button>
  </nav>

  <h2 id="bab1">Bab 1: Awal Petualangan</h2>
  <p>Ini adalah bab pertama novelnya. Kamu bisa ganti teks ini dengan ceritamu sendiri! Ceritanya bisa panjang dan berisi dialog, deskripsi, atau apa pun yang kamu inginkan.</p>

  <h2 id="bab2">Bab 2: Misteri Terungkap</h2>
  <p>Ini adalah bab kedua. Terus tambahkan bab berikutnya sesuai kreativitasmu. Bisa ada konflik, kejutan, atau twist cerita supaya pembaca penasaran.</p>

  <h2 id="bab3">Bab 3: Kejutan di Akhir</h2>
  <p>Bab ketiga bisa menjadi klimaks atau penutup sementara. Kamu bisa terus menambahkan bab baru dengan menyalin struktur <code>&lt;h2&gt;</code> dan <code>&lt;p&gt;</code> ini.</p>

  <nav>
    <button onclick="prev()">Previous Bab</button>
    <button onclick="next()">Next Bab</button>
  </nav>

  <footer>
    &copy; 2026 Novelku Estetik. Semua hak cipta dilindungi.
  </footer>

  <script>
    const babs = ['bab1', 'bab2', 'bab3'];
    let current = 0;

    function goTo(id) {
      document.getElementById(id).scrollIntoView({behavior: 'smooth'});
      current = babs.indexOf(id);
    }

    function next() {
      current = (current + 1) % babs.length;
      goTo(babs[current] || babs[current]);
    }

    function prev() {
      current = (current - 1 + babs.length) % babs.length;
      goTo(babs[current] || babs[current]);
    }
  </script>
</body>
</html>
