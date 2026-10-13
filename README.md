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

## Dasar Teori

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

### 5. HTML5 Semantics Elements
HTML5 memperkenalkan elemen semantik yang memberikan makna struktural bagi peramban web (*browser*), perayap mesin pencari (*search engine bot*), dan pembaca layar (*screen reader*).
- `<header>`: Mendefinisikan kepala dokumen atau bagian pembuka.
- `<nav>`: Mendefinisikan kumpulan tautan navigasi utama.
- `<section>`: Mendefinisikan babak atau bagian tematik dalam dokumen.
- `<article>`: Mendefinisikan konten mandiri dan independen.
- `<aside>`: Mendefinisikan konten pelengkap/pendukung di samping konten utama (seperti *sidebar*).
- `<footer>`: Mendefinisikan kaki halaman atau bagian penutup.

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
