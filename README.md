# 🥬 Klasifikasi Gambar Sayuran (Vegetable Image Classification)
**Submission Bintang 5 ⭐️⭐️⭐️⭐️⭐️ - Kelas Belajar Pengembangan Machine Learning (Dicoding)**

## 📌 Deskripsi Proyek
Proyek ini merupakan model *Machine Learning* berbasis *Convolutional Neural Network* (CNN) yang dibangun menggunakan TensorFlow dan Keras. Model ini dilatih untuk mengenali dan mengklasifikasikan 15 jenis gambar sayuran secara otomatis. Proyek ini disusun sebagai tugas akhir (submission) untuk kelas **Belajar Pengembangan Machine Learning** di Dicoding Academy.

## ✨ Fitur & Pencapaian (Kriteria Bintang 5)
Proyek ini telah dievaluasi dan memenuhi seluruh kriteria utama beserta kriteria opsional tingkat lanjut:
* **Dataset Skala Besar:** Menggunakan kumpulan data skala besar (total 15.000 gambar untuk data latih).
* **Pembuktian Resolusi Natural:** Melakukan inspeksi menggunakan *library* `PIL` untuk membuktikan bahwa dataset asli memiliki variasi resolusi yang tidak seragam (natural) sebelum masuk ke tahap *preprocessing* (`ImageDataGenerator`).
* **Data Splitting Manual:** Memisahkan data mentah secara mandiri menggunakan modul `split-folders` dengan rasio pembagian **80% Train, 10% Validation, dan 10% Test**.
* **Implementasi Custom Callback:** Membangun fungsi *callback* untuk menghentikan proses *training* secara otomatis ketika metrik akurasi telah menyentuh target **> 96%** guna mencegah *overfitting* dan menghemat waktu komputasi.
* **Deployment-Ready:** Model telah sukses diekspor ke dalam beberapa format untuk kebutuhan *deployment*, yaitu **SavedModel** dan **TF-Lite** (`model.tflite`).
* **Pembuktian Inferensi:** Melakukan pengujian prediksi (*inference*) langsung di dalam *notebook* menggunakan model TF-Lite terhadap gambar sayuran baru.

## 📊 Hasil Pelatihan dan Evaluasi
Model berhasil mempelajari fitur dataset dengan sangat baik dan konstan, melampaui batas minimum akurasi 95% yang disyaratkan oleh penilai. Berikut adalah metrik hasil akhir dari evaluasi model:

* **Data Training** -> Akurasi: **96.69%** | Loss: `0.1011`
* **Data Validation** -> Akurasi: **97.21%** | Loss: `0.1006`
* **Data Testing** -> Akurasi: **97.70%** | Loss: `0.0905`

## 🗂️ Struktur Direktori Utama
```text
submission/
├── saved_model/           # Direktori hasil ekspor model dalam format SavedModel
├── tflite/
│   ├── model.tflite       # File model yang sudah dikonversi ke TensorFlow Lite
│   └── label.txt          # Daftar 15 nama kelas sayuran
├── notebook.ipynb         # Source code lengkap (Training, Evaluasi, Inferensi)
├── requirements.txt       # Daftar dependency dan library yang digunakan
└── README.md              # Dokumentasi proyek
