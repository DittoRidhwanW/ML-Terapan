# Laporan Proyek Machine Learning - Ditto Ridhwan Wibowo

## Domain Proyek

Indonesia merupakan negara kepulauan yang kaya akan keindahan alam dan keanekaragaman budaya, menjadikannya salah satu destinasi wisata utama di Asia Tenggara. Namun, meskipun potensinya besar, promosi dan rekomendasi destinasi wisata di Indonesia masih belum optimal. Banyak wisatawan, baik lokal maupun mancanegara, kesulitan menemukan destinasi wisata yang sesuai dengan preferensi mereka.

Permasalahan ini dapat diatasi dengan penerapan sistem rekomendasi destinasi wisata berbasis machine learning. Sistem ini akan membantu pengguna menemukan destinasi wisata yang relevan berdasarkan preferensi pribadi maupun pengalaman pengguna lain.

Menurut Ricci et al., sistem rekomendasi mampu memberikan saran yang dipersonalisasi dengan memanfaatkan informasi historis maupun konten (content) dari item yang tersedia. Dalam konteks ini, pendekatan seperti Content-based Filtering dan Collaborative Filtering sangat sesuai untuk mengembangkan sistem rekomendasi destinasi wisata [1].

Lebih lanjut, sistem rekomendasi modern juga telah menunjukkan efektivitas tinggi dalam konteks pariwisata digital. Sebagaimana dinyatakan oleh Isinkaye et al. (2020), pendekatan berbasis machine learning dan data historis sangat membantu dalam meningkatkan relevansi rekomendasi destinasi wisata dan meningkatkan pengalaman pengguna [2]. Hal ini juga didukung oleh penelitian terbaru oleh Narducci et al. (2020) yang menunjukkan bahwa Content-based Filtering sangat efektif ketika pengguna memiliki preferensi eksplisit yang dapat diidentifikasi dari interaksi atau deskripsi destinasi [3].
    
### Referensi
[1] Ricci, F., Rokach, L., & Shapira, B. (2011). Introduction to Recommender Systems Handbook. Springer.

[2] Isinkaye, F. O., Folajimi, Y. O., & Ojokoh, B. A. (2020). Recommendation systems: Principles, methods and evaluation. Egyptian Informatics Journal, 21(2), 119-135. https://doi.org/10.1016/j.eij.2019.07.001

[3] Narducci, F., Musto, C., de Gemmis, M., Lops, P., & Semeraro, G. (2020). Content-based recommender systems: State of the art and trends. In Recommender Systems Handbook (pp. 227–263). Springer. https://doi.org/10.1007/978-3-030-38744-9_7

## Business Understanding

Pariwisata merupakan sektor ekonomi penting bagi Indonesia yang menyumbang pendapatan negara, membuka lapangan kerja, dan mempromosikan budaya lokal. Namun, masih banyak tantangan dalam mengoptimalkan potensi sektor ini, terutama dalam hal pemanfaatan teknologi informasi untuk mendukung pengalaman wisatawan.

Di era digital, banyak wisatawan mengandalkan platform online untuk mencari informasi mengenai destinasi wisata. Sayangnya, informasi yang tersedia seringkali tidak terpersonalisasi sehingga wisatawan kesulitan menemukan destinasi yang sesuai dengan minat dan kebutuhan mereka. Oleh karena itu, perlu dikembangkan sistem rekomendasi destinasi wisata berbasis machine learning yang dapat membantu menyajikan saran destinasi yang relevan dan disesuaikan dengan preferensi pengguna.

Proyek ini bertujuan untuk mengembangkan sistem rekomendasi destinasi wisata menggunakan pendekatan Content-based Filtering dan Collaborative Filtering. Pendekatan ini tidak hanya memberikan rekomendasi berdasarkan deskripsi konten destinasi, tetapi juga mempertimbangkan preferensi pengguna lain yang memiliki pola minat serupa. Dengan demikian, sistem dapat memberikan rekomendasi yang lebih akurat dan bermanfaat.

Sistem ini dapat digunakan oleh platform pariwisata, aplikasi perjalanan, maupun lembaga pemerintah untuk meningkatkan pengalaman wisatawan, memperluas eksposur destinasi wisata lokal, dan mendorong pertumbuhan ekonomi daerah.


### Problem Statements

1. Bagaimana cara merekomendasikan destinasi wisata di Indonesia berdasarkan preferensi pengguna?
2. Bagaimana sistem dapat memberikan rekomendasi yang relevan berdasarkan kesamaan dengan pengguna lain?

### Goals

1. Mengembangkan sistem rekomendasi berbasis konten yang memberikan saran destinasi berdasarkan preferensi pengguna.
2. Mengembangkan sistem rekomendasi berbasis kolaboratif untuk menemukan destinasi populer di kalangan pengguna dengan minat serupa.

### Solution statements
1. Solution 1: Content-based Filtering
   - Menggunakan atribut seperti kota, kategori wisata, deskripsi dan nama tempat untuk menentukan kesamaan antar destinasi.
2. Solution 2: Collaborative Filtering
   - Menggunakan interaksi pengguna-destinasi (rating atau kunjungan) untuk membangun sistem rekomendasi berdasarkan preferensi pengguna lain yang serupa.

## Data Understanding
Pada dataset tourism ini terdapat 3 file yaitu tourism_data, user_rating_data dan place_ratings_data yang diambil dari Kaggle dengan link sebagai berikut
Link Dataset : https://www.kaggle.com/datasets/aprabowo/indonesia-tourism-destination
1. tourism_with_id

   Dataset ini memiliki 437 baris dengan 13 kolom dimana terdapat missing value pada kolom Time_Minutes sebanyak 232 baris dan kolom Unnamed 11 sebanyak 437. Untuk itu hal yang akan dilakukan adala menghapus kolom Time_Minutes, Unnamed 11 dan Unnamed 12 karena kolom-kolom tersebut tidak akan digunakan. Berikut detail atributnya:
   * Place_Id = Id dari tempat wisata
   * Place_name = nama tempat wisata
   * Description = Deskripsi tempat wisata
   * Category = kategori tempat wisata
   * City = kota dari tempat wisata
   * Price = harga tempat wisata
   * Rating = rating tempat wisata
   * coordinate = titik koordinat tempat wisata
   * Lat = garis lintang tempat wisata
   * Long = garis bujur tempat wisata

2. user
   
   Dataset ini memiliki 300 baris dengan 3 kolom dimana dataset ini tidak ada missing value. Berikut detail atributnya:
   * User_Id = id dari user
   * Location = lokasi tempat tinggal user
   * Age = usia user
    
3. tourism_rating

    Pada dataset place_ratings_data terdapat 10000 baris dengan 3 kolom, dalam dataset tersebut juga kondisinya sudah bersih tidak terdapat missing value. Berikut detail atributnya:
   * User_Id = id dari user
   * Place_Id = id dari tempat wisata
   * Place_Ratings = rating dari tempat wisata
  
### Distribusi
![download](https://github.com/user-attachments/assets/e61cc4d4-5830-4122-81b6-bf31984fdde6)

Insight: Berdasarkan distribusi rating tempat, rata-rata rating yang diberikan oleh user tidak jauh dari 3 atau 4 sebanyak 2000+. Ini mengindikasikan bahwa wisata di Indonesia sangat direkomendasikan untuk dikunjungi oleh wisatawan.

![download](https://github.com/user-attachments/assets/b9bfe469-159a-4323-83ca-c5493adf8d25)

Insight: Berdasarkan hasil distribusi kota yang paling banyak dikunjungi adalah Kota Yogyakarta, diikuti dengan Kota Bandung. Hal ini dapat dilihat dari banyaknya tempat wisata dari kedua kota tersebut, sehingga banyak wisatawan yang datang kesana.

![download](https://github.com/user-attachments/assets/6639f75a-9514-4a41-9303-ee7e7c9e2056)

Insight: Dari hasil distribusi usia, wisatawan yang sering berkunjung terbanyak ada pada kisaran usia 30 tahun sebanyak 35+ wisatawan. Sedangkan untuk rentang usia 17+ dan 30+ juga tidak terlalu banyak dan tidak terlalu sedikit juga yaitu berada dibawah 30 wisatawan.


## Data Preparation
Tahap yang dilakukan adalah menghapus kolom yang memiliki missing value dan menghapus kolom yang tidak digunakan, dimana terdapat missing value pada kolom Time_Minutes sebanyak 232 baris dan kolom Unnamed 11 sebanyak 437. Untuk itu hal yang akan dilakukan adala menghapus kolom Time_Minutes, Unnamed 11 dan Unnamed 12 karena kolom-kolom tersebut tidak akan digunakan.

![image](https://github.com/user-attachments/assets/1bbd04ae-2919-4c7d-91d8-0e06a98b3e17)

Selain itu, dilakukan juga penggabungan dua fitur, yaitu Category dan City, menjadi fitur baru bernama combined_features. Penggabungan ini bertujuan untuk mempermudah proses ekstraksi informasi kontekstual dalam metode Content-Based Filtering.

Selanjutnya, dilakukan proses TF-IDF Vectorization terhadap fitur combined_features untuk mengubah data teks menjadi representasi numerik yang dapat diproses oleh algoritma machine learning. Meskipun tahap ini berkaitan erat dengan pemodelan, secara teknis TF-IDF merupakan bagian dari proses persiapan data karena mengubah bentuk representasi data sebelum masuk ke model.

Terakhir, untuk kebutuhan model Collaborative Filtering, data dibagi menjadi data latih dan data uji menggunakan metode train-test split. Langkah ini penting dilakukan agar performa model dapat divalidasi dan diukur secara objektif.


## Modeling
1. Content Based Filtering
   
![image](https://github.com/user-attachments/assets/1e80bcf6-1a70-4a74-ac0f-f6f120f0d9a9)

Sistem rekomendasi berbasis konten ini dirancang untuk menyarankan destinasi wisata yang mirip berdasarkan informasi deskriptif dari setiap tempat. Setelah fitur Category dan City digabungkan menjadi combined_features, proses transformasi dilakukan menggunakan TF-IDF Vectorization.

Selanjutnya, dihitung cosine similarity antar tempat wisata menggunakan representasi TF-IDF tersebut. Matriks similarity berukuran (437, 437) ini menjadi dasar pencarian tempat yang paling mirip. Contoh penerapan dilakukan dengan input 'Candi Prambanan', dan sistem merekomendasikan 10 tempat dengan tingkat kemiripan tertinggi.

2. Collaborative Filtering
   
   ![image](https://github.com/user-attachments/assets/351a1a7b-57a7-45d3-bebc-262d34bc30b9)

   Pendekatan Collaborative Filtering digunakan untuk memprediksi preferensi pengguna berdasarkan interaksi historis antar pengguna dan tempat wisata. Dua algoritma yang digunakan adalah SVD (Singular Value Decomposition) dan KNNBasic (item-based collaborative filtering).

📈 Evaluasi Model RMSE (Root Mean Squared Error) digunakan sebagai metrik evaluasi untuk mengukur seberapa baik model dalam memprediksi rating/penilaian yang diberikan pengguna terhadap destinasi wisata.

Hasil evaluasi:

SVD Model (Singular Value Decomposition) menghasilkan RMSE sebesar 1.4119.

KNN Item-Based Model (berbasis kemiripan antar item) menghasilkan RMSE yang lebih baik yaitu 1.3954, yang berarti model ini sedikit lebih akurat dalam memprediksi preferensi pengguna.


## Evaluation
1. Content Based Filtering
   
![image](https://github.com/user-attachments/assets/d5d254c4-bef7-41dd-ab25-b22d183e3af0)

Sistem rekomendasi ini menggunakan pendekatan Content-Based Filtering, yaitu merekomendasikan destinasi wisata yang memiliki kemiripan konten dengan destinasi yang disukai pengguna. Kemiripan dihitung berdasarkan fitur tekstual seperti nama tempat, kategori (Category), kota (City), dan atribut lainnya yang telah direpresentasikan ke dalam matriks TF-IDF.

🔍 Analisis Hasil:

Skor Similarity = 1.0 Destinasi seperti Pulau Tidung, Pulau Bidadari, Pantai Ancol, dll., memiliki kesamaan sempurna (skor 1.0) dengan input yang digunakan untuk evaluasi. Ini berarti fitur-fitur tekstual mereka (nama, kategori Bahari, kota Jakarta, dll.) sangat identik atau sangat mirip. Artinya, sistem berhasil mengelompokkan destinasi bahari di Jakarta secara tepat.

Skor Similarity = 0.63375 Destinasi seperti Pantai Goa Cemara atau Pantai Kukup juga termasuk dalam kategori Bahari, tetapi berasal dari kota yang berbeda (Yogyakarta). Ini menyebabkan skor kemiripan yang lebih rendah, namun tetap dianggap relevan. Sistem mampu mengenali bahwa meskipun lokasi berbeda, destinasi ini masih dalam kategori wisata air/bahari.


2. Collaborative Filtering
   
   ![image](https://github.com/user-attachments/assets/9708de81-7e22-46cb-b7cb-9ed04a4186ef)

   Sistem ini memprediksi ketertarikan pengguna terhadap tempat wisata berdasarkan interaksi historis pengguna lainnya, tanpa melihat konten destinasi secara langsung. Dua pendekatan utama yang digunakan:

* SVD (Singular Value Decomposition) – memetakan user dan item ke dalam vektor laten untuk memperkirakan rating.

* KNN Item-Based – menggunakan kemiripan antar item berdasarkan rating pengguna untuk memberikan rekomendasi.

📏 Evaluasi Performa Model Dengan menggunakan SVD didapatkan hasil RMSE 1.4119 dan MAE 1.2143, sedangkan dengan menggunakan KNN Item-Based didapatkan hasil RMSE 1.3954 dan MAE 1.2016

* RMSE (Root Mean Squared Error): Mengukur rata-rata kesalahan kuadrat antara rating prediksi dan rating aktual.

* MAE (Mean Absolute Error): Mengukur rata-rata kesalahan absolut prediksi.

📌 KNN Item-Based sedikit lebih baik dari SVD berdasarkan kedua metrik tersebut, meskipun selisihnya kecil.


# Kesimpulan
Proyek ini berhasil mengembangkan sistem rekomendasi destinasi wisata di Indonesia dengan dua pendekatan utama: Content-Based Filtering dan Collaborative Filtering. Sistem ini bertujuan membantu wisatawan menemukan tempat wisata yang sesuai dengan preferensi pribadi mereka, serta meningkatkan efisiensi promosi destinasi wisata lokal.

Berdasarkan hasil eksperimen:

1. Content-Based Filtering mampu memberikan rekomendasi yang relevan berdasarkan kemiripan atribut seperti nama tempat, deskripsi, kategori, dan kota. Sistem ini sangat efektif untuk pengguna dengan preferensi eksplisit terhadap jenis wisata tertentu. Misalnya, ketika pengguna tertarik pada destinasi bahari, sistem mampu merekomendasikan tempat lain dengan karakteristik serupa, meskipun berada di kota yang berbeda.

2. Collaborative Filtering, khususnya pendekatan KNN Item-Based, menunjukkan performa evaluasi yang lebih baik dibandingkan metode SVD, dengan nilai RMSE 1.3954 dan MAE 1.2016. Ini menunjukkan bahwa pendekatan kolaboratif dapat memprediksi preferensi pengguna dengan cukup akurat berdasarkan perilaku pengguna lain yang memiliki kesamaan pola kunjungan atau rating.

Secara keseluruhan, sistem rekomendasi yang dibangun dapat menjadi solusi inovatif dalam mendukung pengembangan pariwisata digital di Indonesia. Sistem ini dapat diintegrasikan ke dalam platform pariwisata atau aplikasi perjalanan untuk meningkatkan pengalaman pengguna, memperluas jangkauan destinasi lokal, dan berkontribusi terhadap pertumbuhan ekonomi daerah melalui sektor pariwisata.

