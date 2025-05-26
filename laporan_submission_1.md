![image](https://github.com/user-attachments/assets/a79d2bcd-c47d-4237-8264-bb28492f8726)# Laporan Proyek Machine Learning - Ditto Ridhwan Wibowo

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

Kesehatan mental adalah aspek penting dalam kehidupan seseorang yang semakin mendapat perhatian luas, terutama sejak pandemi COVID-19. Banyak individu mengalami tekanan psikologis, namun tidak semuanya memiliki akses atau kesadaran untuk mendapatkan bantuan profesional. Oleh karena itu, pendekatan berbasis data sangat dibutuhkan untuk mengidentifikasi potensi gangguan kesehatan mental sejak dini, terutama melalui model berbasis machine learning.

Proyek ini bertujuan untuk membantu mengidentifikasi kondisi kesehatan mental seseorang berdasarkan data survei yang memuat informasi demografi, pekerjaan, akses terhadap dukungan kesehatan mental, dan persepsi pribadi mereka terhadap isu ini. Dengan pemodelan yang tepat, sistem prediktif ini dapat dimanfaatkan oleh lembaga pendidikan, perusahaan, atau institusi kesehatan untuk memberikan intervensi lebih dini dan tepat sasaran.

### Problem Statements

Menjelaskan pernyataan masalah latar belakang:
- Banyak individu dengan potensi gangguan kesehatan mental tidak terdeteksi secara dini, baik karena keterbatasan akses terhadap layanan psikologis maupun kurangnya kesadaran individu terhadap kondisi mereka sendiri.
- Belum ada pendekatan otomatis dan berbasis data yang secara efisien memanfaatkan informasi latar belakang individu untuk memprediksi kemungkinan mereka mengalami gangguan kesehatan mental.

### Goals

Menjelaskan tujuan dari pernyataan masalah:
- Mengembangkan model klasifikasi berbasis machine learning yang mampu memprediksi apakah seseorang kemungkinan besar memerlukan perawatan kesehatan mental atau tidak, berdasarkan atribut survei yang diberikan.
- Mengidentifikasi fitur-fitur penting yang memengaruhi status kesehatan mental individu.

### Solution statements
- Mengimplementasikan dan membandingkan kinerja beberapa model klasifikasi untuk menemukan model terbaik.
- Melakukan hyperparameter tuning pada model dengan performa terbaik untuk mengoptimalkan hasil klasifikasi dan meningkatkan akurasi prediksi.
- Menggunakan metode interpretabilitas seperti feature importance atau SHAP analysis untuk mengetahui fitur apa yang paling berdampak terhadap prediksi dan dapat dijadikan dasar dalam kebijakan intervensi.

## Data Understanding
Dataset yang digunakan diambil dari platform Kaggle yaitu, (https://www.kaggle.com/datasets/bhavikjikadara/mental-health-dataset) yang memiliki 17 kolom dimana 16 kolom fitur dan 1 kolom target.

### Variabel-variabel pada Mental Health dataset adalah sebagai berikut:
- Timestamp : waktu responden submit pengisian survey
- Gender : jenis kelamin
- Country : asal negara responden
- Occupation : pekerjaan responden
- self_employed : apakah responden merupakan wiraswasta / pekerja mandiri
- family_history : apakah responden memiliki riwayat keluarga dengan penyakit mental
- treatment : apakah responden sudah pernah melakukan treatment terkait kesehatan mental
- Days_indoors : berapa lama kegiatan diluar
- Growing_Stress : apakah ada peningkatan terkait stress
- Change_Habits : apakah ada perubahan kebiasaan yang dilakukan
- Mental_Health_History : apakah responden memiliki masalah kesehatan mental sebelumnya
- Mood_Swings : tingkatn perubahan mood responden
- Coping_Struggles : apakah responden dapat menangani kesulitan
- Work_Interest : apakah responden memiliki ketertarikan dalam bekerja
- Social_Weakness : apakah responden memiliki kelemahan dalam sosial
- mental_health_interview : apakah responden akan mengungkapkan masalah kesehatan mental kepada HR dalam sebuah interview kerja
- care_options : prediksi apakah responden membutuhkan penanganan kesehatan mental atau tidak

## Data Preparation
- Missing Values : Melakukan penanganan pada data yang hilang, pada proyek ini hal yang akan dilakukan untuk menangani data yang hilang adalah dengan menggunakan teknik imputasi yaitu modus, karena dataset tersebut bertipe kategorikal sehingga tidak bisa menggunakan nilai mean atau median. 
- Duplicate : Menghapus data yang memiliki duplikasi agar tidak ada bias data dan tidak mengalami overfitting pada saat evaluasi model.
- Drop Column : Menghapus kolom yang tidak digunakan
- Encoding : Melakukan transformasi data dengan mengubah nilai setiap kategori ke dalam bentuk numerik, teknik yang akan digunakan adalah label encoding karena beberapa fitur memiliki kategori lebih dari 2.
- Split data : Setelah melakukan cleaning data, disini akan membagi antara data latih dan data uji dengan perbandingan 80:20

## Modeling
Pada tahap ini, beberapa algoritma klasifikasi machine learning digunakan untuk memprediksi apakah seseorang membutuhkan penanganan kesehatan mental atau tidak berdasarkan data survei yang telah disiapkan.

1. Decision Tree
   Decision Tree bekerja dengan memetakan fitur dari data ke dalam serangkaian aturan logika yang membentuk struktur pohon keputusan. Setiap node dalam pohon memisahkan data berdasarkan nilai dari suatu fitur, dan proses ini berlanjut hingga mencapai node daun yang memberikan prediksi kelas.
   - Kelebihan

     a. Mudah diinterpretasikan dan divisualisasikan
     
     b. Bisa menangani fitur numerik dan kategorikal
     
   - Kekurangan
     
     a. Rentan terhadap overfitting jika tidak dilakukan pruning
     
2. Random Forest
   Random Forest adalah kumpulan dari banyak pohon keputusan (decision trees) yang dilatih dengan data acak dan subset fitur yang berbeda. Hasil akhir ditentukan berdasarkan voting mayoritas dari semua pohon. Pendekatan ini mengurangi varian model dan membantu menghindari overfitting.
   - Kelebihan
     
     a. Akurasi yang lebih tinggi daripada decision tree tunggal
     
     b. Lebih tahan terhadap overfitting
     
     c. Memberikan feature importance
     
   - Kekurangan
     a. Kurang interpretatif dibanding decision tree tunggal
     
     b. Sedikit lebih lama dalam pelatihan

## Hyperparameter Tuning
Melakukan tuning pada model yang memiliki akurasi terbaik menggunakan metode GridSearch yang dimana metode tersebut akan mengecek semua parameter untuk memilih best parameter. Parameter yang akan digunakan untuk memilih yang terbaik antara lain:
- 'criterion': ['gini', 'entropy'] -> parameter ini digunakan untuk menentukan fungsi yang mengukur kualitas pemisahan (split) pada setiap node.
- 'max_depth': [None, 10, 20, 30] -> parameter ini digunakan untul menentukan kedalaman maksimum pohon (berapa banyak level node dari akar ke daun) untuk mencegah adanya overfitting.
- 'min_samples_split': [2, 5, 10] -> parameter ini digunakan untuk menentukan jumlah minimum sampel yang dibutuhkan untuk membagi (split) sebuah node yang nanti dapat mencegah pembentukan node yang terlalu kecil dan kurang bermakna.
- 'min_samples_leaf': [1, 2, 4] -> parameter ini digunakan untuk menentukan jumlah minimum sampel yang harus ada di setiap node daun (leaf). Tujuannya untuk mengontrol jumlah data minimum di daun agar model lebih general.

## Interpretabilitas Model dengan SHAP
Untuk memahami pengaruh setiap fitur terhadap hasil prediksi, proyek ini menggunakan pendekatan interpretabilitas model berbasis SHAP (SHapley Additive exPlanations).

SHAP merupakan metode berbasis teori permainan (game theory) yang memberikan penjelasan kuantitatif terhadap kontribusi setiap fitur dalam prediksi model. SHAP menghitung nilai kontribusi setiap fitur dengan mempertimbangkan semua kemungkinan kombinasi fitur yang mungkin.

a. Alasan Menggunakan SHAP
 - Memberikan penjelasan yang akurat dan konsisten terhadap kontribusi fitur.
 - Menjelaskan pengaruh fitur secara global (keseluruhan dataset) dan lokal (prediksi individu).

## Evaluation
1. Akurasi : Mengukur proporsi prediksi yang benar dari keseluruhan prediksi.
2. Precision : Mengukur proporsi prediksi positif yang benar-benar positif.
3. Recall (Sensitivity) : Mengukur seberapa baik model dapat mendeteksi kasus positif.
4. F1-Score : Harmonik rata-rata dari precision dan recall. Cocok untuk data tidak seimbang.

Berikut adalah hasil akurasi dengan menggunakan model Decision Tree antara sebelum tuning dan sesudah tuning
-> Sebelum Hyperparameter Tuning

![image](https://github.com/user-attachments/assets/f4ed6e8f-1096-4b38-b31b-8b619ab07dfd)

-> Sesudah Hyperparameter Tuning

![image](https://github.com/user-attachments/assets/c4dbae00-2c5f-4caa-acd9-52f0c2ba36e4)

Berdasarkan gambar diatas setelah mendapatkan parameter terbaiki yaitu,  {'criterion': 'entropy', 'max_depth': 10, 'min_samples_leaf': 2, 'min_samples_split': 10} hasil akurasi pada saat menggunakan hyperparameter tuning memiliki peningkatan menjadi 59% dimana sebelum menggunakan hyperparameter tuning akurasi yang diperoleh adalah 53%. Ini menunjukkan bahwa model telah berkembang lebih akurat setelah tuning juga relevan secara bisnis, karena mampu membantu pihak-pihak terkait dalam mengenali individu yang membutuhkan perhatian lebih sejak dini. 

![confusion matrix](https://github.com/user-attachments/assets/cecbbb9d-94a7-4ba7-924a-ea93a86c9b3f)
