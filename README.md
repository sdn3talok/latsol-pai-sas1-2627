# Latihan Soal SAS 1 PAI - SD Negeri 3 Talok (Kelas 1 s.d. 6)

Aplikasi web interaktif latihan soal Asesmen Sumatif Akhir Semester (SAS / ASAS) Ganjil mata pelajaran **Pendidikan Agama Islam dan Budi Pekerti (Kurikulum Merdeka)** untuk **SD Negeri 3 Talok**, Kecamatan Turen, Kabupaten Malang, Tahun Pelajaran 2026/2027.

Lengkap mencakup **seluruh jenjang kelas (Kelas 1, 2, 3, 4, 5, dan 6)** dengan pendekatan desain **Neo-Brutalist-Lite / Bold Color Blocking** (terinspirasi dari *bold-job-board-ui*), memadukan tipografi geometris tebal, palet warna solid khusus per kelas, timer hitungan mundur 90 menit otomatis, validasi kelengkapan jawaban, serta pembahasan kunci jawaban dan penskoran resmi.

---

## 🎨 Identitas Warna & Cakupan Tiap Jenjang Kelas

| Jenjang | Fase | Identitas Warna | Hex Token | Jumlah Butir | Status Konten |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Kelas 1** | Fase A | Brand Indigo | `#4F46E5` | **35 Butir** | ✅ **Aktif 100%** |
| **Kelas 2** | Fase A | Tangerine Amber | `#EA580C` | **35 Butir** | ✅ **Aktif 100%** |
| **Kelas 3** | Fase B | Emerald Teal | `#0D9488` | **40 Butir** | ✅ **Aktif 100%** |
| **Kelas 4** | Fase B | Royal Violet | `#7C3AED` | **40 Butir** | ✅ **Aktif 100%** |
| **Kelas 5** | Fase C | Coral Rose | `#E11D48` | **45 Butir** | ✅ **Aktif 100%** |
| **Kelas 6** | Fase C | Deep Slate / Lime | `#18181B` | **45 Butir** | ✅ **Aktif 100%** |

---

## 🚀 Fitur Unggulan

1. **Struktur Soal Lengkap Standar ASAS Kurikulum Merdeka (Skor Maksimal 100):**
   - **Kelas 1 & 2 (35 Butir):**
     - Pilihan Ganda (20 butir @ 2 poin = 40)
     - Isian Singkat (5 butir @ 3 poin = 15)
     - Menjodohkan (5 butir @ 3 poin = 15)
     - Uraian Panjang (5 butir @ 6 poin = 30)
   - **Kelas 3 & 4 (40 Butir):**
     - Pilihan Ganda (20 butir @ 2 poin = 40)
     - Pilihan Ganda Kompleks / Multicentrang (5 butir @ 2 poin = 10)
     - Isian Singkat (5 butir @ 2 poin = 10)
     - Menjodohkan (5 butir @ 2 poin = 10)
     - Uraian Panjang (5 butir @ 6 poin = 30)
   - **Kelas 5 & 6 (45 Butir):**
     - Pilihan Ganda (25 butir @ 2 poin = 50)
     - Pilihan Ganda Kompleks / Multicentrang (5 butir @ 2 poin = 10)
     - Isian / Uraian Singkat (5 butir @ 2 poin = 10)
     - Menjodohkan (5 butir @ 2 poin = 10)
     - Uraian Panjang (5 butir @ 4 poin = 20)

2. **Dukungan Soal Pilihan Ganda Kompleks:**
   - Input ramah sentuhan dengan kotak centang (*checkboxes*) untuk memilih lebih dari satu jawaban yang benar.
   - Penskoran otomatis sesuai standar asesmen nasional:
     - Skor 2: Jawaban benar penuh tanpa ada pilihan salah.
     - Skor 1: Jawaban benar sebagian tanpa ada pilihan salah.
     - Skor 0: Memilih opsi yang keliru atau tidak menjawab.

3. **Timer Hitungan Mundur 90 Menit:**
   - Melayang (*sticky*) di bagian atas layar PC & ponsel.
   - Peringatan visual warna kuning (10 menit tersisa) dan merah berkedip (5 menit tersisa).
   - Pengumpulan otomatis jika waktu habis (00:00).

4. **Validasi Kunci Jawaban (Iron Rule):**
   - Kunci jawaban dan nilai terkunci sebelum seluruh butir soal diisi oleh siswa.
   - Jika terdapat soal yang terlewat, muncul pop-up peringatan disertai nomor soal yang belum terisi yang dapat diklik langsung untuk menuju soal tersebut.

5. **Mobile First & Responsif:**
   - Target sentuhan minimal 48px, ramah diakses dari layar smartphone Android / iPhone.
   - Teks Arab menggunakan font *Amiri* berharakat tajwid yang jelas.

6. **Siap Cetak / Unduh PDF:**
   - Tombol cetak hasil pengerjaan rapi untuk arsip asesmen guru atau orang tua siswa.

7. **Zero Dependencies & GitHub Pages Ready:**
   - Seluruh logika dan data terintegrasi ke dalam `index.html` tunggal, langsung bekerja saat dibuka secara lokal maupun di-host gratis di GitHub Pages.

---

## 📦 Cara Deploy / Update ke GitHub Pages

Jalankan perintah berikut di PowerShell untuk mengunggah pembaruan:

```powershell
# 1. Tambahkan semua berkas baru
git add .

# 2. Buat commit pembaruan
git commit -m "feat: integrasi lengkap latihan soal SAS 1 PAI SDN 3 Talok (Kelas 1 s.d. 6)"

# 3. Dorong ke GitHub
git push origin main
```

Situs web Anda di GitHub Pages (`https://<username>.github.io/<repo>/`) akan otomatis terupdate dalam 1–2 menit!
