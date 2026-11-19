---
name: latihan-soal-sas-pai
description: >-
  Pembuat dan pengelola aplikasi web interaktif Latihan Soal Sumatif Akhir Semester (SAS / ASAS) PAI dan Budi Pekerti
  SD Negeri 3 Talok (Kelas 1 s.d. 6) dengan estetika Neo-Brutalist-Lite (Bold Color Blocking), timer hitungan mundur 90 menit,
  dukungan Pilihan Ganda Kompleks, validasi kelengkapan jawaban sebelum kunci jawaban terbuka, dan optimasi responsif mobile untuk GitHub Pages.
---

# Latihan Soal SAS 1 PAI - SD Negeri 3 Talok (Kelas 1 s.d. 6)

Panduan dan arsitektur pembuatan aplikasi web asesmen interaktif untuk Latihan Soal Asesmen Sumatif Akhir Semester (ASAS / SAS) 1 mata pelajaran Pendidikan Agama Islam dan Budi Pekerti SD Negeri 3 Talok, Kecamatan Turen, Kabupaten Malang.

---

## 1. Identitas & Lingkup Asesmen

- **Judul Aplikasi:** `Latihan Soal SAS 1 PAI - SD Negeri 3 Talok`
- **Satuan Pendidikan:** SD Negeri 3 Talok, Kec. Turen, Kab. Malang
- **Mata Pelajaran:** Pendidikan Agama Islam dan Budi Pekerti (Kurikulum Merdeka)
- **Fase / Kelas:**
  - **Fase A:** Kelas 1 (35 Butir) & Kelas 2 (35 Butir)
  - **Fase B:** Kelas 3 (40 Butir) & Kelas 4 (40 Butir)
  - **Fase C:** Kelas 5 (45 Butir) & Kelas 6 (45 Butir)
  - *Status Konten:* Seluruh kelas 1 sampai 6 **100% Aktif & Lengkap**.
- **Durasi Timer:** Hitungan mundur 90 menit (01:30:00) otomatis.
- **Komposisi Soal per Jenjang (Skor Maksimal 100):**
  - **Kelas 1 & 2 (35 Butir):** PG (20x2=40), Isian (5x3=15), Menjodohkan (5x3=15), Uraian (5x6=30).
  - **Kelas 3 & 4 (40 Butir):** PG (20x2=40), PG Kompleks (5x2=10), Isian (5x2=10), Menjodohkan (5x2=10), Uraian (5x6=30).
  - **Kelas 5 & 6 (45 Butir):** PG (25x2=50), PG Kompleks (5x2=10), Isian (5x2=10), Menjodohkan (5x2=10), Uraian (5x4=20).

---

## 2. Standar UI / Desain (Bold Neo-Brutalist-Lite)

Mengadopsi prinsip desain dari `bold-job-board-ui`:
- **Canvas / Background:** `#FBF9F5` (Warm Cream) dengan kontras tinggi.
- **Flat Solid Color Blocking per Jenjang:**
  - **Kelas 1:** `#4F46E5` (Brand Indigo) - teks putih kontras tinggi.
  - **Kelas 2:** `#EA580C` (Tangerine Amber) - teks putih kontras tinggi.
  - **Kelas 3:** `#0D9488` (Emerald Teal) - teks putih kontras tinggi.
  - **Kelas 4:** `#7C3AED` (Royal Violet) - teks putih kontras tinggi.
  - **Kelas 5:** `#E11D48` (Coral Rose) - teks putih kontras tinggi.
  - **Kelas 6:** `#18181B` (Near Black / Dark Slate) - teks putih & badge aksen lime `#D4F479`.
- **Kartu & Sudut:** `rounded-2xl` (16px–24px) dengan padding internal lega (16px–24px).
- **Tipografi:** Sans-serif geometris tegas (`font-extrabold` / `font-black`), huruf besar pada label status (`text-xs uppercase tracking-wider`).
- **Mobile-First & Touch Target:** Minimal 44px–48px untuk tombol opsi radio, checkbox multicentrang, dan dropdown agar ramah sentuhan layar ponsel.

---

## 3. Logika & Alur Pengguna (User Flow)

1. **Beranda / Pemilihan Kelas (Hub):**
   - Siswa disambut oleh header sekolah yang bersih dan gagah.
   - Kartu kelas 1 sampai 6 ditampilkan dalam grid responsif dengan palet warna khas masing-masing.
   - Seluruh Kelas 1 s.d. 6 berstatus **"Aktif / Mulai Latihan Sekarang"**.
2. **Halaman Asesmen & Identitas Siswa:**
   - Siswa mengisi formulir identitas (Nama Lengkap, Nomor Absen, Tanggal).
   - Timer 90 menit langsung aktif dan melayang (*sticky header*) dengan indikator visual.
3. **Mengerjakan Soal:**
   - Menjawab Pilihan Ganda (tombol opsi radio besar).
   - Menjawab Pilihan Ganda Kompleks (checkbox centang ganda dengan penskoran proporsional).
   - Mengisi Isian Singkat.
   - Menghubungkan Pasangan Menjodohkan dengan selector ramah mobile.
   - Menulis Uraian Panjang.
   - Terdapat **Progress Tracker** yang menampilkan jumlah soal yang sudah diisi secara riil (misal: `38 / 40 Terjawab`).
4. **Validasi Kelengkapan Jawaban:**
   - Tombol *"Kumpulkan & Buka Kunci Jawaban"* memeriksa apakah seluruh butir telah diisi.
   - **Jika belum lengkap:** Muncul modal peringatan yang mencantumkan nomor soal yang belum terisi sehingga siswa tidak melewatkan soal.
   - **Jika sudah lengkap:** Ujian selesai, timer dihentikan, dan sistem membuka halaman Pembahasan & Kunci Jawaban.
5. **Kunci Jawaban & Evaluasi Nilai:**
   - Rekapitulasi perolehan skor otomatis (Pilihan Ganda + PG Kompleks + Menjodohkan + Isian).
   - Tampilan kunci jawaban resmi dan rubrik penskoran untuk uraian.
   - Komparasi jawaban siswa vs kunci yang benar dengan status warna hijau/merah.

---

## 4. Distribusi & Deployment ke GitHub Pages

- Dibuat menjadi satu bundle berkas statis `index.html` (*zero-dependency* / *self-contained* dengan font Google & Tailwind CSS CDN) agar langsung dapat di-host gratis melalui GitHub Pages tanpa build-step.
- Kompatibel dengan semua browser modern di PC, tablet, maupun smartphone Android / iOS.
- Mendukung direct deep-link (contoh: `index.html#kelas1`, `index.html#kelas2`, `index.html#kelas3`, `index.html#kelas4`, `index.html#kelas5`, `index.html#kelas6`).
