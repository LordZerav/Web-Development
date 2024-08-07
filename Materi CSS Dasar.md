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

Box model terdiri dari:

- margin yaitu area terluar yang kosong setelah border. Margin bersifat transparan.
- border yaitu garis tepi yang membungkus padding dan konten.
- padding yaitu area kosong di antara konten dan border. Padding bersifat transparan.
- content yaitu konten (value/nilai) dari HTML element. Bisa berupa teks, gambar, video, ataupun suara.

Jika digambarkan, box model berbentuk seperti ini:

![alt text](image.png)

```
<!DOCTYPE html>
<html>
  <head>
    <style>
      p {
        background-color: lightgrey;
        width: 300px;
        height: 100px;
        border: 15px solid black;
        padding: 50px;
        margin: 20px;
      }
    </style>
  </head>
  <body>
    <h2>Contoh Box Model</h2>

    <p>
        Tulisan ini adalah konten dari box. Konten sendiri memiliki lebar
        (width) sebesar 300px dan tinggi (height) sebesar 100px. Pada box, kita
        menambahkan padding sebesar 50px, border berwarna hitam sebesar 15px,
        dan margin sebesar 20px.
    </p>
  </body>
</html>

Kalau kalian lihat ada kotak berwarna hitam tebal, itu adalah border dari element <p> kita yang sudah kita atur ketebalannya menjadi 15px.

Ada juga sedikit jarak di antara border dan teks "Contoh Box Model". Jarak itu adalah margin dari element <p> kita.

Nah jarak di antara border dan content kita itulah padding dari element <p> kita.
```

- Perhitungan Ukuran Lebar dan Tinggi Box Model

```
<!DOCTYPE html>
<html>
  <head>
    <style>
      p {
        background-color: lightgrey;
        width: 300px;
        height: 100px;
        border: 15px solid black;
        padding: 50px;
        margin: 20px;
      }
    </style>
  </head>
  <body>
    <h2>Contoh Box Model</h2>

    <p>
        Tulisan ini adalah konten dari box. Konten sendiri memiliki lebar
        (width) sebesar 300px dan tinggi (height) sebesar 100px. Pada box, kita
        menambahkan padding sebesar 50px, border berwarna hitam sebesar 15px,
        dan margin sebesar 20px.
   </p>
  </body>
</html>

Jika kita perhatikan kode di atas, properti width dan height yang kita tulis berfungsi untuk mengatur lebar dan tinggi dari konten dalam element <p>, bukan lebar dan tinggi dari seluruh element <p> itu sendiri.

Dari kode di atas, total lebar box yang mengelilingi element <p> sebenarnya adalah:

Lebar box = lebar konten (width) + padding kiri (left padding) + padding kanan (right padding) + border kiri (left border) + border kanan (right border) + margin kiri (left margin) + margin kanan (right margin)

Lebar box = 300px + 50px + 50px + 15px + 15px + 20px + 20px = 470px

Sementara, total tinggi box sebenarnya adalah:

Tinggi box = tinggi konten (height) + padding atas (top padding) + padding bawah (bottom padding) + border atas (top border) + border bawah (bottom border) + margin atas (top margin) + margin bawah (bottom margin)

Tinggi box = 100px + 50px + 50px + 15px + 15px + 20px + 20px = 270px
```

- Alternatif lain dari Perhitungan Ukuran Lebar dan Tinggi Box Model dengan Box-sizing

Saat kita memberi properti box-sizing: border-box pada sebuah element, pemberian properti width dan height tidak lagi menentukan lebar dan tinggi dari konten, melainkan lebar dan tinggi dari element.

Jadi, ukuran element: ukuran konten + padding + border.

```
<!DOCTYPE html>
<html>
  <head>
    <title>Inline CSS</title>
  </head>
  <style>
    div {
      width: 600px;
      background: lightblue;
    }
    img {
      width: 150px;
      background: lightgreen;
      padding: 10px;
      border: 2px solid black;

      /* tambahkan properti box-sizing: border-box */
      box-sizing: border-box;
    }
  </style>
  <body>
    <div>
      <img
        src="https://static-assets.skilvul.com/lesson/intro-to-css/cat.jpg"
      />
      <img
        src="https://static-assets.skilvul.com/lesson/intro-to-css/cat.jpg"
      />
      <img
        src="https://static-assets.skilvul.com/lesson/intro-to-css/cat.jpg"
      />
      <img
        src="https://static-assets.skilvul.com/lesson/intro-to-css/cat.jpg"
      />
    </div>
  </body>
</html>
```

## CSS Display

Properti display adalah salah satu yang sering digunakan dalam pengembangan web. Dari topik sebelumnya kita belajar kalau tiap element dalam halaman web itu berbentuk box. Dengan properti display, kita bisa mengatur bagaimana box tersebut ditampilkan: apa box tersebut ditampilkan sebaris dengan box lain? atau satu box menempati satu baris penuh? bahkan kita juga bisa mengatur apakah box tersebut ditampilkan atau disembunyikan.

- display: none

Dengan mengganti-ganti nilai dari properti display, kita bisa mengatur untuk ditampilkan atau tidaknya element menu itu.

Tapi kalian tahu tidak? Kalau kita menggunakan properti display: none, tampilan dari element di sekitarnya juga ikut berubah. Kenapa? Saat kita menggunakan properti itu, halaman web kita akan ditampilkan seolah-olah element tersebut tidak ada.

- visibility: hidden

Ada properti CSS lain yang fungsinya mirip dengan display, yaitu visibility. Properti visibility mengatur ditampilkan atau tidaknya sebuah element. Perbedaannya dengan display: none terletak di bagaimana ia mempengaruhi posisi element di sekitarnya. Saat kita memberi nilai hidden pada properti visibility si gambar, ia akan tidak ditampilkan, namun ruang yang tadinya ia tempati tetap akan ada di situ. Karena ruang yang ia tempati masih ada, element paragraf di sebelahnya tidak akan berubah posisi. Hal ini akan membuat pengunjung web merasa lebih nyaman saat membaca paragrafnya.

- displat: block

Properti display memiliki beberapa nilai lainnya selain none seperti yang kalian pelajari di topik sebelumnya. Selain untuk mengatur tampil-tidaknya sebuah element, properti display juga dapat mengatur bagaimana element tersebut ditampilkan. Secara default, setiap element HTML memiliki properti display dengan nilai inline atau block.

Element yang memiliki properti display: block; akan menempati satu baris penuh (atau bahkan beberapa baris) meskipun kontennya tidak sebesar itu. Jadi jika kalian memiliki kode seperti ini.

```
<body>
  <p>Element paragraf adalah</p>
  <p>block-level element</p>
  <p>Ia akan menempati</p>
  <p>satu baris penuh</p>
</body>

Setiap element <p> tersebut akan menempati baris baru.
```

Element lainnya yang merupakan block-level element adalah:

```
<h1> sampai <h6>
<li> dan <ol>
<table>
<video>
<html> dan <main>

Inline-level element yang diberi properti display: block juga akan mempunyai karakter yang sama.
```

Mari kita perhatikan contoh di bawah ini:

```<!-- Pada File HTML -->
<body>
  <span>Element paragraf adalah</span>
  <span>block-level element</span>
  <span>Ia akan menempati</span>
  <span>satu baris penuh</span>
</body>
<!-- Pada Style.css -->
span {
   display: block;
}

Hasil dari kode di atas akan sama dengan kode sebelumnya yang menggunakan element <p>. Itu dikarenakan <span> yang merupakan salah satu inline-level element telah diubah properti display-nya menjadi block.
```

- display: inline

Setelah block-level element seperti <div> dan <p>, ada juga element seperti <span> dan <img> yang merupakan inline-level element. Apa lagi tuh? Inline-level element merupakan element yang secara default memiliki properti display: inline.

Keberadaan properti display: inline pada sebuah element akan membuat ukuran box dari element tersebut tidak lagi sebaris penuh seperti dalam kasus display: block, melainkan hanya sebesar konten di dalamnya saja. Hal ini memungkinkan adanya element lain untuk ditempatkan di sebelah element dengan display: inline ini.

Salah satu contoh inline-level element yang kalian mungkin masih ingat dari kelas HTML adalah <span>. Mirip seperti <p>, element <span> menampilkan sebuah teks. Bedanya, box dari element <span> hanya sebesar konten dari element itu saja; tidak sebaris penuh seperti <p>.

```
<!DOCTYPE html>
<html>
  <head>
    <style>
      .green-text {
        background: lightgreen;
      }
      .blue-text {
        background: lightblue;
      }
    </style>
  </head>
  <body>
    <p class="green-text">Teks dengan latar belakang hijau</p>
    <p class="blue-text">Teks dengan latar belakang biru</p>
    <span class="green-text">Teks dengan latar belakang hijau</span>
    <span class="blue-text">Teks dengan latar belakang biru</span>
  </body>
</html>

Untuk kedua element <p>, meskipun panjang teksnya hanya sekitar 2/3 dari panjang baris, box mereka tetap memenuhi satu baris penuh. Sebab <p> adalah block-level element.

Sementara untuk <span> dengan latar belakang hijau, ukuran box hanya selebar teks "Teks dengan latar belakang hijau" saja. Oleh karena itu ada ruang sedikit di sebelah kanannya yang bisa diisi oleh element <span> dengan latar belakang warna biru.
```

Element lain yang merupakan inline-level element adalah
```
<a>
<img>
<label> dan <input>
<select>
```

Oh iya, ada satu hal yang perlu kalian ingat saat menggunakan properti display: inline. Element yang kita beri properti itu tidak bisa diatur lebar maupun tingginya.

```
<style>
  .green-text {
    background: lightgreen;
    height: 30px;
  }
  .blue-text {
    background: lightblue;
    height: 30px;
  }
</style>

Element <p> tentu akan berubah tingginya. Namun tinggi dari element <span> tidak berubah karena secara default ia memang memiliki properti display: inline. Jadi kalaupun kita menambahkan properti tinggi padanya, tingginya tidak akan terpengaruh.
```

- display: inline-block

Berbeda dengan element yang memiliki properti display: inline di mana lebar dan tinggi element tidak dapat kita atur, element dengan display: inline-block bisa kita atur lebar dan tingginya.

Berbeda juga dengan element dengan properti display: block yang selalu mengambil penuh ruang dalam satu baris, element dengan display: inline-block secara default hanya akan mengambil ruang sebesar konten di dalamnya. Dengan adanya sisa ruang di sebelah kiri atau kanannya, element dengan display: inline-block bisa ditempatkan bersebelahan dengan yang lainnya.

```
<style>
  h1 {
    display: inline-block;
    background: lightblue;
  }
  #demo1 {
    width: 150px;
    height: 100px;
  }
  #demo2 {
    width: 200px;
    height: 150px;
  }
</style>

Tinggi dan lebar dari element <h1> akan berubah mengikuti nilai yang kita berikan. Element dengan display: inline tidak melakukan hal seperti ini.
```

Kita bisa simpulkan bahwa properti inline-block itu seperti persilangan antara inline dan block. Ada beberapa karakteristik dari inline dan beberapa dari block yang diikuti saat kita menggunakan inline-block, antara lain:

```
1. lebar box sebanding lebar dari konten di dalamnya; tidak sebaris penuh.
2. element dengan display: inline atau display: inline-block bisa ditempatkan di sebelah kiri atau kanannya.
3. jika kita memberikan nilai untuk properti height dan width, ia akan mengikutinya.
```

## CSS Position

- position: static

Secara default, seluruh properti position dari HTML element memiliki nilai static. Element dengan properti tersebut tidak akan terpengaruh oleh properti top, bottom, left, dan right. Element tersebut akan selalu berada sesuai dengan alur normal penempatan element dalam halaman web.

```

<!DOCTYPE html>
<html>
  <head>
    <style>
      .container {
        background: lightgreen;
        width: 600px;
        height: 150px;
      }

      .yellow-boxes {
        display: inline-block;
        margin: 10px;
        background: yellow;
        width: 100px;
        height: 100px;
      }
    </style>
  </head>

  <body>
    <div class="container">
      <div class="yellow-boxes" style="top: 20px;"></div>
      <div class="yellow-boxes" style="right: 20px;"></div>
      <div class="yellow-boxes" style="bottom: 20px;"></div>
      <div class="yellow-boxes" style="left: 20px;"></div>
    </div>
  </body>
</html>

Keempat kotak kuning akan ditempatkan sebagaimana mestinya tanpa ada perubahan posisi.

```

- position: relative

Element dengan posisi relative akan diposisikan relatif dari posisi normalnya. Kita bisa memberikan properti top, right, bottom, dan left pada element dengan posisi relative. Element lain di sekitar element dengan posisi relative tidak akan disesuaikan dengan ruang yang ditinggalkan oleh element.

```

<!DOCTYPE html>
<html>
  <head>
    <style>
      .inline-block {
        background: blue;
        width: 100px;
        height: 100px;
        margin: 4px;
        display: inline-block;
      }
    </style>
  </head>

  <body>
    <div>
      <div class="inline-block"></div>
      <div class="inline-block"></div>
      <div class="inline-block"></div>
    </div>
  </body>
</html>

Kode di atas akan menampilkan tiga buah kotak berukuran 100px x 100px berwarna biru dalam satu baris.

Sekarang coba tambahkan kode berikut ke dalam element <style>

/* Pada style.css */

.relative {
  position: relative;
  top: 40px;
}

Lalu ubah kode HTML untuk kotak-kotaknya menjadi seperti ini

<!-- Pada index.html -->

<div class="inline-block"></div>
<div class="inline-block relative"></div>
<div class="inline-block"></div>

Kotak kedua baru saja kita beri properti position: relative dan top: 40px yang berarti posisi ia sekarang adalah 40px lebih ke bawah dari yang biasanya.

```

- position: absolute

Element dengan posisi absolute akan diposisikan relative dengan posisi ancestor terdekat yang posisinya bukan static.

```

<!-- Pada index.html -->

<body>
<div id="A">
    <div id="B">
        <div id="C">
            <div id="D"></div>
        </div>
        <div id="E"></div>
    </div>
</div>
</body>

Ancestor dari sebuah element merupakan semua element yang berada di tingkat atasnya. Misalnya element <div id="D">, ia dibungkus oleh 3 buah element lainnya:

<div id="C">
<div id="B">
dan <div id="A">
Ketiga itu merupakan ancestor dari element <div id="D">. Sebab kalau kalian gambar diagram pohonnya, ketiga element tersebut memiliki posisi yang lebih di atas dan terhubung langsung element <div id="D">.

```

```

<!DOCTYPE html>
<html>

<head>
	<style>
		.small-square {
			position: absolute;
			right: 0;
			height: 80px;
			width: 80px;
			background: yellow;
		}

		.medium-square {
			height: 200px;
			width: 300px;
			background: red;
		}

		.big-square {
			position: relative;
			height: 400px;
			width: 400px;
			background: deepskyblue;
		}
	</style>
</head>

<body>
	<div class="big-square">
		<div class="medium-square">
			<div class="small-square"></div>
		</div>
	</div>
</body>

</html>

```

Element <div class="small-square"> memiliki properti ` position:absolute dan right:0. `

Sementara kalau kita analisa, yang manakah ancestor terdekatnya yang memiliki properti bukan ` position: static? `

Element <div class="medium-square"> merupakan parentnya. Tapi kita tidak memberinya properti position. Dari topik sebelumnya, kalian tahu kalau secara default, sebuah element itu memiliki properti position: static. Jadi ancestor yang kita inginkan bukan element ini.

Lalu ada <div class="big-square">. Nah kali ini ia memiliki properti position: relative. Berarti element <div class="small-square"> akan diposisikan relatif terhadap element ini.

` Kotak yang kecil (kuning) memiliki properti right:0. Tapi itu relatif terhadap kotak yang besar (biru), bukan yang berukuran sedang (merah). `

- position: fixed

Element dengan posisi fixed akan diposisikan relatif terhadap viewport browser, di mana akan selalu berada di tempat yang sama jika walaupun halaman website di-scroll.

Ini biasa dipakai untuk element-element yang memang posisinya selalu konstan seperti navigation bar dari sebuah halaman web yang selalu berada di bagian atas halaman atau chatbox yang selalu ada di pojok layar agar mudah diakses.

Kita bisa memberikan properti top, bottom, right, dan left pada element yang memiliki style position: fixed. Posisinya relatif pada viewport browser, jadi kalau diberi properti left:0px maka ia akan terus berada di bagian kiri jendela browser.

Element dengan posisi fixed tidak akan menempati ruang pada halaman seperti element dengan attribute position yang lainnya.

```

<!DOCTYPE html>
<html>
  <head>
    <style>
      div.fixed {
        position: fixed;
        top: 100px;
        width: 300px;
        padding: 10px 20px;
        background: #73ad21;
      }
    </style>
  </head>
  <body>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
      tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
      veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
      commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
      velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat
      cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id
      est laborum.
    </p>

    <div class="fixed">
      This div element has position: fixed;
    </div>
  </body>
</html>

```

Pada kode di atas, element <div class="fixed"> akan berada 100px dari bagian atas viewport browser (karena diberi properti top: 100px) meskipun halaman webnya di-scroll.

- position: sticky

Element dengan posisi sticky akan diposisikan berdasarkan scroll halaman dari user.position:sticky pada dasarnya adalah seperti gabungan dari position:relative dan position: fixed.

Awalnya, element dengan properti ini akan memiliki posisi seperti dia memiliki properti position: relative. Namun ketika user melakukan scroll halaman web hingga element berada di sebuah lokasi relative terhadap viewport, maka posisi element tersebut akan berubah seperti layaknya dia memiliki properti position: fixed. Dengan kata lain ia akan diam di lokasi relatif terhadap viewport tadi.

Untuk melihat hasil dari position:sticky, kita setidaknya butuh mengatur salah satu nilai dari properti top, right, bottom, left.

```

<!DOCTYPE html>
<html>
  <head>
    <style>
      .sticky {
        position: sticky;
        top: 30px;
        padding: 5px;
        background-color: yellow;
        border: 2px solid blue;
      }
      p.content {
          height: 100vh
      }
    </style>
  </head>
  <body>
    <p>Cobalah scroll halaman website ini</p>

    <div class="sticky">I am sticky!</div>

    <p class="content">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
      tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
      veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
      commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
      velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat
      cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id
      est laborum.
    </p>

  </body>
</html>

```

## Mengatur Viewport

Secara umum viewport adalah daerah pada layar yang menampilkan suatu konten. Dalam konteks kita kali ini, tentu viewport adalah daerah yang menampilkan halaman web yang sedang kita akses.

Perlu kalian ingat bahwa ukuran viewport tidak selalu sama dengan resolusi layar perangkat.

Untuk membuat halaman website menjadi responsif, maka kita perlu menambahkan meta data berikut ini di dalam element <head> di file HTML.

``` <meta name="viewport" content="width=device-width, initial-scale=1.0" /> ```

Meta data di atas akan mengatur viewport dari halaman website, di mana meta data tersebut akan memberikan instruksi kepada browser untuk mengatur bagaimana dimensi dan skala dari halaman website kita.

```

📝 Catatan:

Tag <meta> digunakan untuk menulis info tentang suatu dokumen HTML seperti deskripsi, nama pengarang, keywords, dan tanggal terakhir dokumen diperbaharui. Tag <meta> tidak akan tampil di halaman HTML.

```

```

<!DOCTYPE html>
<html>
  <head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Website Pertamaku</title>
  </head>
  <body>
    <h1>Halo Dunia</h1>
    <p>
      Ini adalah contoh untuk mengatur file HTML agar bisa menjadi responsif.
    </p>
  </body>
</html>

```

Penjelasan kode di atas:

` - width=device-widthmemberitahu browser untuk mengikuti lebar layar dari perangkatnya. Sebab lebar layar tiap perangkat berbeda-beda. `

` - initial-scale=1.0 memberitahu browser tingkat pembesaran (zoom level) dari halaman itu. `

- Menggunakan Persentase untuk Menentukan Nilai Lebar Suatu Element

Kita bisa menggunakan persentase untuk menentukan lebar suatu element agar sama dengan lebar parent element-nya.

```

<!DOCTYPE html>
<html>
  <head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Website Pertamaku</title>
    <style>
      div{
        width: 100%;
        background-color: yellow;
      }
      img {
        width: 60%;
      }
    </style>
  </head>
  <body>
    <div>
      <img
        src="https://static-assets.skilvul.com/lesson/intro-to-css/responsive-design-percentage-cat.jpeg"
        alt="kucing"
      />
    <div>
  </body>
</html>

Sekarang lebar foto kucing itu akan selalu sebesar 60% dari lebar <div> dengan latar belakang kuning; berapapun lebar layarnya.

```

- Menggunakan Properti max-width: 100%

Kita bisa menggunakan properti max-width: 100% untuk menentukan lebar maksimal dari suatu element.

Contoh: Kita mengambil gambar kucing dari internet yang memiliki lebar sebesar 640px. Maka, jika kita menggunakan max-width: 100%, lebar gambar tidak akan melebihi 640px. Walaupun begitu, jika kita membuka website kita di handphone, lebar gambar kucing akan mengikuti lebar layar handphone.

Jadi properti max-width itu menentukan batas atas dari lebar suatu element.

```

<!DOCTYPE html>
<html>
  <head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Website Pertamaku</title>
    <style>
      img {
        max-width: 100%;
        height: auto;
      }
    </style>
  </head>
  <body>
    <img
      src="https://static-assets.skilvul.com/lesson/intro-to-css/responsive-design-percentage-cat.jpeg"
      alt="kucing"
    />
  </body>
</html>

```

- Satuan Unit 'vw'

Suatu teks bisa diatur ukurannya dengan menggunakan vw, yang artinya viewport width. Viewport adalah ukuran lebar window browser.

```
📝 Catatan:

- 1vw = 1% lebar viewport
- Jika lebar viewport sebesar 100cm, maka 1vw adalah 1cm

```

```

<!DOCTYPE html>
<html>
  <head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Website Pertamaku</title>
    <style>
      h1 {
        font-size: 5vw;
      }
    </style>
  </head>
  <body>
    <h1>Hello World</h1>
  </body>
</html>

```

- Media Query

Dengan menggunakan media query, kita bisa mengatur lebar suatu element dan/atau memberikan style lain yang berbeda-beda sesuai dengan ukuran dari browser.

```

<!DOCTYPE html>
<html>
  <head>
    <style>
      body {
        max-width: 800px;
      }
      .button-group {
        display: flex;
      }
      button {
        font-size: 25px;
        width: 100%;
      }
    </style>
  </head>

  <body>
    <h1>Cat Ltd.</h1>
    <img
      src="https://static-assets.skilvul.com/lesson/intro-to-css/responsive-design-percentage-cat.jpeg"
      width="100%"
    />
    <div class="button-group">
      <button>Talk to Us</button>
      <button>Download Syllabus</button>
      <button>Be a Partner</button>
      <button>Join Class</button>
    </div>
  </body>
</html>

```

Sekilas terlihat bagus memang. Tapi saat dibuka di layar yang lebih kecil, tombolnya menjadi semakin berdempet dan teks di dalamnya terkesan terlalu besar.

Bagi pengguna komputer/laptop mungkin ini bukan sesuatu yang buruk. Tapi bagi pengguna mobile, website ini akan terlihat aneh.

Coba kalian tambahkan potongan kode ini ke dalam element style:

```

/* Pada style.css */

@media (max-width: 600px) {
  .button-group {
    display: flex;
    flex-direction: column;
  }
}

```

Penjelasan kode di atas:

` @media (max-width: 600px) merujuk kepada jendela browser yang lebarnya maksimal 600px. Dengan kata lain, semua rule/kode CSS di dalam @media ini akan diterapkan jika layarnya memiliki lebar 600px atau kurang. `

Sesuai kode di atas, saat lebar layar itu 600px atau kurang, element dengan class button-group akan memiliki properti ` display:flex ` dan ` flex-direction:column. `

- Flexbox Element

Setelah belajar mengenai display:inline dan display:block pada topik CSS Display sebelumnya, mungkin kalian merasa sulit jika harus mengatur posisi dan lebar dari setiap element secara manual.

Misalnya kita ingin membuat tiga buah kotak dalam satu baris sepanjang layar. Menggunakan property ` inline-block `

```

<!DOCTYPE html>
<html>
  <head>
    <style>
      .inline-block {
        width: 31%;
        height: 100px;
        margin: 4px;
        background: #ec5453;
        display: inline-block;
        font-size: 60px;
        color: white;
        text-align: center;
      }
    </style>
  </head>

  <body>
    <div class="inline-block">1</div>
    <div class="inline-block">2</div>
    <div class="inline-block">3</div>
  </body>
</html>

```
```

📝 Catatan:

width: 31%; itu membuat setiap kotak memiliki lebar 31% (atau sekitar sepertiga) dari ukuran parent element-nya.

```

Flexbox memudahkan para programmer untuk mengatur layout, posisi, dan ukuran dari tiap element di dalamnya.

Ada dua istilah penting saat belajar flexbox:

container adalah element yang membungkus dan mengatur tampilan dari element di dalamnya,
item adalah element dalam container yang diatur tampilannya.

Misalnya untuk contoh tadi, dengan menggunakan flexbox, kodenya cukup seperti ini saja:

```

<!DOCTYPE html>
<html>

<head>
	<style>
		#flex-container {
			display: flex;
			flex-direction:row;
		}
		.flex-item {
			flex-basis: 100%;
			height: 100px;
			margin: 4px;
			background: #ec5453;
			font-size: 60px;
			color: white;
			text-align: center;
		}
	</style>
</head>

<body>
	<div id="flex-container">
		<div class="flex-item">1</div>
		<div class="flex-item">2</div>
		<div class="flex-item">3</div>
	</div>
</body>

</html>

```

Jika ingin menambahkan kotak lagi, cukup dengan menambahkan:

` <div class= "flex-item">4</div>`
` <div class= "flex-item">5</div>`

Dan lebar tiap kotak sekarang akan disesuaikan secara otomatis.

Bagaimana jika kita ingin penomorannya dibalik?

Selain properti ` flex-direction:row `, sistem flexbox juga mempunyai properti ` flex-direction:row-reverse ` yang membalikkan urutan dari semua item dalam container kalau kalian gunakan properti yang baru tersebut.

` justif-content `

Selain mengatur ukuran dari flex item, sistem flexbox juga bisa mengatur tata letak dan ruang di antara item tersebut

```

<!DOCTYPE html>
<html>

<head>
	<style>
        html, body, #flex-container {
            height: 100%;
        }
		#flex-container {
			display: flex;
			flex-direction:row;
			justify-content: flex-start;
		}
		.flex-item {
			width: 100px;
			height: 100px;
			margin: 4px;
			background: #ec5453;
			font-size: 60px;
			color: white;
			text-align: center;
		}
	</style>
</head>

<body>
	<div id="flex-container">
		<div class="flex-item">1</div>
		<div class="flex-item">2</div>
		<div class="flex-item">3</div>
	</div>
</body>

</html>

Ini akan menghasilkan tiga buah persegi berukuran 100px.

```

Propert ` justify-content ` bisa diisi dengan satu dari beberapa nilai berikut: 

` flex-start ` , semua item akan ditempatkan di depan seperti gambar di atas.

` flex-end `, semua item akan ditempatkan di belakang.

` center `, semua item akan ditempatkan di tengah.

` space-between `, akan memberi ruang pada setiap dua item yang bersebelahan.

` space-around `, akan memberi ruang pada sekitar tiap item.

Properti ` justify-content ` dan ` flex-direction ` hanya dua dari banyak sekali properti yang ada dalam sistem flexbox.