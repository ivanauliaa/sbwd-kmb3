# Week 2

## Day 1
### JS Scope & Function
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
```

## Day 2
### JS Data Type
- JS memiliki data type: number, string, boolean, null, undefined, object
- JS memiliki array, namun sebenarnya tipe tersebut merupakan pengembangan dari object
```
let foo = 42; // foo is now a number
foo = "bar"; // foo is now a string
foo = true; // foo is now a boolean
```
- Cara mengakses elemen string
```
'cat'.charAt(1) // gives value "a"
'cat'[1] // gives value "a"
```
- Method charAt merupakan salah satu built in method untuk tipe string
- Tipe array juga memiliki beberapa built in method seperti
```
const array = [1, 2, 3];
array.forEach((a) => ...); // loop for each array element
array.map((a) => ...); // loop for each array element and return it
array.filter((a) => ...); // loop for each array element and return it which fulfill defined boolean expression
```

## Day 3, 4, & 5
### JS DOM
- DOM merupakan cara memanipulasi html agar website lebih dinamis dan interaktif
- Cara memanggil DOM Value yaitu :
  - Memanggil tag HTML berdasarkan ID
  `` console.log(document.getElementByID("header))``
  - Memanggil tag HTML berdasarkan Class Name 
  `` console.log(document.getElementByClassName("text-color-blue"))``
  - Memanggil tag html berdasarkan query selector
  `` console.log(document.querySelector("#header "))`` 
  `` console.log(document.querySelector(".text-color-blue"))``
- Memanipulasi content
  Cara memanipulasi content :
  1. Deklarasi varible header sebagai wadah untuk menyimpan tag HTML
  `` let header = document.getElementById("header"); ``
  2. Memanipulasi Content pada Header Content dari pemilik element dengan ID Header dengan text.Content
  `` document.getElementById("header").textContent = "Teks Heading" `` <br />
     Memanipulasi Content didalam sebuah element dengan .innerHTML
  ```
  <ul id= "list"></ul>

  document.getElementById("list").innerHTML = "<li> item1 </li> <li> item2 </li>"
  ```
- Membuat Element HTML
- Contoh :
  ```
  <div id ="header"></div>

  //untuk membuat sebuah elemnt heading
  const heading = dosument.createElement("h1)
  heading.textContent = "Ini Heading"

  document.getElemntByID("header").appendChild(heading)
  ```

- **DOM Events** merupakan object model yang bertugas untuk membantu interaksi user dengan document HTML
- Contoh HTML DOM events
  - Click
  - Scroll
  - Change
  - Focus
  - Hover
  - Submit
  - Blur
- Menangkap Interaksi User
  - Element.addEventListener("event)
  - Element.onevent
- EventListener <br />
  Dengan menggunakan Element.addEventListener("event") dapat menerapkan beberapa hal yaitu :
  - Bisa dihilangkan
  - Bisa ada beberapa event listener yang sama untuk 1 element
  - Memiliki argument tambahan {options}
- Contoh EventListener :
  - EventListener - Click 
    `` <input id="user-input"/> ``
    `` <button id="alert-button">show</button> ``
    Memanggil element berdasarkan id
    `` const input = document.getElementById("user-input") ``
    `` const button = dosument.getElementById("alert-button") ``

    ```
     button.addEventListener("click", function()) {
      alert(input.value)
    } 
    ```
- EventListener - Blur : event dimana sebuah element kehilangan fokus dari user 
- Contoh EventListener - Blur <br />
  Misalkan saat ingin memvalidasi isi dari ``<input id = "username" />`` agar panjangnya minimal 6 karakter

  `` const input = document.getElementById("username") ``

  ```
  input.addEventListener("blur", () => {
    if(input.value.length < 6) alert("Panjang username minimal 6")
  })
  ```
- EventListener - Form Submission
- Contoh EvenListener - Form Submission <br />
  Misalkan terdapat beberapa input dalam sebuah form `` <input name="email"/> `` dan ``<input type="password" name="password"/>`` <br />
  Untuk mendapatkan isi dari kedua inputan tersebut terdapat 2 cara :
  - Memasang event listener di kedua input dan tombol submit, lalu saat tombol diklik, baca value dari kedua input tersebut
  - Memasang event listener di form, lalu gunakan FormData untuk menggambil data dari masing-masing input
  ``` 
    const form = document.getElementById("form")

    form.addEventListener("submit", function(event)){
    event.preventDefault()

    const formData = new FormData(form)
    const values = Object.fromEntries(formData) {
      email: ....
    }
  })
  ```
