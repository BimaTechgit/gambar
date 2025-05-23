# Laporan Proyek Machine Learning Prediksi Performa Akademik Siswa - Bimasakti Faturrahman Soetedjo

## Domain Proyek

Transformasi digital menempatkan pendidikan sebagai fondasi utama pengembangan SDM, dengan performa akademik siswa SMA menjadi indikator krusial efektivitas sistem pendidikan. Pencapaian ini tidak hanya dipengaruhi kemampuan kognitif, tetapi juga oleh berbagai faktor eksternal dan internal. Studi menunjukkan bahwa motivasi intrinsik, efikasi diri, dan regulasi diri (Zhigang et al., 2023) berkorelasi positif dengan kesuksesan akademik. Selain itu, lingkungan sekolah, iklim, dan dukungan guru (Costa et al., 2024) juga signifikan memengaruhi.

Penilaian Performa akademik siswa menjadi sangat krusial dalam menilai efektivitas sistem pendidikan serta kesiapan individu dalam menghadapi tantangan masa depan karena Jika kondisi ini terus dibiarkan, maka potensi siswa dalam menyerap dan mencapai potensi akademik terbaik mereka tidak dapat tercapai. Hal ini berisiko menurunkan kualitas lulusan, memperbesar angka putus sekolah, dan meningkatkan ketimpangan pendidikan. sehingga diperlukan pendekatan yang lebih adaptif dan proaktif dalam memantau dan meningkatkan performa mereka.

Mengingat kompleksitas ini, penting untuk memahami dan mengidentifikasi faktor-faktor penentu performa guna intervensi yang efektif. Kualitas lulusan dan angka putus sekolah terancam jika potensi siswa tidak tercapai. Untuk mengatasi tantangan ini, Educational Data Mining (EDM) dan Learning Analytics (LA) memanfaatkan algoritma Machine Learning (ML) dan Deep Learning (DL) untuk memprediksi performa.

Algoritma ML seperti Random Forest, Support Vector Machine, dan Neural Networks menunjukkan akurasi tinggi; misalnya, Random Forest mencapai 94,9% dalam prediksi motivasi belajar (Orji, Vassileva, 2022). Pendekatan DL seperti Long Short-Term Memory (LSTM) juga efektif dalam menganalisis tren belajar jangka panjang (Wang et al., 2024). Sebuah tinjauan sistematis (Sghir et al., 2022) menegaskan bahwa model prediktif yang menggabungkan data demografi, perilaku, dan kinerja sebelumnya dapat mencapai akurasi tinggi, terutama dengan Deep Neural Networks (DNNs) dan LSTM.

Oleh karena itu, penelitian ini bertujuan mengembangkan model prediktif ML dan DL menggunakan dataset "Student Performance: Academic Success Factors in High School Students", untuk membantu institusi pendidikan merancang strategi intervensi yang lebih efektif dan tepat sasaran.


**Referensi**:

- [Factors Affecting on Academic Success of Senior High School Students](https://so06.tci-thaijo.org/index.php/jomld/article/view/266002),
- [Determinants of academic achievement from the middle to secondary school education: A systematic review](https://link.springer.com/article/10.1007/s11218-024-09941-z)
- [Machine Learning Approach for Predicting Students Academic Performance and Study Strategies based on their Motivation](https://arxiv.org/abs/2210.08186)
- [Research on Education Big Data for Students Academic Performance Analysis based on Machine Learning](https://arxiv.org/abs/2407.16907)
- [Recent advances in Predictive Learning Analytics: A decade systematic review (2012–2022)](https://link.springer.com/article/10.1007/s10639-022-11536-0)

## Business Understanding

### Problem Statements

Menjelaskan pernyataan masalah latar belakang:
1. Pernyataan Masalah 1: Institusi pendidikan kesulitan dalam mengidentifikasi siswa yang berisiko mengalami penurunan performa akademik sejak dini karena kompleksitas faktor yang mempengaruhi, seperti kehadiran, aktivitas ekstrakurikuler, dukungan orang tua, dan kebiasaan belajar.

2. Pernyataan Masalah 2: Belum tersedia analisis prediktif berbasis data yang mampu secara akurat memperkirakan nilai akhir siswa atau kategori kelas akademik (GradeClass), sehingga intervensi pendidik sering kali bersifat reaktif, bukan proaktif.

3. Pernyataan Masalah 3: 
Pemanfaatan algoritma pembelajaran mesin dan pembelajaran mendalam di tingkat pendidikan menengah masih terbatas, terutama dalam hal akurasi prediksi dan interpretabilitas model yang dibutuhkan untuk pengambilan keputusan oleh pendidik.

### Goals

Menjelaskan tujuan dari pernyataan masalah:

1. Memprediksi kelas performa akademik (GradeClass) siswa berdasarkan faktor-faktor demografis, kebiasaan belajar, serta aktivitas di dalam dan luar sekolah.

2. Mengidentifikasi pola dan variabel utama yang paling memengaruhi kesuksesan akademik siswa.

3. Memberikan rekomendasi berbasis data bagi pihak sekolah untuk merancang intervensi pendidikan yang lebih personal dan tepat sasaran.

4. Mendukung pengambilan keputusan strategis dalam peningkatan mutu pendidikan dan pembinaan siswa berisiko rendah maupun tinggi.

Semua poin di atas harus diuraikan dengan jelas. Anda bebas menuliskan berapa pernyataan masalah dan juga goals yang diinginkan.

### Solution statements

1. **Solusi 1:**
Mengimplementasikan dan membandingkan beberapa algoritma supervised learning dalam memprediksi GradeClass siswa. Hasil model akan dievaluasi dengan metrik klasifikasi seperti Accuracy, Precision, Recall, dan F1-score seperti:

  * Random Forest

  * Naive Bayes

  * Desicion Tree

  * Artificial Neural Network (ANN)

2. **Solusi 2:** Melakukan hyperparameter tuning menggunakan teknik seperti Grid Search atau Randomized Search untuk meningkatkan performa baseline model.

3. **Solusi 3 (Opsi Pertimbangan - untuk perbandingan pendekatan):** Mengembangkan model Deep Learning berbasis Sequential (ANN) dengan variasi layer dan dropout, lalu membandingkannya dengan model tradisional ML untuk menilai keefektifan pendekatan deep learning dalam kasus prediksi akademik.

#### **Evaluasi:**

Semua solusi akan dievaluasi menggunakan:

1. Confusion Matrix: Untuk melihat performa per algorima


## Data Understanding
Dataset perfoma akademik yang digunakan adalah:
https://www.kaggle.com/datasets/rabieelkharoua/students-performance-dataset

Dataset ini terdiri dari 2392 baris dan 15 kolom, yang mencakup berbagai informasi penting tentang karakteristik siswa, lingkungan keluarga, kebiasaan belajar, serta performa akademik mereka. Variabel-variabel dalam dataset ini mencakup data numerik murni yang dapat digunakan untuk memprediksi kesuksesan akademik berdasarkan faktor-faktor personal dan eksternal menggunakan metode klasifikasi.

### Variabel-variabel pada Student Perfomance Academic dataset adalah sebagai berikut:

### 1. Kolom Target (GradeClass)
Kolom GradeClass adalah variabel dependen (target) yang akan diprediksi oleh model dalam tugas klasifikasi. Nilai dari GradeClass berbentuk kategori numerik diskrit:

* 0.0: Sangat Baik

* 1.0: Baik

* 2.0: Cukup

* 3.0: Kurang

* 4.0: Sangat Kurang

Tujuan analisis prediktif adalah memprediksi kelas nilai siswa berdasarkan berbagai faktor karakteristik dan kebiasaan mereka.

### 2. Indeks Prestasi Kumulatif (GPA)

Kolom GPA adalah nilai akademik akhir dalam skala desimal (misal: 0.0 – 4.0).

* 0-0.99: Sangat kurang (Failing)

* 1-1.99: Kurang (Poor)

* 2-2.99: Cukup (Average)

* 3-3.49: Baik (Good)

* 3.5-4.00: Sangat Baik (Excellent)

GPA bisa digunakan sebagai fitur prediktor terhadap GradeClass dengan analisis Hubungan antara GPA dan GradeClass bersifat kuat dan langsung, menjadikan GPA salah satu fitur utama dalam model prediksi.

### 3. Usia Siswa (Age)

Kolom Age menunjukkan usia siswa (dalam tahun), yang umumnya berada di rentang 15 hingga 18 tahun, sesuai dengan usia sekolah menengah atas.

* Kelompok usia 16–17 tahun kemungkinan menjadi mayoritas.

* Perlu dianalisis apakah usia lebih tua terkait dengan pengulangan kelas atau nilai rendah.

* Sebaliknya, siswa yang lebih muda dan mendapat nilai baik bisa mencerminkan siswa berprestasi.

### 4. Jenis Kelamin (Gender)
Kolom Gender dikodekan sebagai:

* 0: Laki-laki

* 1: Perempuan

### 5. Etnis Siswa (Ethnicity)

Kolom Ethnicity menunjukkan latar belakang etnis siswa, dikodekan numerik (0, 1, 2, dst). pengkodean dikatagorikan sebagai berikut:

* 0: Asia
* 1: Kulit Putih
* 2: Hispanik
* 3: Afrika-Amerika

Analisis dapat mengungkap disparitas pencapaian akademik antar kelompok etnis dan menginformasikan kebijakan pendidikan yang inklusif.

### 6. Pendidikan Orang Tua (ParentalEducation)

Kolom ParentalEducation merepresentasikan tingkat pendidikan tertinggi orang tua:

* 0: Tidak sekolah
* 1: SD
* 2: SMP
* 3: SMA
* 4: Perguruan Tinggi

### 7. Waktu Belajar per Minggu (StudyTimeWeekly)

Kolom StudyTimeWeekly menunjukkan jumlah jam yang dihabiskan siswa untuk belajar setiap minggu (angka desimal).

* Semakin tinggi waktu belajar, umumnya berkorelasi positif dengan GPA dan GradeClass.
* Namun perlu diperhatikan: efisiensi dan kualitas belajar lebih penting daripada kuantitas semata.

### 8. Jumlah Ketidakhadiran (Absences)

Kolom Absences mencatat jumlah hari siswa tidak hadir di sekolah.

* Siswa dengan absensi tinggi (misalnya >10 hari) umumnya memiliki korelasi negatif terhadap nilai akhir.

* Kolom ini penting sebagai fitur prediktor utama dalam model klasifikasi.

### 9. Ikut Les Tambahan (Tutoring)

Kolom Tutoring menunjukkan apakah siswa mengikuti les/bimbingan belajar:

* 0: Tidak ikut les
* 1: Ikut les

Les tambahan sering meningkatkan pemahaman konsep akademik. Bisa menjadi indikator dukungan keluarga dan motivasi siswa.

### 10. Dukungan Orang Tua (ParentalSupport)

Kolom ini menggambarkan tingkat keterlibatan orang tua dalam pendidikan anak, dikodekan ordinal:

* 0: Tidak ada
* 1: Rendah
* 2: Sedang
* 3: Tinggi
* 4: Sangat tinggi

Dukungan orang tua mungkin memiliki pengaruh signifikan dalam membentuk perilaku belajar siswa dan motivasi internal.

### 11. Kegiatan Penunjang Lainnya

**A. Partisipasi Ekstrakurikuler (Extracurricular)**

Kolom ini menunjukkan seberapa aktif siswa terlibat dalam kegiatan non-akademik seperti klub, organisasi, atau komunitas:

* 0: Tidak ikut
* 1: Ikut

**B. Aktivitas Olahraga (Sports)**

Kolom Sports menunjukkan apakah siswa aktif secara fisik:

* 0: Tidak
* 1: Ya

Olahraga dapat meningkatkan fokus, regulasi stres, dan energi belajar — relevan sebagai fitur dalam prediksi kinerja akademik.

**C. Aktivitas Musik (Music)**

Kolom Music menunjukkan partisipasi dalam kegiatan musik:

* 0: Tidak
* 1: Ya

Aktivitas musik dikaitkan dengan kemampuan berpikir abstrak, konsentrasi, dan kreativitas, yang semuanya dapat berdampak pada performa akademik.

**D. Kegiatan Sukarela (Volunteering)**

Kolom ini merepresentasikan apakah siswa aktif dalam kegiatan sosial/relawan:

* 0: Tidak
* 1: Ya

Siswa yang aktif dalam kegiatan sukarela cenderung memiliki keterampilan sosial, empati, dan motivasi intrinsik yang tinggi.

![Confusion Matrix](![Confusion Matrix](https://raw.githubusercontent.com/BimaTechgit/gambar/main/download%20(11).png)

**Rubrik/Kriteria Tambahan (Opsional)**:
- Melakukan beberapa tahapan yang diperlukan untuk memahami data, contohnya teknik visualisasi data atau exploratory data analysis.

## Data Preparation
Pada bagian ini Anda menerapkan dan menyebutkan teknik data preparation yang dilakukan. Teknik yang digunakan pada notebook dan laporan harus berurutan.

**Rubrik/Kriteria Tambahan (Opsional)**:
- Menjelaskan proses data preparation yang dilakukan
- Menjelaskan alasan mengapa diperlukan tahapan data preparation tersebut.

## Modeling
Tahapan ini membahas mengenai model machine learning yang digunakan untuk menyelesaikan permasalahan. Anda perlu menjelaskan tahapan dan parameter yang digunakan pada proses pemodelan.

**Rubrik/Kriteria Tambahan (Opsional)**:
- Menjelaskan kelebihan dan kekurangan dari setiap algoritma yang digunakan.
- Jika menggunakan satu algoritma pada solution statement, lakukan proses improvement terhadap model dengan hyperparameter tuning. **Jelaskan proses improvement yang dilakukan**.
- Jika menggunakan dua atau lebih algoritma pada solution statement, maka pilih model terbaik sebagai solusi. **Jelaskan mengapa memilih model tersebut sebagai model terbaik**.

## Evaluation
Pada bagian ini anda perlu menyebutkan metrik evaluasi yang digunakan. Lalu anda perlu menjelaskan hasil proyek berdasarkan metrik evaluasi yang digunakan.

Sebagai contoh, Anda memiih kasus klasifikasi dan menggunakan metrik **akurasi, precision, recall, dan F1 score**. Jelaskan mengenai beberapa hal berikut:
- Penjelasan mengenai metrik yang digunakan
- Menjelaskan hasil proyek berdasarkan metrik evaluasi

Ingatlah, metrik evaluasi yang digunakan harus sesuai dengan konteks data, problem statement, dan solusi yang diinginkan.

**Rubrik/Kriteria Tambahan (Opsional)**:
- Menjelaskan formula metrik dan bagaimana metrik tersebut bekerja.

**---Ini adalah bagian akhir laporan---**

_Catatan:_
- _Anda dapat menambahkan gambar, kode, atau tabel ke dalam laporan jika diperlukan. Temukan caranya pada contoh dokumen markdown di situs editor [Dillinger](https://dillinger.io/), [Github Guides: Mastering markdown](https://guides.github.com/features/mastering-markdown/), atau sumber lain di internet. Semangat!_
- Jika terdapat penjelasan yang harus menyertakan code snippet, tuliskan dengan sewajarnya. Tidak perlu menuliskan keseluruhan kode project, cukup bagian yang ingin dijelaskan saja.

