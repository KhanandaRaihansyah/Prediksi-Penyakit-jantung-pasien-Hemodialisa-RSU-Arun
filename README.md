<<<<<<< HEAD
# Prediksi-Penyakit-jantung-pasien-Hemodialisa-RSU-Arun
Proyek ini bertujuan untuk membangun model Machine Learning (Klasifikasi) yang mampu memprediksi risiko penyakit jantung (cardiovascular complications) pada pasien gagal ginjal kronis yang sedang menjalani terapi Hemodialisa (Cuci Darah) di RSU Arun.
=======
# 📋 Prediksi Penyakit Jantung Pasien Hemodialisa RSU Arun

Proyek ini bertujuan untuk membangun model **Machine Learning (Klasifikasi)** yang mampu memprediksi risiko penyakit jantung (*cardiovascular complications*) pada pasien gagal ginjal kronis yang menjalani terapi **Hemodialisa (Cuci Darah)** di **RSU Arun**.

---

## 📌 Ringkasan Proyek
Komplikasi kardiovaskular merupakan salah satu penyebab utama mortalitas pada pasien hemodialisa. Dengan memanfaatkan data medis dan klinis pasien, model ini dikembangkan untuk mendeteksi dini risiko penyakit jantung sehingga tenaga medis dapat memberikan penanganan pencegahan yang lebih tepat dan cepat.

---

## 📊 Dataset & Fitur Medis
Dataset yang digunakan berasal dari data rekam medis pasien RSU Arun (`Data_Hd_Arun.csv`) berjumlah **160 sampel pasien** dengan 11 fitur klinis awal dan **1 variabel target binary**:
* **`target`**: `0` = Pasien Stabil / Tanpa Komplikasi Jantung, `1` = Pasien Berisiko Penyakit Jantung.

### Fitur-Fitur Klinis Utama:
- **`age`**: Usia pasien (tahun).
- **`sex`**: Jenis kelamin (0 = Perempuan, 1 = Laki-Laki).
- **`Tensi_Pre_HD`**: Tekanan darah sistolik sebelum hemodialisa (mmHg).
- **`Tensi_Post_HD`**: Tekanan darah sistolik setelah hemodialisa (mmHg).
- **`IDWG`** (*Interdialytic Weight Gain*): Kenaikan berat badan pasien antar sesi hemodialisa (kg).
- **`Hemoglobin`**: Kadar hemoglobin darah (g/dL).
- **`Ureum`**: Kadar ureum darah (mg/dL).
- **`Kreatinin`**: Kadar kreatinin serum (mg/dL).
- **`Riwayat_Diabetes`**: Riwayat medis diabetes mellitus (0 = Tidak, 1 = Ya).
- **`Riwayat_Hipertensi`**: Riwayat medis hipertensi (0 = Tidak, 1 = Ya).
- **`Lama_Bulan_HD`**: Durasi pasien telah menjalani terapi hemodialisa (bulan).

### 🛠️ Feature Engineering:
- **`Drop_Tensi`** (`Tensi_Pre_HD - Tensi_Post_HD`): Mengukur besarnya penurunan tekanan darah pasca-cuci darah (indikator hipotensi intradialitik).
- **`Rasio_Ur_Cr`** (`Ureum / Kreatinin`): Menilai efektivitas adekuasi dialisis dan status katabolisme protein pasien.

---

## 🏆 Hasil Evaluasi Model
Model terbaik yang diperoleh setelah optimasi hyperparameter (*GridSearchCV*) adalah **Support Vector Machine (SVM Optimized)** dengan kernel `linear`:

* **Akurasi (Accuracy)**: **96.88%** (31 dari 32 data uji terklasifikasi benar)
* **ROC-AUC Score**: **0.9988** (~99.88%)
* **Precision (Kelas Risk)**: **1.00** (100%)
* **Recall (Kelas Risk)**: **0.94** (94.4%)
* **F1-Score**: **0.97**

---

## 💻 Teknologi yang Digunakan
- **Python 3**
- **Pandas** & **NumPy**
- **Matplotlib** & **Seaborn**
- **Scikit-Learn** (`StandardScaler`, `DecisionTreeClassifier`, `RandomForestClassifier`, `SVC`, `GridSearchCV`, `classification_report`, `confusion_matrix`, `roc_auc_score`)

---

## 📁 Berkas Utama
- `Prediksi_Penyakit_jantung_pasien_Hemodialisa_RSUArun.ipynb`: Notebook Jupyter berisi alur data, EDA, pemodelan, dan evaluasi.
- `Data_Hd_Arun.csv`: Dataset klinis pasien hemodialisa RSU Arun.
>>>>>>> 07d244b (Add project notebook, dataset, and documentation for Prediksi Penyakit Jantung Pasien Hemodialisa RSU Arun)
