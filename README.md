# Wikipedia Page Views Analysis using Wikipedia Big Data Dataset

# Project Overview
Project ini bertujuan untuk membangun model machine learning / data analytics dalam menganalisis jumlah kunjungan artikel Wikipedia berdasarkan waktu menggunakan dataset Wikipedia Page Views.
Dataset ini berisi data jumlah kunjungan artikel Wikipedia pada berbagai timestamp, yang dapat digunakan untuk menganalisis pola trafik pengguna, tren popularitas artikel, dan prediksi jumlah kunjungan di masa depan.

# sumber data 
Dataset Wikipedia Page Views berasal dari data trafik Wikipedia yang dipublikasikan secara terbuka oleh:
Wikimedia Foundation
Dataset ini dikembangkan untuk mendukung analisis trafik web, penelitian big data, dan pengembangan sistem prediksi berbasis data.
 Dapat diakses melalui:
 • kaggle : https://www.kaggle.com/datasets/vladtasca/wikipedia-pageviews
 • Harvard dataverse : https://dumps.wikimedia.org/other/pageviews



# Objectives
1. Mengembangkan model analisis jumlah kunjungan artikel Wikipedia
2. Mengidentifikasi pola trafik pengguna
3. Menganalisis tren popularitas artikel
4. Mengevaluasi performa model prediksi
5. Mengembangkan model prediksi trafik berbasis waktu

# Tujuan Analisis
1. Mengidentifikasi artikel populer berdasarkan jumlah kunjungan (views)
2. Menganalisis tren dan pola akses artikel berdasarkan waktu
3. Mendeteksi lonjakan (spike) popularitas pada artikel tertentu
4. Memahami perilaku pengguna berdasarkan data pageviews 

# Dataset
Dataset yang digunakan adalah Wikipedia Page Views dataset, dengan karakteristik:
1. Data kunjungan artikel Wikipedia
2. Terdiri dari beberapa artikel Wikipedia
3. Data berbentuk time-series
4. Memiliki informasi timestamp dan jumlah views

# Big Data Characteristics (5V + 3V)

• volume 
Dataset memiliki sekitar 64,9 juta baris data dengan 6 kolom utama dan penggunaan memori mencapai ±2.9 GB. Jumlah data yang besar ini menunjukkan bahwa dataset termasuk dalam kategori big data dari aspek volume

•Velocity
Dari timestamp, terlihat bahwa data diperbarui setiap hari dengan interval yang konsisten (±1 hari), dan seluruh data tercatat pada jam yang sama (00:00). Ini menunjukkan bahwa data masuk secara rutin dan terjadwal.

Selain itu, dari grafik terlihat bahwa jumlah views terus berubah dari waktu ke waktu. Ada pola naik turun dan beberapa lonjakan pada periode tertentu. Meskipun sudah dihaluskan, perubahan tersebut tetap terlihat jelas. Gabungan antara pembaruan data yang rutin dan perubahan nilai yang terus terjadi menunjukkan bahwa data memiliki velocity tinggi.

•Variety
Dataset terdiri dari 6 kolom yang mencakup berbagai jenis data, seperti nama artikel (article), waktu akses (timestamp), jumlah kunjungan (views), serta hasil turunan waktu (year, month, day). Dari sisi isi, data yang digunakan juga beragam karena mencakup banyak artikel yang berbeda dengan jumlah views yang bervariasi pada setiap waktu.

•veracity
Sebelum dilakukan proses cleaning, dataset memiliki 82.486.038 data dengan 16.787.538 data duplikat dan 7.674 missing value pada kolom article. Kondisi ini menunjukkan bahwa data awal masih memiliki tingkat keakuratan dan keandalan yang rendah karena adanya data ganda dan nilai yang hilang.

Setelah dilakukan preprocessing, jumlah data menjadi 64.944.259, dengan duplikat dan missing value berhasil dihilangkan (0). Hal ini menunjukkan bahwa kualitas data telah meningkat, sehingga data menjadi lebih akurat, konsisten, dan dapat diandalkan untuk analisis lebih lanjut.

•value
Berdasarkan hasil analisis, diperoleh beberapa top artikel dengan jumlah views tertinggi. Artikel Donald_Trump menempati posisi pertama dengan total 297.839.586 views, diikuti oleh Cleopatra dengan 261.053.158 views, serta YouTube dengan 251.416.404 views. Hal ini menunjukkan bahwa ketiga artikel tersebut merupakan konten yang paling banyak diminati oleh pengguna.

Kemudian Berdasarkan grafik tren views artikel Donald_Trump, terlihat lonjakan views yang sangat signifikan pada beberapa periode tertentu. Spike tertinggi terjadi sekitar tahun 2016-2017, yang bertepatan dengan masa kampanye dan kemenangan Donald Trump dalam Pemilu Presiden Amerika Serikat 2016. Lonjakan kedua terlihat sekitar 2021, yang kemungkinan berkaitan  peristiwa Capitol Hill pada Januari 2021. Setelah periode tersebut, jumlah views cenderung menurun namun masih mengalami kenaikan kecil pada momen-momen tertentu. Hal ini menunjukkan bahwa minat pengguna terhadap artikel Donald Trump sangat erat kaitannya dengan peristiwa politik yang sedang berlangsung.

# insight sementara 
Berdasarkan tren views artikel World_War_II, artikel ini memiliki views yang relatif stabil di angka 20.000-40.000 per hari. Spike tertinggi terjadi sekitar 2022, kemungkinan berkaitan dengan invasi Rusia ke Ukraina yang memicu pengguna membandingkan konflik tersebut dengan Perang Dunia II.
Berbeda dengan Donald Trump yang spikenya tajam lalu turun drastis, World_War_II memiliki baseline views yang konsisten sepanjang waktu. Hal ini menunjukkan bahwa perilaku pengguna terbagi dua — ada topik yang viral sesaat, dan ada topik yang selalu relevan sepanjang masa.

# Pengembangan Analisis (Tambahan Dataset)
Dataset tambahan berasal dari Kaggle dan berisi 100 artikel Wikipedia dengan views tertinggi yang diperbarui setiap hari. Berbeda dengan dataset utama yang mencakup seluruh artikel, dataset ini berfokus pada artikel yang sedang populer dan memiliki atribut rank serta kolom date yang lebih jelas, sehingga mempermudah analisis tren harian.
Dengan menggabungkan keduanya, analisis menjadi lebih komprehensif — dataset utama memberikan gambaran tren jangka panjang, sementara dataset tambahan membantu mengidentifikasi artikel yang sedang trending. Kombinasi ini meningkatkan keampuhan analisis dalam memprediksi popularitas artikel di masa mendatang.
