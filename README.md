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

## 📦 Requirements

Install semua dependensi dengan:

```bash
pip install -r requirements.txt
