# Week 5

# Web Server & RESTful API
**24 Oktober 2022** <br> <br>

## Web Server 

**Apa itu Web Server?** <br>
web server adalah sebuah perangkat lunak yang terinstall di dalam komputer server, yang berfungsi untuk menerima permintaan dan juga request berupa halaman website melalui HTTP atau HTTPS dari user atau client, dan kemudian mengirimkannya kembali dalam bentuk halaman web yang berbentuk dokumen HTML. Web Server sendiri terdiri dari komponen penting yaitu hardware (perangkat keras) dan software (perangkat lunak).

**Apa itu Static Web Server?** <br>
Static web server merupakan sebuah tumpukan yang terdiri dari komputer (perangkat keras) dengan server HTTP (perangkat lunak). Kami menyebutnya `statis` karena server mengirimkan file yang dihosting apa adanya ke browser kita.

**Apa itu Dynamic Web Server?** <br>
Dinamic web server meruapakan sebuah server web dinamis yang terdiri dari server web statis ditambah perangkat lunak tambahan, paling sering server aplikasi dan database. Kami menyebutnya `dinamis` karena server aplikasi memperbarui file yang dihosting sebelum mengirim konten ke browser Anda melalui server HTTP.

**Server Side Programming** <br>
Server side programming adalah sebuah server web yang dimana dia menunggu pesan permintaan dari klien, kemudian memprosesnya saat pesan itu tiba, dan membalas browser web dengan pesan respon HTTP. Respons berisi baris status yang menunjukkan apakah permintaan berhasil atau tidak (mis. "HTTP/1.1 200 OK" untuk berhasil). Isi respons yang berhasil atas permintaan akan berisi sumber daya yang diminta (misalnya halaman HTML baru, atau gambar, dll), yang kemudian dapat ditampilkan oleh browser web.

**Static Side** <br>
Static side nerupakan situs yang mengembalikan konten hard-coded yang sama dari server setiap kali sumber daya tertentu diminta. Pada saat pengguna ingin menavigasi ke halaman, browser akan mengirimkan permintaan "GET" HTTP yang menentukan URL nya. Berikut ini merupakan sebuah gambar arsitektur server web dasar untuk static side. <br> <br>
![static side](static.png)

**Dynamic Side** <br>
Dynamic side merupakan situs di mana beberapa konten respons dihasilkan secara dinamis, hanya bila diperlukan. Di situs web dinamis, halaman HTML biasanya dibuat dengan memasukkan data dari database ke dalam placeholder di template HTML (ini adalah cara yang jauh lebih efisien untuk menyimpan konten dalam jumlah besar daripada menggunakan situs web statis). Berikut ini merupakan sebuah gambar arsitektur server web dasar untuk dynamic side. <br> <br>
![dynamic side](dynamic.png)
<br> <br>

## Restful API

**Apa itu REST?** <br>
REST atau Representational State Transfer merupakan suata gaya arsitektur untuk menyediakan standar antara sistem komputer di web, sehingga memudahkan sistem untuk berkomunikasi satu sama lain. Sistem yang sesuai dengan REST sering disebut sistem RESTful, dicirikan oleh bagaimana mereka tidak memiliki kewarganegaraan dan memisahkan masalah klien dan server.

**Komunikasi antara Client dan Server**

- **Making Requests** <br>
REST mengharuskan klien membuat permintaan ke server untuk mengambil atau mengubah data di server. Permintaan umumnya terdiri dari :

    - kata kerja HTTP, yang mendefinisikan jenis operasi apa yang harus dilakukan.
    - header, yang memungkinkan klien untuk menyampaikan informasi tentang permintaan.
    - jalan menuju sumber daya
    badan pesan opsional yang berisi data.
<br> <br>

- **HTTP VERBS**
Terdapat 4 kata kerja HTTP dasar yang kami gunakan dalam permintaan untuk berinteraksi dengan sumber daya dalam sistem REST :

    - GET — mengambil sumber daya tertentu (berdasarkan id) atau kumpulan sumber daya.
    - POST — buat sumber daya baru.
    - PUT — perbarui sumber daya tertentu (berdasarkan id).
    - DELETE — menghapus sumber daya tertentu dengan id.


<br> <br>

# Intro Node JS
**25 Oktober 2022** <br>

**Apa itu Node.js?** <br>
Node.js adalah lingkungan runtime JavaScript open-source, lintas platform, back-end yang berjalan pada mesin V8 dan mengeksekusi kode JavaScript di luar browser web. Node.js memungkinkan pengembang menggunakan JavaScript untuk menulis alat baris perintah dan untuk skrip sisi server—menjalankan skrip sisi server untuk menghasilkan konten halaman web dinamis sebelum halaman dikirim ke browser web pengguna. Node.js secara sederhana merupakan sebuah platform javascript yang dapat berjalan di backend atau server side di komputer kita secara langsung. <br> <br>
![node](node.png)

**Node JS Arsitektur** <br>
- **Single Thread** <br>
Thread merupakan sebuah eksekusi dalam menjalankan beberapa tugas atau program secara bersamaan. Setiap unit yang mampu mengeksekusi kode disebut thread. Javascript menggunakan konsep single thread, yang berarti hanya memiliki satu tumpukan panggilan yang digunakan untuk menjalankan program. <br> <br>
![arc](arc.png)

    Javascript menggunakan call stack untuk melakukan manajemen single thread. Ketika terdapat perintah baru maka akan ditambahkan (push) dan akan di keluarkan ketika perintahnya sudah selasai (pop).

- **Even Loop** <br>
Walaupun menggunakan single thread namun kita dapat melihat javascript seperti saat menggunakan multi thread, yaitu dengan menggunakan konsep arsitektur javascript. Terdapat event queue yang berguna sebagai penampung ketika terdapat perintah baru yang akan dieksekusi. Event loop akan memfasilitasi kondisi ini, event loop akan memeriksa terus menerus, ketika antrian kosong di call stack maka akan menambah antrian baru dari event queue sampai semua perintah selesai di eksekusi.

- **Server Side Scripting** <br>
Pada dasarnya javascript merupakan bahasa pemrograman yang digunakan di front end side. Sehingga kita hanya bisa mengerjakan javascript dengan menggunakan browser untuk menampilkan hasil eksekusinya. 
Tetapi dengan menggunakan NodeJS kita dapat menjalankan javascript di server side menggunakan terminal command line menggunakan perintah “node”. 

```javascript
    console.log("Hallo wisnu");
    hallo wisnu
```

**Javascipt Untuk Node JS** <br>
Terdapat beberapa hal yang perlu kita pelajari guna mempermudah kita dalam memahami Node Js, yaitu :

- Arrow function expression <br>
Arrow expression merupakan fitur terbaru dari javascript, yaitu mempermudah membuat sintaks function menggunakan “=>” 

```javascript
    // tanpa arrow function
    function countLength(val1, val2) {
        return val1.length + val2.length
    }

    // dengan arrow function
    const countLengthChar = (val1, val2) => return val1.length + val2.length
```

- Asynchronous <br>
Asynchronous merupakan konsep yang paling penting dari javascript. Pada dasarnya, javascript mengeksekusi code secara single thread dan berurutan baris per baris yang disebut dengan synchronous. Sedangkan asynchronous memungkinkan mengeksekusi code tanpa berurutan dengan cara “skip” code dan melanjutkan eksekusi code selanjutnya. Konsep ini menungkinkan code kita tidak terjadi blocking dan lebih efisien.

```javascript
    console.log("halo");
    setTimeout(() => {console.log('Javascript')}, 100)
    console.log('Wisnu');

    /* OUTPUT
    halo
    Wisnu
    Javascript
    */
```
- JSON
JSON atau Javascript Object Notation merupakan format yang digunakan untuk menyimpan dan mengirim data menggunakan konsep object di javascript. JSON dapat digunakan di hampir semua bahasa pemrograman sehingga sangat cocok untuk dipelajari.

```javascript
    {"users": [
        {"username" : "Wisnu", "tempat" : "Karawang"},
        {"username" : "Bambang", "tempat" : "Zimbabwe"},
        {"username" : "Getuk", "tempat" : "Magelang"},
        {"username" : "Dayat", "tempat" : "Merauke"},
    ]}
```
<br> <br>

# Express JS
**26 Oktober 2022** <br> <br>
**Apa itu Express JS** <br>
Express Js merupakan sebuah adalah kerangka kerja aplikasi web back end untuk Node.js, dirilis sebagai perangkat lunak bebas dan sumber terbuka di bawah Lisensi MIT. Ini dirancang untuk membangun aplikasi web dan API. Ini telah disebut sebagai kerangka kerja server standar de facto untuk Node.js. Express adalah salah satu package NodeJS yang memungkinkan kita untuk membuat HTTP REST API ataupun aplikasi web dengan mudah. Dengan menggunakan express, kita dapat membuat berbagai hal dengan cepat dibangingkan membuatnya secara manual. 



Salah satu hal yang dapat kita buat dengan cepat menggunakan express adalah Parsing Request Body From HTTP. Dimana Req.body berfungsi untuk menangkap nilai/data yang dikirimkan user dari interface / dari postman. Untuk menggunakan req.body kita harus memanggil library body-parser. Body-parser adalah library untuk menangani application/x-www-form-urlencoded (data JSON yang dikirim melalui form-html/interface).

```javascript 
    const bodyParser = require('body-parser');

    app,use(bodyParser.urlencoded({ extended: false}))

    app.use(bodyParser.json())
```

**Basic Routes** <br>

- **Routes** <br>
Routes adalah sebuah end point yang diapat kita akses menggunakan URL di website. Didalam routes kita perlu menentukan method API, alamat dan response apa saja yang akan dikeluarkan. Kita dapat menjalankan aplikasi sederhana kita dengan cara menggunakan “node”. Dan aplikasi kita akan berjalan di alamat http://localhost:3000. Kemudian kita dapat mengaksesnya di website dan menambah route yang akan kita akses yaitu “/”.

- **Method** <br>
Dengan menggunakan method kita dapat melakukan perintah seperti POST, PUT, PATCH, dan DELETE.

    ```javascript
        app.Post('/posting', (req, res) => {
            res.send("posting berhasil yeay")
        })

        app.Delete('/deleting', (req, res) => {
            res.send("Berhasil Terhapus yeay)
        })
    ```

- **Response** <br>
Di dalam route kita dapat mengirim response menggunakan parameter dari route express.js yaitu “res.Send()” untuk mengirim plain text ketika kita mengakses route tersebut. Kita dapat mengirim response berupa output json yang biasa dipakai untuk back end application. Dengan menggunakan output json maka kita dapat mengirim data yang mudah diakses 

    ```javascript
        app.get('/hai', (req, res) => {
            res.json({
                nama : "wisnu",
                umur : 21,
                pesan : "jangan lupa senyum"
            })
        })
    ```

- **Status Code** <br>
Dalam pengaplikasian back end application, kita sangat perlu memberikan status code sebagai informasi apakah route yang kita akses berjalan sebagaimana mestinya dan tidak terjadi error.

- **Query** <br>
Query merupakan parameter yang digunakan untuk membantu menentukan tindakan yang lebih spesifik daripada hanya sekedar router biasa. Biasanya query ditaruh di akhir route dengan memberikan informasi diawali dengan “?” kemudian tedapat key dan data yang dapat ditindak lanjuti. Contoh : “?q=hai&umur=21”. Query route ini biasanya dapat kita temukan ketika kita sedang melakukan searching di google. pada ExpressJS juga kita dapat membaca query menggunakan req.query, kemudian informasi tersebut dapat kita olah atau kita kembaliakan lagi.

- **Nested Route** <br>
Nested route digunakan ketika terdapat banyak route yang memiliki nama yang sama atau ingin membuat route yang lebih mendalam.

**Express Middleware** <br>
Middleware Express adalah fungsi yang dijalankan selama siklus hidup permintaan ke server Express . Setiap middleware memiliki akses ke permintaan dan respons HTTP untuk setiap rute (atau jalur) yang dilampirkannya.

**Apa saja yang dapat dilakukan oleh Function Middleware?**

Middleware function dapat melakukan tugas-tugas berikut ini, diantaranya :

- Menjalankan kode apapun
- Memodifikasi Object Request dan Object Response.
- Menghentikan request-response cycle.
- Melanjutkan ke middleware function selanjutnya atau ke handler function dalam suatu request response cycle.

**Jenis Express Middleware Berdasarkan Cara Pengunaannya** <br>
Express Middleware dapat dikelompokkan berdasarkan dari dimana middleware function itu digunakan :

- Application Level Middleware
- Router Level Middleware
- Error Handling Middleware

<br> <br>

# Design Database with MySQL
**27 - 28 Oktober 2022** <br>

**Apa itu Database?** <br>
database merupakan suatu kumpulan informasi atau data yang tersusun rapi dalam perangkat komputer secara sistematis dan dapat dikelola menggunakan program aplikasi DBMS (Database Management System).

**Apa itu MySQL?** <br>
MySQL merupakan sebuah implementasi dari sistem manajemen basis data relasional ( RDBMS) yang didistribusikan secara gratis di bawah lisensi GPL (General Public License). Setiap pengguna dapat secara bebas menggunakan, mendistribusikan, dan membuat karya turunan dari MySQL.

**Cara membuat table pada MySQL** <br>
Table merupakan kumpulan dari field dan record. Namun, tabel juga dapat diartikan sebagai susunan antara baris dan kolom, sehingga strukturnya lebih kompleks. Tabel sering digunakan pada penelitian, analisis data, hingga basis data. Database sendiri bentuknya berupa table, dna dalam table tersebut berisi kumpulan data yang kompleks, data tersebut diolah kembali hingga menampilkan berbagai bentuk bisa berupa diagram, daftar data yang di inginkan, dan sebagainya. Berikut ini merupakan cara membuat sebuah table pada MySQL.

```javascript
    CREATE TABLE users (
        id_user varchar(10) primary key,
        nama varchar(50) not null,
        alamat varchar(50) not null,
        no_telp varchar(20) not null, 
        tgl_lahir varchar(20) not null
    );
```

**Primary Key** <br>
Primary Key disebut juga dengan Kunci Primer. Kunci utama dipilih sebagai pengidentifikasi untuk membedakan satu baris dalam tabel dari yang lain. Pada dasarnya, setiap tabel hanya memiliki satu kunci utama. Kunci utama yang terkandung dalam tabel pertama terkait dengan tabel kedua, sehingga disebut sebagai kunci asing di tabel kedua.

**Foreign Key** <br>
Foreign Key adalah kolom atau field pada suatu tabel yang berfungsi sebagai kunci tamu dari tabel lain. Foreign Key sangat berguna bila kita bekerja dengan banyak tabel yang saling berelasi satu sama lain. Tujuan adanya foreign key adalah untuk dapat direlasikan data di tabel induk dan tabel anak.

**Proses Design Database** <br>
Proses desain terdiri dari langkah-langkah berikut ini:

- Menentukan tujuan database kita. Ini membantu mempersiapkan kita untuk langkah yang tersisa.

- Menemukan dan menata informasi yang diperlukan. Kumpulkan semua tipe informasi yang mungkin ingin kita Rekam dalam database, seperti nama produk dan nomor pesanan.

- Membagi informasi ke dalam tabel. Membagi item informasi kita ke dalam entitas utama atau subjek, seperti produk atau pesanan. Setiap subjek kemudian menjadi tabel.

- Ubah item informasi menjadi kolom. Putuskan informasi yang ingin kita simpan di setiap tabel. Setiap item menjadi bidang, dan ditampilkan sebagai kolom dalam tabel. Misalnya, tabel karyawan mungkin menyertakan bidang seperti nama belakang dan tanggal Penyewaan.

- Menentukan kunci utama. Pilih kunci utama setiap tabel. Kunci utama adalah kolom yang digunakan untuk mengidentifikasi secara unik setiap baris. Contohnya mungkin id produk atau ID pesanan.

- Menyiapkan hubungan tabel. Lihat setiap tabel dan putuskan bagaimana data dalam satu tabel terkait dengan data dalam tabel lain. Tambahkan bidang ke tabel atau Buat tabel baru untuk mengklarifikasi hubungan, sebagaimana diperlukan.

- Memperbaiki desain kita. Menganalisis desain kita untuk kesalahan. Buat tabel dan tambahkan beberapa data sampel data. Lihat apakah kita bisa mendapatkan hasil yang kita inginkan dari tabel kita. Sesuaikan desain sesuai keperluan.

- Menerapkan aturan normalisasi. Terapkan aturan normalisasi data untuk melihat apakah tabel Anda terstruktur dengan benar. Lakukan penyesuaian pada tabel, jika diperlukan.

**Entity Relationship Diagram (ERD)** <br>
Entity Relationship Diagram adalah diagram untuk menggambarkan desain database yang akan dibuat. Di dalam ERD akan terlihat semua tabel yang akan dirancang, primary key masing-masing tabel, serta foreign key, dan kolom-kolom apa saja yang nantinya tersedia. ERD memiliki berbagai versi, baik yang berbentuk balon, maupun tabel. ERD inilah sebagai blueprint dari database yang akan dirancang.

![erd](erd.jpg) <br>

**Normalisasi Database** <br>
Normalisasi database (Database normalization) adalah proses penyusunan kolom dan tabel untuk meminimalkan redundansi data (data yang berulang). Normalisasi biasanya akan membagi tabel besar menjadi beberapa tabel kecil yang saling terhubung. Hal ini dilakukan agar mudah dalam mengatur, dan mengorganisasi data yang ada. Contohnya, untuk tabel data_mahasiswa, jika terjadi perubahan nama jurusan, misalnya dari Ilmu Komputer menjadi Teknik Informatika, maka kita harus merubah satu-satu  tiap mahasiswa. Namun jika di bagi menjadi 2 tabel, kita hanya tinggal merubah baris no urut 14 dari tabel  kode_jurusan menjadi Teknik Informatika. Dan otomatis setiap mahasiswa yang memiliki kode_jurusan 14, adalah mahasiswa Teknik Informatika.

Normalisasi database memiliki beberapa tahapan. Normalisasi database setidaknya memiliki 9 tahapan. Pada setiap tahapan, ada syarat yang harus dipenuhi, sampai sebuah tabel tidak lagi memiliki kolom yang redundant. Kita tidak harus mengikuti semua tahap, biasanya hanya dibutuhkan 3 tahapan normalisasi untuk membuat sebuah desain database sederhana. Proses normalisasi database tidak akan kita bahas disini, namun setidaknya kita mengetahui bahwa normalisasi database adalah proses untuk mendesain database agar terorganisir.












 


