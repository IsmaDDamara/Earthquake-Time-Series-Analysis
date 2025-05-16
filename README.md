# 🌍 Earthquake Time Series Analysis
## 📌 Deskripsi Proyek
Indonesia berada di wilayah Cincin Api (Ring of Fire) yang merupakan pertemuan lempeng tektonik, sehingga sering mengalami gempa bumi. Berdasarkan data BPS dari BMKG, sepanjang tahun 2022 tercatat 10.843 aktivitas gempa, dengan 217 di antaranya berkekuatan di atas 5 magnitudo. Gempa-gempa ini menimbulkan kerusakan yang signifikan.

## 🎯 Tujuan
Menganalisis data gempa bumi di Indonesia untuk membangun model prediksi kekuatan gempa menggunakan metode machine learning.

## ❓ Permasalahan
- Bagaimana tren kekuatan gempa bumi dari waktu ke waktu?

- Apakah kekuatan gempa dapat diprediksi dari waktu kejadian, lokasi, dan kedalaman?

- Model machine learning apa yang paling efektif dalam memprediksi kekuatan gempa?

## 🗂️ Dataset
Dataset yang digunakan bersumber dari kaggle, dataset ini berisi informasi tanggal, tempat, kedalaman, dan kekuatan gempa yang terjadi dari tahun 2008 - awal tahun 2023 yang diambil oleh Badan Meteorologi Klimatologi dan Geofisika ( BMKG), berikut adalah link datanya : https://www.kaggle.com/datasets/kekavigi/earthquakes-in-indonesia

## 📊 Analisis yang Dilakukan
Analisis yang dilakukan untuk menyelesaikan permasalahan ini, adalah sebgaia berikut: 
- Pra-pemrosesan data: membersihkan data, mengonversi waktu, dan menangani nilai ekstrem dengan Z-Score.

- Visualisasi: menganalisis tren gempa berdasarkan waktu, lokasi, dan kekuatan.

- Modeling: membandingkan beberapa model ML menggunakan LazyPredict, lalu memilih model terbaik (misalnya Linear Regression).

- Evaluasi: menggunakan MSE dan R² Score.

## 💡 Insight Utama
- Model ARIMA digunakan untuk meramalkan deret waktu non-musiman berdasarkan data masa lalu. Kelebihannya adalah sederhana dan akurat untuk jangka pendek, tetapi kurang cocok untuk jangka panjang dan data berpola nonlinier.

- Model Exponential Smoothing meramalkan dengan memberi bobot lebih pada data terbaru. Metode ini cepat dan mudah digunakan, namun kurang akurat untuk jangka panjang dan sensitif terhadap pemilihan parameter.

- Model SARIMAX cocok untuk data musiman dengan variabel eksternal. Kelebihannya adalah mampu menangani pola kompleks, tetapi membutuhkan data lengkap dan komputasi yang lebih berat.

## 🧠 Kesimpulan
Model ARIMA memiliki RMSE terendah (0,340) dibanding Exponential Smoothing dan SARIMAX, sehingga paling akurat dan cocok untuk prediksi kekuatan gempa bumi.

🚀 Cara Menjalankan
Clone repository ini:

```bash
git clone https://github.com/IsmaDDamara/Earthquake-Time-Series-Analysis.git
```

Jalankan Jupyter Notebook:

```bash
jupyter notebook Earthquake_Analysis.ipynb
```