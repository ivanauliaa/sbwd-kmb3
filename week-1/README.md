# Week 1

## Day 1
### Command Line Interface
- Sebuah antarmuka bagi manusia untuk berinteraksi dengan komputer berbasis perintah yang diinputkan dengan menggunakan keyboard.
- `cd` navigasi direktori
- `pwd` melihat 
- `ls` melihat daftar isi file dan direktori
- `touch` membuat file
- `mkdir` membuat direktori
- `cat`, `head`, `tail`, `less` untuk melihat isi file
- `cp` menggandakan file atau direktori
- `mv` memindahkan atau menamai ulang file atau direktori
- `rm` menghapus file atau direktori

### Git & GitHub
- Git merupakan tools dalam memversikan program  
  Git digunakan sebagai version control system serta dapat digunakan untuk melacak segala perubahan pada suatu file atau folder maupun source code 
- Vendor Git yaitu Github, Gitlab, Bitbucket 
  Github merupakan vendor git yang paling umum digunakan dan sebagai tempat penyimpanan Git Repository
- Membuat Repository <br />
  git init (dilakukan didalam folder yang dibuat) 
- git Status digunakan untuk melihat apakah terjadi perubahan atau tidak pada Git 
- git add untuk menambah file baru/file yang telah diubah pada Git  
- git remote menghubungkan remote repository dengan project local yang telah kita buat direktorinya 
- git commit -m "commit message" digunakan untuk menyimpan perubahan pada Git
- git push -u origin master digunakan untuk mengirimkan/perubahan file ke remote repository 
- git branch -b [nama branch] digunakan untuk membuat branch baru
- git checkout digunakan untuk berpindah branch
- git merge digunakan untuk menggabungkan branch cabang ke branch master ( git merge origin/(nama branch))

## Day 2
### HTML
- HTML atau *Hypertext Markup Language* yang berfungsi menampilkan konten di browser
- Tools yang dibutuhkan untuk untuk membuat HTML yaitu web browser dan code editor
- Visual Studio Code merupakan salah satu code editor yang dibuat oleh Misrosoft
- HTML Element terdiri atas opening tag, content, dan closing tag <br /> 
- HTML Attributes : properties dari sebuah element HTML. Contohnya yaitu id,class,name
- Semantic HTML yaitu menggunakan elemen HTML sesuai dengan kebutuhan konten. Contoh yaitu header, footer, nav, section, aside, dll.

## Day 3
- CSS atau *Cascading Style Sheets* yang digunakan untuk mendesain halaman website dengan mengubah warna, menggunakan font custom, editing text format, mengatur tata letak.
- Struktur CSS <br />
  ```
    .elementHTML{  
	   property : value
    } 
  ```
- . (titik) : merupakan selektor yg menuju pada tag html yg memiliki properti kelas
- CSS comment dapat diberika di external css dan internal css ``/* */ ``
- Ada 3 cara menggunakan CSS yaitu : inline tag, internal style dan external style <br />
Inline Tag : menggunakan css lngsng di atribute elemnt html <br />
Internal Tag : menggunakan tag style di bagian head <br />
External Tag : menggunakan file css terpisah dengan html
- Properti CSS contohnya yaitu font-size, color, background-color
- Cara mengakses file .CSS di HTML <br />
``<link href="styles.css" type="text/css" rel="stylesheet"/>``
- CSS - Tag Name <br />
jika menggunakan Tag element HTML maka akan bersifat global yg artinya akan mengubah seluruh html <br />
``` 
  h1 {
      color: blue; 
   } 
```
- CSS - Class Name dengan cara menggunakan selector class <br />
``` 
   .text-color-red{
	        color: red; 
    }
```
- Tag Id dan Tag Class bisa dipake di css namun Tag Class lebih bersifat fleksibel karena dapat diberikan lebih dari 1 nilai sedangkan
Tag Id bersifat kaku karena hanya memiliki 1 nilai
- Nested Element yaitu setiap element yang terdiri atas parent dan child
- !important CSS yaitu styling CSS yang memiliki tingkat paling atas dari ID dan Class.
- Flexbox adalah suatu cara untuk mengatur layout atau tata letak
- Flexbox terdiri 1 parent (container) dan bisa beberapa child
- Flex direction digunakan untuk mengatur letak child
- Flex wrap mengatur tata letak child pada 1 line
- Flex flow yaitu digunakan sebagai shortcut untuk set up flex-direction dan flex-wrap secara bersamaan
- Order digunakan untuk ordering item yang ingin diatur posisinya
- Justify - content digunakan untuk mengatur tata letak antar item child secara horizontal
- Align - content digunakan untuk mengatur tata letak antar item child secara vertikal atau cross axis
- Flex-grow digunakan untuk mengatur size suatu item child pada flexbox
- Flex-shrink digunakan untuk memperkecil size suatu item child secara relatif terhadap item child lainnya
- flex-basis digunakan untuk mengatur width setiap item child

## Day 4
### Algoritma
- Algoritma adalah deskripsi berupa step-step yang dibutuhkan untuk mnyelesaikan suatu masalah
- Algoritma berfungsi untuk menyelesaikan masalah secara runut
- Kualitas suatu algoritma :
  - Input & output harus jelas/ didefinisikan terlebih dahulu dgn tepat
  - Setiap step harus benar -benar clear dan tidak ambigu
  - Algoritma seharusnya tidak mengandung suatu code pada bahas pemrograman tertentu. <br />
    algoritma harus dibuat agar dapat digunakan dlm bahas pemrograman apapun
- Kenapa harus mempelajari algotima :
  - Pemrograman merupakn algoritma dan struktur data
  - Data struktur dgunakan untk mngelola sebuah data
  - Algoritma menyelesaikan suatu permsalahan mnggunakn sbuah data trsbut

### JS Introduction
- **Javascript** merupakan bahasa pemrograman yang digunakan untuk membuat suatu website menjadi **interaktif**
- Cara menjalankan javascript adalah melalui berbagai browser. Namun mozilla dan google chrome merupakan browser yang paling umum digunakan. 
- Pada Javascript dikenal dengan istilah **Syntax** dan **Statement**
> **Syntax** adalah sesuatu yang dapat diibaratkan sebagai kamus dan berperan dalam mengatur tata cara dalam bahasa pemrograman. **Syntax** digunakan untuk membuat statement program, instruksi untuk dijalankan atau dieksekusi oleh web browser dan compiler.
- Contoh Syntax Java Script 
  - Alert 
  - Prompt
  - confirm
- **Console Log** adalah tempat untuk melakukan pengecekan logic pemrograman serta pemeriksaaan apakah terdapat error atau tidak pada pemrograman.
- **Comments**
  - Single Comments: `` // ``
  - Multiline Comments:  `` /* */``
- **Tipe Data** <br />
Ada 6 macam tipe data fundamaental pada javascript yaitu :
  - Number : tipe data yang mengandung semua jenis angka. <br />
  Tipe data number ada 2 macam yaitu **integer** (terdiri dari bilangan bulat positif atau negatif) dan **float** (terdiri dari bilangan desimal)
  - String : tipe data yang terdiri dari huruf, angka, spasi maupun simbol <br />
  Tipe data string ada 2 macam yaitu char dan 
  - Boolean : tipe data yang memiliki nilai true or false
  - Null : tipe data pada sebuah data/variabel yang tidak memiliki nilai
  - Undefined : tipe data yang merepresentasikan varibel/data yang tidak memiliki nilai
  - Object : tipe data yg dapat berisi berbagai nilai dan berhubungan dengan dunia nyata
- **Variabel** merupakan wadah atau tempat untuk menyimpan sebuah nilai
3 hal yang dapat dilakukan pada variabel:
  - variabel harus dibuat dengan nama yang jelas dan menggabarkan tentang data tersebut
  - variabel dapat menimpan dan mengupdate informasi data yang disimpan
  - variabel digunakan untuk menampilkan atau mendapatkan data yang tersimpan
- Ada 3 cara untuk mendefinisikan variabel yaitu :
  - var
  - let
  - const
- Aturan Penamaan variabel yaitu :
  - Harus mendeskripsikan dengan jelas tentang data yang disimpan
  - Tidak bisa menggunakan angka diawal variabel 
  - Menggunakan camelcase untuk nama variabel yg lebih dari 1 kata
- **Operator**
- **Assignment Operator (=)** digunakan untuk menyimpan sebuah nilai pada variabel
 contohnya : `` let myName = 'Chaca'``
- **Mathematical Assignment Operator**
- contohnya : 
  ```
    let x = 10 ; 
    x *= 2 ; 
    console.log(x) // Output: 20
  ```
- **Increment dan Decrement** digunakan untuk menambah atau mengurangi sebesar 1 nilai
- contohnya :
  ```
  let a = 10;
  a++
    console.log(a) // output: 11
  ```
- **Arithmetic Operator** digunakan apabila melibatkan operasi matematika
  - Pertambahan (+)
  - Pengurangan (-)
  - Perkalian (*)
  - Pembagian (/)
  - Modulus (%)
- **Comparism Operator** digunakan untuk membandingkan suatu nilai 
  - Lebih Besar (>)
  - Lebih Kecil (<)
  - Lebih kecil atau samadengan (<=)
  - Lebih besar atau samadengan (>=)
  - Samadengan (===)
  - Tidak Samadengan (!==)
- **Logical Operator** digunakan untuk sebuah kondisi
  - AND operator (&&)
  - OR operator (||)
  - NOT operator (!)

## Day 5
### JS Conditional
### **Conditional**
- **Conditional** merupakan *statement percabangan* yang menggabarkan suatu *kondisi*
- Conditional statement akan melakukan pengecekan pada kondisi fisik dan menjalankan perintah berdasarkan kondisi tersebut
- Contoh Conditional
- IF Statement
- contoh conditional **if statement** :
  - Jika cuaca hari ini cerah, maka kita akan pergi keluar
  - jika saya lapar, maka saya makan
- contoh if statement 
  ```
  let nilai = 10;
  if (nilai === 10){
    console.log('variabel nilai yang disimpan adalah benar 10');
  }
  ```
- IF ... ELSE Statement
- contoh conditional **if else statement**
  ```
  let angka = 12;
  if (angka %2 == 0){
    console.log(angka + " adalah angka genap");
  } else {
    console.log(angka + " adalah angka ganjil")
  }
  ```
- IF ... ELSE IF Statement
- contoh conditional **if else if statement**
  ```
  let num1 = 10
  let num2 = 20

  if (num1 = num2){
      console.log(num1)
  } else if (num1 > num2){
      console.log(num1)
  } else {
      console.log(num2)
  }
  ```

- Switch Case Conditional digunakan jika kondisi percabangan terlalu banyak
- contoh conditional **switch case**

  ```
	let warna = "kuning";
 
		switch (warna){
			case "hitam":
				console.log ("warna hitam");
				break;
			case "merah":
				console.log ("warna merah");
				break;
			case "hijau":
				console.log ("warna hijau");
				break;
			default:
			    console.log ("warna tidak terdeteksi");
		}
  ```
- Ternary Operator merupakan short-syntax dari statement if ... else
- contoh ternary operator
  ```
  let isNowSale = true;
  isNowSale ? console.log('Let's shopping now) : console.log('Shopping later);
  ```

### JS Looping
### **Looping**
- **Looping** merupakan statement yang mengulang suatu instruksi hingga kondisi terpenuhi atau jika kondisi stop atau berhenti
- Ada 3 macam looping yaitu :
  - For Loop 
  - While Loop
  - Nested Loop
- For Loop : digunakan jika kita tahu pasti seberapa banyak pengulangan yang ingin dilakukan pada program yang akan dikembangkan
- contohnya :
```
    let nilai = 1 ; 
    for (nilai; nilai <= 10 ; nilai++){
        console.log(nilai) 
    } 
```
- While Loop : akan menjalankan instruksi pengulangan bernilai TRUE
  Ada 2 macam while loop yaitu while dan do while
- contoh perulangan while :
```
    let count = 1 ; 
    while (count < 10){
        console.log(count);
        count ++ ;
    } 
```
- contoh perulangan do while :
```
    count = 1 ;
    do {
        console.log(count);
        count ++ ;
    } while (count <= 10)
```     
- Nested Loop : digunakan jika ingin membuat perulangan di dalam perulangan

### **Scope dan Function**
- **Scope** merupakan konsep dalam flow data varaiabel. 
Menentukan suatu variabel apakah bisa diakses pada scope atau tidak.
- Scope ada 2 macam yaitu global scope dan local scope
- contoh global scope :
```
    let myName = "chaca" ; 
    function greeting()
        return myName;
    {
        console.log(myName);
```
- contoh local scope :

- **Blocks** merupakan code yang berada dalam curly braces {}. Conditional, function dan looping menggunakan blocks.

- **Function**
- **Function** adalah sebuah code blok dalam sebuah grup untuk menyelesaikan 1 task
- Membuat function 
```
   function greeting() {
      return 'Hello World' ;
   };
```
- Cara memanggil function : 
```
 greeting()
 console.log(greeting()); 
 
 ```
- **Argumen dan Parameter**
- Argumen adalah nilai yang digunakan daat memanggil function. Jumlah argumen harus sama dengan jumlah parameternya. <br />
- contoh argumen :
```
  function penambahan(a,b){
   return a + b;
}
  console.log(penambahan(5,5))
```
- Parameter berfungsi untuk menerima sebuah inputan data yang digunakan untuk melakukan task. <br />
- contoh parameter :
```
function calculateArea(width,height){
  console.log(width * height);
}
```
- **Arrow Function** merupakan cara lain menuliskan function. ini adalah fitur terbaru yang ada pada ES6.
- contoh penulisan arrow function :
```
 const greeting = (a,b) => {
    return a + b;
}
```
- Short Syntax Function
- **Single Line Block** 
- ``const sumNumbers = number => number + number ; ``
- **Multi Line Block
```
  const sumNumbers = number => {
    const sum = number + number;
    return sum;
  }
``` 11QQW