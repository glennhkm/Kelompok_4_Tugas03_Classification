## Anggota Tim (Kelompok 4)
- Glenn Hakim (2208107010072)
- Ahmad Syah Ramadhan (2208107010033)
- Andika Pebriansyah (2208107010058)
- Nisa Rianti (2208107010018)
- Nuri Masyithah (2208107010006)

# 🎯 Prediksi Penempatan Kerja Mahasiswa

Proyek ini bertujuan untuk membangun model klasifikasi guna memprediksi apakah seorang mahasiswa akan mendapatkan penempatan kerja atau tidak, berdasarkan data akademik, latar belakang pendidikan, dan pengalaman kerja.

---

## 📂 Dataset

Dataset diambil dari Kaggle:  
🔗 [Job Placement Dataset by Ahsan81](https://www.kaggle.com/datasets/ahsan81/job-placement-dataset)

Fitur utama dalam dataset ini meliputi:
- Nilai akademik (SSC, HSC, Degree, MBA)
- Subjek dan board pendidikan
- Pengalaman kerja
- Spesialisasi MBA
- Skor tes penempatan kerja
- Status penempatan (`Placed` atau `Not Placed`)

---

## ⚙️ Langkah-langkah Preprocessing

1. ✅ **Penanganan Missing Value**: Tidak ditemukan missing value dalam dataset.
2. 🧬 **Encoding**: Variabel kategorikal diencode menggunakan One-Hot Encoding.
3. 📏 **Standardisasi**: Fitur numerik distandardisasi dengan `StandardScaler`.
4. 🧠 **Feature Engineering**:
   - Selisih nilai akhir dan sekolah
   - Rata-rata akademik
   - Rasio antara nilai akademik dan tes kerja
5. 🎯 **Feature Selection**: Menggunakan `SelectKBest` dengan f_classif.
6. ⚖️ **Handling Imbalanced Class**: Menggunakan SMOTE untuk oversampling kelas minoritas.
7. 🔧 **Hyperparameter Tuning**: GridSearchCV digunakan untuk mencari parameter terbaik model.

---

## 🧪 Modeling dan Evaluasi

Beberapa model telah diuji:
- Logistic Regression (dengan tuning)
- K-Nearest Neighbors
- Naive Bayes
- Decision Tree

📌 **Model Terbaik**: `Logistic Regression (Optimized)`
- **Akurasi**: 87.04%
- **ROC AUC**: 0.9364
- **Log Loss**: 0.3064

**Evaluasi Model Terbaik (Class: Placed)**:
- Precision: 0.9167
- Recall: 0.8919
- F1-Score: 0.9041

---

## 🔍 Insight dan Temuan

1. **Skor Ujian Penempatan (emp_test_percentage)** adalah fitur paling penting.
2. **Pengalaman kerja** juga mempengaruhi status penempatan secara signifikan.
3. Model menghasilkan prediksi yang sangat baik dengan AUC di atas 0.93.

---

## ✅ Rekomendasi

- 🎯 Tingkatkan skor pada ujian penempatan kerja.
- 💼 Dapatkan pengalaman kerja sebelum melamar pekerjaan.
- 🧭 Fokus pada spesialisasi MBA dengan tingkat penempatan tinggi.
- 📚 Pertahankan konsistensi nilai akademik di setiap jenjang pendidikan.

---

## Hasil Analisis

![image](https://github.com/user-attachments/assets/ff33577d-ef3a-4015-8cd6-730c2196a33b)

Model Logistic Regression menunjukkan bahwa faktor yang paling meningkatkan peluang penempatan kerja adalah pengalaman kerja dan performa akademik yang konsisten (ssc_percentage, overall_academic_avg, hsc_percentage). Sebaliknya, spesialisasi Marketing & HR, nilai MBA tinggi, dan perbedaan nilai antar jenjang pendidikan justru menurunkan peluang. Faktor seperti jenis kelamin dan jurusan memiliki pengaruh kecil terhadap hasil akhir.

## Hasil Analisis
================================================================================
KESIMPULAN HASIL ANALISIS
================================================================================
Model terbaik adalah Logistic Regression (Optimized) dengan akurasi 0.8704
ROC AUC: 0.9364
Log Loss: 0.3064

Metrik Evaluasi Model Terbaik:
Precision (Ditempatkan): 0.9167
Recall (Ditempatkan): 0.8919
F1-Score (Ditempatkan): 0.9041

Preprocessing dan feature engineering yang diterapkan:
1. Penanganan missing values (tidak ada missing values dalam dataset)
2. One-Hot Encoding untuk variabel kategorikal
3. Standardisasi fitur numerik
4. Pembuatan fitur baru: selisih nilai, rata-rata akademik, dan rasio
5. Pemilihan fitur menggunakan SelectKBest
6. Penanganan ketidakseimbangan kelas menggunakan SMOTE
7. Tuning hyperparameter untuk meningkatkan performa model

Temuan Penting:
1. Fitur yang paling berpengaruh dalam prediksi penempatan kerja adalah persentase pada ujian penempatan (emp_test_percentage)
2. Pengalaman kerja juga berpengaruh signifikan terhadap keberhasilan penempatan kerja
3. Model berhasil mencapai akurasi lebih dari 93%, yang mengindikasikan prediksi yang sangat baik
...
1. Fokus pada peningkatan performa di ujian penempatan kerja
2. Mendapatkan pengalaman kerja sebelum melamar pekerjaan sangat direkomendasikan
3. Fokus pada spesialisasi yang memiliki tingkat penempatan lebih tinggi
4. Mempertahankan nilai akademik yang konsisten di setiap tingkat pendidikan
