# Laporan Proyek Machine Learning Prediksi Performa Akademik Siswa - Bimasakti Faturrahman Soetedjo

## Domain Proyek

Dalam era globalisasi dan transformasi digital saat ini, pendidikan memainkan peran sentral dalam membentuk sumber daya manusia yang kompeten dan adaptif. Performa akademik siswa menjadi indikator utama dalam menilai efektivitas sistem pendidikan serta kesiapan individu dalam menghadapi tantangan masa depan. Pendidikan menengah atas merupakan fase krusial dalam perkembangan akademik siswa, di mana pencapaian akademik tidak hanya mencerminkan kemampuan kognitif, tetapi juga dipengaruhi oleh berbagai faktor eksternal dan internal. Faktor-faktor seperti latar belakang keluarga, motivasi belajar, keterlibatan orang tua, demografis, dukungan orang tua, dan partisipasi dalam kegiatan ekstrakurikuler dapat memengaruhi kinerja akademik siswa. Oleh karena itu, penting untuk mengidentifikasi dan memahami faktor-faktor yang memengaruhi performa akademik guna merancang intervensi yang efektif.

sebagai referensi, Penelitian oleh [(Zhigang et al, 2023)](https://so06.tci-thaijo.org/index.php/jomld/article/view/266002) menemukan bahwa motivasi intrinsik, efikasi diri, dan regulasi diri serta efikasi diri belajar juga berkontribusi terhadap keberhasilan akademik dan memiliki korelasi positif yang signifikan dengan kesuksesan akademik siswa sekolah menengah atas. disisi lain, kompleksitas faktor-faktor yang memengaruhi keberhasilan akademik serta tantangan dalam pendidikan menengah atas tidak hanya berasal dari faktor individu siswa dan keluarga. hal ini dibuktikan oleh Studi oleh [(Costa et al, 2024)](https://link.springer.com/article/10.1007/s11218-024-09941-z?) yang menyoroti bahwa faktor-faktor Lingkungan sekolah, seperti iklim sekolah dan dukungan dari guru termasuk kualitas pengajaran dan dukungan sosial, juga memainkan peran penting yang dapat memengaruhi pencapaian akademik siswa.

Penilaian Performa akademik siswa menjadi sangat krusial dalam menilai efektivitas sistem pendidikan serta kesiapan individu dalam menghadapi tantangan masa depan karena Jika kondisi ini terus dibiarkan, maka potensi siswa dalam menyerap dan mencapai potensi akademik terbaik mereka tidak dapat tercapai. Hal ini berisiko menurunkan kualitas lulusan, memperbesar angka putus sekolah, dan meningkatkan ketimpangan pendidikan. sehingga diperlukan pendekatan yang lebih adaptif dan proaktif dalam memantau dan meningkatkan performa mereka.

Dalam menjawab tantangan tersebut, pendekatan berbasis data seperti Educational Data Mining (EDM) dan Learning Analytics (LA) telah digunakan untuk menganalisis dan memprediksi performa akademik siswa. Dengan memanfaatkan algoritma Machine Learning (ML) dan Deep Learning (DL), institusi pendidikan dapat mengidentifikasi pola-pola yang tersembunyi dalam data siswa, memungkinkan prediksi yang lebih akurat terhadap kinerja akademik mereka.

Penggunaan algoritma ML seperti Random Forest, Support Vector Machine, dan Neural Networks mampu menjadi solusi dalam memprediksi performa akademik dengan akurasi yang tinggi. Misalnya, penelitian oleh [(Orji, Vassileva 2022)](https://arxiv.org/abs/2210.08186) menunjukkan bahwa model Random Forest dapat mencapai akurasi prediksi hingga 94,9% dalam memprediksi performa akademik mahasiswa berdasarkan atribut motivasi belajar. Selain itu, pendekatan DL seperti Long Short-Term Memory (LSTM) telah digunakan untuk menganalisis data pendidikan secara mendalam, memungkinkan identifikasi tren jangka panjang dalam perilaku belajar siswa [(Wang et al., 2024)](https://arxiv.org/abs/2407.16907)

Lebih lanjut, review sistematis oleh [(Sghir et al. 2022)](https://link.springer.com/article/10.1007/s10639-022-11536-0) mengidentifikasi bahwa model prediktif yang menggabungkan data demografis, perilaku belajar, dan kinerja akademik sebelumnya dapat mencapai akurasi prediksi yang tinggi, terutama ketika menggunakan teknik DL seperti Deep Neural Networks (DNNs) dan Long Short-Term Memory (LSTM). Hal ini menunjukkan potensi besar dari pendekatan ini dalam meningkatkan kualitas pendidikan melalui analisis data yang mendalam.

Dengan mempertimbangkan pentingnya prediksi performa akademik dalam meningkatkan kualitas pendidikan, penelitian ini bertujuan untuk mengembangkan model prediktif menggunakan algoritma ML dan DL berdasarkan dataset "Student Performance: Academic Success Factors in High School Students". Model ini diharapkan dapat membantu institusi pendidikan dalam merancang strategi intervensi yang lebih efektif dan tepat sasaran.

**Referensi**:

- [Factors Affecting on Academic Success of Senior High School Students](https://so06.tci-thaijo.org/index.php/jomld/article/view/266002),
- [Determinants of academic achievement from the middle to secondary school education: A systematic review](https://link.springer.com/article/10.1007/s11218-024-09941-z)
- [Machine Learning Approach for Predicting Students Academic Performance and Study Strategies based on their Motivation](https://arxiv.org/abs/2210.08186)
- [Research on Education Big Data for Students Academic Performance Analysis based on Machine Learning](https://arxiv.org/abs/2407.16907)
- [Recent advances in Predictive Learning Analytics: A decade systematic review (2012–2022)](https://link.springer.com/article/10.1007/s10639-022-11536-0)

## Business Understanding

### Problem Statements

Menjelaskan pernyataan masalah latar belakang:
1. Pernyataan Masalah 1: Institusi pendidikan kesulitan dalam mengidentifikasi siswa yang berisiko mengalami penurunan performa akademik sejak dini, karena kompleksitas faktor yang mempengaruhi, seperti kehadiran, aktivitas ekstrakurikuler, dukungan orang tua, dan kebiasaan belajar.

2. Pernyataan Masalah 2: Belum tersedia analisis prediktif berbasis data yang mampu secara akurat memperkirakan nilai akhir siswa atau kategori kelas akademik (GradeClass), sehingga intervensi pendidik sering kali bersifat reaktif, bukan proaktif.

3. Pernyataan Masalah 3: 
Pemanfaatan algoritma pembelajaran mesin dan pembelajaran mendalam di tingkat pendidikan menengah masih terbatas, terutama dalam hal akurasi prediksi dan interpretabilitas model yang dibutuhkan untuk pengambilan keputusan oleh pendidik.

### Goals

Menjelaskan tujuan dari pernyataan masalah:

1. Mengembangkan model prediktif GradeClass siswa berdasarkan data demografis, kebiasaan belajar, dan aktivitas siswa, guna mengidentifikasi siswa yang berisiko rendah atau tinggi performa akademiknya secara dini.
  
2. Membangun sistem klasifikasi berbasis data yang dapat secara akurat memetakan kategori nilai akademik akhir siswa, sehingga sekolah dapat melakukan intervensi yang lebih proaktif dan terarah.

3. Mengeksplorasi dan membandingkan efektivitas algoritma machine learning dan deep learning, untuk menghasilkan model yang akurat, stabil, dan cukup interpretatif dalam mendukung pengambilan keputusan pendidik.

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

### visualisasi data atau exploratory data analysis.
![gradeclass](https://github.com/BimaTechgit/gambar/blob/main/download%20(11).png?raw=true)
![GPA](https://github.com/BimaTechgit/gambar/blob/main/download%20(12).png?raw=true)
![Absences](https://github.com/BimaTechgit/gambar/blob/main/download%20(13).png?raw=true)
![StudyTimeWeekly](https://github.com/BimaTechgit/gambar/blob/main/download%20(14).png?raw=true)

### Analisis Data berdasarkan Grafik

Distribusi GradeClass menunjukkan ketidakseimbangan kelas yang signifikan, di mana kelas nilai terendah (4.0) mendominasi dengan 1.211 siswa , sementara jumlah siswa pada kategori nilai lebih tinggi semakin menurun (3.0: 414 siswa, 2.0: 391 siswa, 1.0: 269 siswa, dan 0.0: 107 siswa). Pola ini mengindikasikan bahwa pencapaian akademik tinggi relatif langka dalam dataset, sedangkan hasil rendah lebih umum. Ketidakseimbangan ini berpotensi memengaruhi performa model prediktif karena algoritma cenderung "memprediksi" kelas mayoritas. Faktor seperti absensi, waktu belajar, atau dukungan lingkungan mungkin menjadi penyebab utama dominasi kelas 4.0, sehingga perlu analisis lebih lanjut untuk mengidentifikasi intervensi pendidikan yang tepat.

---


Distribusi GPA (Indeks Prestasi Kumulatif) menunjukkan pola unimodal dengan mayoritas siswa berada di rentang 1.5–2.5 , sedangkan jumlah siswa menurun secara bertahap untuk GPA di bawah 1.0 atau di atas 3.0 . Hal ini mencerminkan bahwa sebagian besar siswa memiliki kemampuan akademik stabil di kategori menengah, tetapi sedikit yang mencapai nilai sangat tinggi atau sangat rendah. Beberapa siswa dengan GPA tinggi (>3.0) mungkin mendapat dukungan eksternal seperti les privat atau memiliki strategi belajar efisien, sementara yang berada di GPA rendah (<1.0) mungkin memerlukan pendekatan khusus untuk meningkatkan prestasi. Korelasi kuat antara GPA dan GradeClass menunjukkan bahwa kedua variabel ini saling terkait erat dalam menentukan performa akademik.

---

Visualisasi distribusi absensi berdasarkan GradeClass mengungkapkan tren positif : semakin rendah kelas nilai akhir (semakin tinggi angka GradeClass), semakin tinggi tendensi jumlah absensi. Siswa dengan GradeClass 4.0 memiliki median absensi tertinggi (>20 hari) , sementara GradeClass 0.0 memiliki median absensi terendah (>3–4 hari). meskipun ada pengecualian seperti 33 siswa GradeClass 0.0 dengan absensi >10 hari, Ini menunjukkan bahwa walaupun siswa tersebut jarang masuk, faktor lain—seperti efisiensi belajar atau dukungan orang tua—dapat "menutupi" dampak negatif absensi. Intervensi seperti program bimbingan khusus atau monitoring absensi perlu diprioritaskan untuk kelas 3.0–4.0, sementara siswa GradeClass tinggi perlu dievaluasi untuk mencegah burnout atau kelelahan belajar.

---

Distribusi StudyTimeWeekly berdasarkan GradeClass menunjukkan tren negatif semakin tinggi kelas nilai akhir (semakin rendah angka GradeClass), semakin tinggi tendensi waktu belajar mingguan. Siswa dengan GradeClass 0.0 memiliki median waktu belajar ~12–15 jam/minggu , sementara GradeClass 4.0 hanya mencatat ~8–10 jam/minggu . Meski ada outlier seperti siswa dengan waktu belajar ekstrem (>18 jam/minggu) di GradeClass 0.0, sebagian besar pola ini selaras dengan hipotesis bahwa waktu belajar adalah indikator penting dalam pencapaian akademik. Namun, beberapa siswa dengan waktu belajar rendah tetap mencapai GradeClass baik, mengindikasikan bahwa kualitas belajar atau faktor lain (misalnya, les tambahan) mungkin lebih berpengaruh. Korelasi negatif kuat antara StudyTimeWeekly dan GradeClass memperkuat hubungan ini, tetapi hubungan tersebut tidak mutlak karena ada kasus di mana waktu belajar tinggi tidak selalu menghasilkan nilai terbaik.


---

Secara keseluruhan, data menunjukkan hubungan kuat antara GradeClass dengan absensi dan waktu belajar. Kelas nilai yang tidak seimbang, dominasi GPA menengah, serta tren jelas pada absensi dan waktu belajar mengindikasikan bahwa faktor-faktor ini saling terkait erat dalam menentukan performa akademik. Namun, pengecualian pada beberapa siswa menunjukkan bahwa kualitas belajar, dukungan eksternal, atau efisiensi belajar juga merupakan variabel penting yang perlu dipertimbangkan untuk intervensi pendidikan yang lebih personal.

![heatmap](https://github.com/BimaTechgit/gambar/blob/main/download%20(18).png?raw=true)
![heatmap](https://github.com/BimaTechgit/gambar/blob/main/download%20(19).png?raw=true)

### **Analisis Matrix Korelasi**

Berdasarkan heatmap matriks korelasi yang Anda tampilkan, berikut adalah analisis mendalam mengenai hubungan antar fitur numerik dalam dataset "Student Performance: Academic Success Factors in High School Students":

### 1. Korelasi Positif Terkuat

- **GradeClass vs Absences: +0.73**

- Artinya, semakin tinggi jumlah ketidakhadiran (Absences), maka semakin tinggi pula nilai GradeClass. Karena GradeClass direpresentasikan dalam bentuk label diskrit, nilai lebih besar mungkin mewakili performa akademik yang lebih buruk (misalnya, kelas 4 berarti nilai terendah).Maka korelasi positif ini menunjukkan: Absensi tinggi berkorelasi dengan performa akademik buruk.

### 2. Korelasi Negatif Terkuat

- **GPA vs Absences: -0.92**

- Ini adalah hubungan negatif yang sangat kuat. Artinya: semakin sering siswa tidak hadir, semakin rendah GPA-nya. Hal ini masuk akal secara intuitif, karena absensi berlebih menyebabkan kehilangan materi pelajaran.

- **GPA vs GradeClass: -0.78**

- Korelasi negatif tinggi menunjukkan bahwa semakin tinggi GPA siswa, maka GradeClass semakin rendah (berarti lebih baik). Mengonfirmasi bahwa GradeClass kemungkinan besar mewakili kategori performa, dari baik (0) ke buruk (4).

### 3. Korelasi Antar Variable/Korelasi Lemah/Tidak Signifikan

- StudyTimeWeekly & GPA :

- Korelasi +0.18 (merah muda) menunjukkan hubungan positif sedang : jam belajar tinggi menunjukan bahwa siswa yang meluangkan waktu belajar extra akan memiliki GPA tinggi walaupun tidak signnifikan karena GPA tinggi tidak menjamin gradeclass bagus yang terbukti dengan korelasi -0.13 antara StudyTimeWeekly dan ClassGrade yang menyatakan hubungan negatif sedang

- ParentalSupport

- Korelasi +0.19 (merah muda) menunjukkan hubungan positif sedang : dukungan orang tua cenderung meningkatkan partisipasi siswa dan motivasi untuk terus belajar walaupun korelasi ini terdapat -0.14 pada hubungan parentalsupport dan gradeclass yang menunjukan korelasi negatif sedang yang juga berarti walaupun dapat dukungan penuh orang tua, kemauan siswa untuk belajar dan meningkatkan perfoma kembali pada diri sendiri.

- Tutoring & GPA :
- Korelasi +0.15 (merah muda) mengindikasikan bahwa siswa yang menggunakan bimbingan les untuk menunjang perfoma akademik mereka tetapi tutoring ini memiliki korelasi negatif sedang dengan gradeclass sebesar -0.11 yang berarti bimbingan belajar tidak menjamin perfoma akademik membaik secara signifikan dan perfoma akademik ditentukan oleh diri sendiri.

**Kesimpulan:**

Matriks korelasi menunjukkan bahwa Absences dan GPA dan absences memiliki pengaruh paling signifikan terhadap GradeClass, dengan korelasi positif kuat (+0.73) untuk absensi dan negatif kuat (-0.78 dan -0.92) untuk GPA. Waktu belajar mingguan (StudyTimeWeekly ) juga berkontribusi signifikan (korelasi 0.18), meski hubungannya lebih lemah. Variabel seperti dukungan orang tua (ParentalSupport ) dan partisipasi ekstrakurikuler (Extracurricular ) memiliki korelasi positif moderat, sementara aktivitas seperti olahraga atau musik kurang relevan. Korelasi rendah antar variabel lain menunjukkan bahwa faktor seperti bimbingan les (Tutoring ) atau kegiatan sukarela (Volunteering) tidak secara langsung memengaruhi hasil akademik. Secara keseluruhan, absensi dan GPA menjadi fokus utama intervensi, sementara faktor lain perlu analisis lebih lanjut untuk memahami interaksi kompleksnya.

## Data Preparation

Karena dataset sepenuhnya terdiri dari fitur numerik, maka tahap data preparation bisa dilakukan tanpa perlu One-Hot Encoding. Kita hanya perlu:

- Memisahkan fitur (X) dan target (y).
- Proses: Fitur (X): Semua kolom atau variabel dalam dataset yang akan digunakan untuk memprediksi sesuatu. Ini adalah data input. Target (y): Kolom atau variabel tunggal yang ingin diprediksi oleh model. Ini adalah data output yang menjadi tujuan model.
- Alasan: Model machine learning belajar dari data masukan (fitur) untuk memprediksi atau mengklasifikasikan keluaran yang diinginkan (target). Pemisahan ini esensial karena model perlu tahu apa yang harus dipelajari (fitur) dan apa yang harus diprediksi (target). Tanpa pemisahan ini, model tidak akan tahu tujuan belajarnya.

- Melakukan normalisasi (MinMaxScaler).
- Proses: Data numerik dinormalisasi menggunakan teknik Min-Max Scaling agar setiap fitur memiliki skala yang sama.
- Alasan: Normalisasi diperlukan untuk mencegah bias pada fitur tertentu yang memiliki skala lebih besar dibandingkan fitur lainnya dan membuat model konvergen lebih optimal.

- Membagi data menjadi train dan test set.
- Proses: Data dibagi menjadi data latih (80%) dan data uji (20%) menggunakan train_test_split.
- Alasan: Pembagian ini diperlukan untuk mengevaluasi performa model secara objektif pada data yang belum pernah dilihat model sebelumnya.

## Modeling

### **Random Forest**

Random Forest adalah algoritma ensemble learning berbasis decision tree yang menggabungkan banyak pohon keputusan (trees) untuk menghasilkan prediksi yang lebih kuat dan stabil. Ia bekerja dengan membuat banyak pohon (forest) pada data training dan menggabungkan hasil prediksi dari setiap pohon melalui vote mayoritas (klasifikasi) atau rata-rata (regresi).

### **Parameter Penting Random Forest**

| Parameter           | Fungsi                                                                                         |
| ------------------- | ---------------------------------------------------------------------------------------------- |
| `n_estimators`      | Jumlah pohon dalam hutan (semakin banyak, semakin stabil tapi lebih lambat)                    |
| `max_depth`         | Kedalaman maksimal tiap pohon (menghindari overfitting jika terlalu dalam)                     |
| `min_samples_split` | Jumlah minimal sampel untuk membagi node                                                       |
| `min_samples_leaf`  | Jumlah minimal sampel di setiap daun pohon                                                     |
| `max_features`      | Jumlah fitur yang dipertimbangkan untuk split terbaik (misalnya `'sqrt'`, `'log2'`, atau None) |
| `class_weight`      | Menyeimbangkan bobot kelas jika target tidak seimbang (misalnya `'balanced'`)                  |
| `random_state`      | Untuk memastikan hasil yang konsisten saat dijalankan berulang kali                            |

### **Tahapan Pemodelan dengan Random Forest**
**1. Data Preparation**
- Dataset dipisahkan menjadi fitur (X) dan target (y).

- Karena semua kolom bersifat numerik, dilakukan normalisasi dengan MinMaxScaler agar semua fitur berada pada skala yang seragam (0–1).

- Data dibagi menjadi data latih dan data uji menggunakan train_test_split dengan rasio 80:20.

**2. Inisialisasi Model Random Forest Menggunakan RandomForestClassifier dari sklearn.ensemble.**

- Model dibuat dengan beberapa parameter penting untuk mengatur kompleksitas dan performa.

**3. Pelatihan Model**
- Model dilatih menggunakan X_train dan y_train.

- Proses ini melibatkan pembentukan banyak pohon keputusan dan pembelajaran dari data latih.

**4. Prediksi**
- Model yang telah dilatih digunakan untuk memprediksi kelas target (GradeClass) pada data uji (X_test).

**5. Evaluasi**

- Accuracy: Persentase prediksi yang benar.

- Classification report: Mencakup precision, recall, dan f1-score.

- Confusion matrix: Untuk melihat detail prediksi benar vs salah per kelas

### **Kelebihan Random Forest**

- Akurat & powerful pada banyak jenis dataset.

- Tidak mudah overfitting berkat averaging dari banyak pohon.

- Dapat Menangani data numerik dan kategorikal.

- Tahan terhadap noise & outlier.

- Dapat menghitung feature importance untuk interpretasi model.

### **Kekurangan Random Forest**

- Kurang interpretatif dibanding model tunggal seperti Decision Tree.

- Waktu training & prediksi bisa lambat jika jumlah pohon besar.

- Model besar dan kompleks (tidak cocok untuk deployment ringan seperti di mobile).

### **XGBoost Classifier**

XGBoost (Extreme Gradient Boosting) adalah algoritma boosting yang sangat powerful untuk tugas klasifikasi dan regresi. Ia bekerja dengan cara membangun banyak model (pohon keputusan) secara berurutan. Setiap model baru mencoba memperbaiki kesalahan dari model sebelumnya.

XGBoost dikenal karena efisiensi, fleksibilitas, dan performanya yang tinggi di kompetisi data science.

| Parameter          | Fungsi                                                          |
| ------------------ | --------------------------------------------------------------- |
| `n_estimators`     | Jumlah pohon boosting                                           |
| `learning_rate`    | Ukuran langkah tiap iterasi pembelajaran                        |
| `max_depth`        | Kedalaman maksimum pohon                                        |
| `subsample`        | Proporsi sampel pelatihan yang digunakan per pohon              |
| `colsample_bytree` | Proporsi fitur yang digunakan saat membangun pohon              |
| `objective`        | Fungsi tujuan; untuk klasifikasi multiclass → `'multi:softmax'` |
| `num_class`        | Jumlah kelas target (wajib jika multiclass)                     |
| `random_state`     | Untuk reproducibility hasil                                     |

### **Tahapan Pemodelan XGBoost**
1. Inisialisasi model dengan parameter:
  - objective='multi:softmax'

  - num_class=jumlah_kelas
  
  - n_estimators=100, learning_rate=0.1, max_depth=5

2. Training model menggunakan X_train dan y_train

3. Prediksi menggunakan X_test

4. Evaluasi menggunakan accuracy, classification report, dan confusion matrix

### **Kelebihan**
- Akurasi tinggi, cocok untuk dataset kompleks

- Mendukung regulasi (mengurangi overfitting)

- Cepat dan efisien

- Cocok untuk data numerik

### **Kekurangan**
- Tidak terlalu transparan/interpretatif

- Butuh tuning parameter untuk performa optimal

- Bisa overfitting jika data terlalu kecil atau noise tinggi

### **Logistic Regression**

Logistic Regression adalah algoritma linier untuk klasifikasi yang memperkirakan probabilitas kelas target menggunakan fungsi sigmoid. Meskipun namanya "regression", algoritma ini digunakan untuk klasifikasi biner atau multiklas. Cocok untuk baseline model dan dataset yang fitur-fiturnya berhubungan secara linier dengan target.

### **Parameter Penting**
| Parameter     | Fungsi                                                          |
| ------------- | --------------------------------------------------------------- |
| `penalty`     | Jenis regularisasi (`'l2'` umum digunakan)                      |
| `solver`      | Algoritma optimisasi (`'lbfgs'` cocok untuk multiclass)         |
| `multi_class` | `'multinomial'` untuk multi-kelas                               |
| `max_iter`    | Iterasi maksimum untuk konvergensi                              |

### **Tahapan Pemodelan Logistic Regression**

1. Inisialisasi model dengan parameter:

  - multi_class='multinomial'

  - solver='lbfgs'

  - max_iter=1000

2. Training model menggunakan X_train dan y_train

3. Prediksi menggunakan X_test

4. Evaluasi menggunakan accuracy, classification report, dan confusion matrix

### **Kelebihan**
- Mudah diinterpretasikan

- Cepat dan efisien

- Cocok sebagai baseline

- Tidak mudah overfitting pada data sederhana

### **Kekurangan**
- Kurang cocok untuk hubungan non-linear

- Kurang powerful untuk data besar/kompleks

- Kurang akurat dibanding model kompleks seperti XGBoost/Random Forest

### **Artificial Neural Network (ANN)**

Artificial Neural Network (ANN) adalah model deep learning yang terinspirasi dari jaringan saraf biologis. ANN terdiri dari lapisan-lapisan neuron (unit), yang dibagi menjadi Input Layer untuk menerima data masukan, Hidden Layer(s) untuk memproses input dengan bobot dan fungsi aktivasi, Output Layer untuk menghasilkan prediksi. ANN cocok digunakan untuk klasifikasi dan regresi, termasuk klasifikasi multikelas seperti dataset performa akademik yang sedang kamu kerjakan.

### **Parameter Penting dalam ANN**

| Parameter       | Keterangan                                                                      |
| --------------- | ------------------------------------------------------------------------------- |
| `input_dim`     | Jumlah fitur dari data masukan.                                                 |
| `hidden_layers` | Jumlah lapisan tersembunyi.                                                     |
| `units`         | Jumlah neuron dalam tiap layer.                                                 |
| `activation`    | Fungsi aktivasi (ReLU, Sigmoid, Softmax, dsb).                                  |
| `optimizer`     | Metode optimasi (Adam, SGD, RMSprop).                                           |
| `loss`          | Fungsi loss (categorical\_crossentropy atau sparse\_categorical\_crossentropy). |
| `epochs`        | Jumlah iterasi pelatihan model.                                                 |
| `batch_size`    | Ukuran batch data pada setiap iterasi.                                          |
| `metrics`       | Metode evaluasi seperti accuracy, precision, dll.                               |

### **Tahapan & Parameter Pemodelan ANN**
1. Normalisasi Data: Skala semua fitur ke rentang [0, 1] agar ANN cepat konvergen.

2. Split Data: Membagi data ke train/test seperti sebelumnya (misalnya 80:20).

3. Arsitektur Model

  - Input layer: jumlah fitur numerik.

  - Hidden layer 1–2 lapisan: misalnya 64–128 neuron.

  - Output layer: jumlah kelas (GradeClass = 5 → 5 output neurons).

4. Fungsi Aktivasi

  - ReLU untuk hidden layers.

  - Sigmoid untuk output layer prediksi probabilitas (klasifikasi biner)

5. Optimizer: Adam umumnya terbaik untuk kecepatan dan akurasi.

6. Loss Function: sparse_categorical_crossentropy jika target berupa label numerik, bukan one-hot.

### **Kelebihan ANN**
- Mampu menangani kompleksitas non-linear dengan baik.

- Bisa belajar representasi fitur secara otomatis.

- Sangat fleksibel dan scalable.

### **Kekurangan ANN**
- Membutuhkan banyak data agar efektif.

- Interpretasi hasil sulit (black-box).

- Overfitting jika tidak diberi regularisasi.

| **Model**             | **Akurasi** | **Precision**  | **Recall**  | **F1 Score**  |
|------------------------|-------------|---------------|-------------|---------------|
| Logistic Regression    | 0.9206      | 0.9199        | 0.9206      | 0.9189        |
| Random Forest          | 0.9206      | 0.9225        | 0.9206      | 0.9190        |
| Support Vector Machine | 0.7432      | 0.7332        | 0.7432      | 0.7353        |
| Deep Learning          | 0.8162      | 0.8206        | 0.8162      | 0.8137        |


berdasarkan hasil membangun model dan juga hasil akurasi dari 4 algoritma yang ada, Model Terbaik adalah XGBoost Classifier

model ini menghasilkan akurasi tertinggi dan identik (92.07%). walaupun random forest juga menghasilkan akurasi yang sama yaitu (92.07%) namun berbedaan skor yang unggul ada para presicion dan F1-Score XGboost yang sedikit lebih unggul walaupun berbedaan ini sangat tipis. Maka dari itu, Dipilih: XGBoost sebagai solusi terbaik, dengan alasan:

Akurasi sama dengan Random Forest, tapi lebih cepat dalam training dan menangani data yang besar.

XGboost lebih interpretatif dan diunggulkan terhadap data numerik pada dataset yang ada, cocok untuk deployment awal atau produksi.

XGBoost sangat powerful dan lebih kompleks, cocok untuk kompetisi atau data sangat besar.

## Evaluation

### **Kesimpulan Evaluasi Model:**

 Berdasarkan hasil evaluasi model menggunakan metrik Akurasi, Precision, Recall, dan F1 Score, berikut adalah analisis dari masing-masing model:

 ![confussion](https://github.com/BimaTechgit/gambar/blob/main/download%20(17).png?raw=true)

1. Random Forest:

  - Akurasi: 0.9206
  - Precision: 0.9199
  - Recall: 0.9206
  - F1 Score: 0.9189

| Kelas | TP  | FN | FP | TN  |
| ----- | --- | -- | -- | --- |
| 0     | 12  | 9  | 2  | 458 |
| 1     | 48  | 6  | 7  | 420 |
| 2     | 74  | 4  | 5  | 398 |
| 3     | 74  | 9  | 5  | 393 |
| 4     | 233 | 11 | 12 | 328 |

2. XGBoost:

  - Akurasi: 0.9206
  - Precision: 0.9225
  - Recall: 0.9206
  - F1 Score: 0.9190

| Kelas | TP  | FN | FP | TN  |
| ----- | --- | -- | -- | --- |
| 0     | 11  | 10 | 5  | 455 |
| 1     | 50  | 4  | 10 | 417 |
| 2     | 75  | 2  | 5  | 399 |
| 3     | 73  | 7  | 10 | 386 |
| 4     | 232 | 10 | 6  | 328 |

3. Logistic Regression:

  - Akurasi: 0.7432
  - Precision: 0.7332
  - Recall: 0.7432
  - F1 Score: 0.7353

| Kelas | TP  | FN | FP | TN  |
| ----- | --- | -- | -- | --- |
| 0     | 4   | 21 | 13 | 448 |
| 1     | 21  | 34 | 32 | 399 |
| 2     | 53  | 15 | 31 | 387 |
| 3     | 49  | 33 | 24 | 380 |
| 4     | 229 | 14 | 25 | 338 |

4. Artificial Neural Network (ANN):

  - Akurasi: 0.8162
  - Precision: 0.8206
  - Recall: 0.8162
  - F1 Score: 0.8137

| Kelas | TP  | FN | FP | TN  |
| ----- | --- | -- | -- | --- |
| 0     | 6   | 16 | 11 | 453 |
| 1     | 39  | 15 | 18 | 414 |
| 2     | 57  | 21 | 18 | 390 |
| 3     | 66  | 20 | 26 | 375 |
| 4     | 223 | 18 | 16 | 330 |

---

#### **Metrik Evaluasi yang Digunakan**
- Accuracy: Persentase prediksi yang benar terhadap total prediksi.

- Precision: Kemampuan model untuk menghindari false positive.

- Recall: Kemampuan model untuk mendeteksi semua kasus positif.

- F1 Score: Harmonik rata-rata Precision dan Recall (digunakan saat data tidak seimbang).

---

### **Penjelasan Metrik Evaluasi**

| Metrik        | Formula                                         | Penjelasan                                                                                |
| ------------- | ----------------------------------------------- | ----------------------------------------------------------------------------------------- |
| **Accuracy**  | (TP + TN) / (TP + TN + FP + FN)                 | Persentase total prediksi yang benar. Cocok saat kelas seimbang.                          |
| **Precision** | TP / (TP + FP)                                  | Seberapa tepat model saat memprediksi suatu kelas positif. Menghindari False Positive.    |
| **Recall**    | TP / (TP + FN)                                  | Seberapa baik model mendeteksi semua instance positif. Penting saat False Negative mahal. |
| **F1 Score**  | 2 × (Precision × Recall) / (Precision + Recall) | Kombinasi dari precision dan recall. Cocok saat terjadi ketidakseimbangan antar kelas.    |

---


#### **Hasil Proyek Berdasarkan Metrik Akurasi**
Model dengan performa terbaik adalah:

- Random Forest dan XGBoost, keduanya meraih akurasi 0.9207, precision dan recall yang tinggi (>0.91).

- Tetapi yang paling diunggulkan yaitu XGBoost unggul sedikit di precision (0.9225) dan F1-Score (0.9190) sementara Random Forest presicion (0.9199) dan F1-Score(0.9189).

- Model ANN menghasilkan akurasi 0.8162. Meskipun cukup baik, ia memiliki sedikit penurunan pada recall (sensitivitas) dibanding Random Forest/XGBoost.

- Model Logistic Regression menunjukkan performa yang paling rendah di semua metrik, dengan akurasi hanya 0.7432, menunjukkan model ini tidak mampu menangani kompleksitas data multiklas dengan baik meskipun sudah menerapkan hyperparameter turning pada model ini.

#### **Hasil Proyek Berdasarkan Evaluasi (TP, FP, FN, TN)**
Untuk memperkuat interpretasi dari metrik evaluasi nilai True Positive (TP), False Positive (FP), False Negative (FN), dan True Negative (TN) untuk masing-masing model berdasarkan pendekatan one-vs-rest per kelas GradeClass (0–4):

1. Random Forest

- TP tertinggi ada pada kelas 4 (233) dan kelas 2–3 (74).

- Kelas 0 memiliki FN = 9 dan FP = 2 → menandakan masih ada prediksi salah pada siswa berkinerja sangat baik.

- Total kesalahan minim: hanya beberapa kesalahan antar kelas tetangga (misal kelas 3 salah diprediksi sebagai kelas 4).

- TN tertinggi menunjukkan model mampu mengenali siswa bukan dari kelas target dengan sangat baik.

2. XGBoost

- TP sangat merata: kelas 2 (75), kelas 3 (73), kelas 4 (232).

- FP lebih rendah dibanding Random Forest pada beberapa kelas, mendukung nilai Precision tertinggi (0.9225).

- FN juga rendah, khususnya di kelas 1–2 → recall kuat di area performa sedang.

- Stabil secara prediksi per kelas, cocok untuk aplikasi di dunia nyata.

3. Logistic Regression

- TP relatif rendah (contoh kelas 1 hanya 21), FN dan FP cukup tinggi di semua kelas.

- TN cukup besar tapi tidak menutupi kelemahan model dalam membedakan antar kelas.

- Ini mendukung akurasi rendah (0.7432) dan menunjukkan bahwa model ini kurang efektif dalam menangani kompleksitas interaksi antar fitur siswa.

4. Artificial Neural Network (ANN)

- TP cukup tinggi di kelas tengah (2: 57, 3: 66), namun kelas 0–1 memiliki FN dan FP yang lumayan besar.

- FP dan FN lebih tinggi dari XGBoost dan RF, menunjukkan model masih bisa ditingkatkan melalui tuning atau arsitektur lebih kompleks.

- Cocok sebagai baseline untuk pendekatan deep learning, tetapi belum sebaik model tree-based untuk dataset ini.

---

#### **Justifikasi Pemilihan Model Berdasarkan Metrik**

- XGBoost	Precision dan F1 tertinggi → tepat dan stabil dalam klasifikasi setiap GradeClass, minim false positive/negative.

- Random Forest	Akurasi dan Recall sangat tinggi → cocok untuk deteksi siswa berisiko secara menyeluruh.

- ANN	Performa baik, tapi belum setara dengan model tree-based. Cocok untuk pendekatan deep learning yang bisa ditingkatkan.

- Logistic Regression	Performa rendah, kurang cocok untuk menangani kompleksitas dan interaksi antar faktor dalam data pendidikan.

---

#### **Kesesuaian Metrik Evaluasi dengan Konteks**

Karena tujuan utama proyek adalah mendeteksi secara akurat siswa yang akan berada di level performa akademik tertentu, maka penggunaan metrik berikut sangat relevan dan tepat dengan beberapa alasan:

- Accuracy: Memberikan gambaran umum seberapa sering prediksi model tepat. Cocok digunakan karena data relatif seimbang antar kelas.

- Precision	Penting untuk mengetahui apakah prediksi kategori tertentu (misalnya: “siswa sangat berprestasi” atau “berisiko rendah”) benar-benar akurat. Bermanfaat agar tidak salah memetakan siswa ke level tinggi tanpa justifikasi yang benar.

- Recall Penting untuk menangkap sebanyak mungkin siswa dalam kategori kritis (misal: siswa dengan potensi rendah). Recall tinggi berarti intervensi dini bisa dilakukan tanpa banyak siswa terlewat.

- F1-Score	Berguna untuk menyeimbangkan Precision dan Recall, terutama saat kita peduli pada kedua aspek, yaitu akurasi deteksi dan minim kesalahan dalam identifikasi.

---

#### **Kesimpulan Akhir**

Berdasarkan evaluasi metrik dan confusion matrix:

- XGBoost dipilih sebagai model terbaik karena memiliki kombinasi precision dan f1-score paling stabil dan sangat baik dalam mengklasifikasikan data multiklas tanpa overfitting.

- Model ini sangat cocok untuk kasus fraud detection multiklas yang membutuhkan akurasi tinggi dan minim kesalahan klasifikasi.

Dengan mempertimbangkan performa dan kebutuhan sumber daya, XGBoost dapat direkomendasikan sebagai model terbaik untuk mendukung strategi prediksi dan intervensi pendidikan yang akurat, stabil, dan bisa diandalkan.

**---Ini adalah bagian akhir laporan---**
