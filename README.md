# Symbool

Symbool adalah aplikasi berbasis web yang dikembangkan untuk membantu pengguna memahami dan menyederhanakan ekspresi logika Boolean secara interaktif. Aplikasi ini menyediakan beberapa metode penyederhanaan, yaitu Boolean Simplification, Karnaugh Map (K-Map), dan Quine-McCluskey, serta fitur pembuatan tabel kebenaran, visualisasi K-Map, dan proses penyederhanaan untuk mempermudah analisis logika Boolean.

Symbool dikembangkan sebagai proyek akademik dengan fokus menghadirkan solusi digital yang praktis dan interaktif untuk mempelajari serta mengeksplorasi konsep logika Boolean, khususnya dalam proses penyederhanaan ekspresi logika.

---

## Panduan Penggunaan Aplikasi

### 1. Halaman Beranda (Welcome Page)
Saat pertama kali membuka aplikasi, pengguna akan disambut dengan halaman utama yang menampilkan *hero section* berisi penjelasan singkat mengenai aplikasi. Terdapat tombol **Get Started** untuk langsung menuju ke halaman kalkulator.
> **Gambar Halaman Beranda:**
> ![Home Page](https://hdaphuncqwjfxysgmcew.supabase.co/storage/v1/object/public/images/s01.avif)

### 2. Halaman Kalkulator (Calculator Page)
Halaman utama untuk melakukan penyederhanaan ekspresi logika Boolean. 

- **Input Ekspresi & Pilihan Metode:** Pada tampilan awal, pengguna dapat memasukkan ekspresi logika Boolean (misalnya: `(A ∧ B) ∨ ¬C`) atau menggunakan tombol *shortcut* operator yang disediakan (`¬`, `∧`, `∨`, `↑`, `↓`, `⊕`, `↔`, `→`). Pengguna juga dapat memilih metode penyederhanaan melalui *dropdown* **Metode**.
> **Gambar Halaman Kalkulator (Input):**
> ![Calculator Input Page](https://hdaphuncqwjfxysgmcew.supabase.co/storage/v1/object/public/images/s02.avif)

- **Hasil Simplify (Boolean Simplification):** Jika pengguna memilih metode *Simplify (default)* dan menekan tombol **Optimalisasi**, aplikasi akan menampilkan hasil ekspresi yang disederhanakan, penjelasan singkat, waktu proses, serta **Tabel Kebenaran** secara otomatis.
> **Gambar Hasil Simplify:**
> ![Simplify Result](https://hdaphuncqwjfxysgmcew.supabase.co/storage/v1/object/public/images/s03.avif)

- **Hasil Karnaugh Map (K-Map):** Jika pengguna memilih metode **Karnaugh Map**, aplikasi akan menampilkan hasil penyederhanaan beserta visualisasi **Peta Karnaugh** dan daftar **Hasil Minterm**.
> **Gambar Hasil Karnaugh Map:**
> ![Karnaugh Map Result](https://hdaphuncqwjfxysgmcew.supabase.co/storage/v1/object/public/images/s04.avif)

- **Hasil Quine-McCluskey (Proses):** Jika pengguna memilih metode **Quine-McCluskey**, aplikasi akan menampilkan proses penyederhanaan langkah demi langkah. Ini mencakup tabel *Prime Implicant*, tabel *Prime Implicant Chart*, hingga penentuan *Essential Prime Implicants*.
> **Gambar Quine-McCluskey (Proses 1):**
> ![Quine-McCluskey Process 1](https://hdaphuncqwjfxysgmcew.supabase.co/storage/v1/object/public/images/s05.avif)
> **Gambar Quine-McCluskey (Proses 2):**
> ![Quine-McCluskey Process 2](https://hdaphuncqwjfxysgmcew.supabase.co/storage/v1/object/public/images/s06.avif)

- **Hasil Akhir Quine-McCluskey & Tabel Kebenaran:** Setelah proses selesai, hasil akhir ekspresi logika yang paling sederhana akan ditampilkan, diikuti dengan Tabel Kebenaran lengkap di bagian bawah halaman.
> **Gambar Quine-McCluskey (Hasil Akhir):**
> ![Quine-McCluskey Final Result](https://hdaphuncqwjfxysgmcew.supabase.co/storage/v1/object/public/images/s07.avif)

### 3. Halaman Tentang (About Page)
Halaman ini berisi penjelasan singkat mengenai latar belakang dan tujuan dibuatnya aplikasi Symbool, yaitu untuk mempermudah optimasi fungsi logika secara otomatis.
> **Gambar Halaman Tentang:**
> ![About Page](https://hdaphuncqwjfxysgmcew.supabase.co/storage/v1/object/public/images/s08.avif)

---

## Struktur Project & Instalasi

Untuk informasi lebih lanjut mengenai cara mengunduh project, konfigurasi database, migrasi, dan cara menjalankannya di komputer lokal, silakan baca panduan lengkapnya di file:

**[INSTALLATION.md](INSTALLATION.md)**

## Kontribusi
Jika Anda ingin berkontribusi pada project ini, silakan lakukan *fork* pada repository ini, buat *branch* baru untuk fitur Anda, dan ajukan *Pull Request*.

---
*Copyright © 2026 Symbool. All rights reserved.*