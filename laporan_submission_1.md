# Laporan Proyek Machine Learning - Ditto Ridhwan Wibowo

## Domain Proyek

    Kesehatan mental merupakan aspek penting dalam menunjang produktivitas dan kualitas hidup individu, terutama di lingkungan kerja. Gangguan mental seperti depresi, stres, dan kecemasan telah menjadi penyebab utama berkurangnya produktivitas dan meningkatnya angka absensi di tempat kerja. Menurut WHO, gangguan kesehatan mental menyebabkan kerugian ekonomi global sebesar $1 triliun setiap tahunnya akibat kehilangan produktivitas [1].
    Seiring berkembangnya teknologi, pendekatan data-driven seperti machine learning menjadi solusi potensial dalam mendeteksi kesehatan mental secara dini. Model klasifikasi berbasis data survei dapat membantu organisasi dalam mengidentifikasi individu yang berisiko mengalami gangguan mental, sehingga memungkinkan intervensi lebih cepat dan tepat [2].
    Studi terdahulu menunjukkan bahwa faktor-faktor seperti jenis kelamin, usia, riwayat keluarga, dukungan perusahaan, dan stigma terhadap isu kesehatan mental sangat memengaruhi keputusan seseorang dalam mencari bantuan [3], [4]. Selain itu, persepsi terhadap kerahasiaan data dan kenyamanan saat membicarakan isu ini juga merupakan faktor penting [5].
    Dataset  yang dianalisis dalam proyek ini mencerminkan berbagai kondisi sosial dan struktural yang memengaruhi kesehatan mental. Melalui pendekatan klasifikasi, diharapkan dapat ditemukan pola-pola prediktif yang mendukung pengambilan keputusan berbasis data dalam manajemen sumber daya manusia.

### Referensi
[1] V. Patel, A. J. Flisher, S. Hetrick, and P. McGorry, “Mental health of young people: a global public-health challenge,” The Lancet, vol. 369, no. 9569, pp. 1302–1313, 2007.
[2] C. R. Clough, M. O. Casey, and L. P. Zhan, “Predicting mental health from social media data using machine learning: A review,” ACM Computing Surveys (CSUR), vol. 54, no. 4, pp. 1–36, 2021.
[3] A. Gulliver, K. M. Griffiths, and H. Christensen, “Perceived barriers and facilitators to mental health help-seeking in young people: a systematic review,” BMC Psychiatry, vol. 10, no. 1, pp. 1–9, 2010.
[4] D. Rickwood, F. P. Deane, C. Wilson, and J. Ciarrochi, “Young people’s help-seeking for mental health problems,” Australian e-Journal for the Advancement of Mental Health, vol. 4, no. 3, pp. 218–251, 2005.
[5] L. Clement et al., “What is the impact of mental health-related stigma on help-seeking? A systematic review of quantitative and qualitative studies,” Psychological Medicine, vol. 45, no. 1, pp. 11–27, 2015.

**Rubrik/Kriteria Tambahan (Opsional)**:
- Jelaskan mengapa dan bagaimana masalah tersebut harus diselesaikan
- Menyertakan hasil riset terkait atau referensi. Referensi yang diberikan harus berasal dari sumber yang kredibel dan author yang jelas.
- Format Referensi dapat mengacu pada penulisan sitasi [IEEE](https://journals.ieeeauthorcenter.ieee.org/wp-content/uploads/sites/7/IEEE_Reference_Guide.pdf), [APA](https://www.mendeley.com/guides/apa-citation-guide/) atau secara umum seperti [di sini](https://penerbitdeepublish.com/menulis-buku-membuat-sitasi-dengan-mudah/)
- Sumber yang bisa digunakan [Scholar](https://scholar.google.com/)

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

