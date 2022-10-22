# Writing and Presentation Test Week 1 
## Command Line Interface
Shell merupakan istilah cara user berinteraksi dengan sistem komputer. 
Shell terbagi menjadi dua, berbasis teks dan berbasis grafis. Contoh shell berbasis teks : 
- sh
- bash
- zsh
- cmd.exe  

Command Line merupakan jenis shell yang berbasis teks. Command Line Interface merupakan tampilan dari terminal yang digunakan untuk menjalankan program dan mengelola file. Aplikasi yang digunakan untuk mengakses CLI yaitu terminal emulator 

## FIle System 
File system adalah cara sistem operasi mengatur file dan direktori dalam bentuk pohon.

### Command Navigation
- pwd digunakan untuk melihat posisi directory terkini 
- ls digunakan untuk melihat isi file yang ada di sebuah directory 
- cd digunakan untuk berpindah directory 
- mkdir digunakan untuk membuat directory baru 

### Memanipulasi FIle 
- touch digunakan untuk membuat sebuah file 
- cp digunakan untuk menyalin files atau directory 
- mv digunakan untuk memindahkan files atau directory, bisa juga digunakan untuk rename
- rm digunakan untuk menghapus file directory 

## Git dan Github
Git adalah salah satu tool yang sering digunakan dalam proyek pengembangan software sebagai tempat peyimpanan file pemograman. Git juga sebagai version control system yang artinya bertugas mencatat setiap perubahan pada file pada suatu proyek.

### Setup Awal 
- Konfigurasi 
  ``git config --global user.name "Dina Rosalina"`` 
  ``git config --global user.email "dinarosalina34@gmail.com"``
- Cek apakah setup berhasil 
  `` git config --list``
- Membuat repository
  ``git init namafile``
- git status untuk melihat apakah terjadi perubahan atau tidak 
  ``git status``
- git add untuk menambah file baru atau file yang telah diubah 
  ``git add .``
- git commit -m "message" untuk menyimpan perubahan pada git 
  ``git commit -m "menambahkan username dan useremail pada git"``
- git push -u origin main untuk menyimpan perubahan file ke remote repository 
  ``git push -u origin main``
- git branch -m main untuk membuat branch baru
   ``git branch -m main``
- git chekout untuk berpindah branch 
  ``git checkout``

## HTML 
HTML merupakan singkatan dari Hypertext Markup Language yang berfungsi untuk menampilkan konten pada browser. Tools yang dibutuhkan untuk membuat HTML yaitu Code Editor dan Browser. Visual Studio Code adalah salah satu code editor yang dikembangkan oleh Microsoft. Keunggulan dari Visual Studio Code yaitu dia memiliki IntelliSense, Run and Debug, Built-in Git, dan Extensions. 

### HTML Structure 
``` 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Blog</title>
    <link href="coba.css" type="text/css" rel="stylesheet"/>
</head>
    <body>
        <div>
            <h1 class="header">Hi! This is my Blog</h1>
            <p>I love learning and sharing</p>
        </div>
    </body>
</html>
```
### HTML Element 
Terdiri dari :
- Opening tag : ``<p>``
- Content : ``Hell World!``
- Closing tag : ``</p>``
```
        <p>Hello World!</p>
``` 
### HTML Atribute 
Merupakan properti dari sebuah HTML element. Contohnya id, class, name 
### HTML Comment
Comment tidak akan dieksekusi oleh sistem, comment hanya untuk dibaca oleh user berguna untuk memberikan keterangan pada code ``<!--  -->``.

## CSS 
CSS digunakan untuk mendesain halaman website dengan mengubah warna, menggunakan font custom, editing text format, dll. 
Struktur CSS 
``` 
    .elementHTML{
         property : value}
```
Tanda (.) menunjukan item tag yang akan diberi desain. properti CSS contohnya font-size, color, background-color. Ada 3 jenis cara penggunaan CSS, yaitu 
- CSS inline : menambahkan CSS langsung pada atribut element HTML.
- CSS internal : menggunakan tag style pada bagian head 
- CSS external : menggunakan file CSS yang terpisah dengan file HTML, dengan menggunakan link akses 
``<link href="style.css" type="text/css" rel="stylesheet"/>`` 

### CSS - Tag Name 
Menggunakan tag element HTML secara langsung pada CSS. Tag ini bersifat global yang artinya satu perubahan bisa mempengaruhi seluruh tag element HTML yang ada pada file tersebut. 

### CSS - Class Name
Kita bisa menggunakan attribute class pada element HTML lalu memanggil nama class tersebut pada CSS. HTML yang memiliki class yang sama, akan mempunyai atyling yang sama saat digunakan pada CSS. Gunakan (.) saat memanggil class pada CSS. 
Nested Element : konsep CSS dan HTML sama, setiap element memiliki parent dan child. 
## Flexbox 
Yaitu cara untuk mengatur layout. Flexbox ini banyak digunakan karena penggunaannya yang mudah dan didukung oleh kebanyakan brwoser. Felxbox terdiri dari 1 parent/container dan bisa memiliki beberapa child/item.
- Flex-direction digunakan untuk mengatur letak item child. 
- Flex-wrap mengatur tata letak child pada 1 line 
- Flex-flow sebagai shortcut untuk set up flex-direction dan fles-wrap bersamaan
- Order pada flex berfungsi untuk orgering item mana yang ingin kita atur posisinya
- Justify-content untuk mengatur tata letak dan space antar item child secara horizontal atau main axis
- Align-content untuk mengatur tata letak dan space antar item child secara vertikal atau cross axis
- Flex-grow untuk mengatur size suatu item child pada flexbox
- Flex-shrink properti untuk membuat size suatu item child mengecil secara relatif terhadap item child yang lainnya. 
- Flex- basis untuk mengatur width dari setiap item child

## Algorithm and Pseudocode 
Algoritma merupakan langkah-langkah yang dibutuhkan untuk menyelesaikan satu masalah secara terurut. Kualitas dari algoritma :
- Input dan output harus didefinisikan terlebih dahulu dengan tepat
- Setiap step harus benar-benar clear dan tidak ambigu 
- Algoritma seharusnya tidak mengandung suatu code pada bahasa pemrograman tertentu.
- Algoritma harus dibuat agar dapat digunakan dalam pemograman apapun 

Kenapa harus belajar algoritma?
- Programming itu adalah algoritma dan struktur data
- Data struktur digunakan untuk mengelola/manajemen sebuah data
- Dan algoritma yang akan menyelesaikan suatu permasalahan menggunakan data tersebut

Contoh algoritma membalas pesan 
- Buka handphone
- Masuk ke pesan
- Klik pesan yang ingin dibalas
- Ketik pesan yang ingin dikirimkan
- Kemudian klik kirim

Algoritma deskriptif
1. variabel i = 3
2. apakah i < 20?
3. jika iya, maka ke no 5 
4. jika tidak, maka ke no 6
5. tampilkan "lebih kecil dari 20"
6. tampilkan "lebih besar dari 20"
7. selesai

Pseudocode adalah menuliskan algoritma dengan umumnya bahasa inggris sebelum kita implementasikan ke bahasa pemograman tertentu.Panduan menulis pseudocode
- Menggunakan huruf kapital untuk menulis perintah 
- 1 statement hanya terdiri dari 1 baris 
- Menggunakan identasi
- Harus bersifat spesifik dan simple

contoh pseudocode 
``` 
Deskripsi
var panjang, lebar, luar : integer;

panjang ← 100;
lebar ← 64;
luas ← panjang*lebar;
PRINT luas;
```

Jenis Pseudocode :
  - Procedural : cara berpikir runut 
  - Conditional: jika dibutuhkan suatu percabangan masalah (if else)
  - Looping    : sebuah perintah yg diulang-ulang
  - Recursive  : sebuah perintah yang memanggil method/function didalam sebuah function


## Javascript 
Bahasa pemrograman yang digunakan dalam pengembangan website.

### Tipe Data 
- String 
- Number 
- Boolean 
- Null
- Undefined
- Object 

Operator pada Javascript 
- increment dan decrement, yaitu untuk menambah atau mengurangi sebesar 1 nilai
- Aritmatika :
- 1. Penjumlahan (+)
- 2. Pengurangan (-)
- 3. Perkalian (*)
- 4. Pembagian (/)
- 5. Modulus (%)

Conditional 
Merupakan statment percabangan yang menggambarkan suatu kondisi.
- If 
- If else 
- If else if 

Looping 
Statement yang mengulang atau biasa disebut dengan perulangan

- For 
- While 
- Do while 


