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




## Data Preparation


## Modeling



## Evaluation


# Kesimpulan


