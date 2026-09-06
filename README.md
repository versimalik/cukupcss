# CUKUP.css

**Versi:** 0.1

> "Sederhana itu cukup. Dan itu sudah bagus."

Cukup.css adalah kerangka kerja (*framework*) CSS yang mengutamakan kesederhanaan. Proyek ini menyediakan utilitas dasar dengan tema warna monokrom, sehingga Anda bisa fokus membangun tampilan yang rapi tanpa perlu repot memikirkan paduan warna.

## Mengapa Memilih Cukup.css?

*Framework* ini dibuat dari sudut pandang pengembang (*developer*) yang bukan desainer UI/UX.

*   **Pemilihan Warna yang Praktis:** Terinspirasi dari Pico CSS, namun disederhanakan menjadi satu tema monokrom bawaan. Anda tidak perlu bingung lagi memadukan warna.
*   **Tata Letak Responsif:** Mengadopsi kepraktisan sistem *grid* (baris dan kolom) dari Bootstrap agar website tetap rapi di HP maupun di laptop.
*   **Ringan dan Logis:** Menggabungkan elemen yang otomatis rapi tanpa banyak class, ditambah beberapa utilitas penting yang sering dipakai.

## Cara Instalasi

Cukup sisipkan satu baris kode berikut ke bagian `<head>` pada file HTML Anda:

```html
<link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/gh/versimalik/cukupcss@v0.1/css/cukup.css">
```

## Prinsip Desain

Cukup.css dirancang agar elemen-elemen dasar HTML Anda sudah bekerja dengan sendirinya.

*   **Warna Monokrom:** Mengandalkan warna hitam pekat (`#111827`) untuk teks dan tombol utama, putih (`#ffffff`) untuk latar, serta abu-abu untuk elemen pendukung.
*   **Ukuran Teks Dinamis:** Anda tidak perlu mengatur ukuran teks untuk tiap ukuran layar. Ukuran huruf dasar membesar secara bertahap mengikuti lebar layar, mulai dari `< 576px` hingga `≥ 1400px`.
*   **Font Bawaan Sistem:** Tidak perlu mengunduh font tambahan. Cukup.css memakai font bawaan perangkat pengguna sehingga website terasa ringan.

## Sistem Tata Letak (Grid)

Untuk menyusun posisi elemen, Cukup.css memakai sistem 12 kolom yang mudah dipahami.

```html
<div class="row">
  <div class="col-12 col-md-8">Konten Utama</div>
  <div class="col-12 col-md-4">Bilah Samping (Sidebar)</div>
</div>
```

*   `.row`: wadah utama untuk membuat baris.
*   `.col-1` hingga `.col-12`: menentukan seberapa lebar sebuah elemen.
*   **Responsif:** Gunakan `.col-sm-*` (HP besar), `.col-md-*` (tablet), dan `.col-lg-*` (laptop) untuk mengatur lebar kolom pada perangkat yang berbeda.
*   **Wadah (*Container*):** class `.container` membatasi lebar website di tengah layar (maksimal 1080px), sedangkan `.container-wide` untuk ukuran lebih lebar (maksimal 1400px).

## Komponen Tersedia

Cukup.css memiliki dua jenis gaya tampilan: yang otomatis rapi tanpa class, dan yang menggunakan class tambahan.

### 1. Langsung Rapi Tanpa Class

Cukup menulis HTML standar, elemen-elemen berikut sudah memiliki desain yang enak dilihat:

*   **Formulir & Input:** Kolom teks, radio/checkbox, dan tombol unggah file sudah disesuaikan agar nyaman digunakan.
*   **Tabel & Daftar:** Header tabel tersorot otomatis dan baris bereaksi saat kursor diarahkan (*hover*). Daftar (`<ul>` / `<ol>`) sudah dirapikan.
*   **Gambar & Media:** Semua gambar otomatis menyesuaikan layar dan diberi efek *grayscale* (hitam putih) untuk memperkuat tema monokrom.

### 2. Elemen dengan Class Tambahan

Jika butuh variasi, tambahkan class berikut pada kode HTML:

| Nama Komponen | Class yang Digunakan | Fungsi |
| :--- | :--- | :--- |
| **Tombol (Button)** | `.btn`, `.btn-outline`, `.btn-secondary`, `.btn-sm`, `.btn-lg` | Membuat tombol dengan berbagai ukuran dan warna. |
| **Kartu (Card)** | `.card`, `.card-title` | Membuat kotak konten berbingkai yang rapi. |
| **Label (Badge)** | `.badge`, `.badge-outline`, `.badge-secondary`, `.badge-muted` | Label teks kecil bersudut untuk status atau kategori. |
| **Tab Menu** | `.tabs` | Menu tab interaktif yang bisa ditekan tanpa bantuan JavaScript. |
| **Pesan (Alert)** | `.alert`, `.alert-secondary`, `.alert-outline` | Kotak peringatan atau informasi penting. |
| **Menu Tarik (Dropdown)** | `details.dropdown` | Menu yang bisa dibuka/tutup tanpa JavaScript; daftar muncul di bawah tombol. Cocok ditaruh di dalam item navigasi. |
| **Grup (Group)** | `[role="group"]`, `[role="search"]` | Membuat beberapa elemen form/tombol menempel menyatu tanpa celah antar-anggotanya. `[role="search"]` membuat input menggembang mengisi sisa ruang di samping tombol. |

### 3. Navigasi (Navbar)

Anda bisa membuat menu navigasi di bagian atas website yang otomatis lengket (*sticky*) tanpa JavaScript. Cukup gunakan struktur `<nav>` berisi satu daftar `<ul>`. Menu tampil mendatar (*horizontal*); saat item terlalu banyak, menu bisa digulir ke samping. Anda bebas menentukan isinya — cukup *list* biasa, atau selipkan komponen *dropdown* di salah satu item.

## Utilitas Tambahan

Untuk mempercepat pekerjaan, tersedia beberapa class bantuan (utilitas):

*   **Jarak (Spacing):** `.mt-0`, `.mt-1`, `.mt-2` untuk menambah jarak atas (margin-top), dan `.mb-*` untuk jarak bawah. Catatan: elemen berurutan di dalam artikel atau kartu sudah otomatis berjarak, jadi utilitas ini hanya dipakai saat benar-benar diperlukan.
*   **Perataan Teks:** `.text-center` (tengah), `.text-right` (kanan), `.text-secondary` (teks abu-abu).

## Melihat Demo

Penasaran dengan hasilnya? Anda bisa langsung melihat demonstrasi Cukup.css di:
https://versimalik.com/produk/cukupcss/demo (sedang dalam pengembangan)

## Cara Kustomisasi

Desainnya mudah diubah. Anda cukup menimpa variabel dasar di file CSS utama tanpa perlu membongkar kode Cukup.css.

Contoh mengubah warna utama dan lebar maksimal website:

```css
:root {
  --primary: #1F2937; /* Mengubah warna hitam pekat menjadi warna lain */
  --container: 1200px; /* Memperlebar batas maksimal website */
}
```

## Rencana ke Depan (*Roadmap*)

Fokus pengembangan berikutnya adalah **perbaikan bug**, lalu menghadirkan **Mode Gelap (*Dark Mode*)**, dan selanjutnya pilihan tema warna lain sebagai alternatif dari tema monokrom.
