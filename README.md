# Perbandingan Kinerja Arsitektur CNN (MobileNetV2, ResNet50V2, dan InceptionV3) pada Klasifikasi Multi-Kelas Citra Medis Penyakit Mata

## 📌 Deskripsi Proyek
Proyek ini bertujuan untuk melakukan analisis komparatif terhadap tiga arsitektur *Convolutional Neural Network* (CNN) populer—yaitu **MobileNetV2**, **ResNet50V2**, dan **InceptionV3**—dalam mengklasifikasikan citra medis kondisi mata ke dalam 4 kategori (3 jenis penyakit mata dan kondisi normal). 

Penggunaan metode *Transfer Learning* dievaluasi untuk menentukan model terbaik berdasarkan tingkat akurasi, efisiensi komputasi, dan performa klasifikasi citra medis secara keseluruhan.

---

## 👤 Informasi Penulis
* **Nama:** Najwa Handaria Suparna
* **NIM:** A11.2024.16039
* **Mata Kuliah:** Pembelajaran Mesin (Machine Learning)

---

## 📁 Struktur Dataset
Dataset dikelompokkan ke dalam 4 kelas citra medis mata:
1. `cataract` (Katarak)
2. `diabetic_retinopathy` (Retinopati Diabetik)
3. `glaucoma` (Glaukoma)
4. `normal` (Kondisi Mata Normal)

Struktur direktori dataset yang digunakan dalam proyek:
```text
dataset/
├── cataract/
├── diabetic_retinopathy/
├── glaucoma/
└── normal/
```

---

## 🛠️ Teknologi & Library
Proyek ini dikembangkan menggunakan bahasa pemrograman **Python** di lingkungan **Google Colab** / **Jupyter Notebook** dengan pustaka-pustaka utama sebagai berikut:

* **Deep Learning Framework:** `TensorFlow`, `Keras`
* **Data Manipulation & Processing:** `NumPy`, `OpenCV` (`cv2`)
* **Data Visualization:** `Matplotlib`
* **Utilities:** `os`, `random`

---

## 🏗️ Arsitektur Model yang Dibandingkan

1. **MobileNetV2:** Model yang didesain ringan (*lightweight*) dan efisien, cocok untuk perangkat seluler atau komputasi terbatas.
2. **ResNet50V2:** Arsitektur deep residual learning yang memanfaatkan *identity mapping* untuk mengatasi masalah *vanishing gradient* pada jaringan yang sangat dalam.
3. **InceptionV3:** Arsitektur yang menggunakan *Inception modules* (faktor filter bertingkat) untuk mengekstrak fitur pada berbagai skala spasial.

---

## 🚀 Langkah-Langkah Eksperimen

1. **Persiapan Lingkungan & Dataset:**
   * Penguncian *random seed* untuk memastikan reprodusibilitas hasil eksperimen.
   * *Mounting* Google Drive untuk akses lokasi dataset.
2. **Eksplorasi Data (EDA):**
   * Perhitungan dan visualisasi distribusi jumlah sampel di setiap kelas.
   * Visualisasi sampel acak citra medis dari masing-masing kategori penyakit.
3. **Pra-pemrosesan Data & Augmentasi:**
   * Resizing citra sesuai kebutuhan input arsitektur CNN target.
   * Pembagian data (*Train/Validation/Test Split*).
   * Penerapan data augmentasi untuk mencegah *overfitting*.
4. **Pelatihan Model (*Model Training*):**
   * Penerapan *Transfer Learning* menggunakan *pre-trained weights* (ImageNet).
   * Konfigurasi *hyperparameter* (Optimizer, Learning Rate, Batch Size, Epochs).
5. **Evaluasi & Perbandingan Kinerja:**
   * Evaluasi metrik performa (Accuracy, Precision, Recall, F1-Score).
   * Visualisasi *Loss/Accuracy Curve* dan *Confusion Matrix*.

---

## 💻 Cara Menjalankan Notebook

1. **Clone / Download** repository atau file notebook `.ipynb`.
2. Buka notebook di **Google Colab** atau **Jupyter Lab/Notebook** lokal.
3. Pastikan struktur folder dataset disesuaikan pada variabel `base_dir`:
   ```python
   base_dir = '/content/gdrive/MyDrive/PEMBELAJARAN MESIN/PROJECT UAS NAJWA 16039/dataset'
   ```
4. Jalankan sel-sel kode secara berurutan (*Run All*).

---

## 📊 Hasil & Kesimpulan
*(Dapat diperbarui/diisi sesuai dengan nilai akurasi dan metrik akhir yang diperoleh dari hasil eksekusi eksperimen)*
