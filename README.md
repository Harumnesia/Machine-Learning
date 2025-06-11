# Machine-Learning

## Project Overview
Proyek ini mengembangkan dua model rekomendasi parfum berbasis machine learning dengan memanfaatkan data parfum lokal serta gabungan lokal dan internasional. Model pertama menyajikan rekomendasi berdasarkan input pengguna seperti gender, situasi, konsentrasi, ukuran, harga, dan deskripsi parfum. Deskripsi tersebut diproses menggunakan Gemini API dan LangChain untuk menghasilkan informasi notes, yang kemudian diolah melalui scaling, one-hot encoding, dan TF-IDF. Hasilnya direduksi menggunakan autoencoder dan dikelompokkan dengan K-Means, sehingga preferensi pengguna dapat dicocokkan ke dalam klaster dan diberikan rekomendasi menggunakan cosine similarity. Sementara itu, model kedua menggunakan similarity, dengan merepresentasikan notes parfum menggunakan TF-IDF Vectorization dan mengonversinya ke format TensorFlow. Kedua model ini diintegrasikan ke sistem aplikasi melalui file .h5 dan .pkl, membentuk fondasi rekomendasi yang cepat, relevan, dan adaptif terhadap preferensi pengguna.

## Dataset
Ada dua dataset yang digunakan dalam proyek ini: 
1. **Dataset Parfum Lokal**
   Dikumpulkan dan dibuat sendiri, dan dapat diakses di
   [Akses Dataset Lokal](https://github.com/Harumnesia/Machine-Learning/blob/main/Dataset/Dataset_Clean/Dataset_Harumnesia_clean.csv).
2. **Dataset Gabungan (Lokal + Luar)**
   Gabungan dataset parfum lokal yang telah dibuat sendiri dengan dataset parfum luar yang di peroleh dari kaggle
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

- Deskripsi parfum diproses menggunakan Gemini API dan LangChain untuk mengekstrak informasi notes parfum
- Fitur kemudian diolah menjadi data numerik melalui:
  - **TF-IDF Vectorization** untuk notes
  - **One-hot encoding** untuk fitur kategorikal
  - **Scaling** untuk fitur numerikal
- Semua fitur digabungkan menjadi satu matriks fitur
  
#### b. Model Kedua
- Notes parfum diolah dengan **TF-IDF Vectorization** 

### 4. **Model Development**:
   
#### a. Model Pertama
   
- **Autoencoder** untuk feature extraction
- **Clustering dengan K-Means** untuk mengelompokkan parfum
- **Cosine Similarity** untuk mengukur kemiripan rekomendasi parfum
   
#### b. Model Kedua

- **Convert TF-IDF ke TensorFlow**
- **Cosine Similarity** untuk mengukur kemiripan rekomendasi parfum

### 5. **Training**:
   
- Model dilatih menggunakan TensorFlow dan Keras

### 6. **Evaluasi**:
    
- **Autoencoder** di evaluasi menggunakan **Mean Square Error (MSE)**
- **K-Means** di evaluasi menggunakan **Silhouette Score**

---

## How to Run the Code
