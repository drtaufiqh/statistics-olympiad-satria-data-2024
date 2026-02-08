# Implementasi Geographically Weighted Regression (GWR)

## Analisis Tingkat Pengangguran Terbuka (TPT) di Pulau Jawa

### National Statistics Competition (NSC)

---

## 📌 Deskripsi Proyek

Proyek ini mengkaji **Tingkat Pengangguran Terbuka (TPT)** di Pulau Jawa dengan mempertimbangkan **efek spasial** menggunakan metode **Geographically Weighted Regression (GWR)**. Pendekatan spasial digunakan karena karakteristik sosial-ekonomi antar kabupaten/kota di Pulau Jawa bersifat **heterogen secara geografis**, sehingga model regresi global berpotensi menghasilkan estimasi yang bias dan kurang efisien.

Penelitian ini disusun dalam rangka **National Statistics Competition (NSC)** dan bertujuan memberikan pemahaman spasial terhadap faktor-faktor yang memengaruhi TPT sebagai dasar perumusan kebijakan ketenagakerjaan yang lebih tepat sasaran.

---

## 🎯 Tujuan Penelitian

1. Mendeskripsikan pola spasial **Tingkat Pengangguran Terbuka (TPT)** di Pulau Jawa.
2. Menganalisis faktor-faktor yang memengaruhi TPT menggunakan **model regresi global (OLS)** dan **model lokal (GWR)**.
3. Membandingkan performa model global dan model GWR.
4. Mengidentifikasi perbedaan pengaruh variabel penjelas antar wilayah kabupaten/kota.

---

## 🗺️ Data dan Variabel

### Sumber Data

* **Badan Pusat Statistik (BPS)**
* Unit analisis: **Kabupaten/Kota di Pulau Jawa**
* Jenis data: **Cross-section**

### Variabel Dependen

* **Tingkat Pengangguran Terbuka (TPT)**

### Variabel Independen

* Persentase Rumah Tangga dengan **Sanitasi Layak**
* **Persentase Penduduk Miskin**
* **Rata-rata Lama Sekolah**
* **Usia Harapan Hidup**
* **Pengeluaran per Kapita per Bulan**

---

## 🧠 Metodologi

### 1️⃣ Analisis Deskriptif Spasial

* Pemetaan TPT dan variabel penjelas
* Identifikasi pola spasial antar wilayah

### 2️⃣ Pemodelan Regresi Global (OLS)

* Estimasi parameter menggunakan Ordinary Least Squares
* Uji asumsi klasik:

  * Normalitas (Shapiro–Wilk)
  * Homoskedastisitas (Breusch–Pagan)
  * Multikolinieritas (Variance Inflation Factor / VIF)

### 3️⃣ Pemodelan Geographically Weighted Regression (GWR)

* Pengujian beberapa fungsi kernel:

  * Fixed Gaussian
  * Fixed Bisquare
  * Fixed Exponential
  * Adaptive Gaussian
  * Adaptive Bisquare
  * Adaptive Exponential
* Pemilihan bandwidth optimal berdasarkan:

  * AICc
  * BIC
  * Adjusted R-Squared

### 4️⃣ Evaluasi dan Perbandingan Model

* Perbandingan model OLS dan GWR menggunakan:

  * AICc
  * BIC
  * Adjusted R-Squared
* Identifikasi variabel signifikan secara spasial

---

## 📈 Hasil Utama

### 🔹 Pola Spasial TPT

* TPT cenderung **bervariasi dan relatif rendah di wilayah tengah hingga timur Pulau Jawa**.

### 🔹 Model Terbaik

* Model **GWR dengan kernel Fixed Bisquare** memberikan performa terbaik.
* Perbandingan model:

  * Adjusted R² OLS: **25,95%**
  * Adjusted R² GWR: **45,88%**
  * AICc dan BIC model GWR lebih rendah dibanding model global.

### 🔹 Signifikansi Variabel

* **Sanitasi layak** dan **usia harapan hidup** signifikan memengaruhi TPT di seluruh wilayah.
* **Pengeluaran per kapita** signifikan di **10 kabupaten/kota** tertentu.
* **Rata-rata lama sekolah** tidak signifikan secara spasial di Pulau Jawa.

---

## 🧩 Segmentasi Wilayah

Berdasarkan variabel yang signifikan, terbentuk **dua kelompok wilayah kabupaten/kota** dengan karakteristik ekonomi dan sosial yang berbeda, yang menunjukkan perlunya **kebijakan ketenagakerjaan berbasis wilayah**.

---

## 🛠️ Tools & Teknologi

* **R** (R Markdown)
* Library utama:

  * sp, sf
  * GWmodel
  * spdep
  * ggplot2
  * tmap

---

## 👤 Penulis

**Dutatama Rosewika Taufiq Hadihardaya**
Politeknik Statistika STIS
National Statistics Competition (NSC)
Statistika Ria dan Festival Sains Data (Satria Data) 2024

---

## 📜 Lisensi

Proyek ini disusun untuk **keperluan National Statistics Competition (NSC) Satria Data 2024**.
Data bersumber dari BPS dan digunakan sesuai ketentuan yang berlaku.

---

> *“Pendekatan spasial bukan hanya meningkatkan akurasi model, tetapi juga memperkaya pemahaman kebijakan berbasis wilayah.”*
