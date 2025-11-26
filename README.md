# 🚗 Used Car Price Prediction (US Market)  
📌 Machine Learning Regression Model with Business Impact Analysis

---

## 📖 Overview

Project ini dibuat berdasarkan business case dimana perusahaan membutuhkan sistem untuk membantu menilai harga beli mobil bekas secara objektif dan data-driven. Dengan model Machine Learning, perusahaan dapat meningkatkan efisiensi proses appraisal, meminimalkan human bias, dan mempercepat keputusan pembelian.

Model ini dapat dijadikan fondasi untuk:

- 🔹 Sistem internal penilaian harga (buying decision support)
- 🔹 Marketplace pricing model (similar to Carfax / Kelley Blue Book)
- 🔹 Automation appraisal untuk dealer atau leasing company

---

## 🎯 Business Problem

Saat ini penentuan harga mobil bekas masih banyak dilakukan secara manual dan subjektif. Hal ini menghasilkan:

- Ketidak konsistenan pricing antar cabang/dealer  
- Potensi kerugian akibat overpaying (membeli terlalu mahal)  
- Proses appraisal yang memakan waktu  

---

## 🎯 Project Goal

✔️ Membantu perusahaan menentukan harga beli mobil bekas yang **terstandarisasi** berdasarkan model Machine Learning.

---

## 🎯 Objectives

- Membangun tools/model Machine Learning untuk memprediksi harga mobil bekas berdasarkan kondisi asli kendaraan.
- Mengubah proses appraisal yang sebelumnya manual menjadi **data-driven automation**.

---

## 📈 Business Metrics

| Indicator | Dampak |
|----------|--------|
| 🏷️ Sales Pembelian | Membantu menentukan harga optimal untuk pembelian |
| ⏱️ Efisiensi Waktu | Mengurangi proses manual penilaian kendaraan |
| 🎯 Accuracy Pricing | Membantu menghindari underpricing atau overpaying |

---

## 🧪 Dataset Summary

Dataset berisi data kendaraan dengan informasi seperti:

- Tahun kendaraan (`year`)
- Jarak tempuh (`odometer`)
- Kondisi kendaraan (`condition`)
- Merk & model (`make`, `body_type`)
- Warna (`color`)
- Harga aktual kendaraan (`price`)

📝 Detail eksplorasi dan preprocessing tersedia di: https://github.com/MuhArifBudiman/Car-Used-Price/blob/master/Final_Project_Car_Used_Price(Rev).ipynb


---

## 🧠 Modeling & Selected Model

Beberapa model telah dicoba, dan setelah evaluasi serta tuning, model terbaik yang dipilih adalah:

👉 **XGBoost Regressor**  

Model ini dipilih karena:

- Performa terbaik dalam hal R² score
- Dapat menangani fitur kategorikal dan numerikal dengan baik
- Mendukung interpretabilitas melalui feature importance

---

## 📊 Feature Importance

Hasil menunjukkan fitur yang paling mempengaruhi harga mobil bekas:

| Rank | Feature | Insight |
|------|---------|--------|
| 1 | odometer | Semakin besar jarak tempuh → harga turun signifikan |
| 2 | body_label | Jenis body memengaruhi daya tarik pembeli |
| 3 | year | Mobil lebih baru → harga lebih tinggi |
| 4 | make_label | Brand memiliki nilai pasar berbeda |
| 5 | condition | Semakin baik kondisi → semakin mahal |
| 6 | color_label | Relatif kecil namun tetap berpengaruh |

📈 Visualisasi tersedia di folder `/visualization`.

---

## 🚀 Recommendations

Berdasarkan hasil model dan analisis fitur, langkah selanjutnya yang direkomendasikan:

- Membangun **web-based application** untuk internal atau publik sebagai pricing engine.
- Integrasi data real-time dari marketplace untuk retraining.
- Mengimplementasikan approval rule engine berdasarkan confidence score model.

---

## 🧪 Running the Project

### 1️⃣ Clone Repository
```sh
git clone https://github.com/username/used-car-price-prediction.git
cd used-car-price-prediction
```

🧾 Business Value Summary

Model ini membantu menciptakan:

- ✔️ Konsistensi dalam penentuan harga beli mobil bekas
- ✔️ Pengambilan keputusan lebih cepat dan objektif
- ✔️ Dasar sistem appraisal otomatis untuk dealer/marketplace
