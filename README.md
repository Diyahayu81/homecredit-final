# homecredit-final
"Studi Kasus Home Credit - Kredit Scoring"
# Home Credit Default Risk Prediction

## 🎯 Objective
Memprediksi risiko gagal bayar kredit menggunakan data pelanggan Home Credit. Hasil model digunakan untuk membantu pengambilan keputusan pemberian pinjaman.

## 📁 Dataset
- `application_train.csv`, `application_test.csv`
- Ditambah: `bureau.csv`, `POS_CASH_balance.csv`, dll.

## 🔍 EDA & Preprocessing
- Analisis missing value, outlier
- Feature engineering: skor eksternal, usia, penghasilan

## ⚙️ Modeling
- Logistic Regression (dengan `class_weight=balanced`)
- XGBoost (tuned)

## 📊 Hasil Evaluasi
- ROC AUC XGBoost (tuned): **0.7537**
- Recall gagal bayar: **0.67**

## 🧠 Insight
- Skor eksternal dan usia paling menentukan
- Nasabah muda & skor rendah lebih berisiko gagal bayar

## 📦 Files
- `HomeCredit_Final.ipynb`: seluruh pipeline
- `submission_xgb_tuned.csv`: hasil prediksi test
- `slides/Presentasi_HomeCredit.pptx`: slide 10 halaman

## 🔗 Link Presentasi
[Masukkan link Google Drive atau PDF GitHub untuk slide]
