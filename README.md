# Portofolio Ari Julianto

Situs portofolio statis (HTML, CSS, JavaScript). Tidak perlu instalasi atau build.

## Struktur folder

```
portofolio-ari/
├── index.html        Halaman utama (Home, About, Portfolio, Contact)
├── css/
│   └── style.css     Semua gaya tampilan
├── js/
│   └── main.js       Animasi intro, kartu ID, partikel, tab, formulir
├── assets/
│   ├── img/          Taruh foto profil dan screenshot proyek di sini
│   └── docs/         Taruh CV (PDF) di sini
└── README.md
```

## Menjalankan di komputer

Buka `index.html` di browser. Atau dengan server lokal:

```
python3 -m http.server 8000
```

lalu buka http://localhost:8000

## Mengunggah (hosting gratis)

- **GitHub Pages:** unggah folder ke repositori, lalu Settings > Pages > pilih branch `main` dan folder `/ (root)`.
- **Netlify:** buka app.netlify.com/drop, lalu seret folder `portofolio-ari`.

## Yang perlu kamu ganti

- Foto profil: ganti siluet di kartu ID dan avatar (bagian About) di `index.html` dengan `<img src="assets/img/foto.jpg" alt="Foto Ari Julianto">`.
- CV: simpan di `assets/docs/CV-Ari-Julianto.pdf`, lalu ubah tombol "Minta CV" di `index.html` menjadi `<a href="assets/docs/CV-Ari-Julianto.pdf" download>`.
- Proyek: edit array `P` di bagian atas `js/main.js` (nama, deskripsi, fitur, teknologi, tautan).
- Teks kutipan dan deskripsi About: edit langsung di `index.html`.

## Catatan perbaikan

- Situs tetap bisa dibaca saat JavaScript mati (sebelumnya layar intro menutup semua halaman).
- Judul tab browser berubah sesuai halaman; fokus keyboard pindah ke konten saat pindah halaman.
- Tab Portfolio mengikuti pola WAI-ARIA dan bisa dipakai dengan tombol panah.
- Tautan "Kunjungi situs" disederhanakan (tanpa skrip popup).
- Label ikon Tech Stack diperbaiki (JS, CI, SQL, dan seterusnya).
- Statistik sertifikat disamakan dengan jumlah kartu (2). Ubah angkanya di `index.html` setelah menambah sertifikat.
- Ditambah favicon, meta tema, Open Graph, preconnect font, dan tautan "Lewati ke konten".
- Tabel tab lebih rapi di layar kecil.

- Judul diganti menjadi IT Developer; skill ditambah Node.js, Vite, dan PostgreSQL.
- Bagian "Dari desain ke kode" memakai wireframe dan desain akhir Figma (`wf-*.jpg` dan `fin-*.jpg`).
- Home menampilkan kartu proyek yang membuka detailnya di halaman Portfolio.
- CV (`assets/docs/CV-Ari-Julianto.pdf`) dan dua sertifikat (`assets/docs/`) sudah terpasang; tombol "Unduh CV" menggantikan "Minta CV".
- Data proyek disesuaikan dengan CV (SIPADU: CodeIgniter, MySQL, Figma; SigerPro: panel admin dan Black Box Testing).
- Kartu ID tidak lagi digeser: titik tali tetap di atas dan kartu berayun seperti bandul pegas ke kiri, kanan, atas, bawah, dan diagonal, lalu melambat sendiri. Berfungsi dengan mouse dan sentuhan.
- Bagian Contact > Terhubung: tiap tautan (Email, LinkedIn, GitHub, Unduh CV) kini menampilkan alamat lengkap dan tanda panah, dan dibuka di tab baru dengan `rel="noopener noreferrer"`.
- Perbaikan bug: variabel `ty` bentrok antara animasi ketik dan kartu ID sehingga teks ketik di Home berhenti setelah satu huruf.
- Tab Tech Stack memakai logo teknologi (HTML, CSS, JavaScript, Node.js, Vite, PHP, CodeIgniter, MySQL, PostgreSQL, Figma) berupa SVG inline dari Simple Icons, tanpa file gambar tambahan. Untuk menambah teknologi baru, tambahkan namanya di array `S` dan path logonya di objek `LG` pada `js/main.js`.
- Tampilan mobile dirapikan (layar sampai 320px, tanpa geser horizontal): header menempel di atas dengan menu pil yang mudah disentuh, kartu ID lebih kecil sehingga judul langsung terlihat, daftar proyek berupa baris geser dengan detail di bawahnya, tab Portfolio selebar layar, Tech Stack 3 kolom, foto About di atas teks, input 16px agar iOS tidak zoom saat diketuk, tombol minimal 44px, dan efek hover dimatikan di layar sentuh. Semua aturannya ada di bagian bawah `css/style.css` (blok "Perbaikan tampilan mobile").
