# Analisis-dan-Prediksi-Tipe-Stres-Berdasarkan-Faktor-Demografis
Repository ini berisi Capstone Project yang saya buat dalam rangka mengikuti program Student Developer Initiative dari HACKTIV8 dan IBM SkillsBuild, dengan topik "Data Classification and Summarization".  Project ini berfokus pada analisis dataset data_stress untuk memahami faktor-faktor yang berhubungan dengan jenis stres yang dialami individu.

# Stress Analysis using Machine Learning  

## 📌 Overview  
Proyek ini menganalisis dataset **data_stress** untuk mengidentifikasi faktor-faktor yang berhubungan dengan jenis stres yang dialami individu.  
Analisis dilakukan menggunakan pendekatan *exploratory data analysis* (EDA) serta pemodelan dengan **Random Forest** dan **XGBoost** untuk klasifikasi.  

Tujuan utama penelitian ini adalah:  
- Mengidentifikasi faktor dominan yang memengaruhi jenis stres.  
- Membandingkan performa model machine learning dalam mengklasifikasikan jenis stres.  
- Memberikan insight mengenai peran faktor sosial-ekonomi dan faktor individu terhadap jenis stres.  

---

## 📂 Dataset  
- **Nama dataset**: `data_stress`  
- **Target variabel**: `Usia, jenis kelamin, pendidikan, dan pendapatan`  
- **Jumlah faktor potensial**: 27 (tidak termasuk target variabel)  

> 🔗 Dataset link: (https://www.kaggle.com/datasets/mdsultanulislamovi/student-stress-monitoring-datasets)

---

## 📊 Insights & Findings  

### 1. Analisis Data  
- **Eustress** adalah jenis stres yang paling dominan, khususnya pada kelompok dengan *High to Moderate Education Level* dan *Lower Middle Income*.  
- Pada kelompok tersebut, **No Stress** lebih umum dialami dibandingkan dengan **Distress**.  
- Analisis usia menunjukkan:  
  - **Distress** lebih banyak dialami individu muda (mean age ~20,6 tahun).  
  - **No Stress** dialami di rentang usia lebih luas (mean age ~19,3 tahun).  
  - **Eustress** muncul pada rentang usia bervariasi dengan standar deviasi lebih tinggi.  
- Individu dengan **Distress** cenderung lebih muda, memiliki pendidikan dan pendapatan rata-rata lebih rendah dibandingkan kelompok **Eustress** atau **No Stress**.  

### 2. Analisis Model  
- **Random Forest**: akurasi 87%, F1-score 0.86.  
- **XGBoost**: akurasi 89%, F1-score 0.88.  
- **Imbalance data** ditangani dengan **SMOTE**, yang meningkatkan performa kedua model.  
- **Optimasi Hyperparameter** (GridSearchCV):  
  - Random Forest → `n_estimators=100`, `max_features='sqrt'`.  
  - XGBoost → `n_estimators=150`, `learning_rate=0.1`, `max_depth=6`, `subsample=0.8`.  
- **XGBoost** menunjukkan kinerja terbaik dalam klasifikasi.  

---

## 🤖 AI Support Explanation  
Selama proses analisis dan pemodelan, saya mendapatkan dukungan dari **IBM Granite** yang berperan dalam:  
- Membantu menemukan berbagai **key findings** dari data, termasuk pola stres berdasarkan usia, pendidikan, dan pendapatan.  
- Memberikan rekomendasi dalam **pemilihan metode penanganan imbalance data** (SMOTE).  
- Membantu dalam **pemilihan serta optimasi hyperparameter** untuk model Random Forest dan XGBoost.  
- Mendukung pembuatan laporan analisis yang lebih terstruktur dan mudah dipahami.  

Dengan bantuan **IBM Granite**, proses analisis menjadi lebih cepat, akurat, dan sistematis.  

---
