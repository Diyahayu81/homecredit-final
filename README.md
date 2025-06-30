# 🏦 Home Credit Default Risk Prediction

## 📌 Project Overview

Studi kasus ini bertujuan untuk membantu Home Credit dalam memprediksi risiko gagal bayar pelanggan menggunakan pendekatan Machine Learning. Dengan sistem prediksi yang tepat, perusahaan dapat:
- Memberikan pinjaman kepada pelanggan yang benar-benar mampu membayar
- Menyesuaikan tenor dan jumlah pinjaman berdasarkan risiko
- Mengurangi kerugian akibat default
  
## 📝 Extended Description

Home Credit berupaya meningkatkan akurasi dalam pemberian pinjaman dengan pendekatan data-driven. Tantangannya adalah membedakan nasabah yang berisiko gagal bayar dari mereka yang mampu membayar secara tepat. Salah satu kesalahan yang mahal adalah menolak calon nasabah yang sebenarnya mampu membayar.

### 🎯 Tujuan Proyek

Tujuan utama proyek ini adalah membangun model Machine Learning untuk memprediksi kemungkinan default pelanggan berdasarkan informasi pribadi, pekerjaan, keuangan, dan riwayat kredit mereka. Proyek ini mencakup eksplorasi data, preprocessing, pembuatan model prediktif, dan analisa dampak bisnisnya.

### 🧾 Dataset

Dataset berasal dari kompetisi Home Credit Default Risk dan terdiri dari:
- `application_train.csv`, `application_test.csv`: data utama aplikasi pinjaman
- `bureau.csv`, `previous_application.csv`, `credit_card_balance.csv`, dll: data tambahan terkait riwayat pinjaman dan aktivitas keuangan nasabah

Beberapa fitur penting meliputi:
- **EXT_SOURCE_1/2/3**: skor eksternal dari lembaga pihak ketiga
- **DAYS_BIRTH**: usia nasabah
- **AMT_INCOME_TOTAL**: total pendapatan tahunan

### ⚙️ Pendekatan Teknis

1. **EDA**: analisis distribusi fitur, missing values, korelasi dengan TARGET
2. **Preprocessing**:
   - Imputasi nilai kosong
   - One-hot encoding fitur kategorikal
   - Feature engineering: rasio pendapatan, durasi kerja, skor eksternal gabungan
   - Penanganan class imbalance dengan class weighting dan scale_pos_weight
3. **Modeling**:
   - Logistic Regression (baseline & balanced)
   - XGBoost (tuned via GridSearch)
4. **Evaluasi**:
   - ROC AUC sebagai metrik utama
   - Recall class 1 untuk menilai kemampuan deteksi default

### 📊 Hasil Evaluasi

| Model                 | ROC AUC | Recall (class 1) | Catatan                      |
|----------------------|---------|------------------|------------------------------|
| Logistic Regression  | 0.745   | 0.67 (balanced)  | Model baseline interpretatif |
| XGBoost (Tuned)      | 0.7536  | 0.67             | Model terbaik dari eksperimen|

Model XGBoost yang telah dituning menghasilkan performa terbaik dengan ROC AUC 0.7536 dan recall 67% pada class default (1).

### 💡 Insight Bisnis

- **Nasabah muda** dengan skor eksternal rendah lebih berisiko gagal bayar.
- Fitur `EXT_SOURCE` sangat dominan, menunjukkan nilai informasi eksternal dalam penilaian kredit.
- Skema pinjaman dapat disesuaikan: tenor pendek dan jumlah cicilan ringan untuk kelompok berisiko tinggi.

### 📦 Deliverables

- `HomeCredit_Final.ipynb`: pipeline analisis end-to-end
- `submission_xgb_tuned.csv`: hasil prediksi test set
- `Presentasi_HomeCredit.pptx`: slide presentasi 10 halaman
- `README.md`: dokumentasi lengkap project


---

## 🎯 Business Objective

Membangun model prediksi default risk berdasarkan data nasabah yang mencakup informasi pribadi, finansial, dan riwayat kredit, untuk mendukung proses approval pinjaman.

---

## 📁 Repository Structure


---

## ⚙️ Methodology

1. **EDA & Preprocessing**
   - Handling missing values
   - Feature engineering (rasio, usia, skor eksternal)
   - Encoding kategorikal & balancing data (class_weight, scale_pos_weight)

2. **Modeling**
   - **Logistic Regression**: baseline interpretable model
   - **XGBoost (tuned)**: model terbaik dengan ROC AUC 0.7536
   - Evaluasi: ROC AUC, Recall, Confusion Matrix

---

## 🧠 Insights & Recommendations

- Fitur `EXT_SOURCE_1`, `DAYS_BIRTH`, dan `AMT_INCOME_TOTAL` berkontribusi besar terhadap risiko default
- Nasabah muda dan berpenghasilan rendah memiliki kecenderungan gagal bayar lebih tinggi
- Nasabah dengan risiko tinggi sebaiknya diberikan opsi pinjaman dengan cicilan ringan dan tenor pendek

---

## 📊 Performance Summary

| Model                 | ROC AUC | Recall (class 1) | Catatan                  |
|----------------------|---------|------------------|--------------------------|
| Logistic Regression  | 0.745   | 0.67 (balanced)  | Model baseline interpretatif |
| XGBoost (Tuned)      | 0.7536  | 0.67             | Model final terbaik      |

---

## 🔗 Resources & Link

- 🔍 [Tampilan notebook di nbviewer](https://nbviewer.org/github/Diyahayu81/homecredit-final/blob/main/HomeCredit_Final.ipynb)
- 📤 [GitHub Repository](https://github.com/Diyahayu81/homecredit-final)
- 🎞️ Slide Presentasi: `Presentasi_HomeCredit.pptx`

---

## 🙋‍♀️ About Me

Diyah Ayu – Data Science enthusiast  
Final Project - Home Credit Case Study  
📫 [LinkedIn / Email opsional jika ingin ditambahkan]

---

## 📝 License

This project is for educational use. Dataset source: [Home Credit Default Risk - Kaggle](https://www.kaggle.com/competitions/home-credit-default-risk)
