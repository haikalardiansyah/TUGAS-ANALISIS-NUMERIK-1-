# TUGAS-ANALISIS-NUMERIK-1-
# Analisis Numerik - Regresi dan Break-Even Point Gerai Donat

## Deskripsi

Project ini merupakan tugas mata kuliah Analisis Numerik yang membahas penerapan metode regresi dan pencarian akar pada data laba/rugi harian dari lima gerai donat dengan strategi marketing yang berbeda.

Analisis dilakukan untuk melihat hubungan antara jumlah penjualan dengan revenue serta menentukan jumlah penjualan yang diperlukan setiap gerai untuk mencapai Break-Even Point (BEP).

## Strategi Gerai

Dataset terdiri dari lima gerai donat dengan karakteristik strategi yang berbeda:

- Gerai A (Premium Gourmet): Harga tinggi, niche terbatas, dan kafe specialty.
- Gerai B (Mass Market Volume): Harga murah dengan margin yang tertekan inflasi bahan.
- Gerai C (Promo Agresif): Menggunakan diskon awal dan iklan moderate-high.
- Gerai D (Mall Premium Flagship): Memiliki biaya sewa lokasi yang tinggi.
- Gerai E (Cloud Kitchen): Berfokus pada aplikasi delivery dan terkena komisi platform sebesar 18%.

## Tujuan Analisis

Analisis dalam project ini bertujuan untuk:

1. Membuat plot hubungan jumlah penjualan dengan revenue pada kelima gerai.
2. Menerapkan regresi untuk mengetahui bentuk tren revenue berdasarkan volume penjualan.
3. Mengevaluasi kecocokan model regresi.
4. Membentuk fungsi balance berdasarkan revenue, biaya variabel, dan fixed cost.
5. Menentukan Break-Even Point pada masing-masing gerai menggunakan metode pencarian akar.
6. Memberikan interpretasi terhadap hasil analisis.

## Dataset

Dataset yang digunakan adalah:

`sintesis_data_donat_harian.csv`

Dataset berisi data harian dari lima gerai dengan beberapa variabel, yaitu:

- Gerai
- Harga Jual (Rp)
- Jumlah Terjual (Unit)
- Pendapatan Kotor (Rp)
- Biaya Variabel (Rp)
- Fixed Cost Harian (Rp)
- Balance (Rp)

## Metode yang Digunakan

### 1. Regresi Linear

Regresi linear digunakan untuk mengetahui hubungan antara jumlah produk yang terjual dengan pendapatan kotor.

Model yang digunakan:

Y = aX + b

Keterangan:

- X = jumlah terjual
- Y = pendapatan kotor
- a = koefisien regresi
- b = intercept

Nilai R² digunakan untuk mengevaluasi kecocokan model terhadap data.

### 2. Fungsi Balance

Break-Even Point ditentukan berdasarkan kondisi ketika balance sama dengan nol.

Fungsi yang digunakan:

Balance(X) = Revenue(X) - Biaya Variabel(X) - Fixed Cost

BEP diperoleh ketika:

Balance(X) = 0

### 3. Metode Bisection

Metode Bisection digunakan sebagai metode pencarian akar untuk menentukan nilai volume penjualan yang menghasilkan balance mendekati nol.

Jika titik BEP berada di luar rentang volume penjualan aktual pada dataset, interval pencarian diperluas terlebih dahulu hingga ditemukan perubahan tanda pada fungsi balance.

## Struktur Project

```text
Analisis_Numerik_Donat/
│
├── analisis_numerik_donat.ipynb
├── sintesis_data_donat_harian.csv
└── README.md
