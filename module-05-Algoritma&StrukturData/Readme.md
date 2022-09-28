# Algoritma & Structure Data
- **Pengertian Algoritma** <br>
Algoritma merupakan sebuah prosedur atau tahapan logis dalam memecahkan suatu masalah tertentu secara sistematis. Sederhananya algoritma merupakan sebuah cara atau proses dalam memecahkan suatu masalah tertentu.

- **Pengertian Struktur Data** <br>
Struktur data merupakan cara menyimpan dan mengatur data dengan menyusunnya secara terstruktur pada sistem komputer atau database yang memudahkan dalam akses. Secara teknis, data yang berupa angka, huruf, simbol, dan lainnya ini ditempatkan pada kolom-kolom dan susunan tertentu. Intinya struktur data merupakan sebuah cara penyimpanan, penyusunan, dan pengaturan dara di dalam media penyimpanan komputer agar dapat digunakan secara efisien dan efektif.

- **Manfaat Algoritma dan Struktur Data**
    - Membantu dalam memcahkan suatu permasalahan yang rumit kedalam tahap-tahapan yang sederhana.
    - Memudahkan programmer dalam pembuatan program dan pemecahan suatu masalah.
    - Membantu menyelesaikan suatu masalah dengan logika dan sistematis.

<br>

- **Alasan Pentingnya Algoritma**
    - Programming itu adalah algoritma dan struktur data.
    - Data struktur digunakan untuk mengelola/manajemen sebuah data.
    - Dan Algoritma yang akan menyelesaikan suatu permasalahan menggunakan data tersebut.

<br>

- **Kualitas Wajib Dari Sebuah Algoritma**
    - Input dan output harus didefinisikan terlebih dahulu dengan tepat.
    - Setiap step harus benar-benar clear dan tidak ambigu.
    - Algoritma seharusnya tidak mengandung suatu code pada bahasa pemograman tertentu. Algoritma harus dibuat agar dapat digunakan dalam bahasa pemograman apapun.

<br> 

- **Penggunaan Algortima Sederhana**

    - Kasus : Bantulah bapak dalam membuat segelas kopi dengan cepat. <br> <br>

    ```
    Jawaban :

    Step 1 : Mulai
    Step 2 : Masak air hingga mendidih
    Step 3 : Siapkan gelas
    Step 4 : Tuangkan kopi dan gula kedalam gelas tersebut
    Step 5 : Tuangkan air yang sudah mendidih kedalam gelas
    Step 6 : Aduk hingga merata
    Step 7 : Stop

    ```

- **Penggunaan Algortima Dengan Javascript** <br>
Berikut ini merupakan contoh penggunaan algoritma pada javascript.

    ```javascript
        var a,b,c;
        a = prompt ("Angka Pertama");
        b = prompt ("Angka Kedua");
        c = Number(a) + Number(b);
        console.log(c);
        alert("Result = " + c);
    ```

- **Pengertian Pseudocode** <br>
Pseudocode adalah menuliskan algoritma dengan umumnya bahasa inggris sebelum kita implementasikan ke bahasa pemograman tertentu. 

    - **Berikut ini merupakan panduan menuliskan Pseudocode**
        
        - Menggunakan HURUF BESAR (KAPITAL) pada kata kunci (key command). <br>
        <br>

        Contoh :
        ```javascript
            IF number is > 10 THEN ...
        ```

        - 1 statement = 1 baris.
        - Gunakan indentasi. 
        - Penulisan yang spesifik namun tetap simpel.
<br> <br>

    - **Contoh Penggunaan Pseudocode** <br> <br>
    ``` javascript
        STORE "width" with any number
        STORE "height" with any nummber
        STORE "area" without any value

        CALCULATE "width" times "height"
        SET "area" value with calculation result
        DISPLAY "area"
    ```

- **Berikut merupakan beberapa pseudocode berdasarkan kondisi masalah** <br>
    - **Procedural** <br>
    Procedural adalah cara berpikir secara runtun. Artinya serangkaian perintah yang berurutan.

    <br>

    Contoh :
    ```javascript
        STORE "width" with any number
        STORE "height" with any nummber
        STORE "area" without any value

        CALCULATE "width" times "height"
        SET "area" value with calculation result
        DISPLAY "area"
    ```

    - **Conditional** <br>
    Conditional digunakan saat dibutuhkan percabangan kasus. Komputer akan melakukan suatu tindakan jika suatu kondisi terpenuhi. <br> <br>

        Contoh :

        - Jika hari ini tidak hujan, maka Wisnu pergi ke pasar, jika tidak maka Wisnu dirumah aja.
        - Jika tidak terpenuhi, maka tidak akan dijalankan. <br> <br>

        ```javascript
            IF "ngantuk"
                DO "tidur"
            DISPLAY "nikmatnya rebahan"
        ```

    - **Looping** <br>
    Komputer dapat melakukan sebuah proses yang sama berulang-ulang. Jika membutuhkan perulangan dalam kasus tertentu, kita bisa menggunakan Looping.

        Contoh :
        ```javascript
            STORE "full level" with 0
            
            WHILE "full level" < 5
                ADD "full level" by 1

            DISPLAY "I'm full!"
        ```

    - **Recursive** <br>
    Recursive adalah pola pikir dalam algoritma yang memanggil method/function didalam sebuah function.

<br>

- **Jenis Algoritma** <br>
Terdapat 2 jenis yang harus kita ketahui dari algoritma, yaitu :

    - Gunakan algoritma kita sendiri dalam menyelesaikan masalah (Melatih logika kita untuk berpikir).
    - Gunakan algoritma yang sudah umum disediakan apabila dibutuhkan.