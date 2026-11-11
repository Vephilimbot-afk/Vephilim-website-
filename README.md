# VEPHILIM RP Website

Website statis SPA (hash routing), HTML + CSS + JavaScript vanilla.

## Menjalankan di Termux
1. Ekstrak folder.
2. Masuk ke folder proyek: `cd VEPHILIM-WEBSITE`
3. Jalankan server lokal sederhana: `python -m http.server 8080`
4. Buka `http://127.0.0.1:8080` di browser.

Bisa juga memakai ekstensi/utility server lokal lain. Membuka `index.html` langsung dapat membatasi fetch API tertentu.

## Deploy
- GitHub Pages: unggah seluruh isi folder ke repository, aktifkan Pages dari branch utama.
- Netlify: drag-and-drop folder proyek atau hubungkan repository.

## Yang perlu diedit
Semua konten utama ada di `assets/js/data.js`:
- `staff`: nama, jabatan, avatar, deskripsi.
- `patrons` dan `donationGoal`: data donatur dan target donasi.
- `portfolio`: galeri, URL gambar, deskripsi, kategori, tag.
- `timeline`, `pantheon`, `factions`, `races`, `locations`: lore dunia.
- `rules`: peraturan gameplay dan Discord.
- `faq`, `updates`, `event`, `stats`: informasi halaman.

Ganti gambar hero di `assets/css/style.css` pada `.hero-bg` dan `.page-hero`.
Taruh musik milik sendiri di `assets/audio/ambient.mp3` dan efek klik opsional di `assets/audio/click.mp3`. Musik default mati dan hanya berjalan setelah interaksi pengguna.

## Catatan penting
- IP: `vephilim.com`.
- Discord: `https://discord.gg/4dcCWdBt5`.
- Pembelian rank dan donasi hanya melalui ticket Discord. Tidak ada checkout atau pengumpulan data pembayaran di website.
- Status server memakai API publik mcsrvstat.us dan memiliki fallback.
- Angka statistik, nama staf, donatur, tanggal event, dan konten lore awal adalah placeholder/contoh. Periksa dan ganti sebelum website dipublikasikan.
- Animasi GSAP dan tsParticles memakai CDN. Jika CDN tidak tersedia, konten utama tetap bisa digunakan.
- Gunakan gambar dan audio yang kamu miliki hak penggunaannya. Optimalkan gambar menjadi WebP/AVIF agar ringan di perangkat menengah.
- Fitur cursor khusus otomatis tidak aktif pada perangkat sentuh. prefers-reduced-motion dihormati.
