# Mengenal-Keadaan-Jalan-di-The-Loop-Kota-Chicago-ke-Bandara-O-Hare-pada-Hari-Sabtu-Saat-Cuaca-Hujan
**Pendahuluan <a id='intro'></a>**

Dalam project ini, saya akan mencoba menganalisa data dan melakukan uji hipotesa untuk mengenal situasi/memahami dan menguji perubahan durasi selama perjalanan dari The Loop (salah satu pusat bisnis) di kota Chicago ke bandara international O'Hare, khususnya pada hari Sabtu saat cuaca hujan. Dengan menganalisa secara terstruktur, saya akan mengeksplorasi data, merumuskan hipotesis, dan melakukan pengujian statistik untuk menentukan apakah perubahan yang signifikan terjadi, dan mengambil kesimpulan berdasarkan temuan saya. Proyek ini bertujuan untuk mengenal/memahami situasi keadaan jalan dari The Loop ke bandara international O'Hare Chicago saat kondisi cuaca hujan terhadap perjalanan menuju bandara dan dapat memberikan insight yang berharga bagi industri transportasi dan pengguna jasa transportasi.

**Tujuan:**

Project ini merupakan hasil dari SQL yang akan dianalisis menggunakan Python. Tujuan dari proyek ini adalah untuk memahami apakah terdapat perubahan signifikan dalam durasi perjalanan dari Loop ke Bandara Internasional O'Hare saat kondisi cuaca hujan pada hari Sabtu. Project ini bertujuan untuk menguji hipotesis mengenai pengaruh kondisi cuaca terhadap perjalanan ke bandara dan memberikan wawasan yang berguna dalam industri transportasi. 


Berikut rincian yang akan kita lewati:

*Tahapan yang Dilakukan*

**Langkah 1: Insialisasi**

- Memanggil data library yang dibutuhkan

  -# *List library yang digunakan*
  
     * import pandas as pd
     * import matplotlib.pyplot as plt
     * import seaborn as sns
     * import numpy as np
     * from datetime import datetime, timedelta
     * from scipy import stats
     * from scipy.stats import levene, shapiro, ttest_ind, mannwhitneyu
     

**Langkah 2: Memuat Dataset**

**2.1. Analisis data eksposure (Python) dengan memuat dataset: `/datasets/project_sql_result_01.csv` dan `/datasets/project_sql_result_04.csv`.**

* Ada beberapa Sub Tahapan :

  **2.1.1. Mempelajari isi data**
  
  **2.1.2. Memastikan tipe datanya sudah benar**
  
  **2.1.3. Mengindentifikasi 10 wilayah teratas yang dijadikan sebagai titik pengantaran**
  
  **2.1.4. Membuat grafik untuk perusahaan taksi & jumlah perjalanannya, dan 10 wilayah teratas berdasarkan jumlah pengantaran**
  
  **2.1.5. Menarik kesimpulan berdasarkan grafik yang sudah dibuat dan menjelaskan hasilnya**
  
  
**2.2. Menguji hipotesis (Python) dengan memuat dataset: `/datasets/project_sql_result_07.csv`**

**Langkah 3: Kesimpulan Umum**

**Deskripsi Data**

**Tabel `project_sql_result_01`:**
- company_name — (nama perusahaan taksi)
- trips_amount — (jumlah perjalanan untuk setiap perusahaan taksi pada tanggal 15-16 November 2017)

**Tabel `project_sql_result_04`:**
- dropoff_location_name — (nama wilayah di Chicago tempat perjalanan berakhir)
- average_trips — (jumlah rata-rata perjalanan yang berakhir di setiap wilayah pada bulan November 2017)


**Tabel `project_sql_result_07`:**
- start_ts — (tanggal dan waktu penjemputan)
- weather_conditions — (kondisi cuaca saat perjalanan dimulai)
- duration_seconds — (durasi perjalanan dalam satuan detik)
