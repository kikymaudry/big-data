# Wikipedia Page Views Analysis using Wikipedia Big Data Dataset

# Link Dataset Gabungan (Hasil Scrapping)
Kaggle : https://www.kaggle.com/datasets/purikhairunisa/dataset-gabungan-csv/data

# Link Dashboard
https://khai2094.github.io/dashboard-gacha/

# Project Overview

Project ini bertujuan untuk membangun model machine learning / data analytics dalam menganalisis jumlah kunjungan artikel Wikipedia berdasarkan waktu menggunakan dataset Wikipedia Page Views.
Dataset ini berisi data jumlah kunjungan artikel Wikipedia pada berbagai timestamp, yang dapat digunakan untuk menganalisis pola trafik pengguna, tren popularitas artikel, dan prediksi jumlah kunjungan di masa depan.

### 🚀 Pengembangan pada Tahap EAS

Pada tahap EAS, proyek dikembangkan dengan melakukan **scraping data Wikipedia bahasa Indonesia** menggunakan **Wikimedia Pageviews API**. Data hasil scraping kemudian digabungkan dengan dataset Wikipedia Page Views berbahasa Inggris sehingga menghasilkan dataset gabungan yang memiliki cakupan lebih luas.

Selain peningkatan volume data, analisis juga dikembangkan dari sebelumnya hanya berfokus pada karakteristik **5V** menjadi **8V (Volume, Velocity, Variety, Veracity, Value, Validity, Variability, dan Visualization)**. Pengembangan ini juga dilengkapi dengan dashboard interaktif sehingga hasil analisis dapat dieksplorasi dengan lebih mudah.

---

# Sumber Data

Dataset Wikipedia Page Views berasal dari data trafik Wikipedia yang dipublikasikan secara terbuka oleh:

Wikimedia Foundation

Dataset ini dikembangkan untuk mendukung analisis trafik web, penelitian big data, dan pengembangan sistem prediksi berbasis data.

Dapat diakses melalui:

• Kaggle : https://www.kaggle.com/datasets/vladtasca/wikipedia-pageviews

• Wikipedia Dumps : https://dumps.wikimedia.org/other/pageviews

### 🚀 Pengembangan pada Tahap EAS

Selain menggunakan dataset Wikipedia Page Views dari Kaggle, tahap EAS juga memanfaatkan **Wikimedia Pageviews API** sebagai sumber data untuk melakukan scraping artikel Wikipedia bahasa Indonesia.

Data hasil scraping kemudian digabungkan dengan dataset utama sehingga menghasilkan dataset baru yang mencakup artikel Wikipedia berbahasa Inggris maupun Indonesia. Dengan demikian, analisis tidak lagi terbatas pada satu bahasa, tetapi mampu menggambarkan perilaku pengguna Wikipedia secara lebih luas.

---

# Objectives

1. Mengembangkan model analisis jumlah kunjungan artikel Wikipedia.

2. Mengidentifikasi pola trafik pengguna.

3. Menganalisis tren popularitas artikel.

4. Mengevaluasi performa model prediksi.

5. Mengembangkan model prediksi trafik berbasis waktu.

### 🚀 Pengembangan pada Tahap EAS

Pengembangan yang dilakukan pada tahap EAS meliputi:

6. Melakukan scraping data Wikipedia bahasa Indonesia menggunakan Wikimedia Pageviews API.

7. Menggabungkan dataset Wikipedia English dan Wikipedia Indonesia menjadi satu dataset.

8. Menganalisis karakteristik Big Data menggunakan konsep **8V**.

9. Menganalisis artikel Indonesia seperti **Prabowo Subianto** sebagai pembanding terhadap artikel internasional.

10. Mengembangkan dashboard interaktif untuk mempermudah visualisasi hasil analisis.

---

# Tujuan Analisis

1. Mengidentifikasi artikel populer berdasarkan jumlah kunjungan (views).

2. Menganalisis tren dan pola akses artikel berdasarkan waktu.

3. Mendeteksi lonjakan (spike) popularitas pada artikel tertentu.

4. Memahami perilaku pengguna berdasarkan data pageviews.

### 🚀 Pengembangan pada Tahap EAS

Pada tahap EAS, tujuan analisis diperluas dengan:

- Mengidentifikasi artikel populer dari Wikipedia Indonesia dan Wikipedia English secara bersamaan.
- Menganalisis perubahan popularitas artikel Indonesia, khususnya **Prabowo Subianto**, berdasarkan jumlah page views.
- Membandingkan pola artikel nasional dan internasional berdasarkan peristiwa yang sedang berlangsung.
- Mengevaluasi karakteristik Big Data menggunakan delapan aspek (8V).

---

# Dataset

Dataset yang digunakan adalah Wikipedia Page Views dataset, dengan karakteristik:

1. Data kunjungan artikel Wikipedia.

2. Terdiri dari beberapa artikel Wikipedia.

3. Data berbentuk time-series.

4. Memiliki informasi timestamp dan jumlah views.

### 🚀 Pengembangan pada Tahap EAS

Dataset pada tahap EAS merupakan hasil penggabungan antara dataset Wikipedia Page Views (English) dan data hasil scraping Wikipedia Indonesia.

Karakteristik dataset setelah pengembangan adalah sebagai berikut:

- Dataset gabungan Wikipedia English dan Indonesia.
- Sekitar **125 juta baris data**.
- Ukuran file sekitar **3,96 GB**.
- Memiliki **3 atribut utama**, yaitu:
  - **article**
  - **timestamp**
  - **views**
- Seluruh proses analisis dilakukan menggunakan **Polars LazyFrame** sehingga mampu menangani dataset berukuran besar dengan penggunaan memori yang lebih efisien dibandingkan pendekatan DataFrame biasa.

---
# Big Data Characteristics (5V + 3V)

## • Volume

Dataset memiliki sekitar 64,9 juta baris data dengan 6 kolom utama dan penggunaan memori mencapai ±2.9 GB. Jumlah data yang besar ini menunjukkan bahwa dataset termasuk dalam kategori big data dari aspek volume.

### 🚀 Pengembangan pada Tahap EAS

Pada tahap EAS dilakukan scraping data Wikipedia bahasa Indonesia menggunakan Wikimedia Pageviews API, kemudian hasil scraping digabungkan dengan dataset Wikipedia English. Hasil penggabungan tersebut menghasilkan dataset baru dengan sekitar **125 juta baris data** dan ukuran file sekitar **3,96 GB**.

Walaupun jumlah atribut utama menjadi **3 kolom (article, timestamp, dan views)**, peningkatan jumlah baris hampir dua kali lipat membuat volume data menjadi jauh lebih besar dibandingkan tahap sebelumnya. Dataset hasil penggabungan memberikan cakupan informasi yang lebih luas karena mencakup artikel Wikipedia dari dua bahasa yang berbeda.

Selain itu, ukuran data yang semakin besar menyebabkan proses analisis menggunakan Pandas menjadi kurang efisien. Oleh karena itu, seluruh proses preprocessing dan analisis dilakukan menggunakan **Polars LazyFrame**, sehingga penggunaan memori menjadi lebih hemat dan proses komputasi tetap berjalan dengan baik meskipun dataset berukuran hampir 4 GB.

---

## • Velocity

Dari timestamp, terlihat bahwa data diperbarui setiap hari dengan interval yang konsisten (±1 hari), dan seluruh data tercatat pada jam yang sama (00:00). Ini menunjukkan bahwa data masuk secara rutin dan terjadwal.

Selain itu, dari grafik terlihat bahwa jumlah views terus berubah dari waktu ke waktu. Ada pola naik turun dan beberapa lonjakan pada periode tertentu. Meskipun sudah dihaluskan, perubahan tersebut tetap terlihat jelas. Gabungan antara pembaruan data yang rutin dan perubahan nilai yang terus terjadi menunjukkan bahwa data memiliki velocity tinggi.

### 🚀 Pengembangan pada Tahap EAS

Karakteristik velocity tetap dipertahankan setelah dilakukan penggabungan dataset. Data Wikipedia Indonesia juga memiliki timestamp yang diperbarui secara berkala sehingga pola perubahan data tetap dapat diamati berdasarkan waktu.

Selain itu, bertambahnya artikel Indonesia memungkinkan analisis terhadap perubahan perhatian masyarakat Indonesia terhadap suatu topik. Sebagai contoh, artikel **Prabowo Subianto** menunjukkan peningkatan jumlah page views pada periode yang berkaitan dengan Pemilu Presiden 2024 dan pelantikan Presiden. Hal ini menunjukkan bahwa perubahan data berlangsung secara dinamis mengikuti peristiwa yang sedang terjadi.

---

## • Variety

Dataset terdiri dari 6 kolom yang mencakup berbagai jenis data, seperti nama artikel (article), waktu akses (timestamp), jumlah kunjungan (views), serta hasil turunan waktu (year, month, day). Dari sisi isi, data yang digunakan juga beragam karena mencakup banyak artikel yang berbeda dengan jumlah views yang bervariasi pada setiap waktu.

### 🚀 Pengembangan pada Tahap EAS

Pada tahap EAS, variasi data tidak hanya berasal dari atribut dataset, tetapi juga dari sumber dan bahasa data yang digunakan.

Dataset hasil penggabungan mencakup artikel Wikipedia berbahasa Inggris dan Indonesia sehingga topik yang dianalisis menjadi lebih beragam. Analisis tidak lagi terbatas pada artikel internasional seperti **Donald Trump**, tetapi juga mencakup artikel nasional seperti **Prabowo Subianto**.

Walaupun dataset akhir hanya memiliki tiga atribut utama (article, timestamp, dan views), keberagaman isi data meningkat secara signifikan karena mencakup lebih banyak artikel dari dua versi Wikipedia yang berbeda.

---

## • Veracity

Sebelum dilakukan proses cleaning, dataset memiliki 82.486.038 data dengan 16.787.538 data duplikat dan 7.674 missing value pada kolom article. Kondisi ini menunjukkan bahwa data awal masih memiliki tingkat keakuratan dan keandalan yang rendah karena adanya data ganda dan nilai yang hilang.

Setelah dilakukan preprocessing, jumlah data menjadi 64.944.259, dengan duplikat dan missing value berhasil dihilangkan (0). Hal ini menunjukkan bahwa kualitas data telah meningkat, sehingga data menjadi lebih akurat, konsisten, dan dapat diandalkan untuk analisis lebih lanjut.

### 🚀 Pengembangan pada Tahap EAS

Tahap preprocessing juga diterapkan pada dataset hasil penggabungan Wikipedia English dan Indonesia. Proses tersebut meliputi pengecekan missing value, data duplikat, kesesuaian tipe data, serta validasi struktur dataset.

Karena ukuran dataset mencapai hampir 4 GB, proses preprocessing dilakukan menggunakan **Polars LazyFrame** agar lebih efisien dalam penggunaan memori. Hasil preprocessing menunjukkan bahwa dataset siap digunakan untuk analisis Big Data dengan kualitas data yang tetap terjaga.

---

## • Value

Berdasarkan hasil analisis, diperoleh beberapa top artikel dengan jumlah views tertinggi. Artikel Donald_Trump menempati posisi pertama dengan total 297.839.586 views, diikuti oleh Cleopatra dengan 261.053.158 views, serta YouTube dengan 251.416.404 views. Hal ini menunjukkan bahwa ketiga artikel tersebut merupakan konten yang paling banyak diminati oleh pengguna.

Kemudian Berdasarkan grafik tren views artikel Donald_Trump, terlihat lonjakan views yang sangat signifikan pada beberapa periode tertentu. Spike tertinggi terjadi sekitar tahun 2016-2017, yang bertepatan dengan masa kampanye dan kemenangan Donald Trump dalam Pemilu Presiden Amerika Serikat 2016. Lonjakan kedua terlihat sekitar 2021, yang kemungkinan berkaitan peristiwa Capitol Hill pada Januari 2021. Setelah periode tersebut, jumlah views cenderung menurun namun masih mengalami kenaikan kecil pada momen-momen tertentu. Hal ini menunjukkan bahwa minat pengguna terhadap artikel Donald Trump sangat erat kaitannya dengan peristiwa politik yang sedang berlangsung.

### 🚀 Pengembangan pada Tahap EAS

Nilai (Value) dari dataset semakin meningkat setelah ditambahkan data Wikipedia Indonesia. Analisis tidak hanya dapat dilakukan terhadap artikel internasional, tetapi juga terhadap artikel nasional yang memiliki keterkaitan dengan peristiwa penting di Indonesia.

Salah satu contoh yang dianalisis adalah artikel **Prabowo Subianto**, yang menunjukkan perubahan jumlah page views pada periode tertentu. Dengan adanya artikel Indonesia, dataset menjadi lebih bermanfaat untuk memahami bagaimana perhatian masyarakat berubah terhadap suatu tokoh atau peristiwa, baik dalam lingkup nasional maupun internasional.

Selain itu, hasil analisis juga dimanfaatkan dalam pembuatan dashboard interaktif sehingga informasi yang diperoleh lebih mudah dipahami dan dapat dieksplorasi secara visual.

# Insight Sementara

Berdasarkan tren views artikel World_War_II, artikel ini memiliki views yang relatif stabil di angka 20.000–40.000 per hari. Spike tertinggi terjadi sekitar 2022, kemungkinan berkaitan dengan invasi Rusia ke Ukraina yang memicu pengguna membandingkan konflik tersebut dengan Perang Dunia II.

Berbeda dengan Donald Trump yang spikenya tajam lalu turun drastis, World_War_II memiliki baseline views yang konsisten sepanjang waktu. Hal ini menunjukkan bahwa perilaku pengguna terbagi dua — ada topik yang viral sesaat, dan ada topik yang selalu relevan sepanjang masa.

### 🚀 Pengembangan pada Tahap EAS

Setelah dataset Wikipedia Indonesia digabungkan, insight yang diperoleh menjadi lebih beragam. Analisis tidak hanya berfokus pada artikel internasional, tetapi juga dapat dilakukan terhadap artikel nasional.

Sebagai contoh, artikel **Prabowo Subianto** menunjukkan perubahan jumlah page views pada periode-periode penting seperti Pemilu Presiden Indonesia tahun 2024 dan pelantikan Presiden. Hasil tersebut menunjukkan bahwa pola pencarian informasi masyarakat Indonesia juga sangat dipengaruhi oleh peristiwa aktual.

Dengan adanya dua sumber data (Wikipedia English dan Wikipedia Indonesia), analisis mampu memberikan gambaran yang lebih luas mengenai perubahan perhatian masyarakat terhadap isu nasional maupun internasional.

---

# Pengembangan Analisis (Tambahan Dataset)

Dataset tambahan berasal dari Kaggle dan berisi 100 artikel Wikipedia dengan views tertinggi yang diperbarui setiap hari. Berbeda dengan dataset utama yang mencakup seluruh artikel, dataset ini berfokus pada artikel yang sedang populer dan memiliki atribut rank serta kolom date yang lebih jelas, sehingga mempermudah analisis tren harian.

Dengan menggabungkan keduanya, analisis menjadi lebih komprehensif — dataset utama memberikan gambaran tren jangka panjang, sementara dataset tambahan membantu mengidentifikasi artikel yang sedang trending. Kombinasi ini meningkatkan keampuhan analisis dalam memprediksi popularitas artikel di masa mendatang.

### 🚀 Pengembangan pada Tahap EAS

Selain pengembangan di atas, tahap EAS juga menambahkan beberapa pengembangan baru, yaitu:

- Melakukan scraping Wikipedia Indonesia menggunakan Wikimedia Pageviews API.
- Menggabungkan dataset Wikipedia English dan Wikipedia Indonesia menjadi satu dataset.
- Mengoptimalkan proses preprocessing menggunakan **Polars LazyFrame** agar mampu menangani dataset berskala besar dengan penggunaan memori yang lebih efisien.
- Mengembangkan analisis karakteristik Big Data dari **5V + 3V** menjadi **8V**.
- Menambahkan dashboard interaktif berbasis web sebagai media visualisasi hasil analisis.
- Menambahkan analisis terhadap artikel Indonesia seperti **Prabowo Subianto** sebagai pembanding terhadap artikel internasional.
- Mengembangkan visualisasi tren artikel berdasarkan page views untuk memperoleh insight yang lebih mudah dipahami.

---

# Pengembangan Big Data Characteristics (8V)

Tahap EAS memperluas analisis Big Data dengan menambahkan tiga karakteristik baru sehingga analisis tidak hanya mencakup 5V, tetapi menjadi **8V**.

## • Validity

Validity menunjukkan bahwa data yang digunakan benar-benar sesuai dengan tujuan analisis. Pada tahap EAS dilakukan pengecekan tipe data, struktur dataset, serta kesesuaian nilai pada setiap atribut.

Kolom **article**, **timestamp**, dan **views** berhasil tervalidasi dengan baik sehingga seluruh data dapat digunakan pada proses analisis tanpa mengalami inkonsistensi format.

---

## • Variability

Variability menggambarkan perubahan nilai data dari waktu ke waktu.

Hasil analisis menunjukkan bahwa jumlah page views mengalami perubahan yang dinamis mengikuti berbagai peristiwa yang sedang berlangsung. Beberapa artikel mengalami lonjakan yang sangat tinggi pada periode tertentu, sedangkan artikel lainnya memiliki pola yang relatif stabil.

Perbedaan pola tersebut menunjukkan bahwa perhatian pengguna Wikipedia dapat berubah secara signifikan tergantung pada isu atau peristiwa yang sedang terjadi.

---

## • Visualization

Visualization dilakukan melalui berbagai bentuk visualisasi data, antara lain:

- Perbandingan volume dataset UTS dan EAS.
- Grafik pertumbuhan jumlah data per tahun.
- Grafik tren page views.
- Top artikel berdasarkan jumlah views.
- Dashboard interaktif berbasis web.

Visualisasi tersebut mempermudah proses eksplorasi data serta membantu dalam memahami pola perubahan popularitas artikel secara lebih intuitif.

---

# Dashboard

Untuk mempermudah eksplorasi hasil analisis, dibuat dashboard interaktif yang menampilkan berbagai visualisasi hasil pengolahan data.

Dashboard dapat diakses melalui:

https://khai2094.github.io/dashboard-gacha/

Dashboard menampilkan beberapa informasi penting, seperti:

- Statistik dataset.
- Artikel dengan jumlah views tertinggi.
- Grafik tren page views.
- Visualisasi karakteristik Big Data.
- Ringkasan hasil analisis.

---

# Kesimpulan

Proyek ini berhasil mengembangkan analisis Wikipedia Page Views dari tahap UTS menjadi tahap EAS melalui proses scraping, penggabungan dataset, preprocessing, serta pengembangan analisis Big Data.

Penambahan dataset Wikipedia Indonesia meningkatkan volume data menjadi sekitar **125 juta baris** dengan ukuran sekitar **3,96 GB**, sehingga analisis menjadi lebih komprehensif dibandingkan sebelumnya.

Selain itu, penerapan **Polars LazyFrame** memungkinkan proses pengolahan dataset berskala besar dilakukan secara lebih efisien tanpa mengalami kendala penggunaan memori.

Pengembangan karakteristik Big Data dari **5V + 3V** menjadi **8V**, penambahan dashboard interaktif, serta analisis terhadap artikel Indonesia seperti **Prabowo Subianto** memberikan insight yang lebih luas mengenai perubahan perhatian masyarakat terhadap suatu topik berdasarkan data Wikipedia Page Views.

Secara keseluruhan, proyek ini menunjukkan bahwa data Wikipedia Page Views dapat dimanfaatkan sebagai salah satu sumber Big Data untuk menganalisis tren, perilaku pengguna, serta perubahan popularitas suatu artikel berdasarkan waktu.
