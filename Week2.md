## Scope and Function 
Scope adalah konsep dalam flow data variabel. Scope ada 2 jenis, yaitu
- Global scope : variabel yang kita buat dapat diakses dimanapun dalam suatu file 
contoh global scope 
``` 
let myName = "dinros"
function greeting() {
  return myName;
}
console.log(myName)
```
- Local scope : mendeklarasikan variabel didalam block seperti function, conditional, dan looping 

Function merupakan sebuah blok kode dalam sebuah grup untuk menyelesaikan 1 task/ 1 fitur.
- Membuat function 
```
function greeting() {
  return 'Hello World';
};
```

- Memanggil function 
```
greeting()
console.log(greeting());
```

## Parameter dan Argumen 
- Parameter berguna untuk menerima sebuah inputan data yang digunakan untuk melakukan task
contoh parameter :
```
function pertambahan(a, b) {
   return a + b;
}
```
- Argumen adalah nilai yang digunakan saat memanggil function.
contoh argumen :
```
function pertambahan(a, b) {
   return a + b;
}
console.log(pertambahan(8, 9)) (ini output) 
```

- Default parameter digunakan untuk memberikan nilai awal/default pada parameter function.
contoh 
``` function Film(name = 'Strong Woman') {
  return "Sedang menonton" + name;
}
console.log(Film(' Descendants of The Sun '))
console.log());
```

- Function helper : menggunakan function yang sudah dibuat pada function lain
- Arrow function adalah cara menuliskan function.

## DOM 
DOM merupakan cara memanipulasi tampilan website agar lebih menarik 
Cara memanggil DOM :
- Berdasarkan ID 
`` console.log(document.getElementByID("#header))``
- Berdasarkan class name :
`` console.log(document.getElementByClassName("backgrund-color-yellow"))``
= Berdasarkan query selector :
``console.log(document.querySelector("#header "))``
``console.log(document.querySelector(".backgrund-color-yellow"))``

Membuat element HTML
Contoh :
```
<div id ="header"></div>

//untuk membuat sebuah elemnt heading
const heading = dosument.createElement("h1)
heading.textContent = "Ini Heading"

document.getElemntByID("header").appendChild(heading)
```
#### DOM events 
- Click
- Change 
- Hover 
- Focus 
- Scroll
- Blur 
- Submit 

##### Menangkap Interaksi User
- Element.addEventListener("event")
- Element.onevent

##### EventListener
Dengan cara Element.addEventListener("event") :
- Bisa dihilangkan 
- Bisa ada beberapa event listener yang sama untuk 1 element
- Memiliki argument tambahan {option} 

##### Jenis eventListener
**EventListener - Click** : menampilkan pop up box yang berisi teks di dalam input yang telah kita inputkan sebelumnya.
EventListener - Click ``<input id="user-input"/>`` ``<button id="alert-button">show</button>`` 
Memanggil element berdasarkan id ``const input = document.getElementById("user-input"`` ``const button = dosument.getElementById("alert-button")``
```
button.addEventListener(“click”, function() {
	alert(input.value)
})
```
atau 
```
button.onclick = function() { alert(input.value) }
```
**EventListener - Blur** : event dimana sebuah element kehilangan fokus dari user. 
Misalkan saat ingin memvalidasi isi dari ``<input id = "username" />`` agar panjangnya minimal 6 karakter
``const input = document.getElementById("username")`` 
```
input.addEventListener(“blur”, () => {
	if(input.value.length < 6) alert(“Panjang username minimal 6”)
})
```
**EventListener - Form Submission** : mendapatkan isi dari beberapa input dalam sebuah form. 
Misalkan terdapat beberapa input dalam sebuah form ``<input name="email"/>`` dan ``<input type="password" name="password"/>``
Untuk mendapatkan isi dari kedua inputan tersebut terdapat 2 cara :
1. Memasang event listener di kedua input dan tombol submit, lalu saat tombol diklik, baca value dari kedua input tersebut
1. Memasang event listener di form, lalu gunakan FormData untuk menggambil data dari masing-masing input
```
const form = document.getElementById(“form”)

form.addEventListener(“submit”, function(event) {
	// cegah page refresh
	event.preventDefault()

	const formData = new FormData(form)
	const values = Object.fromEntries(formData) // { email: ... }
})
```
