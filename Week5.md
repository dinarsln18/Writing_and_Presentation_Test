# Writing and Presentation Test Week 4

## RESPONSIVE WEB DESIGN 
Responsive Web Design (RWD) bertujuan untuk membuat desain website kita dapat diakses dalam device apapun. Dalam membuat aplikasi kitabharus memikirkan user yang akan menggunakannya. Device yang umunya digunakan adalah laptop/PC, smartphone, dan tablet. 

### Setting up Chrome Dev Tools
Tools bawaan dari setiap browser yang digunakan developer untuk memudahkan proses development website. Pada browser chrome biasa disebut dengan Chrome Dev Tools. 

- Akses Chrome Dev Tools 
Kita bisa menggunakan shortcut ini untuk membuka browser chrome 
``` 
Windows:
Ctrl + Shift + J
```

### Add viewport in HTML 
```
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

```
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```

### Use Max-width element 
Use max-width digunakan untuk membuat gambar sesuai dengan device yang kita gunakan agar gambar bisa menyesuaikan dan tidak terpotong jika ukuran web browser diperkecil.
dengan menggunakan 
```
<img style="max-width:100%;" src="images/nature.jpg" alt="image"> 
```

### Media Query 
Media query digunakan untuk membuat beberapa styles tergantung pada jenis device. 
Jenis media query 
- Media query untuk respomsive web design umumnya hanya menggunakan 2 jenis media query 
- Keduanya yaitu min width dan max width 

``` 
@media screen and (min-width: your pixel) {
    /*your tag element html and your css */
}

@media screen and (max-width: your pixel) {
    /*your tag element html and your css */
}
```

### Complete Breakpoint Media Query 
Digunakan ketika kita ingin membuat tampilan yang ingin diterapkan pada range ukuran device tertentu. 
Tidak ada aturan baku berapa besaran width dan berapa banyak breakpoint yang harus dilakukan. Responsive web design dilakukan sesuai kebutuhan konten kita. Jika konten yang ditampilkan sudah tidak bisa diakses atau sulit dilihat pada width tertentu, sudah saatnya kamu menggunakan media query. 

## BOOTSTRAP 
Bootstrap digunakan untuk kalian yang ingin membuat website responsive dengan berbagai macam desain yang sudah ada. Desain bootstrap bisa didapatkan pada link bootrstrap di ``https://getbootstrap.com/``



