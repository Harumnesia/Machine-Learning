# Machine-Learning

## Project Overview
Harumnesia adalah suatu web yang menggunakan AI... 

## Dataset
Ada dua dataset yang digunakan dalam proyek ini. Dataset pertama adalah dataset parfum lokal yang dikumpulkan dan dibuat sendiri, dan dapat diakses di [di sini](https://github.com/Harumnesia/Machine-Learning/blob/main/Dataset/Dataset_Clean/Dataset_Harumnesia_clean.csv).
Dataset kedua adalah dataset gabungan yang berisi parfum lokal dan parfum luar. Kami mendapatkan dataset ini dari menggabungkan parfum lokal yang telah kami buat dan dataset yang kami peroleh dari kaggle sebagai dataset parfum luar yang dapat diakses [di sini](https://github.com/Harumnesia/Machine-Learning/blob/main/Dataset/Dataset_Gabungan/dataset_parfum_gabungan.csv).

## Machine Learning Workflow

1. **Data Collection**:
   
   Untuk parfum lokal kami mengumpulkan dataset dari informasi-informasi yang diperoleh melalui online shop dan untuk dataset parfum luar kami menggunakan dataset yang ada di kaggle.
   
3. **Data Cleaning**:
   
   Kami melakukan cleaning dataset sebelum digunakan untuk mengatur huruf kapital atau huruf kecil pada dataset yang ada. Selain itu juga dilakukan penyamaan pada format harga parfum agar tampilannya sama.
   
5. **Data Preprocessing**:
   
   a. Model Pertama
   
      Deskripsi parfum yang diinputkan user diproses menggunakan Gemini API dan LangChain untuk menghasilkan notes yang kemudian setiap inputnya diolah menjadi  data numerik (scaling, one-hot encoding, TF-IDF), yang kemudian dimensinya direduksi dengan autoencoder.
   
7. **Model Development**:
   
   Model yang digunakan pada web Harumnesia ada dua yaitu:
   
   a. Model Pertama
   
     Model yang digunakan autoencoder untuk feature extraction adalah neural network. Untuk melakukan clustering data hasil dari feature extraction autoencoder menggunakan K-Means.
   
   b. Model Kedua
   
      Menggunakan TF-IDF Vectorization untuk mengubah notes parfum menjadi representasi numerik yang kemudian dikonversi ke tensorflow. 
9. **Training**:
   
   Model dilatih menggunakan TensorFlow dan Keras
10. **Evaluasi**:
    
   Model autoencoder di evaluasi menggunakan Mean Square Error (MSE) dan untuk model K-Means di evaluasi menggunakan silhouette score. 
