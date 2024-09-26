<h1>
  CUSTOMER SEGMENTATION MENGGUNAKAN ALGORITMA AGLOMERATIVE
</h1>

<h2>Background</h2>
<p>
Memahami pelanggan adalah sesuatu yang sangat penting terutama dalam konteks industri. Salah satu cara adalah melakukan segmentasi pelanggan untuk mengetahui karakteristik dari pelanggan.
</p>
<h2>Base Line Project</h2>
<p>
pada project ini dilakukann implementasi Principal Component Analysis (PCA) dan Aglomerative Clustering guna melakukan klasterisasi pelanggan.
Dataset dapat diakses di : https://www.kaggle.com/datasets/rodsaldanha/arketing-campaign
</p>
<h2>
  Workflow</h2>
<p>
Hal pertama yang akan dilakukan adalah Data Prepocessing. Pada project ini tahapan awal Data Prepocessing yang dilakukan adalah sebagai berikut: 
<h3>1.Checking Missing Value </h3>
<p>Dilakukan pengecekan missing value pada datasets. Pada dataset ini terdapat 2216 missing value, dan missing value tersebut akan didrop karena proporsi missing value sangat kecil dibanding semua data pada dataset.</p>
<h3>2. Checking Feature</h3>
<ul>
  <li>Ekstrak feature "Age" pelanggan berdasarkan "Year_Birth" yang menunjukkan tahun kelahiran orang tersebut.</li>
  <li>Buat feature lain "Spent" yang menunjukkan total jumlah yang dibelanjakan oleh pelanggan dalam berbagai kategori selama dua tahun.</li>
  <li>Buat feature lain "Living_With" dari "Marital_Status" untuk mengekstrak situasi hidup pasangan.</li>
  <li>Buat feature "Children" untuk menunjukkan total anak dalam satu rumah tangga, yaitu anak-anak dan remaja.</li>
  <li>Untuk mendapatkan kejelasan lebih lanjut tentang rumah tangga, buat feature yang menunjukkan "Family_Size".</li>
  <li>Buat feature "Is_Parent" untuk menunjukkan status sebagai orang tua.</li>
  <li>Terakhir, membuat tiga kategori dalam "Education" dengan menyederhanakan jumlah nilainya.</li>
  <li>Menghapus beberapa feature yang berlebihan, yaitu feature ["Marital_Status", "Dt_Customer", "Z_CostContact", "Z_Revenue", "Year_Birth", "ID"].</li>
</ul>
<h3>label Encoding</h3>
<p>	Dilakukan label encoding untuk mengubah data yang bertipe kategorikal menjadi data yang bertipe numerik. Pada projek ini enconding categorical data dilakukan menggunakan teknik Label Encoding. Jadi setiap kategoril diganti dengan integer(bilangan bulat).</p>
<h3>Feature Scaling: Standarisasi Data</h3>
<p>
Secara sederhana dilakukan standarisasi agar model tidak bias. Jika dilihat dari mean dan std deviasi setiap feature dapat dilihat bahwasannya terdapat proporsi yang inbalance. Misalnya pada  feature age dan spent. Feature Age memiliki nilai mean = 52.17963 dan Spent memiliki nilai mean=607.075361. Proporsi data yang imbalance inilah yang memungkinkan model menjadi bias dan menganggap feature spent lebih penting daripada feature age. Oleh karena itu, dilakukan standarisasi nilai-nilai dari suatu fitur sehingga nilai-nilai tersebut memiliki skala yang sama dengan cara setiap nilai pada sebuah atribut numerik akan dikurangi dengan rata-rata dan dibagi dengan standar deviasi dari seluruh nilai pada sebuah kolom atribut. ![image](https://github.com/user-attachments/assets/be5acefe-3f08-4d34-a248-cce210481738)

</p>
