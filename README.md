# 🚗 Vehicle Classification System using SVM & HOG

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-SVM-orange)
![Computer Vision](https://img.shields.io/badge/Computer%20Vision-HOG-green)
![Status](https://img.shields.io/badge/Status-Prototype-yellow)

## 📖 Overview
Proyek ini adalah sistem **Computer Vision** untuk mengklasifikasikan jenis kendaraan secara otomatis guna mendukung sistem **E-Ticketing** di gerbang tol atau pelabuhan.

Sistem ini dirancang untuk membedakan kendaraan menjadi 4 golongan:
* **Bus**
* **Car (Mobil Pribadi)**
* **Truck**

Menggunakan pendekatan **Machine Learning Klasik** yang ringan dan efisien, sistem ini mengekstraksi fitur visual menggunakan **HOG (Histogram of Oriented Gradients)** dan mengklasifikasikannya menggunakan **SVM (Support Vector Machine)**.

---

## 🛠️ Tech Stack & Methodology
Proyek ini dibangun menggunakan teknologi open-source:
* **Language:** Python
* **Libraries:** OpenCV, Scikit-learn, Scikit-image, Matplotlib, NumPy/Pandas.
* **Feature Extraction:** HOG (Histogram of Oriented Gradients) - Dipilih karena ketangguhannya mengenali bentuk geometris kendaraan.
* **Classifier:** Support Vector Machine (SVM) dengan Kernel RBF.

### Kenapa HOG + SVM?
Berbeda dengan Deep Learning (CNN) yang membutuhkan resource GPU besar, kombinasi HOG + SVM sangat **ringan (lightweight)**, cepat dilatih, dan dapat berjalan di perangkat dengan spesifikasi rendah (seperti Raspberry Pi atau Mini PC di gerbang tol).

---

## 📊 Performance & Results
Saat ini model dilatih menggunakan dataset gabungan (Kaggle + Crawling) dengan hasil sebagai berikut:

| Metric | Score |
| :--- | :--- |
| **Training Accuracy** | **99%** |
| **Input Resolution** | 64x64 px (Initial Version) |
| **Classes** | 4 (Bus, Car, Truck, Motorcycle) |

*(Disini kamu bisa masukkan screenshot Confusion Matrix kamu nanti. Caranya: Upload gambar ke issue github atau imgur, lalu taruh linknya disini)*

---

## 🚀 How to Run (Cara Menjalankan)
Proyek ini dibuat menggunakan Jupyter Notebook (Google Colab). Anda bisa langsung mencobanya tanpa instalasi lokal.

1.  Buka file `vehicle_classification_svm.ipynb` di repository ini.
2.  Klik tombol **"Open in Colab"** (jika ada) atau download file `.ipynb` tersebut.
3.  Upload dataset kendaraan Anda.
4.  Jalankan cell secara berurutan.

---

## 🚧 Challenges & Future Roadmap (Jujur & Kritis)
Proyek ini masih dalam tahap pengembangan (*Work In Progress*). Beberapa tantangan yang sedang diselesaikan:

* **Isu Geometri (Resizing):** Saat ini menggunakan resize 64x64 tanpa padding, yang menyebabkan kendaraan lebar (seperti kendaraan taktis/sport) terdistorsi menjadi gepeng dan terdeteksi sebagai Truck.
    * *Solusi:* Akan mengimplementasikan teknik **Image Padding** agar rasio aspek gambar tetap terjaga.
* **Resolusi:** Meningkatkan input ke 128x128 px untuk menangkap detail fitur yang lebih baik.

---

## 👤 Author
**Sahryan Hikmal Pradnaa**
* Mahasiswa Informatika - Bumigora
* Minat: Computer Vision, Machine Learning, AI.
* [Link LinkedIn Kamu (Opsional)]

---
*Disclaimer: Proyek ini merupakan bagian dari Tugas Akhir/Skripsi.*
