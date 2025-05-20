# Laporan Proyek Machine Learning - Ditto Ridhwan Wibowo

## Domain Proyek

Kesehatan mental telah menjadi topik yang semakin penting dalam berbagai aspek kehidupan, terutama setelah pandemi COVID-19 yang berdampak besar terhadap kesejahteraan psikologis masyarakat global. Gangguan seperti kecemasan, depresi, dan stres kini tidak hanya dialami oleh pekerja formal, tetapi juga oleh pelajar, pelaku usaha, ibu rumah tangga, hingga kalangan profesional. Tekanan sosial, ketidakpastian ekonomi, dan kurangnya akses terhadap dukungan psikologis menjadi faktor utama yang memperparah kondisi ini [1].
    
Menurut studi global oleh Santomauro et al. (2021), terdapat peningkatan signifikan dalam prevalensi gangguan kecemasan (26%) dan depresi mayor (28%) pada tahun pertama pandemi [2]. Hal ini menunjukkan kebutuhan mendesak akan pendekatan yang dapat mendeteksi potensi gangguan mental secara dini dan akurat.
    
Pendekatan berbasis machine learning menawarkan potensi besar untuk menyaring dan menganalisis data kesehatan mental secara otomatis. Model klasifikasi seperti data survei memungkinkan prediksi status kesehatan mental individu berdasarkan faktor-faktor seperti demografi, pekerjaan, dukungan sosial, dan persepsi pribadi terhadap kesehatan mental [3]. Ini sangat berguna untuk memperluas cakupan intervensi kepada populasi yang lebih luas, tidak hanya terbatas pada lingkungan kerja.

Beberapa studi menunjukkan bahwa faktor-faktor seperti jenis kelamin, usia, riwayat keluarga, dan kenyamanan berbicara mengenai kesehatan mental berperan penting dalam perilaku pencarian bantuan psikologis [4], [5]. Melalui pemodelan machine learning, kita tidak hanya dapat melakukan klasifikasi, tetapi juga mengidentifikasi fitur-fitur yang paling relevan untuk membantu dalam desain kebijakan dan intervensi kesehatan mental.
    
Dataset  yang dianalisis dalam proyek ini mencerminkan berbagai kondisi sosial dan struktural yang memengaruhi kesehatan mental. Melalui pendekatan klasifikasi, diharapkan dapat ditemukan pola-pola prediktif yang mendukung pengambilan keputusan dalam kebutuhan untuk cek kesehatan mental.
    
### Referensi
[1] S. Vindegaard and M. Benros, “COVID-19 pandemic and mental health consequences: Systematic review of the current evidence,” Brain, Behavior, and Immunity, vol. 89, pp. 531–542, Jul. 2020.

[2] D. F. Santomauro et al., “Global prevalence and burden of depressive and anxiety disorders in 204 countries and territories in 2020 due to the COVID-19 pandemic,” The Lancet, vol. 398, no. 10312, pp. 1700–1712, Nov. 2021.

[3] A. Islam, A. M. Iftekhar, T. Rahman, and S. Jahan, “Mental health prediction using machine learning: A survey,” ACM Computing Surveys (CSUR), vol. 55, no. 2, pp. 1–36, 2022.

[4] N. M. van der Velden et al., “Anxiety and depression symptoms, and lack of emotional support among the general population before and during the COVID-19 pandemic. A prospective national study on prevalence and risk factors,” Journal of Affective Disorders, vol. 277, pp. 540–548, Jan. 2021.

[5] S. E. McGinty, E. Presskreischer, H. Han, and C. Niederdeppe, “Psychological distress and COVID-19–related stressors reported in a longitudinal cohort of US adults in 2020,” JAMA, vol. 324, no. 24, pp. 2555–2557, Dec. 2020.

## Business Understanding

Pada bagian ini, kamu perlu menjelaskan proses klarifikasi masalah.

Bagian laporan ini mencakup:

### Problem Statements

Menjelaskan pernyataan masalah latar belakang:
- Pernyataan Masalah 1
- Pernyataan Masalah 2
- Pernyataan Masalah n

### Goals

Menjelaskan tujuan dari pernyataan masalah:
- Jawaban pernyataan masalah 1
- Jawaban pernyataan masalah 2
- Jawaban pernyataan masalah n

Semua poin di atas harus diuraikan dengan jelas. Anda bebas menuliskan berapa pernyataan masalah dan juga goals yang diinginkan.

**Rubrik/Kriteria Tambahan (Opsional)**:
- Menambahkan bagian “Solution Statement” yang menguraikan cara untuk meraih goals. Bagian ini dibuat dengan ketentuan sebagai berikut: 

    ### Solution statements
    - Mengajukan 2 atau lebih solution statement. Misalnya, menggunakan dua atau lebih algoritma untuk mencapai solusi yang diinginkan atau melakukan improvement pada baseline model dengan hyperparameter tuning.
    - Solusi yang diberikan harus dapat terukur dengan metrik evaluasi.

## Data Understanding
Paragraf awal bagian ini menjelaskan informasi mengenai data yang Anda gunakan dalam proyek. Sertakan juga sumber atau tautan untuk mengunduh dataset. Contoh: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Restaurant+%26+consumer+data).

Selanjutnya uraikanlah seluruh variabel atau fitur pada data. Sebagai contoh:  

### Variabel-variabel pada Restaurant UCI dataset adalah sebagai berikut:
- accepts : merupakan jenis pembayaran yang diterima pada restoran tertentu.
- cuisine : merupakan jenis masakan yang disajikan pada restoran.
- dst

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

