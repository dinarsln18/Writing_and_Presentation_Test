# Writing Test Week 1
# Web Server & Restful API 
Web server adalah sebuah software (perangkat lunak) yang memberikan layanan berupa data. Berfungsi untuk menerima permintaan HTTP atau HTTPS dari klien atau kita kenal dengan web browser (Chrome, Firefox). Selanjutnya ia akan mengirimkan respon atas permintaan tersebut kepada client dalam bentuk halaman web. Web server juga menggunakan SMTP (Simple Mail Transfer Protocol) dan FTP (File Transfer Protocol) dalam memproses file untuk email atau penyimpanan.
### Hardware 
Di sisi perangkat keras, server web adalah komputer yang menyimpan perangkat lunak server web dan file komponen situs web. (misalnya, dokumen HTML, gambar, lembar gaya CSS, dan file JavaScript) Server web terhubung ke Internet dan mendukung pertukaran data fisik dengan perangkat lain yang terhubung ke web.

### Software 
Di sisi perangkat lunak, server web menyertakan beberapa bagian yang mengontrol cara pengguna web mengakses file yang dihosting. Minimal, ini adalah server HTTP. Server HTTP adalah perangkat lunak yang memahami URL (alamat web) dan HTTP (protokol yang digunakan browser Anda untuk melihat halaman web). Server HTTP dapat diakses melalui nama domain dari situs web yang disimpannya, dan mengirimkan konten dari situs web yang dihosting ini ke perangkat pengguna akhir.

### Static web server 
Server web statis, atau tumpukan, terdiri dari komputer (perangkat keras) dengan server HTTP (perangkat lunak). Kami menyebutnya "statis" karena server mengirimkan file yang dihosting apa adanya ke browser Anda.

### Dynamic web server 
Server web dinamis terdiri dari server web statis ditambah perangkat lunak tambahan, paling sering server aplikasi dan database. Kami menyebutnya "dinamis" karena server aplikasi memperbarui file yang dihosting sebelum mengirim konten ke browser Anda melalui server HTTP

### Static sites 
Diagram pada slide berikutnya menunjukkan arsitektur server web dasar untuk situs statis (situs statis adalah situs yang mengembalikan konten berkode keras yang sama dari server setiap kali sumber daya tertentu diminta). Saat pengguna ingin menavigasi ke suatu halaman, browser mengirimkan permintaan "GET" HTTP yang menentukan URL-nya.

### Dynamic sites 
Situs web dinamis adalah salah satu tempat beberapa konten respons dihasilkan secara dinamis, hanya jika diperlukan. Di situs web dinamis, halaman HTML biasanya dibuat dengan memasukkan data dari database ke placeholder dalam template HTML (ini adalah cara yang jauh lebih efisien untuk menyimpan konten dalam jumlah besar daripada menggunakan situs web statis).

### Rest 
REST, atau REpresentational State Transfer, adalah gaya arsitektur untuk menyediakan standar antar sistem komputer di web, sehingga memudahkan sistem untuk berkomunikasi satu sama lain.


Sistem yang sesuai dengan REST, sering disebut sistem RESTful, dicirikan oleh bagaimana mereka tidak memiliki kewarganegaraan dan memisahkan urusan klien dan server

# Design Database with MySQL
MySQL adalah sebuah database management system (manajemen basis data) menggunakan perintah dasar SQL (Structured Query Language) yang cukup terkenal. Database management system (DBMS) MySQL multi pengguna dan multi alur ini sudah dipakai lebih dari 6 juta pengguna di seluruh dunia.

### Kelebihan MySQL 
- Mendukung Integrasi Dengan Bahasa Pemrograman Lain.
- Tidak Membutuhkan RAM Besar.
- Mendukung Multi User.
- Bersifat Open Source
- Tipe Data yang Bervariasi.

### Kekurangan 
- Kurang Cocok untuk Aplikasi Game dan Mobile
- Sulit Mengelola Database yang Besar
- Technical Support yang Kurang Bagus

Langkah - langkah design database 
- Menentukan Entity 
- Menentukan attributes 
- Menentukan Relasi


# Intro & Essential Node JS
### Node JS
Node.js adalah runtime environment lintas platform single-thread yang dibangun berdasarkan engine JavaScript V8 Chrome. Pembuatan aplikasi dengan Node JS dilakukan melalui virtual private server.
Pada arsitekturnya yang asinkron, event loop beroperasi setiap kali peristiwa tertentu terjadi (event-driven). Setelah diterima dari panggilan API sebelumnya, respons akan dimasukkan ke dalam antrean event.
Event loop akan menyelesaikan semua permintaan sebelumnya dan permintaan saat ini sebelum menjalankan fungsi callback untuk mengirimkan respons dari server ke klien.
Karena menggunakan event loop single-thread, Node.js mampu menangani banyak permintaan secara bersamaan dengan waktu eksekusi yang lebih cepat, dan menggunakan resource yang lebih sedikit.
Sebagai perbandingan, software arsitektur sinkron melakukan satu tugas pada satu waktu. Oleh karena itu, event loop biasanya hanya akan pindah ke tugas berikutnya kalau yang sebelumnya sudah selesai.

### Express JS
Express.js adalah framework web app untuk Node.js yang ditulis dengan bahasa pemrograman JavaScript. Framework open source ini dibuat oleh TJ Holowaychuk pada tahun 2010 lalu.
Express.js adalah framework back end. Artinya, ia bertanggung jawab untuk mengatur fungsionalitas website, seperti pengelolaan routing dan session, permintaan HTTP, penanganan error, serta pertukaran data di server. 

### Kelebihan 
- Bebas menentukan sendiri arsitektur dan struktur website yang akan dikembangkan
- Ukuran framework lebih kecil dan ringan, karena hanya berisi package inti
- Kinerja website yang dihasilkan jadi lebih baik, mengingat ringannya framework

### Kekurangan 
- Diperlukan keahlian khusus untuk membuat, mengelola, dan merawat arsitektur website
- Terlalu banyak pilihan plugin dan library untuk digunakan, bisa membingungkan bagi sebagian orang
- Pilihan metode pengembangan yang berbeda-beda, sehingga kurang cocok untuk pemula

### Back End Web Application
Back end app adalah aplikasi yang berjalan di server-side yang bekerja untuk memberikan informasi berupa data sesuai request dari client / browser / front end app. Umumnya server-side app membuat REST API.
Kelebihan dari framework ini terletak pada fitur caching, support dengan Google V8 Engine, JavaScript, serta didukung oleh komunitas dan skalabilitas aplikasi yang baik.


### Middleware 
Middleware function adalah sebuah fungsi yang memiliki akses ke object request (req), object response (res), dan sebuah fungsi next didalam request-response cycle.
Fungsi next biasanya di berikan nama variable next.

### Kemampuan Middleware 
- Menjalankan kode apapun.
- Memodifikasi Object Request dan Object Response.
- Menghentikan request-response cycle.
- Melanjutkan ke middleware function selanjutnya atau ke handler function dalam suatu request response cycle.

