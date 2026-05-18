# 📚 Dashboard Analisis Review Gramedia Digital

Dashboard interaktif berbasis HTML/CSS/JavaScript untuk memvisualisasikan dan menganalisis data ulasan pengguna aplikasi **Gramedia Digital** dari periode **Juli 2013 hingga Mei 2026**.

---

## 🖥️ Demo Halaman

| Halaman | File | Deskripsi |
|---|---|---|
| 🏠 Overview | `index.html` | Ringkasan statistik & navigasi utama |
| 💬 Analisis Sentimen | `sentiment.html` | Distribusi review Positif, Negatif, Netral |
| 📈 Tren Bulanan | `trend.html` | Grafik jumlah review per bulan/kuartal/tahun |
| 📊 Analisis Keluhan | `keyword.html` | Grouped bar chart keluhan per kategori masalah |

---

## 📊 Fitur Visualisasi

### 🏠 Overview
- Kartu ringkasan: Total Review, Negatif, Positif, Rata-rata Rating
- Navigasi ke semua halaman analisis

### 💬 Analisis Sentimen
- **Donut / Pie / Bar chart** distribusi sentimen
- Filter per jenis sentimen (Positif, Negatif, Netral)
- Statistik persentase tiap sentimen

### 📈 Tren Bulanan
- **Line chart** interaktif dengan 155 titik data bulanan
- Filter **rentang tahun** (dari–sampai)
- Granularitas: **Bulanan / Kuartalan / Tahunan**
- Toggle **Moving Average** (3 bulan)
- Statistik: total, bulan tertinggi/terendah, rata-rata

### 📊 Analisis Keluhan per Kategori
- **Bar chart horizontal** menampilkan keyword #1 per kategori
- 3 Kategori masalah:
  - 🔴 **Teknis** — performa aplikasi (lemot, error, crash)
  - 🟡 **Harga** — biaya berlangganan (premium, bayar, langganan)
  - 🔵 **Fitur** — fungsi aplikasi (aplikasi, baca, download)
- **Donut chart** proporsi total keluhan antar kategori
- Tabel detail keyword #1 per kategori

---

## 🗂️ Struktur File

```
dashboard/
├── index.html              # Halaman overview & navigasi
├── sentiment.html          # Analisis sentimen
├── trend.html              # Tren review bulanan
├── keyword.html            # Analisis keluhan per kategori
├── dashboard_gramedia.html # Versi single-page (lama)
├── radial.html             # Treemap (eksperimen)
└── d3.json                 # Data JSON untuk visualisasi D3
```

---

## 🛠️ Teknologi

| Library | Versi | Kegunaan |
|---|---|---|
| [Chart.js](https://www.chartjs.org/) | CDN latest | Semua grafik (bar, line, donut) |
| [D3.js](https://d3js.org/) | v7 CDN | Visualisasi SVG & data binding |
| [Google Fonts – Inter](https://fonts.google.com/specimen/Inter) | — | Tipografi modern |
| HTML5 + Vanilla CSS | — | Struktur & styling |
| Vanilla JavaScript | — | Logika filter & interaktivitas |

> Tidak memerlukan instalasi npm, build tool, atau server backend.

---

## 🚀 Cara Menjalankan

### Langsung di Browser
1. Clone atau download repository ini
2. Buka file `index.html` langsung di browser (double-click)
3. Navigasi antar halaman melalui sidebar

### Via Live Server (Direkomendasikan)
Jika menggunakan **VS Code**, install ekstensi **Live Server**, klik kanan `index.html` → *Open with Live Server*.

Atau menggunakan Python:
```bash
# Python 3
python -m http.server 5500

# Lalu buka: http://localhost:5500/index.html
```

---

## 📈 Data yang Digunakan

| Atribut | Detail |
|---|---|
| Sumber | Ulasan pengguna aplikasi Gramedia Digital |
| Periode | Juli 2013 – Mei 2026 |
| Total Review | 3.000 ulasan |
| Sentimen Positif | 1.758 (58,6%) |
| Sentimen Negatif | 832 (27,7%) |
| Sentimen Netral | 410 (13,7%) |
| Rata-rata Rating | 3,5 / 5 ⭐ |

### Kategori Keluhan
| Kategori | Keyword Utama | Frekuensi Tertinggi |
|---|---|---|
| 🔴 Teknis | lemot, error, crash, bug, force close | lemot (62x) |
| 🟡 Harga | premium, bayar, langganan, mahal, koin | premium (123x) |
| 🔵 Fitur | aplikasi, baca, download, akses, login | aplikasi (138x) |

---

## 🎨 Desain

- **Tema**: Dark mode premium (`#0a0f1e` background)
- **Font**: Inter (Google Fonts)
- **Warna aksen**: Biru (`#38bdf8`), Hijau (`#34d399`), Merah (`#f87171`), Kuning (`#fbbf24`)
- **Komponen**: Glassmorphism cards, sidebar fixed, grafik responsif
- **Interaktivitas**: Hover tooltip, filter tombol, toggle animasi

---

## 📌 Catatan

- Data keluhan pada halaman **Analisis Keluhan** merupakan estimasi berdasarkan konteks keyword dari dataset ulasan.
- File `dashboard_gramedia.html` adalah versi single-page awal sebelum dipisah menjadi multi-halaman.
- File `radial.html` berisi eksperimen Treemap menggunakan ApexCharts.

---

## 👤 Author

Dibuat sebagai bagian dari proyek analisis data ulasan pengguna aplikasi Gramedia Digital.

> Built with ❤️ using pure HTML, CSS, and JavaScript — no framework required.
