# Javascript Dasar
- **Apa itu javacript** <br>
**Javascript** merupakan sebuah bahasa pemrogaman yang digunakan untuk membuat sebuah situs dengan konten website yang dinamis. Javascript sendiri merupakan sebuah bahasa pemrograman yang sangat powerful yang digunakan untuk logic pada sebuah website.

- **Cara menjalankan javascript** <br>
Javascript dijalankan melalui browser pada device setiap user. Contohnya seperti Google Chrome, Mozila Firefox, Opera Mini, Microsoft Edge, Safari, dan lain sebagainya. Namun, umumnya browser Chrome dan Mozilla yang sudah support untuk semua fitur Javascript.

- **Tipe Data (Data Types)** <br>
Tipe data adalah klasifikasi yang kita berikan untuk berbagai macam data yang digunakan dalam programming. Ada 6 tipe data fundamental pada Javascript, yaitu :

    1. Number
    2. String
    3. Boolean
    4. Null
    5. Undifined
    6. Object

<br>

- **Tipe Data Number** <br>
Tipe data number adalah tipe data yang mengandung semua angka termasuk angka desimal.

    Contoh:
    ```
    2, 4, 1200, 23.42
    ```

    ```javascript
        let number1 = 2;
        let number2 = 4;
        let number3 = 1200;
        let number4 = 23.42;
    ```
<br>

- **Tipe Data String** <br>
    Tipe data string adalah grup karakter yang ada pada keyboard laptop/PC kita yaitu letters `(huruf)`, number `(angka)`, spaces `(spasi)`, `symbol`, dan lainnya.

    Harus diawali dan diakhiri dengan single quotes ‘ … ‘ ataupun double quotes “ … “.

    Contoh :

    ```javascript
        let string = "wahh wisnu hebat sekali xixixi";
    ```

<br>

- **Tipe Data Boolean** <br>
Tipe data boolean adalah tipe data yang hanya mempunyai 2 buah nilai. 2 buah nilai tersebut adalah TRUE (benar) or FALSE (salah). Analoginya adalah seperti tombol/button ON/OFF dan juga seperti sebuah jawaban antara YES/NO.

    Contoh :
    ```javascript
        let benar = "true";
        let salah = "false";
    ```

<br>

- **Tipe Data Null** <br>
Tipe data null adalah tipe data yang diartikan bahwa sebuah variable/data tidak memiliki nilai. Null berbeda dengan string kosong. String kosong masih memiliki tipe data string.

    Contoh :
    ```javascript
        let dataPertama = "null";
        let dataKedua = "null";
        let dataKetiga = "";

        console.log(dataPertama);
        console.log(dataKedua);
        console.log(dataKetiga);
    ```

<br>

- **Tipe Data Undifined** <br>
Tipe data undefined adalah tipe data yang merepresentasikan varibel/data yang tidak memiliki nilai. Undefined berbeda dengan null.

    Undefined didapat dari hasil berikut:
    - Nilai dari pemanggilan variabel yang belum didefinisikan
    - Nilai dari pemanggilan element array yang tidak ada
    - Nilai dari pemanggilan property objek yang tidak ada
    - Nilai dari pemanggilan fungsi yang tidak mengembalikan nilai (return)
    - Nilai dari parameter fungsi yang tidak memiliki argumen <br> <br>
    
    Perbedaan antara null dan undifined :
    - **Null** biasanya diperoleh dalam kondisi normal dan sudah kita rencanakan.
    - **Undifined** biasanya didapat dari hasil kesalahan program (error), kelalaian programmer, dan tidak direncanakan. <br> <br>

    Contoh :
    ```javascript
        let a = "wisnu";
        let b = "keren";
        let skill = ["sleep", "eat", "sit"];

        console.log(c); // undifined
        console.log(a); // "wisnu"
        console.log(skill.length) // 3
    ```

<br>

- **Tipe Data Object** <br>
Tipe data object adalah koleksi data yang saling berhubungan (related). Tipe data pbject dapat menyimpan data dengan tipe data apapun (number, string, boolean, dan lainnya). Tipe data object mempunyai key dan value.

    Contoh :
    ```javascript
        var person = {
            firstName = "Wisnu",
            lastName = "Saputra",
            age = 21,
            favoritColor = "Black"
        };
    ```

<br>

- **Variabel** <br>
**Variable** adalah container/tempat untuk menyimpan sebuah nilai. Terdapat 3 cara dalam mendefinisikan sebuah variabel, yaitu dengan menggunakan `let`, `var`, dan `const`.

    Contoh penggunaan :
    - var <br> <br>
    ```javascript
        var namaSaya = "Wisnu";

        console.log(namaSaya); // "Wisnu"
    ```

    - let <br> <br>
    ```javascript
        let hobby = "Sepakbola";
        console.log(hobby); // "Sepakbola"

        hobby = "Basket";
        console.log(hobby) // "Basket
    ```

    - const <br> <br>
    ```javascript
        const warna = "hitam";
        console.log(warna); // "hitam"

        warna = "merah";
        console.log(warna); // Uncaught TypeError: Assignment to constant variabel.
    ```

    - **Aturan penggunaan variabel** <br>
        - Harus mendeskripsikan tentang data yang disimpan
        - Tidak bisa menggunakan number pada awal nama variabel
        - Gunakan camelcase untuk penamaan yang lebih dari 1 kata. <br> <br>
        
        Contoh: myName, myAge

<br>

- **Operator** <br>
**Operator** adalah simbol atau karakter khusus yang digunakan untuk melakukan suatu operasi untuk memanipulasi secara matematis atau logis pada data yang diberikan.

- **Jenis-Jenis Operator** <br>
    - Assignment Operator (=) <br>
    Assignment operator digunakan untuk menyimpan sebuah nilai pada variabel.

    Contoh :
    ```javascript
        let namaSaya = "Wisnu Saputra";
    ```

    ```javascript
        let a = 4;
        a = a + 2;

        console.log(a); // 6
    ```
    <br>

    - **Increment dan Decrement** <br>
    Gunakan increment atau decrement untuk menambah atau mengurangi sebesar 1 nilai.

        Contoh :
        ```javascript
            let a = 5;
            a++;

            console.log(a); // 6
        ```

        ```javascript
            let b = 10;
            a--;

            console.log(b); // 9
        ```
        <br>

    - **Arithmetic Operator** <br>
    Arithmetic operator adalah operator yang melibatkan operasi matematika, diantaranya :

        - Tambah (+)
        - Kuramg (-)
        - Perkalian (*)
        - Pembagian (/)
        - Modulus (%)

        <br>
    
         Contoh :

         ```javascript
            console.log(3 + 4); // output : 7
            console.log(9 - 4); // output : 5
            console.log(10 / 2); // output : 5
            console.log(2 * 4); // output : 8
            console.log(12 % 3); // output : 0
        ```
        <br>

    - **Comparison Operator** <br>
    Comparison operator adalah operator yang membandingkan satu nilai dengan nilai lainnya. Hasil operasi yang melibatkan comparison operator adalah antara **true** or **false**.

        - Simbol comparison operator
            - Lebih kecil dari : <
            - Lebih besar dari: >
            - Lebih kecil atau sama dengan: <=
            - Lebih besar atau sama dengan: >=
            - Sama dengan: ===
            - Tidak sama dengan: !==

            <br>

            Contoh :
            ```javascript
                5 < 20 // Menghasilkan nilai 'true'
                1 > 10 // Menghasilakn nilai 'false'

                'gajah' == 'burung' // Menghasilkan nilai 'false'
                'aku' == 'aku' // Menghasilakn nilai 'true'
            ```
    
    <br>

    - **Logical Operator** <br>
    Logical operator biasa digunakan untuk sebuah **CONDITIONAL** pada pemograman. Menghasilkan nilai **BOOLEAN** yaitu **TRUE** or **FALSE**. <br><br>

    Simbol dari Logical Operator adalah sebagai berikut:
    - AND operator : &&
    - OR operator: ||
    - NOT operator: !

    <br>

    Contoh :
    ```javascript
        // AND (&&) AND akan menghasilkan nilai true jika kedua atau semua premis bernilai TRUE.

        console.log(true && true) // true
        console.log(true && false) // false

        // OR (||) OR akan menghasilkan nilai true jika salah satu premis mengandung nilai TRUE.

        console.log(true || true) // true
        console.log(true || false) // true

        // NOT (!) NOT akan membalikkan sebuah nilai BOOLEAN. TRUE menjadi FALSE dan sebaliknya.

        let bahagia = true;
        console.log(!bahagia) // false

        let sedih = false;
        console.log(!sedih) // true

    ```

<br>

- **Conditional & Looping**
    - **Conditional** merupakan statement percabangan yang menggambarkan suatu kondisi. Conditional statement akan mengecek kondisi spesifik dan menjalankan perintah berdasarkan kondisi tersebut. Yang dicek adalah apakah kondisi tersebut TRUE (benar). Jika TRUE maka code didalam kondisi tersebut dijalankan.

    <br>

    Contoh :
    ```javascript
        let nilai = 85;

        if (nilai >= 85) {
            console.log("Yeay Wisnu Lulus);
        } else {
            console.log("Huuu Wisnu Ga Lulus!);
        }
    ```

    - **Looping** adalah statement yang mengulang sebuah instruksi hingga kondisi terpenuhi atau jika kondisi stop/berhenti tercapai.

        Contoh :
        ```javascript
            for (let i = 0; i < 10; i++>) {
                console.log("Wisnu Keren Banget");
            }
        ```