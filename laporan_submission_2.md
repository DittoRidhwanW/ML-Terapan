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
   * Time Minutes = Total waktu yang dihabiskan di tempat wisata
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
1. Pra-pemrosesan Umum
Langkah awal yang dilakukan adalah membersihkan data dari kolom-kolom yang tidak relevan atau memiliki nilai kosong (missing value) dalam jumlah besar.

- Kolom Time_Minutes memiliki 232 nilai kosong.

- Kolom Unnamed: 11 memiliki 437 nilai kosong.

- Kolom Unnamed: 12 tidak memiliki informasi yang berguna.

Ketiga kolom tersebut dihapus karena tidak digunakan dalam proses analisis lebih lanjut.

![image](https://github.com/user-attachments/assets/1bbd04ae-2919-4c7d-91d8-0e06a98b3e17)

2. Content-Based Filtering
    Pendekatan Content-Based Filtering memerlukan representasi teks yang bermakna dari atribut destinasi. Tahapan yang dilakukan adalah sebagai berikut:

- Penyalinan Dataframe:
    Data asli disalin ke dalam variabel baru data_content = tourism_data.copy() agar proses transformasi tidak mengubah data asli yang mungkin digunakan untuk pendekatan lain.

- Penggabungan Fitur:
    Dua kolom penting yaitu Category dan City digabungkan menjadi fitur baru bernama combined_features.
Tujuannya adalah untuk menyatukan informasi kontekstual dari kategori destinasi dan lokasinya dalam satu kolom agar lebih efektif saat dilakukan ekstraksi fitur berbasis teks.

- TF-IDF Vectorization:
    Fitur combined_features kemudian diubah menjadi bentuk numerik menggunakan TF-IDF Vectorizer.
Meskipun berhubungan erat dengan tahap pemodelan, proses ini tergolong ke dalam persiapan data karena menghasilkan representasi numerik sebelum model digunakan.

3. Collaborative Filtering
    Untuk Collaborative Filtering, pendekatan yang digunakan melibatkan interaksi antara pengguna dan item (destinasi). Proses persiapan data dilakukan sebagai berikut:

- Pemuatan dan Pemformatan Data:
    Data interaksi pengguna disiapkan menggunakan library Surprise. Langkah pertama adalah mendefinisikan format data menggunakan objek Reader, kemudian memuat data ke dalam struktur Surprise dengan Dataset.load_from_df.

- Pembagian Data:
    Setelah diformat, data dibagi menjadi data latih dan data uji menggunakan metode train-test split.
Tahapan ini penting untuk melakukan validasi performa model Collaborative Filtering secara objektif.

## Modeling
1. Content Based Filtering
   
![image](https://github.com/user-attachments/assets/1e80bcf6-1a70-4a74-ac0f-f6f120f0d9a9)

Sistem rekomendasi berbasis konten dirancang untuk menyarankan destinasi wisata yang mirip berdasarkan informasi deskriptif dari setiap tempat. Untuk membangun sistem ini, dua fitur penting yaitu Category dan City digabungkan menjadi fitur baru bernama combined_features. Fitur ini menyatukan konteks kategori dan lokasi destinasi sehingga dapat memberikan gambaran umum karakteristik setiap tempat.

Untuk mengukur kemiripan antar destinasi wisata, digunakan metode Cosine Similarity. Metode ini bekerja dengan mengukur sudut antara dua vektor fitur dalam ruang multidimensi. Jika dua vektor memiliki arah yang hampir sama (sudut kecil), maka nilainya mendekati 1, menandakan bahwa dua item tersebut sangat mirip. Sebaliknya, jika sudut antar vektor besar, nilai Cosine Similarity mendekati 0, yang berarti kedua item tidak mirip.

Hasil perhitungan Cosine Similarity menghasilkan matriks kemiripan berukuran (437, 437) yang menyimpan skor kemiripan antar semua destinasi. Matriks ini menjadi dasar sistem dalam memberikan rekomendasi. Misalnya, jika pengguna memilih "Candi Prambanan" sebagai referensi, maka sistem akan menampilkan 10 destinasi wisata lain yang paling mirip berdasarkan nilai kemiripan tertinggi.

2. Collaborative Filtering
   
   ![image](https://github.com/user-attachments/assets/8f5ce152-5ecf-4259-bdab-d8955afbbf85)
![image](https://github.com/user-attachments/assets/003927ee-258a-40be-b4b2-d39b24d438a0)



   Pendekatan Collaborative Filtering digunakan untuk memprediksi preferensi pengguna berdasarkan riwayat interaksi antara pengguna dan tempat wisata. Tidak seperti pendekatan berbasis konten, metode ini memanfaatkan pola kesamaan preferensi antar pengguna atau antar item. Dua algoritma yang digunakan adalah SVD (Singular Value Decomposition) dan KNNBasic (item-based).

📈 Evaluasi Model RMSE (Root Mean Squared Error) digunakan sebagai metrik evaluasi untuk mengukur seberapa baik model dalam memprediksi rating/penilaian yang diberikan pengguna terhadap destinasi wisata.

Hasil evaluasi:

SVD Model (Singular Value Decomposition) menghasilkan RMSE sebesar 1.4119.

KNN Item-Based Model (berbasis kemiripan antar item) menghasilkan RMSE yang lebih baik yaitu 1.3954, yang berarti model ini sedikit lebih akurat dalam memprediksi preferensi pengguna.

Berdasarkan rekomendasi pada User_1 didapatkan hasil:
A. Collaborative Filtering (SVD)

Karakteristik:

- Dominasi tempat dengan nilai budaya dan alam (Cagar Alam, Budaya).

- Sebaran kota cukup beragam (Yogyakarta, Bandung, Surabaya).

- Rentang harga bervariasi (gratis sampai 100.000).

B. Collaborative Filtering (KNNBasic - Item-Based)

Karakteristik:

- Lebih fokus ke destinasi hiburan keluarga dan landmark kota.

- Harga umumnya rendah atau gratis.

- Penekanan lebih kuat pada kota besar populer (Jakarta, Yogyakarta, Bandung).

## Evaluation
1. Content Based Filtering
   
![image](https://github.com/user-attachments/assets/b3a58830-6d7e-40f0-a22c-5de68d355212)


Sistem rekomendasi ini menggunakan pendekatan Content-Based Filtering, yaitu merekomendasikan destinasi wisata yang memiliki kemiripan konten dengan destinasi yang disukai pengguna. 

🔍 Analisis Hasil:
1. Rekomendasi yang dihasilkan untuk Taman Impian Jaya Ancol Antara Lain:

- ['Taman Mini Indonesia Indah (TMII)', 'Atlantis Water Adventure', 'Taman Impian Jaya Ancol', 'Ocean Ecopark', 'Kidzania']

2. Evaluasi dengan metrik:

- Precision@5 = 0.80
Ini berarti dari 5 tempat yang direkomendasikan, 4 tempat benar-benar sesuai dengan ground truth (karena satu adalah tempat input sendiri).
Precision = jumlah rekomendasi benar / total rekomendasi = 4/5 = 0.8

- Recall@5 = 0.01
Recall sangat rendah karena ground truth tempat yang relevan sangat banyak (selain 'Taman Impian Jaya Ancol'), tapi rekomendasi hanya 5 tempat, jadi baru tertangkap sedikit sekali dari semua tempat relevan.


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

