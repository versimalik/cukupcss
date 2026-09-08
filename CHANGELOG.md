# Changelog

Catatan perubahan CUKUP.css per versi.

## v0.4

### Navbar
- Hapus properti `position: sticky` dari navbar di `cukup.css` (diserahkan ke pemakai, mis. lewat inline style). Navbar kini tidak lagi otomatis sticky.

## v0.3

### Komponen Baru
- **Group / Role** — tambah `[role="group"]` dan `[role="search"]` ala Pico: elemen di dalamnya (input, select, button) menempel menyatu tanpa celah. Pada `[role="search"]`, input menggembang otomatis mengisi sisa ruang di samping tombol.

### Navbar
- **Brand** — logo + tulisan di navbar kini sejajar otomatis secara vertikal (`display: flex; align-items: center`), tanpa perlu inline style. Penyesuaian juga pada penggunaan gambar logo di brand.

### Tombol
- Dukungan tombol `input[type="submit"]`, `input[type="button"]`, `input[type="reset"]` setara dengan `button` (gaya, hover, dan state disabled).
- `input[type="reset"]` otomatis mendapat gaya outline.
- Tambah efek hover khusus untuk tombol outline (mengubah background, bukan sekadar opacity).

### Tabs
- Ganti nama class `tab-konten` menjadi `tab-content`.

### Lainnya
- Dukungan cetak (`@media print`).
- `pre` diberi warna latar; `input[type="file"]` diberi hover/disabled state.
- `thead th` gaya selection yang benar; `dialog` ikut aturan pertama-anak margin.

## v0.2

### Dropdown
- Implementasi ulang komponen dropdown ala Pico (`details.dropdown`) tanpa JavaScript — daftar absolute muncul di bawah summary melalui `details[open]`.
- Dropdown bisa ditaruh di dalam item navbar maupun di tempat lain.

### Navbar
- Struktur navbar diubah menjadi **satu `<nav>` berisi dua `<ul>`** (brand kiri + menu kanan), menu horizontal.
- Keselarasan item menu diperbaiki: item yang berisi dropdown dibatasi tingginya agar sejajar dengan link lain.
- Hapus dropdown mobile lama (`.nav-toggle` / `.nav-burger`).

### Lainnya
- Tambah link CDN jsDelivr.

## v0.1

### Rilis Awal
- Inisialisasi CUKUP.css dengan desain token, reset, layout grid 12 kolom, elemen classless, dan komponen awal.
