# Game Kartu Ulang Tahun Interaktif 🌸

Game mencocokkan kartu (Memory Match) berbasis web satu halaman (*single-page web application*) yang interaktif, elegan, dan penuh kejutan. Dibuat khusus sebagai kado ucapan ulang tahun digital.

Halaman ini sangat responsif (*mobile-friendly*) dan dirancang dengan estetika pastel yang hangat, serta dilengkapi alur interaktif mulai dari permainan kartu, animasi pembukaan kado, hingga ucapan selamat ulang tahun yang terintegrasi dengan WhatsApp.

---

## ✨ Fitur Utama

1. **Tema Pastel & Estetika Feminin**:
   - Palet warna lembut kombinasi Soft Pink, Rose Gold, dan Sage Green pastel.
   - Hiasan latar belakang melayang (*floating hearts & sparkles*) yang dianimasikan secara halus dengan CSS.
   - Desain layout *mobile-first* yang optimal untuk dibuka di layar ponsel cerdas.

2. **Permainan Memory Match (Tebak Kartu)**:
   - Permainan membalikkan 8 kartu (4 pasang emoji bermakna: 🎂, 💖, 💵, 🌟).
   - Pengacakan kartu secara dinamis (*Fisher-Yates shuffle*) pada awal permainan.
   - Animasi putaran 3D kartu yang mulus dan bebas glitch pada peramban mobile (iOS WebKit & Android Chrome).
   - Sistem pengaman ketukan (*anti-double-click*) selama kartu sedang melakukan proses putar balik jika terjadi ketidakcocokan.

3. **Kejutan Kotak Kado Interaktif**:
   - Setelah semua kartu cocok, akan muncul animasi kotak kado 3D berpita emas yang bergetar.
   - Terdapat efek tutup kado terlempar (*lid fly-off*) dan badan kado melebur memudar saat diketuk oleh pengguna.

4. **Synthesizer Melodi "Happy Birthday" (Web Audio API)**:
   - Menghasilkan audio melodi instrumen kotak musik (*music box*) yang berdentang jernih menggunakan sinyal osilator bawaan browser.
   - Tanpa ketergantungan berkas MP3 eksternal (100% luring/offline).
   - Dilengkapi efek gema (*Delay & Feedback*) untuk suasana magis.
   - Tombol kontrol suara (*Mute/Unmute*) di bar navigasi atas.
   - Efek suara (*Sound FX*) saat membalik kartu, kartu cocok, dan kartu tidak cocok.

5. **Efek Konfeti Canvas**:
   - Animasi taburan konfeti warna-warni yang meriah yang dirender secara halus pada canvas HTML5 60 FPS.

6. **Integrasi WhatsApp**:
   - Tombol interaktif *"Kirim Pesan ke Jaki Ganteng"* yang langsung menghubungkan pengguna ke WhatsApp dengan format pesan terima kasih otomatis yang sudah terkonfigurasi.

---

## 🛠️ Teknologi yang Digunakan

- **Struktur & Elemen**: HTML5
- **Tampilan & Animasi**: CSS3 (Vanilla CSS, 3D Transforms, Keyframe Animations)
- **Logika & Audio**: JavaScript ES6+ (Web Audio API, HTML5 Canvas API, Web Speech/Audio Context Handler)

---

## 🚀 Cara Menjalankan Project

### 1. Cara Paling Mudah (Tanpa Instalasi)
- Cukup unduh berkas repository ini.
- Klik ganda (double-click) pada berkas `index.html` untuk membukanya secara langsung di browser Anda (Google Chrome, Safari, Microsoft Edge, dll.).

### 2. Menggunakan Local Web Server (Direkomendasikan)
Untuk mendapatkan pengalaman memuat halaman layaknya website publik:

#### Menggunakan Python:
Jalankan perintah berikut pada terminal di dalam folder project:
```bash
python -m http.server 8000
```
Buka peramban Anda dan akses: `http://localhost:8000`

#### Menggunakan Node.js/Npx:
Jalankan perintah berikut pada terminal:
```bash
npx serve
```
Buka peramban sesuai port lokal yang ditampilkan di terminal Anda.

---

## ⚙️ Cara Mengubah Kustomisasi Nomor WhatsApp

Apabila Anda ingin menyesuaikan nomor telepon tujuan atau pesan otomatisnya, Anda dapat mengedit berkas `index.html`:

1. Buka berkas `index.html` dengan teks editor pilihan Anda (VS Code, Notepad, dll.).
2. Cari elemen tautan dengan `id="btn-whatsapp"` (sekitar baris 825):
   ```html
    <a href="https://api.whatsapp.com/send?phone=6282117943618&text=Terima%20kasih%20banyak%20atas%20ucapannya!%20%E2%9D%A4%EF%B8%8F" 
       target="_blank" 
       class="btn-whatsapp" 
       id="btn-whatsapp">
   ```
3. Ganti nilai parameter `phone=6282117943618` dengan nomor WhatsApp Anda dalam format kode negara tanpa spasi/tanda tambah (contoh format Indonesia: `628xxxxxxxxxx`).
4. Ganti nilai parameter `text=...` dengan teks balasan otomatis yang Anda inginkan (gunakan format *URL Encode* untuk spasi atau karakter khusus jika diperlukan).
