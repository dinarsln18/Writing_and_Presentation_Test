# Writing and Presentation Test Week 5
Back-End Bootcamp

## **WEB SERVER & RESTFUL API** 
Web server adalah sebuah software atau perangkat lunak yang memberikan layanan berupa data. Berfungsi untuk menerima permintaan HTTP atau HTTPS dari klien. Kemudian ia akan mengirimkan respon atas permintaan tersebut kepada klien dalam bentuk halaman web. 

Web Server terdiri dari 2 komponen penting :
- Hardware 
- Software 

### Static VS Dynamic Web server 
- Static seb server terdiri dari komputer (perangkat keras) dengan server HTTP (perangkat lunak).  Disebut dinamis karena server mengirimkan file yang dihosting apa adanya ke browser Anda.
- Dynamic web server terdiri dari web server statis ditambah perangkat lunak tambahan.Disebut dinamis karena server aplikasi memperbarui file yang dihosting sebelum mengirim konten ke browser Anda melalui server HTTP. 

### REST 
- REST, atau Representational State Transfer, adalah gaya arsitektur untuk menyediakan standar antara sistem komputer di web, sehingga memudahkan sistem untuk berkomunikasi satu sama lain.
- Sistem yang sesuai dengan REST, sering disebut sistem RESTful, dicirikan oleh bagaimana mereka tidak memiliki kewarganegaraan dan memisahkan masalah klien dan server

### Komunikasi antara Klien dan Server 
HTTP Request 
- Get : mengambil data 
- Post : membuat data 
- Put : memperbaharui data 
- Delete : mengahpus data 

## **NODE JS** 
Merupakan platform javascript yang dapat berjalan di backend atau server-side, di komputer kita secara langsung. Node js bisa membuat CLT (Command Line Tool), Web App, Rest API. 
- Node Repl membuat kita bisa langsung menggunakan dan mengeksekusi kode javascript dengan menjalankan node di terminal. 
- Secara default, Node memiliki beberapa variabel global yang dapat diakses dan dimodifikasi, seperti global, process, dll. Biasanya variabel process.env sering digunakan untuk menyimpan configuration ataupun credentials yang sifatnya rahasia, yang bisa digunakan di dalam aplikasi.


NodeJS module 
- NPM atau (Node Package Manager) adalah package dan dependency manager utama pada NodeJS
- Dependency adalah suatu unsur metode untuk memisahkan dan mengintegrasikan berbagai program berbeda menjadi program yang utuh.

Javascript for NodeJS
- Arrow function expression : merupakan fitur terbaru dari javascript untuk mempermudah sintaks function menggunakan "=>"
- Asynchroous : mengeksekusi kode tanpa berurutan
- JSON : format yang digunakan untuk menyimpan dan mengirim data

Built in module NodeJS
- Console 
- Process 
- OS
- Util
- Events
- Errors
- Buffer 
- FS 
- Timers 

## **EXPRESS** 
Express merupakan kerangka aplikasi back-end untuk NodeJS. 
Back-end web application merupakan  aplikasi yang berjalan di server-side yang bekerja untuk memberikan informasi berupa data sesuai request dari client / browser / front end app. Umumnya server-side app membuat REST API

### REST API
RESTful API / REST API merupakan penerapan dari API (Application Programming Interface). Sedangkan REST (Representional State Transfer) adalah sebuah arsitektur metode komunikasi yang menggunakan protokol HTTP untuk pertukaran data dimana metode ini sering diterapkan dalam pengembangan aplikasi. Dengan tujuannya untuk menjadikan sistem memiliki performa yang baik, cepat dan mudah untuk di kembangkan (scale) terutama dalam pertukaran dan komunikasi data.
Restful API memiliki 4 komponen penting, yaitu 
- URL design 
- HTTP verbs
- HTTPS response code 
- FOrmat response 

### Basic Routes 
Routes adalah sebuah end point yang diapat kita akses menggunakan URL di website. Didalam routes kita perlu menentukan method API, alamat dan response apa saja yang akan dikeluarkan. Kita bisa menjalankan aplikasi sederhana kita dengan cara menggunakan “node”. Dan aplikasi kita akan berjalan di alamat ‘http://localhost:3000’
Kemudian kita dapat mengaksesnya di website dan menambah route yang akan kita akses yaitu “/”

Method :
- POST 
- PUT 
- PATCH
- DELETE

Response : Di dalam route kita dapat mengirim response menggunakan parameter dari route express.js yaitu “res.Send()” untuk mengirim plain text ketika kita mengakses route tersebut. 
Status Code : untuk mengetahui apakah route yang kita akses berjalan sebagaimana mestinya dan tidak terjadi error.
Query : Query merupakan parameter yang digunakan untuk membantu menentukan tindakan yang lebih spesifik daripada hanya sekedar router biasa.
Nested Route : digunakan ketika terdapat banyak route yang memiliki nama yang sama atau ingin membuat route yang lebih mendalam

## **MIDDLEWARE**
Middleware function adalah sebuah fungsi yang memiliki akses ke object request (req), object response (res), dan sebuah fungsi next didalam request-response cycle. Fungsi next biasanya di berikan nama variable next.
Middleware dapat melakukan :
- Menjalankan kode apapun 
- Memodifikasi object request dan object response 
- Menghentikan request response cycle 
- Melanjutkan ke middleware function selanjutnya atau ke handler function dalam suatu request response cycle.

Jenis Express Middleware 
Berdasarkan cara penggunaan dikelompokkan menjadi :
- Application Level Moddleware 
- Router Level Middleware 
- Error Handling Middleware

Berdasarkan source moddleware function dikelompokkan menjadi :
- Express build in middleware 
    1. express.static()
    2. express.json()
    3. express.urlencoded()
- Third party middleware
    Dikelola oleh express JS
    1. cors
    2. body-parser
    3. morgan
    4. multer
    
    Dikelola oleh komunitas :
    1. helmet
    2. passport
    3. espress-validator 
    4. swager-ui-express




