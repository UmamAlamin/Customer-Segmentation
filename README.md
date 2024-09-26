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
<h3>3.label Encoding</h3>
<p>	Dilakukan label encoding untuk mengubah data yang bertipe kategorikal menjadi data yang bertipe numerik. Pada projek ini enconding categorical data dilakukan menggunakan teknik Label Encoding. Jadi setiap kategoril diganti dengan integer(bilangan bulat).</p>
<h3>4.Feature Scaling: Standarisasi Data</h3>
<p>
Secara sederhana dilakukan standarisasi agar model tidak bias. Jika dilihat dari mean dan std deviasi setiap feature dapat dilihat bahwasannya terdapat proporsi yang inbalance. Misalnya pada  feature age dan spent. Feature Age memiliki nilai mean = 52.17963 dan Spent memiliki nilai mean=607.075361. Proporsi data yang imbalance inilah yang memungkinkan model menjadi bias dan menganggap feature spent lebih penting daripada feature age. Oleh karena itu, dilakukan standarisasi nilai-nilai dari suatu fitur sehingga nilai-nilai tersebut memiliki skala yang sama dengan cara setiap nilai pada sebuah atribut numerik akan dikurangi dengan rata-rata dan dibagi dengan standar deviasi dari seluruh nilai pada sebuah kolom atribut. Untuk implementasinya menggunakan Library dari sklearn, yaitu StandardScaler()
</p>
<h3>5.Principal Component Analysis(PCA)</h3>
<p>Selanjutnya adalah melakukan dimensi reduction menggunakan PCA.
  motivasi dari PCA disini adalah untuk meminimalisir data yang dipakai tapi disisi lain tidak boleh ada informasi yang hilang. PCA akan menghasilkan variable baru dengan memanfaatkan variable lama ( kombinasi linear dari variabel lama). Pengimplemntasiannya dilakukan dengan menggunakan library dari skelarn, yaitu PCA().
</p>
<h3>6.Modeling: Algoritma Aglomerative</h3>
<p>
  Agglomerative clustering adalah metode clustering hierarkis. Metode ini melibatkan penggabungan contoh-contoh data sampai jumlah klaster yang diinginkan tercapai.Langkah-langkah dalam Clustering. Aglomerative bekerja dengan menganggap bahwasannya setiap objek tunggal sebagai sebuah cluster yang kemudian secara iterative menggabungkan sepasang cluster yang paling dekat dan mirip (berdasarkan satu ukuran tertentu) menjadi sebuah cluster yang lebih besar.
  <ul>
   <li>metode Elbow untuk menentukan jumlah klaster yang akan dibentuk</li> 
    <li>Clustering dengan menggunakan Agglomerative Clustering</li>
    <li>Memeriksa klaster yang terbentuk melalui scatter plot</li>
  </ul>
</p>

<h3>Conclussion</h3>
<p>
  ![image](https://github.com/user-attachments/assets/314a1168-a5d6-47d9-9327-20940b15c8fe)
</p>
<h4>References</h4>
