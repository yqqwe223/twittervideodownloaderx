# 🐦 Alat Analisis Video X.com

> Alat yang ringan, cepat, dan serbaguna untuk mengekstrak konten video dari X (sebelumnya Twitter)

[🌐 Demo Online](https://twittervideodownloaderx.com/in) • [📝 Panduan Penggunaan](#-panduan-penggunaan) • [❓ Pertanyaan Umum](#-pertanyaan-umum)

---

## 📋 Gambaran Proyek

Proyek ini adalah alat analisis video berbasis web yang dirancang untuk mengekstrak sumber daya video dari publikasi publik di X.com (sebelumnya Twitter) dengan aman, serta menyediakan opsi konversi dan unduhan dalam berbagai format. Tidak memerlukan instalasi perangkat lunak klien atau pendaftaran akun: gunakan langsung melalui browser Anda.

> ⚠️ **Peringatan Penting**: Alat ini dirancang khusus untuk tujuan pembelajaran pribadi, penelitian teknis, dan penggunaan dalam batas yang wajar. Harap patuhi [Perjanjian Pengembang Platform X](https://developer.twitter.com/en/developer-terms/agreement) serta hukum hak cipta yang berlaku di negara Anda. Dilarang keras menggunakan alat ini untuk tujuan yang melanggar hak pihak ketiga.

---

## ✨ Fitur Utama

- 🔗 **Analisis Tautan**: Mendukung URL publikasi X.com standar; deteksi otomatis video dan GIF animasi
- 📥 **Ekspor Multi-Format**:
  - Video MP4 dengan kualitas asli
  - Ekstraksi audio → Format MP3
  - Klip video → Konversi ke GIF animasi
- 🌍 **Antarmuka Multibahasa**: Dukungan untuk bahasa Indonesia, Inggris, Mandarin, Jepang, Korea, dan total 16 bahasa
- 📱 **Kompatibilitas Lintas Platform**: Berfungsi sempurna di Chrome / Firefox / Safari / Edge; pengalaman optimal untuk perangkat seluler dan tablet
- 🔒 **Privitas Diutamakan**: Tidak perlu pendaftaran akun, tidak mengumpulkan data pribadi; proses analisis sepenuhnya anonim
- ⚡ **Pemrosesan Cepat**: Analisis selesai rata-rata dalam waktu kurang dari 5 detik; dukungan untuk permintaan simultan

---

## 🚀 Memulai dengan Cepat

### Penggunaan Online (direkomendasikan)
1. Kunjungi [https://twittervideodownloaderx.com/in](https://twittervideodownloaderx.com/in)
2. Salin tautan publikasi target (contoh: `https://x.com/user/status/123456789`)
3. Tempel tautan ke kolom input → Klik tombol 「Analisis」
4. Pilih format yang diinginkan → Simpan file mengikuti petunjuk browser

### Penyebaran Lokal (untuk pengembang)
```bash
# Clone repositori
git clone https://github.com/your-repo/x-video-parser.git

# Instal dependensi
cd x-video-parser && npm install

# Konfigurasi variabel lingkungan (opsional)
cp .env.example .env

# Jalankan server pengembangan
npm run dev
```

> 💡 Catatan: Proyek ini menggunakan arsitektur berbasis Node.js + Express. Silakan lihat dokumentasi penyebaran lengkap di `/docs/DEPLOY.md`

---

## 🛠 Tumpukan Teknologi

| Modul | Teknologi yang Digunakan |
|-------|--------------------------|
| Frontend | Vue 3 + TypeScript + Vite |
| Backend | Node.js + Express + Axios |
| Pemrosesan Video | ffmpeg.wasm (konversi ringan di sisi klien) |
| Proxy Penerusan | Cloudflare Workers / Middleware Kustom |
| Internasionalisasi | vue-i18n + Paket Bahasa JSON |

---

## 📚 Panduan Penggunaan

### Alur Kerja Dasar
```
1. Dapatkan tautan publikasi
   └─ Buka publikasi target di X.com → Salin URL dari bilah alamat browser

2. Kirim permintaan analisis
   └─ Tempel tautan ke kolom input alat → Klik 「Unduh Video」

3. Pilih format output
   ├─ 🎬 Unduh sebagai MP4: Simpan dengan kualitas asli
   ├─ 🎵 Konversi ke MP3: Ekstrak trek audio
   └─ 🎞 Konversi ke GIF: Buat animasi pendek (direkomendasikan: ≤15 detik)

4. Simpan file
   └─ Sumber daya akan terbuka di tab baru → Klik kanan/menu → 「Simpan sebagai」
```

### Tips Penggunaan di Perangkat Seluler
- iOS Safari: Tombol Bagikan → 「Simpan ke File」
- Android Chrome: Tekan lama pada video → 「Unduh video」
- Jika video diputar otomatis: Klik `⋮` di sudut kanan atas pemutar → Pilih 「Unduh」

---

## ❓ Pertanyaan Umum

**T: Di mana file yang diunduh disimpan?**  
J: File disimpan di folder unduhan yang dikonfigurasi di browser Anda. Anda dapat memeriksa atau mengubah jalur ini di pengaturan browser.

**T: Bisakah saya menganalisis akun pribadi atau konten yang dibatasi?**  
J: Tidak. Alat ini hanya berfungsi dengan publikasi yang diatur sebagai publik dan menghormati pengaturan akses konten asli.

**T: Apakah kualitas gambar/audio berkurang setelah konversi?**  
J: Format MP4 mempertahankan kualitas asli. Format MP3 menggunakan pengodean standar 128 kbps. Format GIF mengoptimalkan frame rate sesuai durasi untuk menyeimbangkan ukuran file dan kelancaran.

**T: Apakah riwayat unduhan atau cache disimpan?**  
J: Tidak. Semua sumber daya ditransmisikan langsung ke perangkat pengguna melalui proxy sementara; server tidak menyimpan permintaan atau file media apa pun.

**T: Apa yang harus dilakukan jika analisis gagal?**  
J: Harap periksa: ① Apakah tautan mengarah ke publikasi publik yang valid ② Apakah koneksi internet Anda stabil ② Coba gunakan browser lain. Jika masalah berlanjut, jangan ragu untuk melaporkannya melalui Issue.

---

## ⚖️ Kepatuhan Regulasi dan Penyangkalan Tanggung Jawab

- Alat ini **tidak melewati atau melanggar langkah perlindungan teknis apa pun** dari platform; alat ini hanya memperoleh metadata melalui antarmuka publik
- Pengguna bertanggung jawab untuk memverifikasi bahwa penggunaan mereka sesuai dengan hukum setempat dan ketentuan layanan platform
- Skenario penggunaan yang direkomendasikan: Pengarsipan pribadi, demonstrasi edukasional, materi referensi untuk pembuatan konten... selalu dalam kerangka penggunaan wajar (Fair Use)
- Jika Anda menemukan konten yang diduga melanggar hak, silakan hubungi saluran resmi [X melalui formulir pelaporan hak cipta ini](https://help.twitter.com/forms/dmca)

---

## 🤝 Panduan Berkontribusi

Kami menyambut Pull Request dan laporan Issue Anda! Sebelum berkontribusi, silakan baca:
- [Standar Kode](/CONTRIBUTING.md)
- [Panduan Terjemahan Multibahasa](/locales/README.md)
- [Persyaratan Keamanan dan Kepatuhan](/SECURITY.md)

---

## 📄 Lisensi

Proyek ini diterbitkan di bawah [Lisensi MIT](/LICENSE). Dapat digunakan secara gratis untuk tujuan pendidikan dan penelitian. Untuk penggunaan komersial, harap periksa dengan cermat kepatuhan terhadap regulasi hukum yang berlaku.

---

> 🌟 Jika alat ini bermanfaat bagi Anda, jangan ragu untuk ✨memberikan Bintang (Star)! Dukungan Anda adalah motivasi terbesar bagi kami untuk terus memelihara dan meningkatkan proyek ini~

*Pembaruan terakhir: Mei 2026 | Versi: v2.1.0*