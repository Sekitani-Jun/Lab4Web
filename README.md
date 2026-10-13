# Lab 4 Web — Layout Sederhana

Proyek praktikum Pemrograman Web yang membahas penyusunan layout halaman menggunakan elemen HTML, CSS `float`, dan clearfix. Materi dimulai dari eksperimen box element, lalu diterapkan pada situs sederhana dengan navigasi, konten utama, sidebar, dan footer.

## Tujuan Praktikum

- Memahami alur elemen HTML block dan pengaruh CSS `float`.
- Mencoba posisi `left`, `right`, dan `clear` pada box.
- Mengatasi elemen induk yang tidak mencakup elemen float dengan clearfix.
- Menyusun halaman menggunakan elemen semantik seperti `header`, `nav`, `section`, `article`, `aside`, dan `footer`.
- Menerapkan layout pada halaman Home, Artikel, About, dan Kontak.

## Struktur Proyek

```text
Lab4Web/
├── lab4_layout.html             # Latihan/eksperimen box element dan float
├── Lab4WebSederhana/
│   ├── home.html                # Beranda dan contoh layout utama
│   ├── artikel.html             # Halaman artikel dengan sidebar
│   ├── about.html               # Profil dan portofolio
│   ├── kontak.html              # Formulir dan informasi kontak
│   └── style.css                # Gaya bersama untuk seluruh halaman
├── screenshoot/                 # Dokumentasi tahapan praktikum
└── README.md
```

## Halaman Situs

| Halaman | Isi |
| --- | --- |
| Home | Hero panel, tiga box konten, artikel ringkas, dan widget sidebar |
| Artikel | Artikel tentang kemajuan teknologi AI dan sidebar kategori/populer |
| About | Profil, deskripsi diri, minat akademik, dan portofolio |
| Kontak | Formulir pesan, informasi kontak, dan jam operasional |

Semua halaman menggunakan stylesheet bersama, yaitu `Lab4WebSederhana/style.css`.

## Menjalankan Proyek

Tidak diperlukan proses build atau instalasi dependensi. Buka `Lab4WebSederhana/home.html` di browser, kemudian gunakan menu navigasi untuk berpindah halaman.

> Beberapa gambar contoh menggunakan layanan `dummyimage.com`, sedangkan font dimuat dari Google Fonts. Keduanya memerlukan koneksi internet; gambar atau font tersebut dapat tidak tampil ketika offline.

## Tahapan Praktikum dan Screenshot

Folder `screenshoot/` menyimpan dokumentasi visual proses pengerjaan. Urutan berikut dikelompokkan berdasarkan materi dan nama file yang tersedia.

### 1. Box element, float, dan clearfix

- [Box tanpa float](screenshoot/box%20elemen%20tanpa%20float.png) — box tersusun normal secara vertikal.
- [Box menggunakan float](screenshoot/box%20elemen%20pakai%20float.png) — perubahan susunan setelah elemen diberi `float`.
- [Eksperimen arah float](screenshoot/box%20elemen%20eksperimen%20%28left%2C%20right%2C%20both%2C%20center%29.png) — percobaan posisi `left`, `right`, `both`, dan `center`.
- [Contoh clearfix](screenshoot/box%20elemen%20clearfix.png) — penggunaan clear untuk mengatur alur setelah elemen float.

### 2. Penyusunan kerangka halaman

- [Kerangka layout sederhana](screenshoot/kerangka%20layout%20sederhana.png)
- [Kerangka header layout sederhana](screenshoot/kerangka%20header%20layout%20sederhana.png)
- [Layout header](screenshoot/layout%20header.png)
- [Layout navigasi](screenshoot/layout%20navigasi.png)
- [Layout hero](screenshoot/layout%20hero.png)
- [Layout hero panel](screenshoot/layout%20hero%20panel.png)
- [Layout sidebar](screenshoot/layout%20sidebar.png)
- [Elemen tambahan pada konten utama](screenshoot/menambahkan%20elemen%20lain%20pada%20main%20content.png)
- [Pengaturan footer](screenshoot/mengatur%20footer.png)

### 3. Pengembangan halaman

- [Konten artikel](screenshoot/menambahkan%20konten%20artikel.png)
- [Halaman Artikel](screenshoot/menambahkan%20bagian%20artikel%20html.png)
- [Halaman About](screenshoot/menambahkan%20bagian%20about%20html.png)
- [Halaman Kontak](screenshoot/menambahkan%20layout%20bagian%20kontak%20html.png)

Contoh hasil halaman Artikel:

![Screenshot halaman Artikel](screenshoot/menambahkan%20bagian%20artikel%20html.png)

## Catatan Implementasi

- `lab4_layout.html` berisi contoh latihan mandiri; saat ini markup eksperimennya berada dalam komentar HTML.
- Situs pada folder `Lab4WebSederhana/` menggunakan satu file CSS untuk menjaga tampilan dan navigasi tetap konsisten.
- Formulir pada halaman Kontak masih berupa tampilan antarmuka. Atribut `action="#"` belum mengirim atau menyimpan data ke backend.

