# ALL ABOUT CSS YOU MUST KNOW!

## Menyisipkan CSS di Dalam File HTML

- Inline CSS
```
<!DOCTYPE html>
<html>
  <head>
    <title>
      Website Pertamaku
    </title>
  </head>
  <body>
    <h1 style="color:blue;">Selamat Datang</h1>
  </body>
</html>
```

- Internal CSS
```
<!DOCTYPE html>
<html>
  <head>
    <title>Website Pertamaku</title>
    <style>
      body {
        background-color: yellow;
      }
      h1 {
        color: blue;
      }
      p {
        color: red;
      }
    </style>
  </head>
  <body>
    <h1>Website Pertamaku</h1>
    <p>Selamat Datang</p>
  </body>
</html>
```

- External CSS
```
<!-- File index.html -->
<!DOCTYPE html>
<html>
  <head>
    <title>Website Pertamaku</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <h1>Website Pertamaku</h1>
    <p>Selamat Datang</p>
  </body>
</html>
/* File styles.css */
body {
  background-color: pink;
}
h1 {
  color: blue;
}
p {
  color: black;
}
```

## CSS Syntax, CSS Selector, Pseudo-Class, and Pseudo-Element

- CSS Syntax
```
<!-- Pada Style.css -->
selector {
  property: value;
}
```

- CSS Selector
```
<!-- Pada Index.html -->
<body>
  <h1>Selamat Datang di Website Pertamaku</h1>

  <div>
    <p>Namaku</p>
    <p>
        <span>Sarah</span>
    </p>
  </div>

  <p>Saya tinggal bersama orang tua saya</p>
</body>

<!-- Pada Style.css -->
div * {
  background-color: yellow;
}

element <p> yang berisi "Namaku";
element <span> yang berisi "Sarah";
Akan diberikan warna latar belakang kuning!

<!-- Pada Index.html -->
<body>
  <h1>Selamat Datang</h1>
  <p>Silahkan scroll ke bawah untuk informasi lebih lanjut</p>

  <h2>Cara Reservasi</h2>
  <p>Reservasi bisa dilakukan dengan menghubungi nomor 08122282xxx</p>
</body>

<!-- Pada Style.css -->
h1,
h2 {
  color: red;
}

Pada kode CSS tersebut, teks di dalam element <h1> dan <h2> akan diberi warna merah. Jadi kalau nanti kalian menambahkan property lain, hal tersebut akan berefek ke kedua element tersebut.

```

- Pseudo-Class

Syntax Pseudo-Class :
```
selector:pseudo-class {
  property: nilai;
}
```

:hover
```
<!-- Pada Index.html -->
<body>
  <h1>Beranda</h1>
  <h1>Galeri</h1>
  <h1>Tentang Kami</h1>
  <h1>Kontak</h1>
</body>

<!-- Pada Style.css -->
h1:hover {
  background: black;
  color: white;
}
```

:nth-child(number)
```
<!-- Pada Index.html -->
<body>
  <p>Nama saya Sarah</p>
  <p>Saya warga negara Indonesia</p>
  <p>Saya tinggal di Tangerang</p>

  <div>
    <p>Kalau mudik ke Jawa Barat</p>
  <div>
</body>

<!-- Pada Style.css -->
p:nth-child(2) {
  background-color: pink;
}

Pada contoh di atas, p:nth-child(2) menunjuk kepada element <p> yang merupakan child kedua dari parentnya -- dalam contoh di atas adalah teks "Saya warga negara Indonesia" karena ia merupakan child kedua dari element <body>.
```

- Pseudo-Element

Digunakan untuk memberikan style pada bagian tertentu dari suatu element.

Contoh:

Memberikan style pada huruf pertama pada suatu kalimat,
Memberikan style pada baris pertama dari dari suatu paragraf,
Menyisipkan konten sebelum atau sesudah suatu element.
Syntax pseudo-element adalah:

Syntax Pseudo-Element :
```
selector::pseudo-element {
  property: nilai;
}
```

::before
```
<!DOCTYPE html>
<html>
  <head>
    <style>
      	a::before {
	        content: "Link - ";
        }
    </style>
  </head>
  <body>
	<ul>
	    <li><a href="#">Download part 1</a></li>
	    <li><a href="#">Download part 2</a></li>
	    <li><a href="#">Download part 3</a></li>
	</ul>
  </body>
</html>
```

::after
```
<!DOCTYPE html>
<html>
  <head>
    <style>
      	a::after {
	        content: " - 720P";
        }
    </style>
  </head>
  <body>
	<ul>
	    <li><a href="#">Download part 1</a></li>
	    <li><a href="#">Download part 2</a></li>
	    <li><a href="#">Download part 3</a></li>
	</ul>
  </body>
</html>
```

::selection
```
<!DOCTYPE html>
<html>
  <head>
    <style>
      h1::selection {
        color: white;
        background: black;
      }
      
      p::selection {
        color: red;
        background: yellow;
      }
    </style>
  </head>
  <body>
    <h1>Cerita Hari ini</h1>
    <p>
      Aku senang sekali hari ini karena mendapatkan nilai sempurna pada
      pelajaran programming.
    </p>
  </body>
</html>
```

::first-letter

Tidak semua properti CSS dapat digunakan dengan ::first-letter. Beberapa yang bisa digunakan adalah:

font,
color,
background,
margin,
padding,
border,
text-decoration,
line-height,
float.

```
<!DOCTYPE html>
<html>
  <head>
    <style>
      p::first-letter {
        font-size: 50px;
        color: red;
      }
    </style>
  </head>
  <body>
    <h1>Cerita Hari ini</h1>
    <p>
      Aku senang sekali hari ini karena mendapatkan nilai sempurna pada
      pelajaran programming.
    </p>
  </body>
</html>
```

::first-line

Properti CSS yang bisa dan sering digunakan dengan ::first-line adalah:

font,
background,
word-spacing,
letter-spacing,
text-transform,
line-height,
color.

```
<!DOCTYPE html>
<html>
  <head>
    <style>
      p::first-line {
        color: red;
      }
    </style>
  </head>
  <body>
    <h1>Cerita Hari ini</h1>
    <p>
      Aku senang sekali hari ini karena mendapatkan nilai sempurna pada
      pelajaran programming. Ternyata jerih payahku belajar dari seminggu yang lalu terbayarkan hari ini.

      Tapi pada saat yang bersamaan aku juga merasa sedih karena teman dekatku sedang sakit. Dia tidak masuk sekolah hari ini. 
    </p>
  </body>
</html>
```

## CSS Box Model

## CSS Display

## CSS Position