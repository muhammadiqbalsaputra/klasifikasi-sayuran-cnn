# 🥬 Vegetable Image Classification

**Submission Bintang 5 ⭐️⭐️⭐️⭐️⭐️ - Kelas Belajar Fundamental Deep Learning (Dicoding)**

## 📌 Deskripsi Proyek

Proyek ini adalah sistem klasifikasi gambar berbasis **Convolutional Neural Network (CNN)** yang mampu mengenali 15 jenis sayuran secara otomatis. Dibangun menggunakan ekosistem TensorFlow, proyek ini dirancang untuk memenuhi kriteria kelulusan tertinggi pada modul *Belajar Pengembangan Machine Learning* di Dicoding Academy.

## ✨ Fitur & Keunggulan Utama

Model ini tidak hanya sekadar melatih data, tetapi menerapkan standar *best practice* dalam pengembangan AI:

* **Dataset Robust:** Mengolah total **15.000 gambar** dengan variasi resolusi alami (natural) yang divalidasi menggunakan library `PIL`.
* **Pipeline Data Profesional:** Menggunakan `split-folders` untuk pembagian data yang presisi (**80% Train, 10% Val, 10% Test**) serta `ImageDataGenerator` untuk augmentasi gambar.
* **Smart Training:** Implementasi **Custom Callback** yang menghentikan pelatihan saat akurasi menyentuh target **> 96%**, mengoptimalkan waktu komputasi dan mencegah *overfitting*.
* **Deployment-Ready:** Model telah dikonversi ke berbagai format untuk kebutuhan produksi:
* 📦 **SavedModel** (Server-side/Cloud)
* 📱 **TF-Lite** (Mobile & Edge Devices)
* 🌐 **TFJS** (Web/Browser Integration)



---

## 📊 Hasil Pelatihan & Evaluasi

Model menunjukkan performa yang sangat impresif dengan tingkat akurasi di atas 96% pada seluruh subset data.

### Ringkasan Metrik

| Dataset | Akurasi | Loss |
| --- | --- | --- |
| **Training** | `96.69%` | `0.1011` |
| **Validation** | `97.21%` | `0.1006` |
| **Testing** | **97.70%** | **0.0905** |

> **Note:** Hasil evaluasi pada data testing yang lebih tinggi dari data training menunjukkan model memiliki kemampuan generalisasi yang sangat baik terhadap data baru.

---

## 🗂️ Struktur Proyek

```bash
.
├── saved_model/          # Standar TensorFlow model format
├── tflite/               # Optimasi untuk Mobile/IoT
│   ├── model.tflite
│   └── label.txt
├── tfjs_model/           # Deployment untuk ekosistem Web
│   ├── model.json
│   └── group1-shard1of1.bin
├── notebook.ipynb        # Source code lengkap (End-to-End)
├── requirements.txt      # Library dependencies
└── README.md             # Dokumentasi Proyek

```

## 🚀 Cara Menjalankan Inferensi (TF-Lite)

Kamu bisa menguji model ini menggunakan cuplikan kode Python berikut:

```python
import interpreter from tflite_runtime.interpreter as tflite

# Load model TFLite
interpreter = tflite.Interpreter(model_path="tflite/model.tflite")
interpreter.allocate_tensors()

# Proses prediksi lanjut di notebook...

```

---

**Author:** [Muhammad Iqbal Saputra](https://www.google.com/search?q=https://github.com/username-kamu)
*Student at Universitas Harkat Negeri | AI, Web & Mobile Developer Enthusiast*
