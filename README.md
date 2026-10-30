# Symbool — Sistem Penyederhanaan Logika Boolean Interaktif

**Symbool** adalah aplikasi web edukatif berbasis Python dan JavaScript yang dirancang untuk menyederhanakan ekspresi logika Boolean secara otomatis menggunakan metode populer seperti **Simplify**, **Karnaugh Map (K-Map)**, dan **Quine-McCluskey**. Aplikasi ini ideal untuk mahasiswa, dosen, dan praktisi logika digital atau Matematika Diskrit.

**Coba aplikasi langsung**: [[https://symbool-app.onrender.com]](https://symbool-app.onrender.com))

---

## Fitur Utama

- Input ekspresi simbolik langsung (contoh: `A'B + AB' + ABC`)
- Penyederhanaan otomatis menggunakan:
  - **Simplify** (default) — via symbolic logic
  - **Karnaugh Map (K-Map)** — untuk ekspresi hingga 4 variabel
  - **Quine-McCluskey** — untuk ekspresi lebih dari 4 variabel
- Tabel kebenaran otomatis dan dapat diekspor
- Visualisasi K-Map interaktif
- Proses logika ditampilkan secara transparan
- Fitur ekspor tabel kebenaran ke format CSV


## Cara Menjalankan Secara Lokal

### 1. Clone Repository

```bash
git clone https://github.com/username/symbool.git
cd symbool

---

**### 2. Buat Aplikasi Virtual Environtment**

python -m venv venv
source venv/bin/activate   # Untuk Linux/Mac
venv\Scripts\activate      # Untuk Windows

---

**### 3. Install Dependensi**

pip install -r requirements.txt

(atau manual jika requirements.txt belum tersedia)
pip install flask sympy

---

**### 4. Jalankan Aplikasi**

python app.py

Buka browser dan akses: http://localhost:5000

---

**## Contoh Ekspresi Boolean**

A'B + AB' + ABC
(A and B) or (not C)
A & ~B | B & ~A

---

**## Teknologi yang Digunakan**

Python + Flask — backend dan server aplikasi
SymPy — pemrosesan ekspresi Boolean dan logika simbolik
HTML, CSS, JavaScript — antarmuka pengguna
Multithreading — eksekusi paralel pada ekspresi kompleks
Render — untuk deployment online

---

MIT License © 2025 — Kevin Yulian Pamungkas
