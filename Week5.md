# Writing Test Week 2 Back-End Bootcamp 

## **DATABASE** 
Database adalah kumpulan informasi yang disimpan didalam komputer secara sistematik dan saling berelasi. Untuk membuat Database diperlukan sebuah software yang dinamakan dengan DBMS(Database Management System)
DBMS adalah software yang dapat digunakan oleh user untuk berkomunikasi dengan data yang ada dalam media penyimpanan.
Tipe utama pada Database management System antara lain, Hierarchical, Network, Relational, Non Relational, and Object Oriented.

Istilah pada Database 
- Table : kumpulan value yang dibangun oleh baris dan kolom, yang didalamnya berisi atribut dari sebuah data.
- Field : kolom dari sebuah tabel dimana masing-masing field memiliki tipe data.
- Record : kumpulan nilai yang saling terikat.

## **SQL**
SQL atau Structured Query Language merupakan suatu bahasa (Language) yang digunakan untuk mengakses database. SQL adalah Bahasa Query yang digunakan untuk melakukan interaksi di RDMS (Relational Database Management System) 

SQL dapat melakukan : 
- Membuat, menampilkan dan menghapus data didalam database 
- Mengatur "Permission" 
- Membuat dan menghapus database 

Tipe data SQL :
- Number 
- String
- Boolean 
- Date time 

Key SQL :
- Primary key
- Foreign key
- Case Study

SQL Command :
- Database command
- Table command 
- Insert into
- Select
- Select alias (AS)
- Where 
- And, Or, Not
- Group by
- Limit 
- Update 
- Delete 


### DDL (Data Definition Language)
DDL merupakan kumpulan perintah SQL yang digunakan untuk membuat, mengubah dan menghapus struktur dan definisi metadata dari objek-objek Database.
 
Perintah pada DDL :
- Alter : untuk mengubah strukutur dari tabel yang ada
- Drop : menghapus database, table, dan view atau index 


### DML (Data Manipulation Language)
Perintah pada DML : 
- Select : untuk menyeleksi data berdasarkan syarat yang diberikan. 
- Insert : memasukkan data ke kolom-kolom yang terdapat pada table/index.
- Where, and, or, not, like 
- Update : unruk melakukan editing pada isi dari kolom (field) yang dipilih. 
- Delete : untuk menghapus data dalam tabel yang diinginkan. 


### DCL (Data Control Language)
Perintah pada DCL : 
- Grant : untuk memberikan hak akses pada user
- Revoke : untuk mencabut hak akses yang telah diberikan pada user. 


### Database Relationship 
Database relationship adalah relasi atau hubungan antara beberapa tabel dalam bahasa yang kita miliki. Relasi antar tabel dihubungkan oleh Primary key dan foreign key.
Primary key adalah atribut yang tidak hanya mengidentifikasi secara unik suatu kejadian, tapi juga mewakili setiap kejadian suatu entitas.
Contoh : NIP dalam tabel Dosen, merupakan nilai yg Unik yang tidak mungkin bersifat ganda.
Foreign key adalah atribut yang melengkapi relationship dan menunjukan hubungan antara tabel induk dengan tabel anak.

Tipe database relationship : 
- One to one 
- One to many and many to one
- Many to many 
- Self referencing relationship 


## SQL Table Join 
Join, adalah penggabungan tabel yang dilakukan melalui kolom/key tertentu yang memiliki nilai terkait untuk mendapatkan satu set data dengan informasi lengkap.
- Inner join : menampilkan data hanya yang sesuai di kedua tabel.
- Left join : menampilkan semua data sebelah kiri dari tabel yang di joinkan dan menampilkan data sebelah kanan yang cocok dengan kondisi join. Jika tidak ditemukan kecocokan, maka akan di set NULL secara otomatis. 
- Right Join : menampilkan semua data sebelah kanan dari tabel yang di joinkan dan menampilkan data sebelah kiri yang cocok dengan kondisi join. Jika tidak ditemukan kecocokan, maka akan di set NULL secara otomatis.

### Aggregate Function 
- MIN : mengembalikan nilai terkecil dari kolom yang dipilih.
- SUM : mengembalikan jumlah total kolom numerik.
- COUNT : mengembalikan jumlah baris yang cocok dengan kriteria yang ditentukan.
- AVG : mengembalikan nilai rata-rata kolom numerik
- UNION : menggabungkan kumpulan hasil dari dua atau lebih pernyataan SELECT.
- GROUP BY : Mengelompokkan baris yang memiliki nilai yang sama ke dalam baris ringkasan
- HAVING : HAVING ditambahkan ke SQL karena kata kunci WHERE tidak dapat digunakan dengan aggregate functions.
- LIKE & Wildcards : Operator LIKE digunakan dalam klausa WHERE untuk mencari pola tertentu dalam kolom. Karakter wildcard digunakan untuk menggantikan satu atau lebih karakter dalam sebuah string.



### Database Normalization 
Merupakan teknik analisis data yang mengorganisasikan atribut-atribut data dengan cara mengelompokkan sehingga terbentuk entitas yang non-redundant, stabil, dan fleksible.
Tujuan database ini adalah 
- Menghilangkan redundan data pada database. 
- Memudahkan juka ada perubahan struktur table database. 
- Memperkecil pengaruh jika ada perubahan dari struktur table database.

Jika tidak melakukan database normalization maka akan menimbulkan : 
- Insert anomali : Situasi dimana tidak memungkinkan memasukkan beberapa jenis data secara langsung di database.
- Delete anomali : Penghapusan data yang tidak sesuai dengan yang diharapkan, artinya data yang harusnya tidak terhapus mungkin ikut 
- Update anomali : Situasi dimana nilai yang diubah menyebabkan inkonsistensi database, dalam artian data yang diubah tidak sesuai dengan yang diperintahkan atau yang diinginkan.

### Bentuk database Normalization 
1. First Normal Form (1NF) : menghilangkan multiple value pada sebuah kolom
degan ketentuan : 
- Setiap kolom bernilai tunggal (single value)
- Setiap kolom meniliki nama yang unik
- Urutan penyimpanan data tidak jadi masalah 

2. Second Normal Form (2NF) 
- Harus sudah dalam bentuk 1NF untuk mendapatkan 2NF. 
- Menghapus beberapa subset data yang ada pada tabel dan menempatkan mereka pada tabel terpisah.

3. Third Normal Form (3NF) 
- Menghilangkan seluruh atribut atau field yang tidak berhubungan dengan primary key. Dengan demikian tidak ada ketergantungan transitif pada setiap kandidat key.

## Authentication & Authorization 
Authentication adalah proses dimana seorang user (melalui berbagai macam akses fisik berupa komputer dll) mendapatkan hak akses kepada suatu entity. Sebagai contoh, seorang user melakukan login kedalam suatu infrastruktur jaringan dan sistem mengenali user ID dan menerimanya untuk kemudian diberikan akses, sesuai dengan authorisasi yang dia terima.
Authorization adalah proses penentuan apakah user tersebut diizinkan / ditolak untuk melakukan satu atau beberapa action akses terhadap resources tertentu dalam sistem. Sebagai contoh, User login terhadap sistem dengan menggunakan user-ID dan password, kemudian sistem mengenalinya dan user mendapatkan akses atau ditolak terhadap suatu resource sistem tertentu. 

## JSON Web Token 
JSON Web Token adalah sebuah JSON Object yang didefinisikan dalam RFC 7519 sebagai cara aman untuk mewakili sekumpulan informasi antara dua pihak.
Token terdiri dari Header, Content, Signature.
Passport JS adalah middleware authentication untuk Node.JS. Passport JS sangat fleksibel dan modular. Passport dapat dengan mudah digunakan ke aplikasi web berbasis Express. Passport juga mendukung otentikasi menggunakan nama pengguna dan kata sandi, Facebook, Twitter dan lainnya. 
Authenticating request di dalam passport dapat dilakukan dengan mudah, hanya dengan menggunakan passport.authenticate() 
Secara default, Passport akan mengembalikan respond dengan 401 status, jika authentication gagal.
Redirect biasanya digunakan untuk melanjutkan setelah authentication request. Redirect biasanya dikombinasikan dengan Flash Messages, untuk menampilkan status informasi kepada User.

