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
