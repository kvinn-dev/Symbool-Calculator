# Installation Guide - Symbool

Panduan ini menjelaskan langkah-langkah instalasi dan konfigurasi project Symbool dari awal hingga aplikasi dapat dijalankan di lingkungan lokal.

## Teknologi yang Digunakan

- Python
- Flask
- SymPy
- HTML
- CSS
- JavaScript
- Jinja2
- Multithreading
- Render
- Git & GitHub

## Struktur Singkat Project

```bash
Symbool-Calculator/
├── .github/
│   └── workflows/          # GitHub Actions workflows
├── static/                 # Frontend assets
│   ├── css/                # Stylesheets
│   ├── js/                 # JavaScript files
│   └── ...
├── templates/              # HTML templates
├── app.py                  # Flask application entry point
├── optimizer.py            # Boolean logic optimization
├── requirements.txt        # Python dependencies
├── render.yaml             # Render deployment configuration
├── README.md               # Project documentation
└── LICENSE                 # MIT License
```

> **Catatan:** Folder `__pycache__/` dan file hasil instalasi virtual environment tidak perlu di-upload ke GitHub karena dapat dibuat kembali secara otomatis.

---

## 1. Persiapan Instalasi

Pastikan perangkat sudah memiliki software berikut:

- Python 3.
- pip (Python package manager).
- Git.

Pastikan seluruh software tersebut sudah terpasang dan dapat diakses melalui terminal.

Untuk memeriksa instalasi, jalankan:

```bash
python --version
pip --version
git --version
```

Pada macOS atau Linux, gunakan `python3 --version` jika perintah `python` tidak tersedia.

## 2. Clone Repository

Buka terminal, kemudian clone repository Symbool:

```bash
git clone https://github.com/kvinn-dev/Symbool-Calculator.git
```

Masuk ke direktori project:

```bash
cd Symbool-Calculator
```

Pastikan terminal berada di direktori root project yang memiliki file `app.py` dan `requirements.txt`.

## 3. Buat Virtual Environment

Buat virtual environment untuk mengisolasi dependency project:

```bash
python -m venv venv
```

Aktifkan virtual environment sesuai sistem operasi yang digunakan.

### macOS / Linux

```bash
source venv/bin/activate
```

### Windows (Command Prompt)

```bash
venv\Scripts\activate
```

### Windows (PowerShell)

```powershell
.\venv\Scripts\Activate.ps1
```

Jika berhasil, nama environment `(venv)` akan muncul pada bagian awal terminal.

## 4. Install Dependencies

Pastikan virtual environment sudah aktif, kemudian install seluruh dependency yang tercantum dalam `requirements.txt`:

```bash
pip install -r requirements.txt
```

Dependency utama yang digunakan dalam project ini:

- **Flask** - Framework Python untuk menjalankan aplikasi web dan menangani request.
- **SymPy** - Library untuk pemrosesan matematika simbolik dan penyederhanaan logika Boolean.

Perintah tersebut akan mengunduh seluruh package yang dibutuhkan ke dalam virtual environment.

## 5. Konfigurasi Aplikasi

Symbool tidak memerlukan konfigurasi database maupun file environment `.env` untuk menjalankan aplikasi secara lokal.

Setelah dependency berhasil diinstal, pastikan file utama berikut tersedia:

- `app.py`
- `optimizer.py`
- `requirements.txt`

File `app.py` berfungsi sebagai entry point aplikasi Flask, sedangkan `optimizer.py` menangani proses optimasi dan penyederhanaan ekspresi logika Boolean.

## 6. Jalankan Project Symbool

Setelah seluruh proses instalasi selesai, jalankan aplikasi menggunakan perintah berikut:

```bash
python app.py
```

Jika menggunakan macOS atau Linux dan perintah `python` tidak tersedia, gunakan:

```bash
python3 app.py
```

Perintah ini akan menjalankan Flask Development Server pada port `10000`.

Secara default, aplikasi dapat diakses melalui:

```text
http://127.0.0.1:10000
```

Setelah server berhasil dijalankan, buka browser dan akses alamat tersebut untuk menggunakan aplikasi Symbool.

---

## Alur Instalasi Lengkap untuk Developer Baru

Berikut ringkasan perintah instalasi dari awal hingga aplikasi siap dijalankan di lingkungan lokal.

### macOS / Linux

```bash
git clone https://github.com/kvinn-dev/Symbool-Calculator.git

cd Symbool-Calculator

python3 -m venv venv

source venv/bin/activate

pip install -r requirements.txt

python3 app.py
```

### Windows

```bash
git clone https://github.com/kvinn-dev/Symbool-Calculator.git

cd Symbool-Calculator

python -m venv venv

venv\Scripts\activate

pip install -r requirements.txt

python app.py
```

Setelah server berhasil dijalankan, buka browser dan akses:

```text
http://127.0.0.1:10000
```

## Alur Menjalankan Project Setelah Instalasi

Untuk menjalankan kembali project yang sudah pernah di-setup sebelumnya, cukup masuk ke direktori root project dan jalankan perintah berikut.

**macOS / Linux:**

```bash
cd Symbool-Calculator

source venv/bin/activate

python3 app.py
```

**Windows:**

```bash
cd Symbool-Calculator

venv\Scripts\activate

python app.py
```

Tidak perlu mengulangi pembuatan virtual environment atau instalasi dependency selama environment dan dependency project tidak berubah.

---

## Troubleshooting

### 1. Python is not recognized

Artinya Python belum terdeteksi oleh terminal.

Pastikan Python sudah terinstal dan telah ditambahkan ke PATH sistem. Pada macOS atau Linux, coba gunakan perintah `python3`.

### 2. Error: No module named 'flask' atau 'sympy'

Artinya dependency yang dibutuhkan belum terinstal pada environment aktif.

Pastikan virtual environment sudah aktif, kemudian jalankan:

```bash
pip install -r requirements.txt
```

### 3. Virtual Environment Cannot Be Activated

Pastikan perintah aktivasi sesuai dengan sistem operasi dan terminal yang digunakan.

Untuk Windows PowerShell, jika muncul pembatasan execution policy, kamu dapat menggunakan Command Prompt atau menyesuaikan pengaturan execution policy pada perangkat.

### 4. Error: Address Already in Use

Artinya port `10000` sedang digunakan oleh aplikasi lain.

Hentikan proses yang menggunakan port tersebut sebelum menjalankan Symbool kembali.

### 5. Application Cannot Be Accessed

Pastikan aplikasi Flask masih berjalan pada terminal dan tidak terdapat error ketika proses startup.

Kemudian akses alamat berikut melalui browser:

```text
http://127.0.0.1:10000
```

### 6. Dependency Installation Failed

Jika proses instalasi dependency mengalami kendala, pastikan koneksi internet tersedia dan pip sudah diperbarui:

```bash
python -m pip install --upgrade pip
```

Kemudian ulangi instalasi:

```bash
pip install -r requirements.txt
```

---

## Catatan untuk GitHub

Pastikan file `.gitignore` memiliki konfigurasi berikut agar file hasil instalasi lokal dan file sementara tidak ikut ter-upload ke repository:

```gitignore
/venv/
/.venv/
__pycache__/
*.py[cod]
.env
.DS_Store
```

> **Catatan:** Folder virtual environment dan file cache Python tidak perlu disimpan di repository karena dapat dibuat kembali melalui proses instalasi.

---

## Verifikasi Instalasi

Setelah seluruh langkah instalasi selesai, pastikan aplikasi Flask berjalan tanpa error.

Kemudian buka browser dan akses aplikasi Symbool melalui alamat berikut:

```text
http://127.0.0.1:10000
```

Jika halaman aplikasi berhasil dibuka dan fitur-fitur utama seperti penyederhanaan logika Boolean, Karnaugh Map (K-Map), Quine-McCluskey, serta tabel kebenaran dapat digunakan, berarti proses instalasi telah berhasil.

Untuk informasi mengenai deskripsi project, fitur aplikasi, screenshot, dan informasi lainnya, silakan lihat file **README.md** pada repository Symbool.