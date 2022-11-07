# Week 6 (Backend Week 2)

# MySQL Basic
**31 Oktober 2022**

**Apa Itu Database?** <br>
Database merupakan sebuah kumpulan informasi yang disimpan dalam komputer secara sistematik dan saling berelasi. Atau secara sederhana database merupakan sekumpulan tabel yang berisi inforamsi untuk diolah, kemudian data tersebut dapat digunakan di dalam sebuah sistem. Kita memerlukan DBMS (Database Management System) untuk membuat sebuah database.

**DBMS (Database Management System)** <br>
DBMS adalah software yang dapat digunakan oleh user untuk berkomunikasi dengan data yang ada dalam media penyimpanan. Tipe utama pada Database management System antara lain, Hierarchical, Network, Relational, Non Relational, and Object Oriented.

**Istilah-Istilah Pada Database** <br>

- **Table** <br>
Tabel merupakan kumpulan value yang dibangun oleh baris dan kolom, di dalam table tersebut berisikan sebuah atribut dari sebuah data.

- **Field** <br>
Field merupakan kolom dari sebuah tabel yang dimana masing-masing dari field ini memiliki tipe data masing-masing.

- **Record** <br>
Record sendiri merupakan kumpulan nilai yang saling terkait. Secara sederhana record dapat dikatakan sebagai isi dari sebuah tabel.

- **SQL** <br>
SQL merupakan singkatan dari Structured Query Language yang merupakan sebuah bahasa yang digunakan untuk mengakses database. SQL sendiri adalah bahasa yang digunkaan untuk melakukan interaksi di RDMS (Relational Database Management System).

- **DDL** <br>
DDL merupakan sekumpulan perintah SQL yang digunakan untuk membuat, mengubah, dan menghapus struktur serta definisi metadata dari objek-objek yang ada pada database.

    ```javascript
        Contoh Table pada Database

        CREATE TABLE users (
            id_user varchar(10) primary key,
            nama varchar(50) not null,
            jenis_kelamin varchar(20) not null,
            alamat varchar(50) not null
        );
    ```


- **Alter** <br>
Alter merupakan sebuah istilah atau perintah pada SQL yang digunakan untuk mengubah struktur dari tabel yang ada, contohnya seperti menambahkan atau menghapus kolom/field, membuat atau menghapus primary ket, dan mengubah kolom atau nama tabel.

    ```javascript
        Contoh penggunaan ALTER

        Menambah Primary Key

        ALTER TABLE mahasiswa ADD Primary key (id_mhs)
    ```

- **Drop** <br>
Drop merupakan sebuah perintah yang digunakan untuk menghapus database, table, dan view atau index.

    ```javascript
        Contoh penggunaan DROP

        Menghapus Database

        DROP DATABASE kuliah
    ```
<br>

**DML (Data Manipulation Language)**

- **SELECT** <br>
SELECT merupakan sebuah perintah yang digunakan untuk menyeleksi data berdasarkan syarat yang diberikan.

    ```javascript
        Contoh Penggunaan SELECT

        SELECT * FROM mahasiswa

        SELECT alamat FROM mahasiswa
    ```

- **INSERT** <br>
INSERT merupakan perintah yang digunakan untuk memasukan data ke dalam kolom-kolom yang terdapat pada tabel.

    ```javascript
        Contoh Penggunaan INSERT

        INSERT INTO mahasiswa VALUES (value1, value2, ...., valueN)
    ```

- **Where, And, Or, Not, Like** <br>

    ```javascript
        SELECT kolom1, kolom2
        FROM nama_tabel
        WHERE kondisi1 AND kondisi2 OR kondisi3 NOT kondisi4;

        SELECT * FROM mahasiswa WHERE alamat LIKE "n%";
    ```

- **UPDATE** <br>
UPDATE merupakan perintah yang digunakan untuk melakukan perubahan pada isi dari kolom yang dipilih. Tujuannya adalah untuk memperbaiki data lama apabila terjadi kesalahan atau perubahan.

    ```javascript
        Contoh Penggunaan UPDATE

        UPDATE nama_tabel SET nama_kolom = "data baru" WHERE key_kolom = 1;
    ```

- **DELEETE** <br>
DELETE merupakan perintah yang digunakan untuk menghapus data dalam sebuah tabel yang menjadi target.

    ```javascript
        Contoh Penggunaan DELETE

        DELETE FROM nama_tabel WHERE kondisi;
    ```

**DCL (Data Control Language)** <br>
- **GRANT** <br>
GRANT merupakan sebuah perintah yang digunakan untuk memberikan hak akses pada user.

- **REVOKE** <br>
REVOKE merupakan perintah yang digunakan untuk mencabut hak akses yang telah diberikan pada user.

    ```javascript
        Contoh Penggunaan GRANT dan REVOKE

        GRANT INSERT, UPDATE ON mahasiswa TO PUBLIC

        REVOKE SELECT ON mahasiswa TO PUBLIC
    ```
<br>

**Database Relationship** <br>
Database Relationship merupakan relasi atau hubungan antara beberapa tabel dalam bahasa yang kita miliki. Relasi antar tabel dihubungkan oleh Primary key dan foreign key. Dimana, Primary key adalah atribut yang tidak hanya mengidentifikasi secara unik suatu kejadian, tapi juga mewakili setiap kejadian suatu entitas. Sedangkan, Foreign key adalah atribut yang melengkapi relationship dan menunjukan hubungan antara tabel induk dengan tabel anak.

**Tipe Database Relationship** <br>

- **One to One Relationship** <br>
- **One to Many Relationship**
- **Many to Many Relationship**

**SQL Table Join** <br>
Join merupakan penggabungan tabel yang dilakukan melalui kolom/key tertentu yang memiliki nilai terkait untuk mendapatkan satu set data dengan informasi lengkap.

**Tipe Pada SQL Table Join** <br>

- **Inner Join :** Menampilkan data hanya yang sesuai pada kedua tabel.
- **Left Join :**  Menampilkan semua data sebelah kiri dari tabel yang di joinkan dan menampilkan data sebelah kanan yang cocok dengan kondisi join. Jika tidak ditemukan kecocokan, maka akan di set NULL secara otomatis.
- **Right Join :** Menampilkan semua data sebelah kanan dari tabel yang di joinkan dan menampilkan data sebelah kiri yang cocok dengan kondisi join. Jika tidak ditemukan kecocokan, maka akan di set NULL secara otomatis.

<br>

**NoSQL** <br>
Database NoSQL merupakan database yang tidak memiliki perintah SQL. Konsep penyimpanannya adalah semi struktural atau tidak struktural, dan tidak harus memiliki relasi layaknya tabel-tabel MySQL. Tujuan dari penggunaan database noSQL ini adalah untuk model data spesifik dan memiliki skema fleksibel dalam mengembangkan aplikasi modern, contoh: aplikasi yang bersifat real time.

<br> <br>

# MySQL Lanjutan
**1 November 2022** <br> <br>

**Relantions pada SQL** <br>
- **One to Many :** Paling sering digunakan, dan dalam satu baris tabel dapat memiliki beberapa baris di tabel relasinya.

- **Many to Many :** Digunakan ketika kedua tabel yang berelasi dapat memiliki beberapa baris di tabel relasinya.

- **One to One :** Sangat jarang digunakan, dan diimpelentasikan dengan cara yang sama seperti One to Many akan tetapi dengan kondisi tambahan.

**Database Normalization** <br>
Database Normalization merupakan teknik analisis data yang mengorganisasikan atribut-atribut data dengan cara mengelompokkan sehingga terbentuk entitas yang non-redundant, stabil, dan fleksible.

- **Tujuan Database Normalization** <br>
    - Menghilangkan redundan data pada database.
    - Memudahkan juka ada perubahan struktur table database.
    - Memperkecil pengaruh jika ada perubahan dari struktur table database.

- **Efek Tidak Melakukan Normalization** <br>

    - INSERT Anomali : Situasi dimana tidak memungkinkan memasukkan beberapa jenis data secara langsung di database.


    - DELETE Anomali : Penghapusan data yang tidak sesuai dengan yang diharapkan, artinya data yang harusnya tidak terhapus mungkin ikut terhapus.


    - UPDATE Anomali : Situasi dimana nilai yang diubah menyebabkan inkonsistensi database, dalam artian data yang diubah tidak sesuai dengan yang diperintahkan atau yang diinginkan.

- **Bentuk Database Normalization** <br>

    - First Normal Form (1NF) : Menghilangkan multiple value pada sebuah kolom tabel database.
    
    - Second Normal Form (2NF) : Menghapus beberapa subset data yang ada pada tabel dan menempatkan mereka pada tabel terpisah. Harus sudah dalam bentuk 1NF untuk mendapatkan 2NF.

    - Third Normal Form (3NF) : Menghilangkan  seluruh atribut atau field yang tidak berhubungan dengan primary key. Dengan demikian tidak ada ketergantungan transitif pada setiap kandidat key.

**Keys Pada SQL** <br>
- Super Key : Kumpulan dari satu atau lebih dari satu key yang dapat digunakan untuk mengidentifikasi record secara unik dalam sebuah tabel. Super Key adalah superset dari Candidate Key.

- Candidate Key : Kumpulan satu atau lebih field atau kolom yang dapat mengidentifikasi record secara unik dalam tabel. Setiap Candidate Key dapat digunakan sebgai Primary Key. 

- Primary Key : kumpulan satu atau lebih fields/columns dari sebuah tabel yang secara unik mengidentifikasi sebuah record dalam tabel database. Valuenya tidak boleh berupa null ataupun duplicate value. Hanya boleh salah satu Candidate Key yang bisa menjadi Primary Key.

- Alternate Key : key yang bisa digunakan menjadi primary key. Pada dasarnya, Key ini merupakan candidate key yang tidak dijadikan  primary key.

- Uniqe Key : Kumpulan dari satu atau lebih fields/columns di sebuah table database yang secara unik mengidentifikasi sebuah record dalam table database tersebut. Hampir sama dengan Primary key, namun value dari Unique Key bisa berupa satu buah null value di dalam sebuah table database, dan Unique Key tidak bisa memiliki duplicate values.

- Foreign Key : Field di sebuah table database yang menjadi Primary Key di table database lain. Value dari Foreign key bisa menerima multiple null dan duplicate values.

**Join Multiple Tables** <br>

- Inner Join : Semua baris akan diambil dari kedua table yang akan di JOIN, selama columns cocok dengan kondisi yang sudah di tentukan. Memungkinkan baris dari salah satu tabel muncul di hasil jika dan hanya jika kedua tabel memenuhi kondisi yang ditentukan dalam klausa ON.

    ```javascript
        SELECT nama_kolom(5)
        FROM table1
        INNER JOIN table2
        ON table1.nama_kolom = table2.nama_kolom;
    ```

- Left Join : Semua records dari table di sisi kiri JOIN statement akan di pilih. Jika record yang di pilih dari table kiri tidak memiliki record yang cocok pada table JOIN yang kanan, maka record tersebut masih dipilih, dan kolom pada table yang kanan akan bernilai NULL.

    ```javascript
            SELECT nama_kolom(5)
            FROM table1
            LEFT JOIN table2
            ON table1.nama_kolom = table2.nama_kolom;
    ```

- Right Join : Semua records dari table di sisi kiri JOIN statement akan di pilih, bahkan jika table di sebelah kiri tidak memiliki record yang cocok.

    ```javascript
            SELECT nama_kolom(5)
            FROM table1
            RIGHT JOIN table2
            ON table1.nama_kolom = table2.nama_kolom;
    ```

**Aggregare Functions** <br>

- MAX : Untuk mengembalikan nilai terbesar dari kolom yang dipilih.

    ```javascript

        SELECT MAX(nama_kolom)
        FROM nama_tabel
        WHERE kondisi;
    ```

- MIN : Mengembalikan nilai terkecil dari kolom yang dipilih.

    ```javascript
        
        SELECT MIN(nama_kolom)
        FROM nama_tabel
        WHERE kondisi;
    ```

- SUM : Mengembalikan jumlah total kolom numerik.

    ```javascript
            
        SELECT SUM(nama_kolom)
        FROM nama_tabel
        WHERE kondisi;
    ```

- COUNT : Mengembalikan jumlah baris yang cocok dengan kriteria yang ditentukan.

    ```javascript
        
        SELECT COUNT(nama_kolom)
        FROM nama_tabel
        WHERE kondisi;
    ```

- AVG : Mengembalikan nilai rata-rata kolom numerik.

    ```javascript
        
        SELECT AVG(nama_kolom)
        FROM nama_tabel
        WHERE kondisi;
    ```

- UNION : Menggabungkan kumpulan hasil dari dua atau lebih pertanyaan SELECT.

    ```javascript
        
        SELECT nama_kolom(s) FROM table1
        UNION
        SELECT nama_kolom(s) FROM table2
    ```

- GROUP BY : Mengelompokkan baris yang memiliki nilai yang sama kedalam baris ringkasan.

    ```javascript
        
        SELECT nama_kolom(s)
        FROM nama_tabel
        WHERE kondisi
        GROUP BY nama_kolom(s)
    ```

- HAVING : Having ditambahkan ke SQL karena kata kunci WHERE tidak daapt digunakan dengan aggregate functions.

    ```javascript
        
        SELECT nama_kolom(s)
        FROM nama_tabel
        WHERE kondisi
        GROUP BY nama_kolom(s)
        HAVING kondisi
        ORDER BY nama_kolom(s)
    ```

- LIKE & WILDCARDS : Operator LIKE digunakan dalam klausa WHERE untuk mencari pola tertentu dalam kolom. Sedangkan, karakter wildcard digunakan untuk menggantikan satu atau lebih karakter dalam sebuah string.

    ```javascript
        
        SELECT kolom1, kolom2, ...
        FROM nama_tabel
        WHERE kolomN LIKE pattern;
    ```

<br> <br>

# Authentication & Authorization
**2 November 2022** <br>

**Apa itu authentication?** <br>
Authentication merupakan sebuah proses dimana seorang user (melalui berbagai macam akses fisik berupa komputer dll) mendapatkan hak akses kepada suatu entity. Analoginya adalah ketika seorang user sedang melakukan login kedalam suatu infrastruktrur jaringan, kemudian sistem mengenali user id dan menerimanya untuk diberikan akses, sesuai dengan authorisasi yang dia terima.

**Apa itu authorization?** <br>
Authorization merupakan sebuah proses penentuan apakah user tersebut diizinkan / ditolak untuk melakukan satu atau beberapa action akses terhadap resources tertentu dalam sistem. Analoginya seperti user login terhadap sistem dengan menggunakan user id dan password, kemudian sistem mengenalinya dan user mendapatkan akses atau ditolak terhadap suatu resource sistem tertentu. 
 
**JSON Web Token** <br>
JSON Web Token merupakan sebuah JSON Object yang didefinisikan dalam RFC 7519 sebagai cara aman untuk mewakili sekumpulan informasi antara dua pihak. Token sendiri terdiri dari Header, Content, dan Signature.

**Passport JS** <br>
Passport JS merupakan middleware authentication untuk Node.JS. Passport JS sangat fleksibel dan modular. Passport mudah digunakan ke aplikasi web berbasis express. Passport juga mendukung layanan otentikasi menggunakan username dan password facebook, twitter, dan lain sebagainya.

Cara install passport js

```javascript
    npm install passport
```

**Authenticate** <br>
Authenticating request di dalam passport dapat dilakukan dengan mudah, hanya dengan menggunakan passport.authenticate(). Secara default, Passport akan mengembalikan respond dengan 401 status, jika authentication gagal.

**Redirects** <br>
Redirect biasanya digunakan untuk melanjutkan setelah authentication request.

**Flas Messages** <br>
Redirect biasanya dikombinasikan dengan Flash Messages, untuk menampilkan status informasi kepada User.

**Disable Sessions** <br>
Pada server API biasanya membutuhkan kredensial untuk diberikan dengan setiap permintaan.

**Strategies** <br>
Passport menggunakan “Strategy” untuk mengotentikasi permintaan. “Strategy” dapat memverifikasi nama pengguna dan kata sandi. Otentikasi yang didelegasikan menggunakan OAuth atau otentikasi gabungan.

<br> <br>

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







    



