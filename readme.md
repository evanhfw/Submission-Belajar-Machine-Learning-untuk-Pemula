# **Machine Learning for Beverage Sales: Clustering & Classification**

## **📌 Overview**

Repositori ini berisi proyek **Machine Learning untuk analisis penjualan minuman (Beverage Sales)**. Proyek ini mencakup dua bagian utama:

1. **Clustering** - Mengelompokkan pelanggan berdasarkan pola pembelian mereka menggunakan metode unsupervised learning.
2. **Classification** - Memprediksi kategori pelanggan berdasarkan fitur transaksi menggunakan supervised learning.

## **📂 Struktur Repositori**

```
│── clustering/
│   ├── [Clustering]_Submission_Akhir_BMLP_Evan_Hanif_Widiatama.ipynb
│── classification/
│   ├── [Klasifikasi]_Submission_Akhir_BMLP_Your_Name.ipynb
│── requirements.txt
│── README.md
```

## **📊 Clustering Analysis**

- **Metode yang digunakan:** K-Means Clustering
- **Tujuan:** Mengelompokkan pelanggan berdasarkan transaksi untuk memahami pola pembelian mereka.
- **Hasil utama:**
  - Terbentuk **3 cluster utama** dengan karakteristik yang berbeda.
  - **Cluster 0:** Didominasi pelanggan **B2C**, dengan pembelian kecil dan harga rendah.
  - **Cluster 1:** Pelanggan **B2B** dengan volume pembelian sedang dan harga bervariasi.
  - **Cluster 2:** **Premium buyers**, pelanggan besar dengan harga tinggi dan jumlah pembelian signifikan.

### **Strategi Bisnis Berdasarkan Cluster**

- **Cluster 0 (B2C, Harga Rendah, Volume Kecil):**  
  📌 Targetkan dengan **promo produk satuan & loyalty program** untuk meningkatkan pembelian.  
  📌 Gunakan strategi **diskon langsung atau bundling produk murah**.

- **Cluster 1 (B2B, Harga Rendah-Sedang, Volume Tinggi):**  
  📌 Tawarkan **diskon bulk dan kontrak jangka panjang** untuk menarik lebih banyak pembelian.  
  📌 Gunakan strategi **paket eksklusif untuk pelanggan bisnis kecil-menengah**.

- **Cluster 2 (B2B Premium, Harga Tinggi, Volume Besar):**  
  📌 Fokus pada pelanggan **premium seperti restoran, distributor, atau perusahaan besar**.  
  📌 Berikan **paket eksklusif, harga khusus, dan layanan premium** untuk mempertahankan loyalitas pelanggan.

---

## **🧠 Classification Model**

- **Model yang digunakan:** Random Forest & XGBoost
- **Tujuan:** Memprediksi jenis pelanggan berdasarkan fitur transaksi.

### **Evaluasi Model Sebelum dan Setelah Hyperparameter Tuning**

| **Metrik**              | **Sebelum Tuning** | **Setelah Tuning** |
| ----------------------- | ------------------ | ------------------ |
| **Accuracy**            | 1.00               | 1.00               |
| **Precision (Kelas 2)** | 0.98               | 0.98               |
| **Recall (Kelas 2)**    | 0.96               | 0.96               |
| **F1-Score (Kelas 2)**  | 0.97               | 0.97               |
| **Macro Avg**           | 0.99               | 0.99               |
| **Weighted Avg**        | 1.00               | 1.00               |

🔹 **Kesimpulan:**

- **Tuning tidak memberikan perubahan signifikan**, karena model sudah optimal sejak awal.
- **Recall pada kelas 2 tetap di 0.96**, menunjukkan masih ada sedikit kesalahan klasifikasi pada kelas minoritas.
- **XGBoost lebih unggul dalam mengenali kelas 2 dibandingkan Random Forest**.

---

## **📌 Rekomendasi & Tindakan Lanjutan**

✅ **Gunakan model ini untuk deployment**, karena performanya sudah sangat tinggi.  
🔹 **Lakukan validasi lebih lanjut dengan data baru**, untuk melihat apakah model tetap optimal di kondisi berbeda.  
🔹 **Coba teknik regularisasi pada XGBoost** (menyesuaikan `lambda`, `alpha`) untuk mencegah overfitting.  
🔹 **Tambahkan lebih banyak data untuk kelas minoritas (kelas 2)** agar model lebih seimbang.  
🔹 **Bandingkan dengan model lain seperti LightGBM atau Neural Network** untuk eksplorasi lebih lanjut.

---

## **⚙ Instalasi dan Dependencies**

### **1. Clone repositori**

```bash
git clone https://github.com/your-username/beverage-sales-ml.git
cd beverage-sales-ml
```

### **2. Install dependencies**

Pastikan Anda memiliki **Python 3.8+**, lalu jalankan:

```bash
pip install -r requirements.txt
```

📌 **Dependencies yang digunakan:**

```
pandas
numpy
seaborn
scikit-learn==1.5.2
optuna
matplotlib
category-encoders
```

---

## **🚀 Cara Menjalankan Notebook**

- **Clustering:** Buka `clustering/[Clustering]_Submission_Akhir_BMLP_Evan_Hanif_Widiatama.ipynb` di Jupyter Notebook atau Google Colab.
- **Classification:** Buka `classification/[Klasifikasi]_Submission_Akhir_BMLP_Your_Name.ipynb` dan jalankan sel sesuai urutan.

---

## **📌 Catatan Tambahan**

- Jika ingin meningkatkan model, bisa mencoba **tuning parameter lebih lanjut menggunakan Optuna**.
- Untuk deployment, model dapat disimpan menggunakan `joblib` atau `pickle` untuk prediksi real-time.

---

## **📢 Kontribusi & Feedback**

Jika Anda memiliki saran atau ingin berkontribusi, silakan buat **pull request** atau **issue** di repositori ini.  
Terima kasih! 😊 🚀
