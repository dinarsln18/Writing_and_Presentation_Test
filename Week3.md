<<<<<<< HEAD
# Writing and Presentation Test Week3
## Javascript Intermediate - Arrray
Array  adalah tipe data list order yang dapat menyimpan tipe data apapun di dalamnya. Array dapat menyimpan tipe data string, number, boolean dan lainnya. 
Contoh array yang menyimpan banyak tipe data :
```
let randomData = ['ini string', 20, true];
console.log(randomData[1]); 
```
Membuat Array : array didefinisikan menggunakan square braskets ([])
Memanggil array : array pada javascript dihitung dari index data ke-0. Data pertama adalah index ke-0. 
Update array, contoh :
``` 
let productTeam = ['Product Manager', 'Front end developer', 'Back end developer'];

productTeam[0] = 'Product Designer';
console.log(productTeam);
Output : ['Product Designer', 'Front end developer', 'Back end developer'];
yang artinya index array ke -0 diganti dengan ('Product Designer')
```

## Const in array
Jika menggunakan let, kita dapat mengubah array dengan array baru dan konten nilai yang ada di dalam array dengan nilai lain, seangkan const tidak bisa melakukan uodate data. Namun pada array kita dapat melakukan update konten nilai di dalam array (mutable). Yang tidak bisa adalah mengubah array dengan array yang baru jika menggunakan const.
Conroh :
``` 
const cars = ['tesla', 'honda', 'toyota'];
cars = ['nisan'];
console.log(cars);
// Output : Error. Tidak bisa update array baru
```
Yang benar adalah :
```
const cars = ['tesla', 'honda', 'toyota'];
cars[2] = ['nissan'];
console.log(cars);
// Output : 'tesla', 'honda', 'nissan'
```

## Array properties 
Array memiliki 5 properti yang sering digunakan yaitu **constructor, length, index, input, dan prototype**. Properties adalah fitur yang sudah disediakan oleh Javascript untuk memudahkan developer. 
- Array .length akan mengembalikan nilai dari jumlah panjang data suatu array. 
``` 
let productTeam = ['Product Manager', 'Front end developer', 'Back end developer'];
console.log(productTeam.length);
// Output : 3
```

## Array method
Arraya memiliki method atau biasa disebut built-in methods. kita tidak perlu membuat function lagi jika method yang kita butuhkan sudah tersedia. Contoh array built-in methods :
- .push() method untuk menambahkan item array pada urutan yang paling akhir
- .pop() method untuk menghapus item array index terakhir
- .shift() method untuk menghapus item array pada index pertama
- .unshift() method untuk menambahkan item array pada index pertama
- .sort() method untuk mengurutkan secara ascending atau descending alphanumeric

## Looping pada array 
Array memiliki built-in method untuk melakukan looping yaitu **.map()** dan **forEach()**. 
- .forEach() method untuk melakukan looping pada setiap elemen array. 
```
const cars = ['tesla', 'honda', 'toyota'];
cars.forEach(element => {
console.log(element);
});
// Output : 'tesla', 'honda', 'toyota'
```

- .map() melakukan perulangan/looping dengan membuat array baru.
``` 
let arr = [1, 2, 3, 4, 5];

let doubled = arr.map(num => {
return num * 2;
});
console.log(doubled);
// Output : [2, 4, 6, 8, 10]
``` 
Kita bisa lihat bahwa **.map()** dan **forEach()** sama-sama melakukan looping dan mengembalikan nilai baru dari operasi yang dilakukan. Perbedaannya adalah .forEach tidak dapat membuat Array baru dari hasil operasi yang ada dalam looping. Lalu dari segi performance juga sangat jauh. Jadi, gunakan .forEach() jika hanya memerlukan looping untuk menampilkan saja atau menyimpan ke database, dan gunakan .map() jika akan melakukan operasi pada array seperti yang dapat mengubah nilai array sebelumnya.

## Multidimensional Array 
Multidimensional Array bisa dianalogikan dengan array of array, jadi ada array didalam array.
``` 
let inventory = [
    ['kaos polos', 10],
    ['jaket hoodie', 12],
    ['topi', 24],
    ['celana jeans', 8],
];
console.log(inventory);

// Output :
(4) [Array(2), Array(2), Array(2), Array(2),]
- 0: (2) ["kaos polos", 10]
- 1: (2) ["jaket hoodie", 12]
- 2: (2) ["topi", 24]
- 3: (2) ["celana jeans", 8]
    length: 4
```

- Akses index multidimensional array. 
```
let inventory = [
    ['kaos polos', 10],
    ['jaket hoodie', 12],
    ['topi', 24],
    ['celana jeans', 8],
];
console.log(inventory[1][0]);
// Output : jaket hoodie
```

Sama seperti array satu dimensi. multidimensional array juga dapat menggunakan property dan method built-in. 

- Operation using map in multidimensional array 
- Looping for multidimensional array 

## Javascript intermediate - Object 
Apa itu object? Entah itu benda mati atau benda hidup. Semuanya adalah object. Object didunia nyata dapat kita modelkan didalam programming. Jadi pada programming, object adalah sebuah tipe data pada variabel yang menyimpan properti dan fungsi (method). Properti adalah data lengkap dari sebuah object. Method adalah action dari sebuah object. Apa saja yang dapat dilakukan dari suatu object. 

- membuat object : Sama seperti array, didalam object kita dapat menyimpan properti dengan tipe data apapun.

``` 
let person = {
    name: 'John Doe',
    age: 25,
    isVerified: true,
}
```

- mengakses object dan property object
```
let person = {
    name: 'John Doe',
    age: 25,
    isVerified: true,
} 
// memanggil variable nme to access object
console.log(person);
```
- Bracket notation : kita juga bisa menggunakan bracket notation saat memanggil properti
- update object : Object dapat mengupdate value dari key yang sudah tersedia, dan object dapat menambahkan key dan value baru. jika membutuhkan untuk update seluruh data object gunakan ‘let’ pada saat deklarasi variabel.
- delete object : dapat menghapus properti dari object menggunakan delete operator
- Method : value yang kita masukkan pada property berupa function itu disebut method. 
- Nested object : Object yang berasal dari turunan object lainnya.
- Pass by reference : mengubah data yang ada pada object melalui sebuah function dan memasukkan object sebagai parameter function.
- Looping object : menampilkan seluruh object properti.
- Array of object : dapat menggunakan array of object untuk data yang lebih dari satu.

## Javascript - Recursive 
Recursive adalah function yang memanggil dirinya sendiri sampai kondisi tertentu.
``` 
function recursive() {
    if(codition) {
        // stop calling itself
        // ...
    } else {
        recursive();
    }
}
```

Fungsi rekursif selalu memiliki kondisi yang menyatakan kapan fungsi tersebut berhenti. Kondisi ini harus dapat dibuktikan akan tercapai, karena jika tidak tercapai maka kita tidak dapat membuktikan bahwa fungsi akan berhenti, yang berarti algoritma kita tidak benar. Fungsi rekursif selalu memanggil dirinya sendiri sambil mengurangi atau memecahkan data masukan setiap panggilannya. Hal ini penting diingat, karena tujuan utama dari rekursif ialah memecahkan masalah dengan mengurangi masalah tersebut menjadi masalah-masalah kecil.


## Web Storage 
Web storage adalah salah satu Web API yang dapat menyimpan data secara lokal pada sisi client. Berbeda dengan objek atau array, data yang disimpan pada objek atau array JavaScript bersifat sementara, dan akan hilang jika terjadi reload atau pergantian URL pada browser. Sedangkan data yang disimpan pada Web Storage akan bertahan lebih lama karena data akan disimpan pada storage browser. 
Data yang disimpan web storage tersedia berdasarkan domain. Artinya, data pada suatu domain web hanya dapat diakses oleh domainnya itu sendiri. Web storage dapat menampung sebesar 10MB untuk satu domain. Ada 2 tipe web store, localstorage dan sessionstorage.

## Javascript - Asynchronous 
Javascript adalah bahasa pemrograman single-thread yang artinya hanya dapat mengeksekusi satu task pada satu waktu atau biasa disebut synchronous. Pada konsep pemrograman (web development pada case kita) dikenal istilah Asynchronous. Asynchronous mengizinkan komputer memproses task yang lain sambil menunggu proses yang masih berlangsung. Karena javascript sifatnya synchronous maka kita bisa membuatnya asynchronous secara simulasi, artinya tidak murni asynchronous bisa menggunakan beberapa cara :
1. Callback
2. Promises
3. Async/await 

### 1. Callback 
Callback function adalah function yang kita letakan di dalam argumen/parameter pada function, dan function tersebut akan dieksekusi setelah function pertama menyelesaikan tugasnya.
``` 
const mainFunc = (number1, number2, callBack) => {
    console.log(number1 + number2)
    callBack()
}

const myCallback =() => {
    console.log('Done!')
}

main(1,2,myCallback) // Output 3 Done!
```

Proses asynchronous identik dengan delay, dimana hasil dari proses tersebut membutuhkan selang waktu tertentu untuk menghasilkan output. 

``` 
function p1() {
    console.log('p1 selesai dijalankan')
};
function p2() {
    console.log('p2 selesai dijalankan')
};
function p3() {
    console.log('p3 selesai dijalankan')
};

p1();
p2();
p3();

// Output :
p1 selesai dijalankan 
p2 selesai dijalankan 
p3 selesai dijalankan 
```

- setTimeout digunakan untuk simulasi asynchronous. Karena sebenarnya kita tidak bisa membuat proses asynchronous murni.

### Promises 
Promise adalah salah satu fitur baru di ES6, biasa digunakan untuk melakukan http request/fetch data dari API.
alam pengambilan data, promise memiliki 3 kemungkinan state.
1. Pending(sedang dalam proses)
2. Fulfilled (berhasil)
3. Rejected (gagal)

``` 
const contohPromise = () => {
    new Promise((resolve, reject) => {
        let condition = true;
        if(condition){
            resolve(''request fullfield')
        } else {
            reject(new Error('terjadi kesalahan, reject'))
        }
    }).then(result => concole.log(result))
      .catch(error => console.log(error))
}
contohPromis()
```
### Async-Await 
Async - await adalah salah satu fitur baru dari javascript yang digunakan untuk menangani hasil dari sebuah Promise. Sedangkan await berfungsi untuk menunda sebuah kode dijalankan sampai proses asynchronous berhasil.
``` 
async function hello(){
    let result = await 'Hellooo'
    return result
}
// es6 
const hello1 = async () => {
    let result = await 'Helloo'
    return result 
}
```

### HTTP Request fetch()
Fetch adalah native web API untuk melakukan HTTP calls dari external network.

``` 
const getDataAPI = () => {
    // deklarasi API endpoint
    const API = "https://5.e984............";
    // buat option method untuk fetch()
    const option = {
        method: "GET"
    }
    // jalankan fetch dengan api dan option yang kita buat 
    fetch(API, option)
    // response pertama, kita ambil data json
    .then(response => response.json())
    .then(result => console.log(result))
    // jika terjadi kesalahan, kita tangkap errornya 
    .catch(error => console.log(error, "ERROR"))
}
``` 
```
const getDataAPIwithAsync = async() => {
    const API = "https://35547jdhuf...........";
    const option = {
        method: "GET"
    }
    let response = await fetch(API, option)
    response = await response.json()
    console.log(response);
}
getDataAPIwithAsync()
```
=======
# Writing and Presentation Test Week3
## Javascript Intermediate - Arrray
Array  adalah tipe data list order yang dapat menyimpan tipe data apapun di dalamnya. Array dapat menyimpan tipe data string, number, boolean dan lainnya. 
Contoh array yang menyimpan banyak tipe data :
```
let randomData = ['ini string', 20, true];
console.log(randomData[1]); 
```
Membuat Array : array didefinisikan menggunakan square braskets ([])
Memanggil array : array pada javascript dihitung dari index data ke-0. Data pertama adalah index ke-0. 
Update array, contoh :
``` 
let productTeam = ['Product Manager', 'Front end developer', 'Back end developer'];

productTeam[0] = 'Product Designer';
console.log(productTeam);
Output : ['Product Designer', 'Front end developer', 'Back end developer'];
yang artinya index array ke -0 diganti dengan ('Product Designer')
```

## Const in array
Jika menggunakan let, kita dapat mengubah array dengan array baru dan konten nilai yang ada di dalam array dengan nilai lain, seangkan const tidak bisa melakukan uodate data. Namun pada array kita dapat melakukan update konten nilai di dalam array (mutable). Yang tidak bisa adalah mengubah array dengan array yang baru jika menggunakan const.
Conroh :
``` 
const cars = ['tesla', 'honda', 'toyota'];
cars = ['nisan'];
console.log(cars);
// Output : Error. Tidak bisa update array baru
```
Yang benar adalah :
```
const cars = ['tesla', 'honda', 'toyota'];
cars[2] = ['nissan'];
console.log(cars);
// Output : 'tesla', 'honda', 'nissan'
```

## Array properties 
Array memiliki 5 properti yang sering digunakan yaitu **constructor, length, index, input, dan prototype**. Properties adalah fitur yang sudah disediakan oleh Javascript untuk memudahkan developer. 
- Array .length akan mengembalikan nilai dari jumlah panjang data suatu array. 
``` 
let productTeam = ['Product Manager', 'Front end developer', 'Back end developer'];
console.log(productTeam.length);
// Output : 3
```

## Array method
Arraya memiliki method atau biasa disebut built-in methods. kita tidak perlu membuat function lagi jika method yang kita butuhkan sudah tersedia. Contoh array built-in methods :
- .push() method untuk menambahkan item array pada urutan yang paling akhir
- .pop() method untuk menghapus item array index terakhir
- .shift() method untuk menghapus item array pada index pertama
- .unshift() method untuk menambahkan item array pada index pertama
- .sort() method untuk mengurutkan secara ascending atau descending alphanumeric

## Looping pada array 
Array memiliki built-in method untuk melakukan looping yaitu **.map()** dan **forEach()**. 
- .forEach() method untuk melakukan looping pada setiap elemen array. 
```
const cars = ['tesla', 'honda', 'toyota'];
cars.forEach(element => {
console.log(element);
});
// Output : 'tesla', 'honda', 'toyota'
```

- .map() melakukan perulangan/looping dengan membuat array baru.
``` 
let arr = [1, 2, 3, 4, 5];

let doubled = arr.map(num => {
return num * 2;
});
console.log(doubled);
// Output : [2, 4, 6, 8, 10]
``` 
Kita bisa lihat bahwa **.map()** dan **forEach()** sama-sama melakukan looping dan mengembalikan nilai baru dari operasi yang dilakukan. Perbedaannya adalah .forEach tidak dapat membuat Array baru dari hasil operasi yang ada dalam looping. Lalu dari segi performance juga sangat jauh. Jadi, gunakan .forEach() jika hanya memerlukan looping untuk menampilkan saja atau menyimpan ke database, dan gunakan .map() jika akan melakukan operasi pada array seperti yang dapat mengubah nilai array sebelumnya.

## Multidimensional Array 
Multidimensional Array bisa dianalogikan dengan array of array, jadi ada array didalam array.
``` 
let inventory = [
    ['kaos polos', 10],
    ['jaket hoodie', 12],
    ['topi', 24],
    ['celana jeans', 8],
];
console.log(inventory);

// Output :
(4) [Array(2), Array(2), Array(2), Array(2),]
- 0: (2) ["kaos polos", 10]
- 1: (2) ["jaket hoodie", 12]
- 2: (2) ["topi", 24]
- 3: (2) ["celana jeans", 8]
    length: 4
```

- Akses index multidimensional array. 
```
let inventory = [
    ['kaos polos', 10],
    ['jaket hoodie', 12],
    ['topi', 24],
    ['celana jeans', 8],
];
console.log(inventory[1][0]);
// Output : jaket hoodie
```

Sama seperti array satu dimensi. multidimensional array juga dapat menggunakan property dan method built-in. 

- Operation using map in multidimensional array 
- Looping for multidimensional array 

## Javascript intermediate - Object 
Apa itu object? Entah itu benda mati atau benda hidup. Semuanya adalah object. Object didunia nyata dapat kita modelkan didalam programming. Jadi pada programming, object adalah sebuah tipe data pada variabel yang menyimpan properti dan fungsi (method). Properti adalah data lengkap dari sebuah object. Method adalah action dari sebuah object. Apa saja yang dapat dilakukan dari suatu object. 

- membuat object : Sama seperti array, didalam object kita dapat menyimpan properti dengan tipe data apapun.

``` 
let person = {
    name: 'John Doe',
    age: 25,
    isVerified: true,
}
```

- mengakses object dan property object
```
let person = {
    name: 'John Doe',
    age: 25,
    isVerified: true,
} 
// memanggil variable nme to access object
console.log(person);
```
- Bracket notation : kita juga bisa menggunakan bracket notation saat memanggil properti
- update object : Object dapat mengupdate value dari key yang sudah tersedia, dan object dapat menambahkan key dan value baru. jika membutuhkan untuk update seluruh data object gunakan ‘let’ pada saat deklarasi variabel.
- delete object : dapat menghapus properti dari object menggunakan delete operator
- Method : value yang kita masukkan pada property berupa function itu disebut method. 
- Nested object : Object yang berasal dari turunan object lainnya.
- Pass by reference : mengubah data yang ada pada object melalui sebuah function dan memasukkan object sebagai parameter function.
- Looping object : menampilkan seluruh object properti.
- Array of object : dapat menggunakan array of object untuk data yang lebih dari satu.

## Javascript - Recursive 
Recursive adalah function yang memanggil dirinya sendiri sampai kondisi tertentu.
``` 
function recursive() {
    if(codition) {
        // stop calling itself
        // ...
    } else {
        recursive();
    }
}
```

Fungsi rekursif selalu memiliki kondisi yang menyatakan kapan fungsi tersebut berhenti. Kondisi ini harus dapat dibuktikan akan tercapai, karena jika tidak tercapai maka kita tidak dapat membuktikan bahwa fungsi akan berhenti, yang berarti algoritma kita tidak benar. Fungsi rekursif selalu memanggil dirinya sendiri sambil mengurangi atau memecahkan data masukan setiap panggilannya. Hal ini penting diingat, karena tujuan utama dari rekursif ialah memecahkan masalah dengan mengurangi masalah tersebut menjadi masalah-masalah kecil.


## Web Storage 
Web storage adalah salah satu Web API yang dapat menyimpan data secara lokal pada sisi client. Berbeda dengan objek atau array, data yang disimpan pada objek atau array JavaScript bersifat sementara, dan akan hilang jika terjadi reload atau pergantian URL pada browser. Sedangkan data yang disimpan pada Web Storage akan bertahan lebih lama karena data akan disimpan pada storage browser. 
Data yang disimpan web storage tersedia berdasarkan domain. Artinya, data pada suatu domain web hanya dapat diakses oleh domainnya itu sendiri. Web storage dapat menampung sebesar 10MB untuk satu domain. Ada 2 tipe web store, localstorage dan sessionstorage.

## Javascript - Asynchronous 
Javascript adalah bahasa pemrograman single-thread yang artinya hanya dapat mengeksekusi satu task pada satu waktu atau biasa disebut synchronous. Pada konsep pemrograman (web development pada case kita) dikenal istilah Asynchronous. Asynchronous mengizinkan komputer memproses task yang lain sambil menunggu proses yang masih berlangsung. Karena javascript sifatnya synchronous maka kita bisa membuatnya asynchronous secara simulasi, artinya tidak murni asynchronous bisa menggunakan beberapa cara :
1. Callback
2. Promises
3. Async/await 

### 1. Callback 
Callback function adalah function yang kita letakan di dalam argumen/parameter pada function, dan function tersebut akan dieksekusi setelah function pertama menyelesaikan tugasnya.
``` 
const mainFunc = (number1, number2, callBack) => {
    console.log(number1 + number2)
    callBack()
}

const myCallback =() => {
    console.log('Done!')
}

main(1,2,myCallback) // Output 3 Done!
```

Proses asynchronous identik dengan delay, dimana hasil dari proses tersebut membutuhkan selang waktu tertentu untuk menghasilkan output. 

``` 
function p1() {
    console.log('p1 selesai dijalankan')
};
function p2() {
    console.log('p2 selesai dijalankan')
};
function p3() {
    console.log('p3 selesai dijalankan')
};

p1();
p2();
p3();

// Output :
p1 selesai dijalankan 
p2 selesai dijalankan 
p3 selesai dijalankan 
```

- setTimeout digunakan untuk simulasi asynchronous. Karena sebenarnya kita tidak bisa membuat proses asynchronous murni.

### Promises 
Promise adalah salah satu fitur baru di ES6, biasa digunakan untuk melakukan http request/fetch data dari API.
alam pengambilan data, promise memiliki 3 kemungkinan state.
1. Pending(sedang dalam proses)
2. Fulfilled (berhasil)
3. Rejected (gagal)

``` 
const contohPromise = () => {
    new Promise((resolve, reject) => {
        let condition = true;
        if(condition){
            resolve(''request fullfield')
        } else {
            reject(new Error('terjadi kesalahan, reject'))
        }
    }).then(result => concole.log(result))
      .catch(error => console.log(error))
}
contohPromis()
```
### Async-Await 
Async - await adalah salah satu fitur baru dari javascript yang digunakan untuk menangani hasil dari sebuah Promise. Sedangkan await berfungsi untuk menunda sebuah kode dijalankan sampai proses asynchronous berhasil.
``` 
async function hello(){
    let result = await 'Hellooo'
    return result
}
// es6 
const hello1 = async () => {
    let result = await 'Helloo'
    return result 
}
```

### HTTP Request fetch()
Fetch adalah native web API untuk melakukan HTTP calls dari external network.

``` 
const getDataAPI = () => {
    // deklarasi API endpoint
    const API = "https://5.e984............";
    // buat option method untuk fetch()
    const option = {
        method: "GET"
    }
    // jalankan fetch dengan api dan option yang kita buat 
    fetch(API, option)
    // response pertama, kita ambil data json
    .then(response => response.json())
    .then(result => console.log(result))
    // jika terjadi kesalahan, kita tangkap errornya 
    .catch(error => console.log(error, "ERROR"))
}
``` 
```
const getDataAPIwithAsync = async() => {
    const API = "https://35547jdhuf...........";
    const option = {
        method: "GET"
    }
    let response = await fetch(API, option)
    response = await response.json()
    console.log(response);
}
getDataAPIwithAsync()
```
>>>>>>> 19f23b7 (week4)
