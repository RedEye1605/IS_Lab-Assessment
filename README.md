# 🩺 Diabetes Prediction — Assessment Lab IS 2025  

Proyek ini merupakan implementasi **machine learning** untuk memprediksi status glikemik seseorang (**Normal / Pre-diabetes / Diabetes**) berdasarkan data klinis dan laboratorium.  
Dataset bersumber dari masyarakat Irak (*Medical City Hospital* & *Al-Kindy Teaching Hospital*), diakses melalui [Mendeley Data](https://data.mendeley.com/datasets/wj9rwkp9c2/1).  

## ✨ Tujuan  
- Mengembangkan model prediktif yang akurat dan dapat dipertanggungjawabkan.  
- Mengeksplorasi faktor klinis (HbA1c, BMI, profil lipid, usia, dll) yang berkontribusi pada klasifikasi diabetes.  
- Menangani masalah **class imbalance** dengan SMOTE untuk meningkatkan performa pada kelas minoritas.  

## 🔬 Metodologi  
1. **EDA (Exploratory Data Analysis)** → distribusi data, korelasi, insight klinis.  
2. **Data Cleaning & Preprocessing** → normalisasi label, scaling numerik, one-hot encoding kategorikal.  
3. **Resampling (SMOTE)** → hanya diterapkan pada data training untuk mengatasi imbalance.  
4. **Baseline Models** → Logistic Regression, Random Forest, Gradient Boosting, SVC.  
5. **Model Selection & Tuning** → Gradient Boosting dipilih dan dioptimasi dengan GridSearchCV.  
6. **Evaluation** → Accuracy, F1-weighted, Macro ROC-AUC, Classification Report, Confusion Matrix.  
7. **Interpretasi** → Feature importance & visualisasi.  

## 📊 Hasil Utama  
- **Gradient Boosting Classifier (tuned)** menjadi model terbaik.  
- **HbA1c** terbukti sebagai faktor dominan, diikuti BMI dan biomarker lipid.  
- Performansi model sangat baik dengan F1-weighted tinggi dan Macro ROC-AUC mendekati 1.  

## 📌 Insight  
- Penanganan imbalance (SMOTE) terbukti meningkatkan performa kelas minoritas.  
- Model berbasis boosting lebih unggul dibandingkan baseline linear atau bagging.  
- Potensi besar untuk **clinical decision support system** dalam skrining awal diabetes.  

## 🚀 Struktur Repo  
```
.
├── diabetes_lab_IS2025.ipynb   # Notebook utama (storytelling + code)
├── Dataset of Diabetes .csv    # Dataset (perlu disimpan manual, sesuai lisensi)
├── best_model_diabetes.pkl     # Model terlatih (opsional)
└── README.md                   # Deskripsi proyek
```

## ⚠️ Catatan  
- Dataset tidak berisi PII (sudah dianonimkan).  
- Model ini **hanya alat bantu** → tidak menggantikan diagnosis klinis.  
- Untuk penggunaan nyata, perlu validasi eksternal dan kalibrasi probabilitas.  
