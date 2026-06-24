# Klasifikasi Hasil Panen Padi Menggunakan Metode Ensemble Learning AdaBoost Classifier

## Tugas Besar Machine Learning

Project ini dibuat untuk memenuhi tugas besar mata kuliah Machine Learning. Program ini berfokus pada klasifikasi hasil panen padi menggunakan metode **Ensemble Learning AdaBoost Classifier** berbasis **Decision Tree Stump**.

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

Padi merupakan salah satu komoditas pangan utama yang memiliki peran penting dalam kebutuhan masyarakat. Hasil panen padi dapat dipengaruhi oleh banyak faktor, seperti luas lahan, jenis tanah, penggunaan pupuk, pestisida, curah hujan, suhu, kelembaban, dan kondisi angin.

Dengan adanya data pertanian, metode machine learning dapat digunakan untuk membantu menganalisis pola hasil panen. Program ini menerapkan model klasifikasi untuk membedakan hasil panen padi ke dalam kategori rendah dan tinggi berdasarkan data yang tersedia.

## Gap Penelitian

Beberapa penelitian sebelumnya telah menggunakan algoritma klasifikasi seperti Decision Tree, C4.5, Random Forest, KNN, SVM, dan Naive Bayes untuk prediksi hasil panen padi. Namun, beberapa model masih memiliki keterbatasan dalam meningkatkan performa klasifikasi, terutama ketika data memiliki banyak fitur atau pola yang kompleks.

Pada project ini, digunakan metode **AdaBoost Classifier** karena algoritma ini mampu menggabungkan beberapa model sederhana menjadi model yang lebih kuat. AdaBoost juga dapat memberikan perhatian lebih pada data yang sebelumnya salah diklasifikasikan, sehingga performa model dapat meningkat.

## Tujuan Project

Project ini memiliki beberapa tujuan utama:

1. Membangun model klasifikasi hasil panen padi.
2. Mengelompokkan hasil panen ke dalam kategori Low Yield dan High Yield.
3. Menerapkan metode Ensemble Learning AdaBoost berbasis Decision Tree.
4. Mengevaluasi performa model menggunakan metrik evaluasi klasifikasi.
5. Menjelaskan setiap tahapan program agar mudah dipahami saat presentasi.

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

Dataset yang digunakan adalah dataset padi dengan nama file:

```text
paddydataset.csv
```

Dataset ini memuat data terkait faktor pertanian dan lingkungan yang berhubungan dengan hasil panen padi.

Beberapa jenis variabel yang digunakan antara lain:

1. Luas lahan
2. Jenis tanah
3. Penggunaan pupuk
4. Penggunaan pestisida
5. Curah hujan
6. Suhu
7. Kelembaban
8. Kecepatan dan arah angin
9. Hasil panen padi

## Alur Program

Tahapan program dalam notebook adalah sebagai berikut:

1. Import library
2. Load dataset
3. Menampilkan informasi awal dataset
4. Mengecek missing value
5. Melakukan preprocessing data
6. Membuat target klasifikasi Low Yield dan High Yield
7. Melakukan encoding pada data kategorikal
8. Membagi data menjadi data training dan data testing
9. Membuat model AdaBoost Classifier
10. Melatih model menggunakan data training
11. Melakukan prediksi pada data testing
12. Mengevaluasi model menggunakan accuracy, confusion matrix, dan classification report
13. Menampilkan visualisasi hasil
14. Membuat analisis hasil dan kesimpulan

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

## Output Program

Output utama dari program ini meliputi:

1. Informasi struktur dataset
2. Statistik deskriptif dataset
3. Jumlah data pada kelas Low Yield dan High Yield
4. Hasil training model
5. Nilai akurasi model
6. Confusion matrix
7. Classification report
8. Visualisasi evaluasi model
9. Analisis hasil klasifikasi
10. Kesimpulan akhir

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
2. `paddydataset.csv` berisi dataset yang digunakan.
3. `Tubes_ML_Paddy_AdaBoost.ipynb` berisi program utama machine learning.

## Kesimpulan

Project ini menunjukkan bahwa metode Ensemble Learning AdaBoost dapat digunakan untuk klasifikasi hasil panen padi berdasarkan data pertanian dan lingkungan. Model ini membantu membedakan hasil panen ke dalam kategori Low Yield dan High Yield.

Dengan pendekatan ini, data pertanian tidak hanya ditampilkan sebagai angka, tetapi juga dapat dianalisis untuk mendukung pengambilan keputusan berbasis data.
