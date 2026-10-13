# Laporan Praktikum Lab 4 Web

## Layout Sederhana

Praktikum ini mempelajari penyusunan elemen halaman web menggunakan HTML dan CSS. Materi dimulai dengan mengamati susunan box sebelum dan sesudah memakai `float`, dilanjutkan dengan percobaan `clear`, lalu menerapkan konsep layout pada situs sederhana.

Implementasi pada repositori ini terdiri dari latihan box di `lab4_layout.html` dan situs beberapa halaman di `Lab4WebSederhana/`. Gambar pada setiap bagian berikut memperlihatkan hasil yang tersimpan di folder `screenshoot/`.

## Tujuan

- Mengamati susunan normal elemen block dan perubahan posisinya dengan `float`.
- Mempraktikkan `float: left`, `float: right`, dan penggunaan `clear` setelah elemen float.
- Menyusun kerangka halaman menggunakan header, navigasi, hero, konten utama, sidebar, dan footer.
- Menerapkan layout tersebut pada halaman Home, Artikel, About, dan Kontak.

## Struktur Proyek

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

## Menjalankan Proyek

Tidak diperlukan proses build atau instalasi. Buka `Lab4WebSederhana/home.html` di browser, lalu pilih halaman lain melalui menu navigasi. Latihan box dapat dibuka langsung melalui `lab4_layout.html`.

Gambar contoh pada halaman situs menggunakan `dummyimage.com`, dan font menggunakan Google Fonts, sehingga keduanya memerlukan koneksi internet.

## Catatan

- `float: both` dan `float: center` pada latihan tidak valid sebagai nilai properti CSS `float`; browser mengabaikannya.
- Formulir Kontak masih berupa antarmuka. `action="#"` belum mengirim atau menyimpan data ke backend.
- CSS menetapkan lebar container sebesar `980px`; screenshot menunjukkan hasil visual pada ukuran layar saat dokumentasi dibuat.
