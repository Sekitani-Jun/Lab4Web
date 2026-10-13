# LAPORAN PRAKTIKUM 4: CSS LAYOUT

**Mata Kuliah:** Pemrograman Web  
**Dosen Pengampu:** Agung Nugroho, M.Kom  
**Program Studi:** Teknik Informatika  
**Fakultas:** Teknik  
**Universitas:** Universitas Pelita Bangsa  

---

## DAFTAR ISI
1. [Identitas Mahasiswa](#identitas-mahasiswa)
2. [Tujuan Praktikum](#tujuan-praktikum)
3. [Dasar Teori](#dasar-teori)
4. [Langkah-Langkah Praktikum](#langkah-langkah-praktikum)
5. [Jawaban Pertanyaan dan Tugas](#jawaban-pertanyaan-dan-tugas)
6. [Halaman Tambahan: Menu Artikel](#halaman-tambahan-menu-artikel)
7. [Struktur Direktori Proyek](#struktur-direktori-proyek)
8. [Kesimpulan](#kesimpulan)

---

## Identitas Mahasiswa

| Keterangan | Data Mahasiswa |
| :--- | :--- |
| **Nama Lengkap** | **Jumari** |
| **NIM** | **312510077** |
| **Kelas** | Teknik Informatika |
| **Mata Kuliah** | Pemrograman Web |
| **Dosen Pengampu** | Agung Nugroho, M.Kom |
| **Instansi** | Universitas Pelita Bangsa |

---

## Tujuan Praktikum
1. Mahasiswa mampu memahami struktur dasar pembuatan Web Layout.
2. Mahasiswa mampu memahami konsep Box Element (Box Model) pada CSS.
3. Mahasiswa mampu memahami cara kerja dan implementasi CSS Floating.
4. Mahasiswa mampu memahami dan menerapkan elemen semantik HTML5 (*HTML5 Semantics Elements*).
5. Mahasiswa mampu membuat Layout Web Sederhana yang rapi, fungsional, dan terstruktur.

---

## Dasar Teori

### 1. Web Layout
Web layout merupakan kerangka acuan yang mengatur penempatan serta tata letak elemen pada halaman web, seperti navigasi, header, hero banner, main content, sidebar, dan footer. 

### 2. Box Element (CSS Box Model)
Semua elemen dalam HTML pada dasarnya diperlakukan sebagai sebuah kotak (*box*). CSS Box Model tersusun atas: **Content**, **Padding**, **Border**, dan **Margin**.

### 3. CSS Float Property
Properti CSS `float` digunakan untuk menggeser elemen ke sisi kiri (`left`) atau kanan (`right`), sehingga elemen di sekitarnya dapat mengalir di sampingnya.

### 4. Clearfix Element
Untuk mengatasi kehilangan tinggi asli (*height collapse*) pada elemen induk saat menggunakan float, digunakan properti `clear` (seperti `clear: both;`) atau teknik pseudo-element `::after`.

### 5. HTML5 Semantics Elements
HTML5 memperkenalkan elemen semantik seperti `<header>`, `<nav>`, `<section>`, `<article>`, `<aside>`, dan `<footer>` yang memberikan makna struktural.

---

## Langkah-Langkah Praktikum

### 1. Box Element Dasar Tanpa Float
Menampilkan elemen `<div>` bertipe *block-level* yang tersusun secara vertikal dari atas ke bawah.
**Screenshot Hasil:**  
![Box Element Tanpa Float](box%20elemen%20tanpa%20float.png)

### 2. Penerapan CSS Float Property
Menambahkan properti `float: left;` sehingga elemen mengambang dan berjajar ke samping kiri.
**Screenshot Hasil:**  
![Box Element Dengan Float](box%20elemen%20pakai%20float.png)

### 3. Penerapan Clearfix pada Div 4
Menggunakan `clear: left;` pada elemen keempat agar turun ke baris baru di bawah elemen float.
**Screenshot Hasil:**  
![Box Element Clearfix Div 4](box%20elemen%20clearfix.png)

### 4. Eksperimen Properti Clear (left, right, both)
Eksperimen terhadap penggunaan nilai properti `clear: left;`, `clear: right;`, dan `clear: both;` (termasuk variasi dengan posisi di tengah/bawah).
**Screenshot Hasil:**  
![Box Element Eksperimen](box%20elemen%20eksperimen%20(left,%20right,%20both,%20center).png)

### 5. Membuat Layout Web Sederhana
Menyusun kerangka semantik HTML5 di dalam kontainer `#container`.
**Screenshot Hasil Kerangka:**  
![Layout Kerangka](kerangka%20layout%20sederhana.png)

### 6. Styling Header Layout
Membungkus halaman di dalam kontainer selebar `980px`. Judul header `h1` diberi warna merah marun `#a71616`.
**Screenshot Hasil Header:**  
![Layout Header](layout%20header.png)

### 7. Styling Menu Navigasi
Menambahkan gaya pada bilah navigasi dengan latar belakang merah gelap `#b31e1b` dan efek interaktif `:hover` serta state `.active` warna merah `#a11d1d`.
**Screenshot Hasil Navigasi:**  
![Layout Navigasi](layout%20navigasi.png)

### 8. Membuat Hero Panel
Hero panel sebagai area sorotan utama dengan latar belakang abu-abu terang `#e4e4e5`.
**Screenshot Hasil Hero Panel:**  
![Layout Hero Panel](layout%20hero%20panel.png)

### 9. Mengatur Layout Main dan Sidebar
Membagi area `#wrapper` menjadi dua kolom sejajar (Main: 640px, Sidebar: 260px) menggunakan teknik float.
**Screenshot Hasil Utuh:**  
![Layout Home Lengkap](layout%20hero.png)

---

## Jawaban Pertanyaan dan Tugas

### Tugas 1: Layout Menu About (`about.html`)
Halaman About dibuat menggunakan *single layout* (tanpa sidebar) selebar 100%. Terdiri dari:
1. **Card Profil:** Menampilkan foto profil dengan nama **Jumari (Jun)**, NIM **312510077**, mahasiswa Teknik Informatika Universitas Pelita Bangsa. Deskripsi bio memfokuskan pada ketertarikan di bidang pengembangan web dan Internet of Things (IoT).
2. **Deskripsi Diri & Minat Akademik:** Penjelasan ringkas mengenai pemahaman materi praktikum layouting.
3. **Portofolio Proyek Web:** Struktur tiga kolom (`.box`) yang berjajar rapi berisi contoh proyek web dummy.

### Tugas 2: Layout Menu Contact (`kontak.html`)
Halaman Kontak mengombinasikan area `#main` untuk formulir interaktif dan `#sidebar` untuk informasi statis.
1. **Formulir Kontak (Main):** Memiliki isian nama, email, nomor telepon, pesan/textarea, dan tombol "Kirim Pesan" dengan warna merah senada `#a71616`. Menggunakan Flexbox (`.row-form`) pada kolom email dan telepon agar sejajar.
2. **Sidebar Informasi:** Menampilkan alamat lengkap di Cikarang Pusat, Bekasi, jam operasional, serta email kontak aktif `sekitanijun@pelitabangsa.ac.id`.

---

## Halaman Tambahan: Menu Artikel (`artikel.html`)
Dibuat halaman khusus untuk menu artikel guna memastikan navigasi berfungsi. 
- **Konten Utama:** Menampilkan artikel dengan judul **"Kemajuan Teknologi AI: Transformasi di Era Digital"** lengkap dengan metadata, gambar *featured*, heading, teks bergaya *justify*, dan elemen `<blockquote>`.
- **Sidebar Khusus Artikel:** Berisi widget kategori artikel dan tautan artikel terpopuler.

---

## Struktur Direktori Proyek

```text
Praktikum4/
├── README.md                 # Laporan praktikum (dokumen ini)
├── home.html                 # Halaman utama layout web
├── about.html                # Tugas 1: Halaman profil Jumari (Single Layout)
├── kontak.html               # Tugas 2: Halaman formulir & info kontak
├── artikel.html              # Halaman bacaan artikel AI
└── style.css                 # File CSS eksternal (warna marun/merah)
