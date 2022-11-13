# Sequelize
**4 & 7 November 2022** <br>

**Apa Itu Sequelize?** <br>
Sequelize merupakan ORM (Object Relational Mapping) Node JS yang berbasis promise. Sequelize mendukung sebagian besar relational Database seperti MySQL, PostgresQL, MariaDB, SQLite dan Miscrosoft SQL Server. Atau secara sederhana sequelize merupakan ORM Node JS yang berbasis promise. Dengan menggunakan sequelize, kita dapat mengelola dan mengatur data di database kita dengan cepat dan efisien.

**Apa Itu ORM?** <br>
ORM adalah suatu metode/teknik pemrograman yang digunakan untuk mengkonversi data dari lingkungan bahasa pemrograman berorientasi objek (OOP) dengan lingkungan database relational.  

**Fitur serta fungsi yang ada pada Sequelize** <br>

- authenticate() : Fungsi authenticate() akan melakukan ping ke database jika berhasil maka akan mengembalikan object promise yang bisa then atau catch jika masuk then maka koneksi berhasil jika masuk catch maka koneksi gagal dan ada kesalahan dalam konfigurasi di awal.

- sync() : Berfungsi untuk melakukan sinkronisasi model dengan database, sync() return promise dengan callback dipanggil ketika sudah melakukan sinkronisasi.

- define : Fungsi define menerima dua parameter yang pertama nama model dan yang kedua adalah skema dari tabel tersebut.

- findAll() : berfungsi untuk mencari banyak data dalam database, jika panggil tanpa parameter maka akan mengambil semua data.

- findOne() : berfungsi untuk mencari satu spesifik data dengan kriteria pada parameter.

- create() berfungsi untuk membuat data baru pada database.

- update() berfungsi untuk melakukan pengubahan data.

- destroy() berfungsi untuk menghapus data.

**Sequelize Migrations** <br>
Sequelize sama seperti version control pada Git, sequelize migration bekerja untuk dapat melacak perubahan pada database. Sequelize Migration memiliki 2 functions, yaitu UP and DOWN, dimana yang berfungsi untuk melakukan migrasi, atau mengembalikan data sebelum migrasi. Dengan fungsi sequelize.query kita juga bisa mengatur data apa saja yang akan ditambahkan, sesuai dengan kemauan kita.

<br> <br>

# MongDB & Mongoose
**5 November 2022 & 6 November 2022**
<br> <br>

## MongoDB
**Apa itu MongoDB?** <br>
MongoDB merupakan salah satu produk database noSQL berbasis open source, dimana MongoDB ini menggunakan struktur data JSON untuk menyimpan datanya. MongoDB juga sering dipakai untuk aplikasi berbasis Cloud, Grid Computing, atau Big Data.

**Connect NodeJS dan MongoDB**

1. Install dotenv untuk menampung variabel environment database, dan juga install MongoDB.

    ```javascript
        npm install dotenv --save

        npm install mongodb --save
    ```

2. Buatlah satu file .env untuk menyimpan variabel database.

    ```javascript
        // .env

        MOGODB_URL=mongodb://localhost:27017
        MONGODB_DATABASE=namaDatabase
    ```

3. Buatlah file untuk membuat koneksi, dan interaksi dengan database langsung.

    ```javascript
        require('dotenv').config()

        const url = process.env.MONGODB_URL
        const database = process.env.MONGODB_DATABASE

        MongoClient.connect(url, (err, client) => {
            if(err) throw err

            var db = client.db(database);

            db.collection('Siswa').find().toArray((err, result) => {
                if(err) throw err
                console.log(result);
                client.close()
            })

            db.collection('Siswa').insert({
                username: "Wisnu",
                email: "wisnu@gmail.com",
                country: "Indonesia"
            });
        })
    ```

<br> <br>

## Mongoose

**Apa itu Mongoose?** <br>
Mongoose merupakan sebuah library yang dapat dikatakan sebagai Object Modelling MongoDB untuk NodeJS. Mongoose bisa digunakan untuk mengelola hubungan antara data, menyediakan validasi. Dan juga digunakan untuk menerjemahkan antara objek dalam kode dan representasi Objek tersebut di MongoDB.


**Installasi Mongoose** <br>

Pastikan NodeJS dan MongoDB sudah terinstall sebelumnya.

    ```javascript
        npm install mongoose
    ```

**Create Connection** <br>

1. Membuat koneksi dengan menggunakan MongoDB database, yang diletakan di .env

    ```javascript
        const mongoose = require('mongoose')
        require('dotenv').config()

        const url = process.env.MONGOOSE_URL;

        mongoose.connect(url, {
            useNewUrlParser: true,
            useUnifiendTopology: true,
            useDindAndModify: false
        });

        const db = mongoose.connection;
        db.on('error', console.error.bind(console, 'Connection error'));
        db.once('open', () => console.log('We are Connected'))
    ```

2. Gunakan file .env untuk menyimpan URL atau data rahasia yang tidak perlu dilihat di public.

    ```javascript
        MONGOOSE_URL=mongodb://localhost:27017/dbmongoose
    ```

3. Lalu jalankan file .js dan kita berhasil terhubung 

    ```javascript
        node index.js
    ```

    <br> <br>

    # DOCKER

    **7 November 2022** <br>

**Apa itu Docker?** <br>
Docker merupakan sebuah software yang menjalankan suatu aplikasi menggunakan container. Docker men-sharing kernel dari host OS, serta meng-container-kan suatu aplikasi agar dapat dijalankan dimana saja dan kapan saja. Aplikasi yg berjalan di dalam container docker tidak terpengaruh oleh faktor luar karena terisolasi


**Apa Fungsi Docker?** <br>
Docker berfungsi sebagai penyedia layanan virtual bagi aplikasi yg diinstall pada sebuah host. Docker akan menyediakan hal-hal yang diperlukan untuk aplikasi mulai dari akses file, koneksi internet, hingga port agar aplikasi dapat berjalan dengan mulus.

**Alasan Docker lebih unggul dibandingkan VM** <br>
VM memakan banyak resource dan waktu utk booting karena melakukan virtualisasi pada host hardware-nya. Sedangkan container kebalikannya dari vm, container melakukan virtualisasi pada host OS-nya

**Docker Fundamental** <br>

- Docker File : Blueprint untuk membuat image.

- Image : Template untuk menjalankan container.

- Container : Perwujudan dari image.

- Docker Registry : Tempat untuk upload/download image.

**Perintah Dasar Docker** <br>

1. Docker Pull : Download image dari docker hub.

    ```javascript
        docker pull chuanwen/cowsay
    ```

2. Docker Image : Melihat kumpulan images yang sudah terdownload.

    ```javascript
        docker images
    ```

3. Docker Run : Menjalankan Container.

    ```javascript
        docker run chuanwen/cowsay
    ```

4. Docker Ps : Melihat container yang berjalan.

    ```javascript
        docker ps
    ```

5. Docker File : Merupakan sebuah blueprint untuk membuat image.

    ```javascript
        // Cara membuat sebuah blueprint dengan docker file

        1. Buat file Dockerfile di dalam projek kita.
        2. Tulis beberapa perintah ke dalam dockerfile kita.
        3. Jalankan docker file tersebut menggunakan perintah berikut.

        docker build -t NAMA_IMAGES:TAG .
        docker build -t my-app:1.0
    ```

6, Docker Compose : Cara untuk menjalankan lebih dari 1 container secara bersamaan dan saling terhubung.

```javascript

    // Cara menggunakan docker compose

    1. Buat file NAMA_FILE.yaml di dalam projek yang dibuat.
    2. Tulis beberapa perintah ke dalam file tersebut.
    3. Jalankan menggunakan perintah berikut.

    docker-compose NAMA_FILE.yaml up
```
