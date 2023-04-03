# SPARK
<p align="justify">Pyspark dan Scala keduanya digunakan untuk mengembangkan aplikasi big data pada framework Apache Spark dengan menyediakan antarmuka untuk akses fitur-fitur Spark. Pyspark adalah Python API, sementara Scala adalah bahasa pemrograman fungsional yang mendukung paradigma pemrograman berorientasi objek dan fungsional.</p>

### Memulai Spark
<p align="justify">Digunakan untuk menjalankan Apache Spark pada cluster mode dengan menjalankan semua proses Apache Spark di seluruh node pada cluster menggunakan perintah sudo ./start-all.sh setelah masuk ke direktori sbin pada instalasi Apache Spark. Namun, langkah-langkah tersebut mungkin perlu disesuaikan dengan konfigurasi cluster yang digunakan.</p>
<table border="0">
 <tr>
    <td><b style="font-size:30px">Code</b></td>
    <td><b style="font-size:30px">Output</b></td>
 </tr>
 <tr>
    <td>cd /home/cloudera/spark-2.0.0-bin-hadoop2.7/sbin<br><br>sudo ./start-all.sh</td>
    <td><img alt="Dark" src="Memulai Spark.png"></td>
 </tr>
</table><br>

### Memulai Spark Shell
<p align="justify">spark-shell adalah salah satu komponen dari Apache Spark yang menyediakan lingkungan pengembangan berbasis baris perintah (CLI) untuk interaktif menjalankan perintah-perintah Spark.</p>
<table border="0">
 <tr>
    <td><b style="font-size:30px">Code</b></td>
    <td><b style="font-size:30px">Output</b></td>
 </tr>
 <tr>
    <td>spark-shell</td>
    <td><img alt="Dark" src="SparkShell.png"></td>
 </tr>
  <tr>
    <td>import sys.process._<br>val res = "ls /tmp" !<br>println(res)</td>
    <td><img alt="Dark" src="SparkShell1.png"></td>
 </tr>
 <tr>
    <td>:paste</td>
    <td><img alt="Dark" src="SparkShell2.png"></td>
 </tr>
</table><br>
<h2>Alasan</h2>
<p align="justify">Karena variabel "res" tidak memiliki tipe data yang didefinisikan sebelumnya sebelum digunakan dalam fungsi println() dan terjadi karena metode yang digunakan dalam perintah "ProcessLogger" harus mengembalikan nilai dari tipe "scala.sys.process.ProcessLogger", sedangkan fungsi println() mengembalikan nilai Unit.</p>

### Memulai PySpark
<p align="justify">PySpark adalah API Python untuk kerangka kerja pemrosesan data Apache Spark. Apache Spark sendiri adalah kerangka kerja open-source yang dirancang untuk memproses dan menganalisis data secara terdistribusi dan paralel pada cluster besar.</p>
<table border="0">
 <tr>
    <td><b style="font-size:30px">Code</b></td>
    <td><b style="font-size:30px">Output</b></td>
 </tr>
 <tr>
    <td>pyspark</td>
    <td><img alt="Dark" src="pyspark.png"></td>
 </tr>
</table><br>

  <h1> Broadcast.py</h1>
  <p align="justify">menggunakan broadcast() pada SparkContext untuk mengirim list dari 1 hingga 99 ke setiap worker pada cluster. Nilai tersebut dapat diakses menggunakan .value.</p>
  <img src="broadcast.png">
  
  <h1> UnderstandingRDDs.py</h1>
  <p align="justify">penggunaan PySpark pada mode standalone atau lokal, termasuk cara memulai command line dengan master tertentu dan memeriksa default parallelism. Selain itu, kode juga menunjukkan cara membuat RDD dengan jumlah partisi yang berbeda, mengakses isi setiap partisi, dan mengubah jumlah partisi dengan repartition() dan coalesce(). Terakhir, kode memeriksa grafik lineage RDD dengan toDebugString(). Kode ini dapat digunakan sebagai panduan dasar untuk penggunaan PySpark pada cluster atau mode lokal.</p>
  <img src="UnderstandingRDDs.png">

  <h1> WordCount.py</h1>
  <p align="justify">membaca file teks dari direktori tertentu menggunakan textFile() dari SparkContext dan melakukan penghitungan kata sederhana pada file tersebut. Kode menggunakan flatMap() untuk memisahkan setiap baris menjadi kata-kata, map() untuk menghitung jumlah kemunculan setiap kata, dan reduceByKey() untuk menggabungkan nilai-nilai yang sama menjadi satu nilai akhir. Output akhir dicetak menggunakan loop for. </p>
  <img src="wordcount.png">
  
  <h1> SystemCommandsOutput.scala</h1>
  <p align="justify">mengeksekusi perintah shell hadoop fs -ls menggunakan operator !! dan menampilkan outputnya menggunakan println().</p>
  <img src="SystemCommandsOutput.png">

  <h1> SystemCommandsReturnCode.scala</h1>
  <p align="justify">import package sys.process untuk mengeksekusi perintah shell pada sistem operasi. Kode selanjutnya menjalankan perintah shell "ls /tmp" menggunakan operator ! dan menyimpan hasilnya dalam variabel res. Terakhir, kode mencetak hasil eksekusi perintah shell ke konsol dengan menggunakan println.</p>
  <img src="SystemCommandsReturnCode.png">
  
<h1> Accumulator.py</h1>
  <p align="justify">Program ini membuat objek accumulator dengan nilai awal 0 dan membuat RDD baru dengan elemen yang berasal dari rentang 1 hingga 99. Selanjutnya, program menggunakan foreach untuk menjalankan fungsi lambda pada setiap elemen dari RDD, yang menambahkan nilai elemen ke dalam accumulator. Terakhir, program mencetak nilai akhir dari accumulator ke konsol.</p>
<img src="accumulator.png">

<h1> PairRDD.py</h1>
  <p align="justify">Program ini pertama-tama membuat sebuah list yang berisi tiga angka dan kemudian menjadikannya RDD dengan menggunakan sc.parallelize() dan menyimpannya ke dalam variabel myRDD. Selanjutnya, program memetakan setiap elemen RDD menjadi tuple dengan menggunakan fungsi map() dan menyimpan hasilnya dalam variabel myPairRDD. Kemudian, program menggunakan fungsi keys() untuk mengakses semua kunci dalam Pair RDD myPairRDD dan menyimpan hasilnya dalam variabel keys. Program juga menggunakan fungsi values() untuk mengakses semua nilai dalam Pair RDD myPairRDD dan menyimpan hasilnya dalam variabel values. Terakhir, program mencetak hasil kunci dan nilai ke konsol.</p>
<img src="pairRDD.png">

## Tugas Praktikum 2
### Kode 1
<table border="0">
 <tr>
    <td><b style="font-size:30px">Code</b></td>
    <td><b style="font-size:30px">Penjelasan</b></td>
 </tr>
 <tr>
    <td>sc</td>
    <td><p align="justify"></p>SparkContext (sc) digunakan untuk mengatur koneksi dengan cluster Spark dan membuat RDD</td>
 </tr>
 <tr>
    <td>accumulator</td>
    <td><p align="justify"></p>accumulator digunakan untuk menjumlahkan atau menghitung variabel di seluruh node pada cluster.</td>
 </tr>
 <tr>
    <td>parallelize</td>
    <td><p align="justify"></p>Parallelize adalah metode untuk membuat RDD dari kumpulan data pada driver program dan didistribusikan ke semua node dalam cluster Spark.</td>
 </tr>
  <tr>
    <td>lambda</td>
    <td><p align="justify"></p>Lambda adalah fungsi anonim pada Python untuk mengeksekusi fungsi sederhana, dan sering digunakan untuk membuat fungsi pada operasi RDD seperti map() dan filter().</td>
 </tr>
   <tr>
    <td>value</td>
    <td><p align="justify"></p>Value adalah tipe data pada PySpark untuk menyimpan data tunggal dalam sebuah RDD, dan tidak dapat diubah setelah dibuat.</td>
 </tr>
</table><br>
