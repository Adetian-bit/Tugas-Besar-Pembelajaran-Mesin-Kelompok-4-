# Klasifikasi Hasil Panen Padi Menggunakan Metode Ensemble Learning AdaBoost Classifier

## Tugas Besar Machine Learning

Project ini dibuat untuk memenuhi tugas besar mata kuliah Machine Learning. Program ini berfokus pada klasifikasi hasil panen padi menggunakan metode **Ensemble Learning AdaBoost Classifier** berbasis **Decision Tree Stump**.

Dataset yang digunakan merupakan dataset padi yang berasal dari **India**, sehingga data ini menggambarkan faktor-faktor pertanian dan lingkungan yang berkaitan dengan hasil panen padi pada wilayah tersebut.

Model digunakan untuk mengelompokkan hasil panen padi ke dalam dua kategori, yaitu:

1. **Low Yield**
2. **High Yield**

## Kelompok 4

1. Luluk Nabilah Putri - 103102400057
2. Aghna Shava Akyela Wahjudi - 103102400028
3. Muhammad Ade Sulistiansyah - 103102400045
4. Amanda Faiza Agustin - 103102400060
5. Muhammad Ilham Maulana - 103102400018
6. Ariba Raihana Alyashila - 103102400023

## Latar Belakang

Padi merupakan salah satu komoditas pangan utama yang memiliki peran penting dalam kebutuhan masyarakat, termasuk di India sebagai salah satu negara penghasil padi terbesar. Hasil panen padi dapat dipengaruhi oleh banyak faktor, seperti luas lahan, jenis tanah, varietas padi, penggunaan pupuk, pestisida, curah hujan, suhu, kelembaban, serta kondisi angin.

Dengan adanya data pertanian, metode machine learning dapat digunakan untuk membantu menganalisis pola hasil panen. Program ini menerapkan model klasifikasi untuk membedakan hasil panen padi ke dalam kategori rendah dan tinggi berdasarkan data yang tersedia.

Dataset yang digunakan berasal dari India, sehingga hasil analisis pada project ini menggambarkan pola hubungan antara faktor pertanian dan hasil panen padi berdasarkan data pertanian dari wilayah tersebut.

## Gap Penelitian

Beberapa penelitian sebelumnya telah menggunakan algoritma klasifikasi seperti Decision Tree, C4.5, Random Forest, KNN, SVM, dan Naive Bayes untuk prediksi hasil panen padi. Namun, beberapa model masih memiliki keterbatasan dalam meningkatkan performa klasifikasi, terutama ketika data memiliki banyak fitur atau pola hubungan yang kompleks.

Pada project ini, digunakan metode **AdaBoost Classifier** karena algoritma ini mampu menggabungkan beberapa model sederhana menjadi model yang lebih kuat. AdaBoost juga dapat memberikan perhatian lebih pada data yang sebelumnya salah diklasifikasikan, sehingga performa model dapat meningkat.

## Tujuan Project

Project ini memiliki beberapa tujuan utama:

1. Membangun model klasifikasi hasil panen padi.
2. Mengelompokkan hasil panen ke dalam kategori Low Yield dan High Yield.
3. Menerapkan metode Ensemble Learning AdaBoost berbasis Decision Tree Stump.
4. Mengevaluasi performa model menggunakan metrik evaluasi klasifikasi.
5. Mengetahui fitur-fitur yang berpengaruh terhadap klasifikasi hasil panen padi.
6. Menjelaskan setiap tahapan program agar mudah dipahami saat presentasi.

## Metode yang Digunakan

Metode utama yang digunakan dalam project ini adalah:

**AdaBoost Classifier berbasis Decision Tree Stump**

AdaBoost merupakan metode ensemble learning tipe boosting. Model ini bekerja dengan menggabungkan beberapa weak learner menjadi satu strong learner.

Pada project ini, weak learner yang digunakan adalah Decision Tree dengan kedalaman pohon sederhana. Model seperti ini disebut **Decision Tree Stump**.

Secara umum, proses kerja AdaBoost adalah:

1. Memberikan bobot awal pada setiap data.
2. Melatih model Decision Tree sederhana.
3. Meningkatkan bobot data yang salah diklasifikasikan.
4. Melatih model berikutnya dengan fokus pada data yang lebih sulit.
5. Menggabungkan seluruh model melalui voting berbobot.
6. Menghasilkan prediksi akhir.

## Dataset

Dataset yang digunakan adalah dataset padi dari India dengan nama file:

```text
paddydataset.csv
```

Dataset ini memuat data terkait faktor pertanian dan lingkungan yang berhubungan dengan hasil panen padi. Data tersebut digunakan untuk membangun model klasifikasi hasil panen padi menjadi kategori rendah dan tinggi.

Beberapa jenis variabel yang digunakan antara lain:

1. Luas lahan
2. Blok pertanian
3. Varietas padi
4. Jenis tanah
5. Penggunaan benih
6. Penggunaan pupuk
7. Penggunaan pestisida
8. Curah hujan
9. Suhu
10. Kelembaban
11. Kecepatan dan arah angin
12. Hasil panen padi

Kolom hasil panen padi, yaitu `Paddy yield(in Kg)`, digunakan sebagai dasar untuk membuat target klasifikasi. Nilai hasil panen tersebut dibagi menjadi dua kategori berdasarkan nilai median, yaitu **Low Yield** dan **High Yield**.

## Alur Program

Tahapan program dalam notebook adalah sebagai berikut:

1. Import library
2. Load dataset
3. Menampilkan informasi awal dataset
4. Mengecek missing value
5. Menghapus data duplikat
6. Membuat target klasifikasi Low Yield dan High Yield
7. Menampilkan visualisasi distribusi target
8. Memisahkan fitur dan target
9. Melakukan encoding pada data kategorikal
10. Membagi data menjadi data training dan data testing
11. Membuat model AdaBoost Classifier
12. Melatih model menggunakan data training
13. Melakukan prediksi pada data testing
14. Mengevaluasi model menggunakan accuracy, precision, recall, F1-score, ROC-AUC, dan confusion matrix
15. Melakukan pengecekan overfitting
16. Melakukan cross validation
17. Menampilkan feature importance
18. Membuat model pembanding dengan 6 fitur terpilih
19. Membandingkan performa model
20. Membuat analisis hasil dan kesimpulan

## Evaluasi Model

Model dievaluasi menggunakan beberapa metrik klasifikasi, yaitu:

1. **Accuracy**
   Mengukur jumlah prediksi benar dibandingkan seluruh data.

2. **Confusion Matrix**
   Menampilkan jumlah prediksi benar dan salah pada setiap kelas.

3. **Precision**
   Mengukur ketepatan model saat memprediksi suatu kelas.

4. **Recall**
   Mengukur kemampuan model dalam menemukan data dari suatu kelas.

5. **F1-Score**
   Menggabungkan precision dan recall dalam satu nilai evaluasi.

6. **ROC-AUC**
   Mengukur kemampuan model dalam membedakan kelas Low Yield dan High Yield.

## Output Program

Output utama dari program ini meliputi:

1. Informasi struktur dataset
2. Statistik deskriptif dataset
3. Jumlah data pada kelas Low Yield dan High Yield
4. Hasil preprocessing data
5. Hasil training model
6. Nilai akurasi model
7. Confusion matrix
8. Classification report
9. Nilai ROC-AUC
10. Hasil cross validation
11. Feature importance
12. Perbandingan model semua fitur dan model 6 fitur
13. Visualisasi evaluasi model
14. Analisis hasil klasifikasi
15. Kesimpulan akhir

## Cara Menjalankan Program

Program dapat dijalankan melalui Google Colab atau Jupyter Notebook.

Langkah menjalankan program:

1. Buka file notebook `.ipynb`.
2. Upload dataset `paddydataset.csv`.
3. Jalankan setiap cell dari atas sampai bawah.
4. Perhatikan output dan penjelasan pada setiap step.
5. Gunakan bagian analisis hasil untuk menjelaskan performa model saat presentasi.

## Struktur File

```text
.
├── README.md
├── paddydataset.csv
└── Tugas Besar Pembelajaran Mesin Kelompok 4.ipynb
```

Keterangan:

1. `README.md` berisi dokumentasi project.
2. `paddydataset.csv` berisi dataset padi dari India yang digunakan dalam project.
3. `Tugas Besar Pembelajaran Mesin Kelompok 4.ipynb` berisi program utama machine learning.

## Kesimpulan

Project ini menunjukkan bahwa metode **Ensemble Learning AdaBoost Classifier** dapat digunakan untuk klasifikasi hasil panen padi berdasarkan data pertanian dan lingkungan. Dataset yang digunakan berasal dari India dan berisi berbagai faktor yang berkaitan dengan hasil panen padi, seperti luas lahan, jenis tanah, pupuk, pestisida, cuaca, kelembaban, dan kondisi angin.

Model ini membantu membedakan hasil panen ke dalam kategori **Low Yield** dan **High Yield**. Dengan pendekatan ini, data pertanian tidak hanya ditampilkan sebagai angka, tetapi juga dapat dianalisis untuk mendukung pengambilan keputusan berbasis data.

Berdasarkan hasil evaluasi, AdaBoost mampu memberikan performa klasifikasi yang baik. Selain itu, penggunaan feature importance juga membantu mengetahui faktor-faktor yang berpengaruh terhadap hasil prediksi model.
