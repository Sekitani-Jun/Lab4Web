<<<<<<< HEAD
# Laporan Praktikum Lab 4 Web

## Layout Sederhana

Praktikum ini mempelajari penyusunan elemen halaman web menggunakan HTML dan CSS. Materi dimulai dengan mengamati susunan box sebelum dan sesudah memakai `float`, dilanjutkan dengan percobaan `clear`, lalu menerapkan konsep layout pada situs sederhana.

Implementasi pada repositori ini terdiri dari latihan box di `lab4_layout.html` dan situs beberapa halaman di `Lab4WebSederhana/`. Gambar pada setiap bagian berikut memperlihatkan hasil yang tersimpan di folder `screenshoot/`.

## Tujuan

- Mengamati susunan normal elemen block dan perubahan posisinya dengan `float`.
- Mempraktikkan `float: left`, `float: right`, dan penggunaan `clear` setelah elemen float.
- Menyusun kerangka halaman menggunakan header, navigasi, hero, konten utama, sidebar, dan footer.
- Menerapkan layout tersebut pada halaman Home, Artikel, About, dan Kontak.
=======
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
   - [Web Layout](#1-web-layout)
   - [Box Element (CSS Box Model)](#2-box-element-css-box-model)
   - [CSS Float Property](#3-css-float-property)
   - [Clearfix Element](#4-clearfix-element)
   - [HTML5 Semantics Elements](#5-html5-semantics-elements)
4. [Langkah-Langkah Praktikum](#langkah-langkah-praktikum)
   - [1. Box Element Dasar Tanpa Float](#1-box-element-dasar-tanpa-float)
   - [2. Penerapan CSS Float Property](#2-penerapan-css-float-property)
   - [3. Penerapan Clearfix pada Div 4](#3-penerapan-clearfix-pada-div-4)
   - [4. Eksperimen Properti Clear (left, right, both)](#4-eksperimen-properti-clear-left-right-both)
   - [5. Membuat Layout Web Sederhana (lab4_layout)](#5-membuat-layout-web-sederhana-lab4_layout)
   - [6. Styling Header Layout](#6-styling-header-layout)
   - [7. Styling Menu Navigasi](#7-styling-menu-navigasi)
   - [8. Membuat Hero Panel](#8-membuat-hero-panel)
   - [9. Mengatur Layout Main dan Sidebar](#9-mengatur-layout-main-dan-sidebar)
   - [10. Menambahkan Sidebar Widget](#10-menambahkan-sidebar-widget)
   - [11. Mengatur Footer](#11-mengatur-footer)
   - [12. Elemen Multi-Kolom Box dan Featurette Artikel](#12-elemen-multi-kolom-box-dan-featurette-artikel)
   - [13. Tampilan Utuh Home Layout](#13-tampilan-utuh-home-layout)
5. [Jawaban Pertanyaan dan Tugas](#jawaban-pertanyaan-dan-tugas)
   - [Tugas 1: Layout Menu About (Single Layout: Profil, Deskripsi, & Portfolio)](#tugas-1-layout-menu-about)
   - [Tugas 2: Layout Menu Contact (Form Isian Lengkap & Info Kontak)](#tugas-2-layout-menu-contact)
6. [Halaman Tambahan: Menu Artikel](#halaman-tambahan-menu-artikel)
7. [Struktur Direktori Proyek](#struktur-direktori-proyek)
8. [Petunjuk Git & Pengumpulan Tugas](#petunjuk-git--pengumpulan-tugas)
9. [Kesimpulan](#kesimpulan)

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
>>>>>>> 71d599ec88abd9af22d23379fd270a514857effb

## Dasar Teori

<<<<<<< HEAD
```text
Lab4Web/
├── lab4_layout.html
├── Lab4WebSederhana/
│   ├── home.html
│   ├── artikel.html
│   ├── about.html
│   ├── kontak.html
│   └── style.css
├── screenshoot/
└── README.md
```

`lab4_layout.html` adalah latihan box element. Halaman-halaman di `Lab4WebSederhana/` berbagi aturan tampilan dari `style.css`.

## 1. Percobaan Box Element

### Tanpa float

Ketiga box tampil sebagai elemen block yang memenuhi lebar area dan tersusun vertikal.

![Hasil box element tanpa float](screenshoot/box%20elemen%20tanpa%20float.png)

### Menggunakan float

Setelah elemen diberi float, Div 1, Div 2, dan Div 3 terlihat berdampingan di sisi kiri.

![Hasil box element dengan float](screenshoot/box%20elemen%20pakai%20float.png)

### Percobaan left, right, both, dan center

Screenshot memperlihatkan Div 1 di sisi kiri, Div 2 di sisi kanan, dan Div 3 di antara keduanya. Div 4 berada di baris berikutnya. Pada HTML latihan, `float: both` dan `float: center` bukan nilai CSS yang valid; `clear: left` dan `float: none` pada Div 4 membuatnya mulai setelah float di kiri.

![Eksperimen posisi float dan clear](screenshoot/box%20elemen%20eksperimen%20%28left%2C%20right%2C%20both%2C%20center%29.png)

### Hasil percobaan clear

Pada screenshot ini, Div 1 dan Div 2 berada dalam satu baris, sementara Div 4 tampil sebagai blok biru pada baris setelah elemen float.

![Hasil percobaan clear pada box](screenshoot/box%20elemen%20clearfix.png)

## 2. Penyusunan Layout Sederhana

Tahap ini menunjukkan perkembangan kerangka halaman dari header hingga hero dan footer. Beberapa screenshot merupakan potongan tampilan pada tahap tertentu, sehingga tidak semuanya memperlihatkan halaman lengkap.

### Kerangka layout

Kerangka awal menampilkan judul “Layout Sederhana”, navigasi Beranda/Artikel/About/Kontak, dan teks copyright.

![Kerangka layout sederhana](screenshoot/kerangka%20layout%20sederhana.png)

Screenshot kerangka berikutnya memperlihatkan judul, tautan navigasi, dan copyright dalam tampilan HTML dasar.

![Kerangka header layout sederhana](screenshoot/kerangka%20header%20layout%20sederhana.png)

### Header dan navigasi

Tahap header menampilkan judul merah “Layout Sederhana”.

![Layout header](screenshoot/layout%20header.png)

Navigasi menambahkan menu Home, Artikel, About, dan Kontak di bawah header.

![Layout navigasi](screenshoot/layout%20navigasi.png)

### Hero

Bagian hero berisi judul “Hello World!”, paragraf pengantar, dan tautan “Learn more”.

![Layout hero](screenshoot/layout%20hero.png)

Screenshot panel hero memperlihatkan hero dalam halaman lengkap bersama header, navigasi, dan footer.

![Layout hero panel](screenshoot/layout%20hero%20panel.png)

### Sidebar, konten utama, dan footer

Sidebar berisi widget “Widget Header” dengan daftar tautan dan widget “Widget Text”.

![Layout sidebar](screenshoot/layout%20sidebar.png)

Konten utama menampilkan tiga box dengan gambar lingkaran, heading, deskripsi, dan tautan “View detail”, berdampingan dengan widget sidebar.

![Elemen tambahan pada main content](screenshoot/menambahkan%20elemen%20lain%20pada%20main%20content.png)

Footer menampilkan latar merah dengan teks “© 2021 - Universitas Pelita Bangsa”.

![Pengaturan footer](screenshoot/mengatur%20footer.png)

## 3. Halaman pada Lab4WebSederhana

Menu pada setiap halaman menghubungkan Home, Artikel, About, dan Kontak. Tampilan situs menggunakan stylesheet bersama `style.css`.

### Home

Halaman Home menggabungkan hero, tiga box ringkasan, dua featurette dengan gambar yang bergantian di kiri dan kanan, serta sidebar widget.

### Artikel

Screenshot halaman artikel memperlihatkan artikel “Kemajuan Teknologi AI: Transformasi di Era Digital”, gambar utama, isi artikel, kutipan, kategori artikel, dan daftar artikel populer.

![Halaman artikel tentang AI](screenshoot/menambahkan%20konten%20artikel.png)

Screenshot bernama `menambahkan bagian artikel html.png` menampilkan dua bagian featurette: gambar berada di kiri pada bagian pertama dan di kanan pada bagian kedua.

![Hasil featurette dengan gambar kiri dan kanan](screenshoot/menambahkan%20bagian%20artikel%20html.png)

### About

Halaman About menampilkan kartu profil Jumari, deskripsi diri dan minat akademik, serta tiga kartu portofolio.

![Halaman About](screenshoot/menambahkan%20bagian%20about%20html.png)

### Kontak

Halaman Kontak menampilkan formulir nama, email, telepon, pesan, tombol “Kirim Pesan”, informasi kontak, dan jam operasional.

![Halaman Kontak](screenshoot/menambahkan%20layout%20bagian%20kontak%20html.png)
=======
### 1. Web Layout
Web layout merupakan kerangka acuan yang mengatur penempatan serta tata letak elemen pada halaman web, seperti navigasi, header, hero banner, main content, sidebar, dan footer. Penataan layout yang baik akan membuat halaman web lebih mudah dibaca, lebih rapi, dan lebih profesional.

### 2. Box Element (CSS Box Model)
Semua elemen dalam HTML pada dasarnya diperlakukan sebagai sebuah kotak (*box*). CSS Box Model tersusun atas empat komponen utama:
- **Content:** Area inti tempat teks, gambar, atau media ditampilkan.
- **Padding:** Ruang transparan di antara konten dan border elemen.
- **Border:** Garis pembatas yang mengelilingi padding dan konten.
- **Margin:** Ruang transparan di luar border yang memisahkan elemen tersebut dari elemen lainnya.
- **Box-sizing:** Deklarasi `box-sizing: border-box;` memastikan kalkulasi lebar total elemen sudah mencakup padding dan border.

### 3. CSS Float Property
Properti CSS `float` digunakan untuk menggeser elemen ke sisi kiri (`left`) atau kanan (`right`), sehingga elemen teks atau elemen lain di sekitarnya dapat mengalir di sampingnya. Elemen yang memiliki `float` akan keluar dari alur normal dokumen dan diletakkan pada sisi tertentu.

### 4. Clearfix Element
Ketika elemen-elemen anak (*child elements*) menggunakan `float`, elemen induk (*parent element*) sering kali kehilangan tinggi aslinya (*height collapse*). Untuk mengatasi hal ini, digunakan properti `clear` atau teknik clearfix agar elemen induk tetap menampung tinggi elemen-elemennya.
>>>>>>> 71d599ec88abd9af22d23379fd270a514857effb

### 5. HTML5 Semantics Elements
HTML5 memperkenalkan elemen semantik yang memberikan makna struktural bagi peramban web (*browser*), perayap mesin pencari (*search engine bot*), dan pembaca layar (*screen reader*).
- `<header>`: Mendefinisikan kepala dokumen atau bagian pembuka.
- `<nav>`: Mendefinisikan kumpulan tautan navigasi utama.
- `<section>`: Mendefinisikan babak atau bagian tematik dalam dokumen.
- `<article>`: Mendefinisikan konten mandiri dan independen.
- `<aside>`: Mendefinisikan konten pelengkap/pendukung di samping konten utama (seperti *sidebar*).
- `<footer>`: Mendefinisikan kaki halaman atau bagian penutup.

<<<<<<< HEAD
Tidak diperlukan proses build atau instalasi. Buka `Lab4WebSederhana/home.html` di browser, lalu pilih halaman lain melalui menu navigasi. Latihan box dapat dibuka langsung melalui `lab4_layout.html`.

Gambar contoh pada halaman situs menggunakan `dummyimage.com`, dan font menggunakan Google Fonts, sehingga keduanya memerlukan koneksi internet.

## Catatan

- `float: both` dan `float: center` pada latihan tidak valid sebagai nilai properti CSS `float`; browser mengabaikannya.
- Formulir Kontak masih berupa antarmuka. `action="#"` belum mengirim atau menyimpan data ke backend.
- CSS menetapkan lebar container sebesar `980px`; screenshot menunjukkan hasil visual pada ukuran layar saat dokumentasi dibuat.
=======
---

## Langkah-Langkah Praktikum

### 1. Box Element Dasar Tanpa Float
Sebelum menerapkan float, tiga buah tag `<div>` berturut-turut ditampilkan. Karena elemen `<div>` bertipe *block-level*, masing-masing elemen memakan lebar penuh baris dan tersusun secara vertikal dari atas ke bawah.

**Kode HTML & CSS:**
```html
<style>
    div { padding: 10px; }
    .div1 { background: red; }
    .div2 { background: yellow; }
    .div3 { background: green; }
</style>
<section>
    <div class="div1">Div 1</div>
    <div class="div2">Div 2</div>
    <div class="div3">Div 3</div>
</section>
**Screenshoot Hasil:**
![Box Element Tanpa Float](screenshoot/box elemen clearfix.png)
>>>>>>> 71d599ec88abd9af22d23379fd270a514857effb
