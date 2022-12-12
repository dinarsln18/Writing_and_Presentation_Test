# Writing Test Week 2 Back-End Bootcamp
# Sequilize 
Sequelize adalah ORM (Object Relational Mapping) Node JS yang berbasis promise. Sequelize mendukung sebagian besar relational Database seperti MySQL, PostgresQL, MariaDB, SQLite dan Miscrosoft SQL Server. Dengan fitur fitur di Sequelize, kita bisa mengelola dan mengatur data di database kita dengan cepat, dan efisien.
ORM adalah suatu metode/teknik pemrograman yang digunakan untuk mengkonversi data dari lingkungan bahasa pemrograman berorientasi objek (OOP) dengan lingkungan database relational. 
# Cara menggunakannya 
- install sequilize 
`` npm i -g sequilize-cli ``
- install sequelize dan driver mysql
`` npm i sequelize ``
`` npm i mysql2 ``
- inisialisasi sequilize 
`` npx sequelize-cli init ``
- masuk ke config/config.js 
```
    "username": DB_USER,
    "password": DB_PASS,
    "database": DB_NAME,
    "host": DB_HOST,
    "dialect": "mysql"
```
- membuat model
`` npx sequelize-cli model:generate --name User --attributes name:string,address:text,age:integer ``
- migrate ke database
`` npx sequelize-cli db:migrate ``

# MongoDB 
MongoDB merupakan salah satu jenis database NoSQL yang cukup populer digunakan dalam pengembangan website. Berbeda dengan database jenis SQL yang menyimpan data menggunakan relasi tabel, MongoDB menggunakan dokumen dengan format JSON. 
NoSQL adalah singkatan dari Not Only SQL. Database management system ini bersifat tanpa relasi (non-relational). Artinya, NoSQL bisa mengelola database dengan skema yang fleksibel dan tidak membutuhkan query yang kompleks. 
Komponen MongoDB :
- Database – merupakan wadah dengan struktur penyimpanan yang disebut collection. 
- Collection – merupakan tempat kumpulan informasi data yang berbentuk dokumen. Collection dipadankan seperti tabel-tabel yang berisi data pada database SQL.  
- Document – merupakan satuan unit terkecil dalam MongoDB.  

Keunggulan MongoDB :
- Performa Lebih Cepat 
- Pengelolaan Database Lebih Mudah
- Mampu Menampung Banyak Data yang Bervariasi
- Bisa Mengelola Query Lebih Baik
- Memiliki Kemampuan Skalabilitas Sesuai Kebutuhan
- Dapat Memperbarui Skema Data Tanpa Downtime
- Bisa Digunakan Secara Gratis 

Kekurangan 
- Memakan banyak memori
- Konsistensi data 
- Hanya bisa menampung 16MB setiap dokumen 

# Mongoose 
Mongoose adalah sebuah module pada NodeJS yang di install menggunakan npm, berfungsi sebagai penghubung antara NodeJS dan database nosql MongoDB.
Mongoose menyediakan feature diantaranya, model data application berbasis Schema. Dan juga termasuk built-in type casting, validation, query building, business logic hooks dan masih banyak lagi yang menjadi ke andalan mongoose.

Penggunaan Mongoose 
- install dengan npm 
`` npm install mongoose `` 
- membuat koneksi 
``` 
const mongoose = require('mongoose');
main().catch(err => console.log(err));
async function main() {
  await mongoose.connect('mongodb://localhost:27017/test');
  // use `await mongoose.connect('mongodb://user:password@localhost:27017/test');` if your database has auth enabled
}
```

# Docker 
Docker adalah software open-source yang digunakan untuk meluncurkan (deploy) aplikasi di dalam container virtual. Dengan container virtual ini (containerization), aplikasi bisa dijalankan secara terisolasi di environment yang kompleks sehingga tidak menimbulkan masalah pada environment lainnya. 
Menggunakan Docker memungkinkan pengembang mengirimkan kode lebih cepat, menstandardisasi operasi aplikasi, memindahkan kode dengan lancar, dan menghemat uang dengan meningkatkan pemanfaatan sumber daya. Dengan Docker, pengembang mendapatkan satu objek yang dapat dijalankan di mana saja. Sintaks Docker yang sederhana dan lugas memberi kontrol penuh. Adopsi yang luas berarti ada ekosistem alat yang kuat dan aplikasi off-the-shelf yang siap digunakan dengan Docker.








