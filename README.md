# 🏦 Home Credit Default Risk Prediction

## 📌 Project Overview

Studi kasus ini bertujuan untuk membantu Home Credit dalam memprediksi risiko gagal bayar pelanggan menggunakan pendekatan Machine Learning. Dengan sistem prediksi yang tepat, perusahaan dapat:
- Memberikan pinjaman kepada pelanggan yang benar-benar mampu membayar
- Menyesuaikan tenor dan jumlah pinjaman berdasarkan risiko
- Mengurangi kerugian akibat default

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
