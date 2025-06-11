# Machine-Learning

## Project Overview
Proyek ini mengembangkan dua model rekomendasi parfum berbasis machine learning dengan memanfaatkan data parfum lokal serta gabungan lokal dan internasional. Model pertama menyajikan rekomendasi berdasarkan input pengguna seperti gender, situasi, konsentrasi, ukuran, harga, dan deskripsi parfum. Deskripsi tersebut diproses menggunakan Gemini API dan LangChain untuk menghasilkan informasi notes, yang kemudian diolah melalui scaling, one-hot encoding, dan TF-IDF. Hasilnya direduksi menggunakan autoencoder dan dikelompokkan dengan K-Means, sehingga preferensi pengguna dapat dicocokkan ke dalam klaster dan diberikan rekomendasi menggunakan cosine similarity. Sementara itu, model kedua menggunakan similarity, dengan merepresentasikan notes parfum menggunakan TF-IDF Vectorization dan mengonversinya ke format TensorFlow. Kedua model ini diintegrasikan ke sistem aplikasi melalui file .h5 dan .pkl, membentuk fondasi rekomendasi yang cepat, relevan, dan adaptif terhadap preferensi pengguna.

## Dataset
Ada dua dataset yang digunakan dalam proyek ini: 
1. **Dataset Parfum Lokal**
   Dikumpulkan dan dibuat sendiri, dan dapat diakses di
   [Akses Dataset Lokal](https://github.com/Harumnesia/Machine-Learning/blob/main/Dataset/Dataset_Clean/Dataset_Harumnesia_clean.csv).
2. **Dataset Gabungan (Lokal + Luar)**
   Gabungan dataset parfum lokal yang telah dibuat sendiri dengan dataset parfum luar yang di peroleh dari kaggle.
   [Akses Dataset Gabungan](https://github.com/Harumnesia/Machine-Learning/blob/main/Dataset/Dataset_Gabungan/dataset_parfum_gabungan.csv).

---

## Machine Learning Workflow

### 1. **Data Collection**:
   
- **Parfum Lokal**: Dikumpulkan dari berbagai sumber online shop.
- **Parfum luar**: Diambil dari kaggle.
   
### 2. **Data Cleaning**:
   
- Standarisasi format huruf dan harga
- Menghapus kolom yang tidak relevan
- Menggabungkan notes
   
### 3. **Data Preprocessing**:
   
#### a. Model Pertama
   
- Notes parfum diproses dengan Gemini API dan LangChain
- Notes diolah menjadi  data numerik melalui :
  - **Scaling**
  - **One-hot encoding**
  - **TF-IDF**
- Hasilnya direduksi dengan autoencoder
   
7. **Model Development**:
   
   Model yang digunakan pada web Harumnesia ada dua yaitu:
   
   a. Model Pertama
   
   Model yang digunakan autoencoder untuk feature extraction adalah neural network. Untuk melakukan clustering data hasil dari feature extraction autoencoder menggunakan K-Means.
   
   b. Model Kedua
   
   Menggunakan TF-IDF Vectorization untuk mengubah notes parfum menjadi representasi numerik yang kemudian dikonversi ke tensorflow dan dilanjutkan dengan cosine similarity.
9. **Training**:
   
   Model dilatih menggunakan TensorFlow dan Keras
10. **Evaluasi**:
    
    Model autoencoder di evaluasi menggunakan Mean Square Error (MSE) dan untuk model K-Means di evaluasi menggunakan silhouette score. 
