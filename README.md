# NURPATH v2.0.26

**Engineering Your Taqwa.**

NURPATH adalah sebuah antarmuka web modern yang dirancang untuk memberikan inspirasi dan motivasi spiritual. Proyek ini bertujuan menyebarkan pesan kebaikan melalui integrasi teknologi AI canggih untuk mengoptimalkan penyampaian pesan secara presisi.

![NURPATH Interface] (d:\download\screencapture-127-0-0-1-5500-index-html-2026-02-21-20_51_52.png) 


## 🚀 Tentang Proyek

Aplikasi ini merupakan sebuah "single-page interface" yang memungkinkan pengguna untuk menghasilkan kutipan inspiratif (AI Insight) dengan satu klik. Tema utamanya adalah "Persaudaraan di Bulan Ramadhan", dan output yang dihasilkan oleh AI dirancang agar singkat, persuasif, dan relevan dengan konteks tersebut.

Desainnya futuristik, menggunakan tema gelap (dark mode) dengan aksen gradien dan efek visual modern untuk menciptakan pengalaman pengguna yang imersif.

## ✨ Fitur Utama

- **AI Insight Generator**: Menghasilkan kutipan motivasi menggunakan model AI `gemini-2.0-flash`.
- **Streaming Text**: Output dari AI ditampilkan secara *real-time* (streaming) kata per kata, memberikan efek seperti sedang diketik langsung oleh AI.
- **Desain Modern**: Antarmuka yang bersih dan futuristik dengan efek *glassmorphism*, gradien, dan animasi halus.
- **Prompt Engineering**: Menggunakan prompt yang sangat spesifik untuk memastikan output AI sesuai dengan yang diinginkan (singkat, padat, dan tanpa artefak yang tidak perlu).
- **Zero-Setup**: Tidak memerlukan instalasi atau build step. Cukup buka file `index.html` di browser.

## 🛠️ Teknologi yang Digunakan

- **Frontend**: HTML5
- **Styling**: [Tailwind CSS](https://tailwindcss.com/) (via CDN)
- **AI Integration**: [Puter.js](https://puter.com/) (v2)
- **AI Model**: `gemini-2.0-flash`
- **Fonts**: [Google Fonts](https://fonts.google.com/) (Plus Jakarta Sans & JetBrains Mono)

## ⚙️ Cara Kerja

1.  Pengguna menekan tombol **"Execute AI Insight"**.
2.  Fungsi `streamAI()` di dalam JavaScript akan dipicu.
3.  Sebuah *prompt* yang sudah dirancang secara spesifik dikirim ke `puter.ai.chat`.
    ```javascript
    const prompt = "Tuliskan satu kalimat persuasif tentang keakraban persaudaraan di bulan Ramadhan. Maksimal 15 kata. Tanpa salam, tanpa intro, tanpa markdown, hanya teks polos.";
    ```
4.  API dari Puter.js mengembalikan respons dalam bentuk *stream*.
5.  JavaScript melakukan iterasi pada setiap bagian dari *stream* tersebut, menggabungkan teks, dan secara dinamis memperbarui tampilan di `div#ai-output`.
6.  Setelah selesai, kursor animasi akan hilang dan tombol kembali aktif.

## 🚀 Cara Menjalankan

Tidak ada proses instalasi yang rumit. Cukup ikuti langkah ini:

1.  Pastikan Anda memiliki koneksi internet (untuk memuat CDN Tailwind dan Puter.js).
2.  Buka file `index.html` langsung di browser 
Selesai! Aplikasi siap digunakan.
