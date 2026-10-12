# deeplearninggslc

# Transfer Learning untuk Klasifikasi Citra dengan Data Terbatas 🐶🐱

Repositori ini berisi implementasi dan laporan analisis untuk **Tugas Take-Home Sesi 05: Advanced CNNs and Transfer Learning**. Proyek ini merupakan studi komparatif untuk mengevaluasi berbagai strategi pelatihan Convolutional Neural Network (CNN) pada rezim data terbatas (*small-data regime*).

## 📌 Deskripsi Proyek
Eksperimen ini menggunakan arsitektur **ResNet-18** dan subset 10 kelas dari dataset **Oxford-IIIT Pet**. Tujuannya adalah merumuskan strategi paling optimal antara melatih model dari nol (*from scratch*), ekstraksi fitur murni (*feature extraction*), dan penyesuaian bobot secara bertahap (*progressive fine-tuning*).

### Kondisi Eksperimen yang Diuji:
1. **[B1] Baseline from Scratch:** Melatih model tanpa *pretrained weights*.
2. **[B2] Feature Extraction:** Membekukan seluruh lapisan *backbone* dan hanya melatih *classifier head*.
3. **[B3] Progressive Fine-Tuning:** Membuka pembekuan blok residual terakhir (`layer4`) dengan *differential learning rate*.
4. **[B4] Uji Kontrol Data Augmentation:** Menguji dampak augmentasi data terhadap tingkat *overfitting*.

## 📂 Struktur Repositori
- `Tugas05_2802415744_MathildaRafaellaChristyNugroho.ipynb` : *Jupyter Notebook* berisi kode eksperimen lengkap (PyTorch).
- `log_hasil_eksperimen.csv` : Log metrik mentah yang merekam proses pelatihan dari setiap epoch (Train/Val Loss & Accuracy).
- `Tugas05_2802415744_MathildaRafaellaChristyNugroho.pdf` : Dokumen laporan yang berisi tabel konsolidasi, visualisasi kurva *loss*, dan *failure analysis* dari misklasifikasi.
- `requirements.txt` : Daftar dependensi *library* Python.

## 🚀 Cara Menjalankan Kode
1. *Clone* repositori ini:
   ```bash
   git clone [[https://github.com/username-kamu/nama-repo-kamu.git](https://github.com/asipnana/deeplearninggslc.git)]
   cd deeplearninggslc
