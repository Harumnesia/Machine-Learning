# Machine-Learning

## Project Overview
Harumnesia adalah suatu web yang menggunakan AI... 

## Dataset
Ada dua dataset yang digunakan dalam proyek ini. Dataset pertama adalah dataset parfum lokal yang dikumpulkan dan dibuat sendiri, dan dapat diakses di [di sini](https://github.com/Harumnesia/Machine-Learning/blob/main/Dataset/Dataset_Clean/Dataset_Harumnesia_clean.csv).
Dataset kedua adalah dataset gabungan yang berisi parfum lokal dan parfum luar. Kami mendapatkan dataset ini dari menggabungkan parfum lokal yang telah kami buat dan dataset yang kami peroleh dari kaggle sebagai dataset parfum luar yang dapat diakses [di sini](https://github.com/Harumnesia/Machine-Learning/blob/main/Dataset/Dataset_Gabungan/dataset_parfum_gabungan.csv).

## Machine Learning Workflow
1. **Data Collection**:
   Untuk parfum lokal kami mengumpulkan dataset dari informasi-informasi yang diperoleh melalui online shop dan untuk dataset parfum luar kami menggunakan dataset yang ada di kaggle.
2. **Data Cleaning**:
   Kami melakukan cleaning dataset sebelum digunakan untuk mengatur huruf kapital atau huruf kecil pada dataset yang ada. Selain itu juga dilakukan penyamaan pada format harga parfum agar tampilannya sama.
3. **Data Preprocessing**:
   
4. **Model Development**:
   Model yang digunakan pada web Harumnesia ada dua yaitu://
   
   a. 
      Deskripsi parfum diproses menggunakan Gemini API dan LangChain untuk menghasilkan notes yang kemudian diolah (scaling, one-hot encoding, TF-IDF), kemudian dimensinya direduksi dengan autoencoder dan dikelompokkan dengan K-Means. Input user dicocokkan ke cluster dan direkomendasikan dengan cosine similarity.
   
   b. Model Cosine Similarity//
   
      Menggunakan TF-IDF Vectorization untuk mengubah notes parfum menjadi representasi numerik yang kemudian dikonversi ke tensorflow. 
6. **Training**:
   Model dilatih menggunakan autoencoder
7. **Evaluasi**:
   Model di evaluasi menggunakan
