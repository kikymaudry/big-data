# 📊 Wikipedia Page Views Analysis using Wikipedia Big Data Dataset

Analisis Big Data terhadap Wikipedia Page Views menggunakan dataset Wikipedia English dan Wikipedia Indonesia hasil scraping.

---

## 📂 Link Dataset Gabungan (Hasil Scraping)

Kaggle :
https://www.kaggle.com/datasets/purikhairunisa/dataset-gabungan-csv/data

---

## 🌐 Dashboard

https://khai2094.github.io/dashboard-gacha/

---

## 📑 Table of Contents

- Project Overview
- Sumber Data
- Objectives
- Tujuan Analisis
- Dataset
- Big Data Characteristics (UTS)
- 🚀 Update EAS
- Hasil Analisis
- Dashboard
- Tech Stack
- Repository Structure
- Kesimpulan

- ## 🚀 Update EAS

Tahap EAS merupakan pengembangan dari proyek UTS.

Jika pada UTS analisis hanya menggunakan dataset Wikipedia Page Views berbahasa Inggris, maka pada tahap EAS dilakukan pengembangan dengan melakukan scraping Wikipedia Bahasa Indonesia menggunakan Wikimedia Pageviews API, kemudian menggabungkan kedua dataset menjadi satu dataset berskala lebih besar.

Selain penambahan dataset, dilakukan pula optimalisasi preprocessing menggunakan Polars LazyFrame agar proses pengolahan data menjadi lebih efisien meskipun ukuran dataset meningkat hampir dua kali lipat.

Tahap EAS juga memperluas analisis Big Data dari 5V menjadi 8V dengan menambahkan Validity, Variability, dan Visualization, sehingga analisis menjadi lebih komprehensif.

## 🚀 Update EAS

Selain menggunakan dataset Wikipedia Page Views dari Kaggle sebagai dataset utama, pada tahap EAS dilakukan proses scraping tambahan terhadap Wikipedia Bahasa Indonesia menggunakan Wikimedia Pageviews API.

Dataset hasil scraping kemudian digabungkan dengan dataset utama sehingga menghasilkan dataset baru yang merepresentasikan artikel Wikipedia dari dua bahasa.

## 🚀 Objectives EAS

Pengembangan pada tahap EAS memiliki beberapa tujuan tambahan, yaitu:

- Melakukan scraping data Wikipedia Indonesia.
- Menggabungkan dataset English dan Indonesia.
- Menganalisis karakteristik Big Data menggunakan konsep 8V.
- Membandingkan artikel internasional dan artikel Indonesia.
- Mengembangkan dashboard interaktif.

- ## 🚀 Tujuan Analisis EAS

Selain tujuan pada tahap UTS, tahap EAS menambahkan beberapa analisis baru, yaitu:

- Mengidentifikasi artikel populer pada Wikipedia Indonesia.
- Menganalisis artikel Prabowo Subianto berdasarkan jumlah page views.
- Membandingkan hasil analisis Wikipedia English dan Wikipedia Indonesia.
- Menampilkan visualisasi interaktif untuk mempermudah eksplorasi data.

- ## 🚀 Update Dataset

### Dataset UTS

| Keterangan | Nilai |
|------------|------:|
| Bahasa | English |
| Jumlah Baris | 64.944.259 |
| Jumlah Kolom | 6 |
| Ukuran | ±2.9 GB |

---

### Dataset EAS

Dataset EAS merupakan hasil penggabungan dataset Wikipedia English dan hasil scraping Wikipedia Indonesia.

| Keterangan | Nilai |
|------------|------:|
| Bahasa | English + Indonesia |
| Jumlah Baris | ±125 juta |
| Jumlah Kolom | 3 |
| Ukuran | ±3.96 GB |

Dataset gabungan ini memungkinkan analisis dilakukan tidak hanya terhadap artikel internasional, tetapi juga artikel nasional seperti Prabowo Subianto.

## 🚀 Update EAS

Pada tahap EAS, dilakukan penggabungan dataset Wikipedia English dengan hasil scraping Wikipedia Indonesia sehingga volume data meningkat secara signifikan.

| Tahap | Jumlah Baris | Ukuran |
|------|-------------:|-------:|
| UTS | 64.944.259 | ±2.9 GB |
| EAS | ±125 juta | ±3.96 GB |

Peningkatan volume ini menunjukkan bahwa dataset menjadi hampir dua kali lebih besar dibandingkan tahap UTS. Meskipun ukuran data meningkat, proses pengolahan tetap dapat dilakukan secara efisien dengan memanfaatkan **Polars LazyFrame**, sehingga penggunaan memori tetap terkendali.

Grafik perbandingan volume juga menunjukkan peningkatan jumlah record setelah dataset Wikipedia Indonesia berhasil digabungkan.

## 🚀 Update EAS

Karakteristik velocity tetap dipertahankan pada tahap EAS karena kedua dataset memiliki pola pembaruan data yang sama, yaitu berdasarkan timestamp harian.

Hasil analisis menunjukkan bahwa data diperbarui secara rutin dengan interval sekitar satu hari dan seluruh data direkam pada jam yang sama (00.00 UTC). Hal ini menunjukkan bahwa proses pengumpulan data berlangsung secara terjadwal dan konsisten.

Selain itu, setelah dataset Indonesia digabungkan, pola perubahan jumlah page views tetap bersifat dinamis. Artikel-artikel tertentu mengalami lonjakan pada periode tertentu sesuai dengan peristiwa yang sedang terjadi, sedangkan artikel lainnya memiliki pola yang relatif stabil.

Dengan demikian, karakteristik velocity tetap tergolong tinggi karena data terus mengalami perubahan seiring waktu serta diperbarui secara berkala.

## 🚀 Update EAS

Tahap EAS memberikan peningkatan pada aspek variety karena data tidak lagi hanya berasal dari Wikipedia English, tetapi juga mencakup Wikipedia Indonesia.

Selain keberagaman bahasa, variasi data juga meningkat karena artikel yang dianalisis berasal dari berbagai kategori, seperti politik, sejarah, olahraga, hiburan, teknologi, dan tokoh nasional maupun internasional.

Walaupun dataset hasil gabungan hanya terdiri atas tiga atribut utama (article, timestamp, dan views), keberagaman isi data menjadi jauh lebih luas dibandingkan tahap UTS sehingga analisis yang dihasilkan menjadi lebih representatif.

## 🚀 Update EAS

Setelah proses scraping dan penggabungan dataset dilakukan, tahap preprocessing kembali diterapkan untuk memastikan kualitas data tetap terjaga.

Proses tersebut meliputi:

- pemeriksaan missing value,
- pengecekan data duplikat,
- validasi tipe data,
- serta penyaringan artikel non-ensiklopedis seperti Main_Page, Special, Portal, Template, dan artikel administratif lainnya.

Dengan proses tersebut, dataset hasil gabungan memiliki kualitas data yang lebih baik sehingga layak digunakan untuk proses analisis Big Data.

## 🚀 Update EAS

Pada tahap EAS, nilai (value) yang diperoleh tidak hanya berasal dari artikel Wikipedia English, tetapi juga dari artikel Wikipedia Indonesia.

Selain mengidentifikasi artikel dengan jumlah page views tertinggi, dilakukan pula analisis terhadap artikel nasional seperti **Prabowo Subianto**. Analisis menunjukkan bahwa perubahan jumlah page views suatu artikel sangat dipengaruhi oleh peristiwa yang sedang terjadi.

Hasil tersebut memperlihatkan bahwa data Wikipedia Page Views dapat dimanfaatkan untuk mengidentifikasi topik yang sedang menjadi perhatian masyarakat baik pada tingkat nasional maupun internasional.

Dengan adanya dataset gabungan, insight yang diperoleh menjadi lebih kaya dibandingkan tahap UTS karena mampu menggambarkan perilaku pengguna dari dua sumber data yang berbeda.

# Validity

Validity mengukur apakah data yang digunakan benar-benar sesuai dengan kebutuhan analisis.

Pada tahap EAS dilakukan validasi terhadap seluruh atribut yang digunakan, meliputi:

- tipe data setiap kolom,
- rentang nilai timestamp,
- nilai minimum dan maksimum page views,
- jumlah artikel unik,
- serta konsistensi struktur dataset.

Hasil validasi menunjukkan bahwa seluruh atribut telah memiliki format yang konsisten sehingga data dapat digunakan secara langsung pada proses analisis tanpa memerlukan perubahan struktur tambahan.

# Variability

Variability menggambarkan tingkat perubahan nilai data dari waktu ke waktu.

Berdasarkan hasil analisis, jumlah page views pada setiap artikel menunjukkan pola yang berbeda-beda. Beberapa artikel mengalami lonjakan yang sangat tinggi ketika suatu peristiwa besar terjadi, sedangkan artikel lain memiliki jumlah views yang relatif stabil sepanjang waktu.

Perbedaan pola tersebut menunjukkan bahwa perilaku pengguna Wikipedia sangat dipengaruhi oleh isu dan peristiwa aktual sehingga karakteristik variability pada dataset tergolong tinggi.

# Visualization

Visualisasi dilakukan untuk mempermudah interpretasi terhadap data yang telah dianalisis.

Pada tahap EAS dibuat berbagai visualisasi, antara lain:

- Perbandingan volume dataset UTS dan EAS.
- Grafik pertumbuhan jumlah record.
- Grafik tren page views.
- Top artikel berdasarkan jumlah views.
- Visualisasi karakteristik Big Data.
- Dashboard interaktif berbasis web.

Visualisasi tersebut membantu pengguna memahami pola perubahan popularitas artikel secara lebih cepat dibandingkan hanya melihat data mentah.

# 📊 Hasil Analisis

## Hasil Analisis UTS

Pada tahap UTS, analisis difokuskan pada dataset Wikipedia English sehingga sebagian besar artikel dengan jumlah page views tertinggi berasal dari artikel internasional.

Hasil analisis menunjukkan bahwa **Donald_Trump** menjadi artikel dengan jumlah views tertinggi. Grafik tren juga memperlihatkan beberapa lonjakan (spike) yang bertepatan dengan peristiwa politik besar di Amerika Serikat, seperti Pemilu Presiden Amerika Serikat tahun 2016 serta peristiwa Capitol Hill tahun 2021.

Selain itu, artikel **World_War_II** menunjukkan pola yang berbeda. Jumlah views artikel ini relatif stabil sepanjang waktu dengan beberapa lonjakan ketika terjadi konflik internasional, misalnya invasi Rusia ke Ukraina. Hal tersebut menunjukkan bahwa terdapat artikel yang selalu relevan sepanjang waktu (evergreen content), berbeda dengan artikel yang hanya populer ketika suatu peristiwa sedang berlangsung.

---

## 🚀 Hasil Analisis EAS

Tahap EAS memperluas ruang lingkup analisis dengan menggabungkan dataset Wikipedia English dan Wikipedia Indonesia.

Analisis tidak lagi hanya berfokus pada artikel internasional, tetapi juga mencakup artikel yang berkaitan dengan tokoh nasional Indonesia.

Salah satu artikel yang dianalisis adalah **Prabowo Subianto**. Berdasarkan hasil visualisasi page views, artikel tersebut mengalami perubahan jumlah kunjungan pada periode-periode penting, seperti menjelang Pemilu Presiden Indonesia tahun 2024 serta pelantikan Presiden Republik Indonesia.

Hasil tersebut menunjukkan bahwa peningkatan jumlah page views sangat dipengaruhi oleh peristiwa aktual yang sedang terjadi. Ketika perhatian masyarakat meningkat terhadap suatu tokoh atau isu tertentu, jumlah kunjungan ke artikel Wikipedia terkait juga mengalami peningkatan.

Selain analisis terhadap artikel individu, dilakukan pula identifikasi artikel dengan total page views tertinggi pada dataset gabungan. Analisis ini memberikan gambaran mengenai artikel yang paling banyak diakses oleh pengguna Wikipedia selama periode pengamatan.

# 🌐 Dashboard

Sebagai pengembangan dari tahap UTS, pada tahap EAS dibangun sebuah dashboard interaktif berbasis web untuk mempermudah eksplorasi hasil analisis.

Dashboard dapat diakses melalui:

https://khai2094.github.io/dashboard-gacha/

Dashboard menampilkan berbagai informasi penting, antara lain:

- Statistik dataset.
- Ringkasan karakteristik Big Data.
- Visualisasi artikel dengan jumlah views tertinggi.
- Grafik tren page views.
- Perbandingan volume dataset.
- Hasil analisis artikel Wikipedia.

Dashboard dibuat agar proses eksplorasi data tidak hanya dilakukan melalui notebook Python, tetapi juga dapat diakses secara interaktif melalui browser.

# 🛠 Tech Stack

Proyek ini dikembangkan menggunakan beberapa teknologi berikut.

| Teknologi | Kegunaan |
|-----------|-----------|
| Python | Pemrograman utama |
| Polars | Pengolahan Big Data |
| Pandas | Analisis data |
| NumPy | Operasi numerik |
| Matplotlib | Visualisasi data |
| Kaggle | Dataset utama |
| Wikimedia Pageviews API | Scraping Wikipedia Indonesia |
| GitHub Pages | Dashboard |
| Jupyter Notebook | Eksperimen dan analisis |

# 📁 Repository Structure

```
Wikipedia-PageViews-Analysis/
│
├── dataset/
│   ├── wikipedia_english.csv
│   ├── wikipedia_indonesia.csv
│   └── dataset_gabungan.csv
│
├── notebook/
│   ├── preprocessing.ipynb
│   ├── analysis.ipynb
│   └── visualization.ipynb
│
├── dashboard/
│
├── images/
│
├── README.md
│
└── requirements.txt
```

# 🎯 Kesimpulan

Proyek ini berhasil mengembangkan analisis Wikipedia Page Views dari tahap UTS menjadi tahap EAS melalui proses scraping, penggabungan dataset, preprocessing, visualisasi, serta pengembangan analisis Big Data.

Pada tahap UTS, analisis dilakukan menggunakan dataset Wikipedia English dengan fokus pada karakteristik Big Data 5V dan pengamatan tren artikel internasional, seperti Donald Trump dan World War II.

Tahap EAS memperluas analisis dengan melakukan scraping Wikipedia Indonesia menggunakan Wikimedia Pageviews API, kemudian menggabungkannya dengan dataset Wikipedia English sehingga menghasilkan dataset gabungan dengan volume sekitar **125 juta baris** dan ukuran sekitar **3,96 GB**.

Selain peningkatan volume data, tahap EAS juga mengembangkan analisis menjadi **8V**, yaitu dengan menambahkan aspek **Validity**, **Variability**, dan **Visualization**. Penggunaan **Polars LazyFrame** memungkinkan proses pengolahan dataset berskala besar dilakukan secara lebih efisien tanpa membebani memori.

Pengembangan lainnya meliputi analisis artikel Indonesia seperti **Prabowo Subianto**, visualisasi tren page views, serta pembangunan dashboard interaktif berbasis web untuk mempermudah eksplorasi hasil analisis.

Secara keseluruhan, proyek ini menunjukkan bahwa data Wikipedia Page Views dapat dimanfaatkan sebagai sumber Big Data untuk menganalisis pola akses pengguna, mengidentifikasi artikel yang sedang populer, memahami pengaruh suatu peristiwa terhadap perubahan jumlah kunjungan artikel, serta mendukung pengambilan insight berbasis data.

> **📌 Progress Project**
>
> ✅ UTS : Analisis Wikipedia English (5V + Time Series Analysis)
>
> ✅ EAS : Scraping Wikipedia Indonesia + Dataset Gabungan + Analisis 8V + Dashboard Interaktif
>
> 
