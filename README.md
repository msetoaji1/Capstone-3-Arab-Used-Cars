# 🚗 Prediksi Harga Mobil Bekas di Arab Saudi

## 📌 Gambaran Proyek
Halo! Proyek ini berfokus pada prediksi harga mobil bekas di Arab Saudi menggunakan machine learning. Saya mencoba berbagai algoritma untuk menemukan model terbaik yang dapat memperkirakan harga mobil secara akurat. Proyek ini bisa sangat bermanfaat bagi penjual dan pembeli mobil untuk menentukan harga yang wajar di pasar.

## 📊 Dataset
**Dataset:** Mobil Bekas di Arab Saudi
- **Total Data:** 5624 entri
- **Fitur Utama:**
  - `Price` - Harga mobil (target prediksi)
  - `Year` - Tahun pembuatan
  - `Mileage` - Jarak tempuh (kilometer)
  - `Engine_Size` - Kapasitas mesin (liter)
  - `Region` - Wilayah penjualan
  - `Make` - Merek mobil
  - `Gear_Type` - Jenis transmisi (manual/otomatis)
  - `Options` - Fitur tambahan (sunroof, navigasi, dll.)
  - `Negotiable` - Indikasi apakah harga bisa dinegosiasikan

---

## ⚙️ Alur Kerja Proyek
### 1. **Memahami Masalah**
- **Tujuan:** Memprediksi harga mobil bekas.
- **Siapa yang Diuntungkan?** Dealer mobil, platform otomotif, dan pembeli yang ingin mendapatkan harga yang sesuai.

### 2. **Pembersihan dan Pemrosesan Data**
- **Langkah yang Dilakukan:**
  - Menghapus 4 entri duplikat.
  - Menghilangkan outlier menggunakan metode IQR.
  - Mengisi harga yang kosong (untuk mobil yang dapat dinegosiasikan) dengan median harga mobil serupa.
- **Feature Engineering:**
  - Menambahkan fitur `Age of Car` dengan cara mengurangkan `Year` dari 2024.
  - Melakukan transformasi log pada `Price` untuk mengatasi distribusi yang tidak merata.
  - Mengkategorikan `Mileage`, `Engine_Size`, dan `Car_Age` (Low, Medium, High).
  - Membuat fitur interaksi dengan mengalikan `Engine_Size` dan `Mileage`.

### 3. **Pemodelan dan Evaluasi**
- **Model yang Dicoba:**
  - CatBoost
  - XGBoost
  - Random Forest (**Model Terbaik!**)
- **Metrik Evaluasi:**
  - **Mean Absolute Error (MAE)**
  - **R-squared (R²)**
  - **Mean Relative Error (MRE)**
- **Model Terbaik:**
  - **Random Forest** – R²: **0.91** | MAE: **6523.37** | MRE: **11.96%**

---

## 📈 Hasil Utama dan Insight
- **Faktor yang Paling Mempengaruhi Harga:**
  - **Tahun, Jarak Tempuh, dan Ukuran Mesin.**
  - Merek seperti Toyota dan Hyundai mendominasi pasar.
- Model **Random Forest** memberikan hasil terbaik dengan akurasi tertinggi.
- Mobil dengan jarak tempuh rendah dan mesin yang lebih besar cenderung memiliki harga lebih tinggi.

---

## 📁 Struktur Proyek
```
|-- data
|   |-- saudi_used_cars.xlsx        # Dataset mentah
|-- notebooks
|   |-- used_car_price_prediction.ipynb  # Notebook dengan semua analisis
|-- docs
|   |-- project_report.docx         # Laporan proyek lengkap
|-- README.md                       # File ini
```

---

## 📌 File yang Perlu Diperhatikan
- **data_saudi_used.xlsx** – Dataset yang digunakan.
- **used_car_price_prediction.ipynb** – Semua kode dan langkah pemodelan.
- **Saudi Arabia Used Cars.docx** – Laporan lengkap tentang proyek ini.

---

## 🔮 Pengembangan Selanjutnya
- Tambahkan fitur baru seperti riwayat kecelakaan atau catatan servis.
- Implementasikan model dalam bentuk aplikasi web sederhana.
- Perluas dataset dengan data dari lebih banyak wilayah dan merek.

---

## 📩 Hubungi Saya
Jika ada pertanyaan atau ingin berdiskusi, jangan ragu untuk menghubungi saya!
- **Email:** mwisnusetoaji@gmail.com
- **GitHub:** [msetoaji](https://github.com/msetoaji)

---


