# Implementasi Seleksi Fitur Binary Particle Swarm Optimization pada Algoritma K-NN untuk Klasifikasi Kanker Payudara 

## Domain Proyek
Kanker Payudara adalah jenis kanker paling umum yang sering menyerang kalangan wanita di seluruh dunia. 
Diagnosa awal yang akurat dalam mendeteksi kanker payudara memainkan peran penting dalam pengobatan 
pasien karena semakin cepat kanker di diagnosa semakin cepat juga pengobatan dapat diberikan. Untuk 
menghasilkan diagnosa yang akurat terhadap pasien kanker payudara maka dilakukan penelitian dengan tujuan 
mendapatkan model klasifikasi yang dapat memberikan klasifikasi yang akurat terhadap penyakit kanker 
payudara. Algoritma klasifikasi yang sering digunakan dan cukup terkenal adalah K-Nearest Neighbor (K-NN). 

## Referensi
Hidayat, R., Kartini, D., Mazdadi, M. I., Budiman, I., & Ramadhani, R. (2023). Implementasi Seleksi Fitur 
Binary Particle Swarm Optimization pada Algoritma K-NN untuk Klasifikasi Kanker Payudara. Jurnal Sistem 
dan Teknologi Informasi (JUSTIN), 11(1). DOI: 10.26418/justin.v11i1.53608. 
Harafani, H., & Al-Kautsar, H. A. (2021). Meningkatkan Kinerja K-NN Untuk Klasifikasi Kanker Payudara 
Dengan Forward Selection. Jurnal Pendidikan Teknologi dan Kejuruan, 18(1), 99–106. DOI: 10.23887/jptk
undiksha.v18i1.29905. 
Yunus, W. (2018). Algoritma K-Nearest Neighbor Berbasis Particle Swarm Optimization Untuk Prediksi 
Penyakit Ginjal Kronik. Jurnal Teknik Elektro Cosphi, 2(2), 51–55. Link Artikel. 
Obaid, O. I., Mohammed, M. A., Ghani, M. K. A., Mostafa, S. A., & Al-Dhief, F. T. (2018). Evaluating the 
Performance of Machine Learning Techniques in the Classification of Wisconsin Breast Cancer. International 
Journal of Engineering and Technology, 7(4), 160–166. DOI: 10.14419/ijet.v7i4.36.23737. 
Han, W., Yang, P., Ren, H., & Sun, J. (2010). Comparison Study of Several Kinds of Inertia Weights for PSO. 
Proceedings of the 2010 IEEE International Conference on Progress in Informatics and Computing, 280–284. 
DOI: 10.1109/PIC.2010.5687447. 
Zhang, X., Shi, Z., Liu, X., & Li, X. (2018). A Hybrid Feature Selection Algorithm For Classification 
Unbalanced Data Processing. 2018 IEEE International Conference on Smart Internet of Things (SmartIoT), 
269–275. DOI: 10.1109/SmartIoT.2018.00055.

## Business Understanding

### Problem Statement
1. Bagaimana memanfaatkan data rekam medis untuk memprediksi risiko penyakit kanker payudara secara akurat?
2. Apakah pembobotan atribut pada KNN dapat meningkatkan akurasi penyakit kanker payudara?
3. Sejauh mana kinerja model KNN yang dikembangkan dibandingkan dengan penelitian sebelumnya?

##Dataset
Breast Cancer Wisconsin Diagnostic (Kaggle)

## Langkah Pengerjaan
1. Business Understanding
Memahami tingginya angka kanker payudara dan perlunya deteksi dini.
Tujuan: Membangun model klasifikasi cepat dan akurat.
2. Data Understanding
Menggunakan dataset Breast Cancer Wisconsin Diagnostic (569 sampel, 30 fitur).
Label target: Malignant (ganas) atau Benign (jinak).
3. Exploratory Data Analysis (EDA)
Analisis distribusi kelas dan fitur.
Visualisasi heatmap korelasi antar fitur untuk melihat potensi redundansi.
4. Data Preparation
Cek dan tangani missing values (jika ada).
Normalisasi fitur agar skala seragam (StandardScaler).
Split data: 70% train, 30% test.
5. Feature Selection dengan Binary PSO
Mengimplementasikan Binary PSO untuk memilih subset fitur terbaik dari 30 fitur.
Fitness function mengkombinasikan akurasi klasifikasi dan jumlah fitur minimal.
Output: Fitur terpilih yang optimal untuk klasifikasi.
6. Modeling dengan K-NN
Menggunakan algoritma K-NN dengan parameter k ganjil (1-21) untuk menghindari seri.
Melatih model dengan data train pada dua skenario:
K-NN tanpa seleksi fitur.
K-NN dengan fitur hasil seleksi BPSO.
7. Evaluation
Menggunakan Confusion Matrix untuk visual evaluasi.
Menghitung metrik:
Accuracy
Precision
Recall
F1-score
Membandingkan hasil K-NN vs K-NN+BPSO.

## Kesimpulan
Model K-NN+BPSO mencapai akurasi 95,32% (lebih tinggi dari K-NN biasa, 94,15%).
Jumlah fitur berhasil direduksi dari 30 menjadi 5 tanpa menurunkan akurasi.
Model lebih cepat dan efisien untuk digunakan sebagai pendukung keputusan medis.





