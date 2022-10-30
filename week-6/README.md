# Week 6

## Day 1

### Web Server

- Static web server merupakan layanan yang menyajikan halaman dengan data statis
- Dynamic web server merupakan layanan yang menyajikan halaman dengan data yang dapat berubah-ubah sesuai dengan perintah user

### RESTful API

- RESTful API merupakan sebuah aturan untuk merancang HTTP API
- RESTful API merujuk pada tata cara resource naming di endpoint, penerapan HTTP verb, dan pengembalian response code yang sesuai
- Naming resources harus menggunakan plural
- HTTP verbs yang umum digunakan adalah POST, GET, PUT, dan DELETE
- Response code berfungsi untuk memberitahukan apakah request yang diminta client memberikan respon sukses, error, atau pengalihan
- Success response berada di range 2xx
- Client error response berada di range 4xx
- Server error response berada di range 5xx
- Redirect response berada di range 3xx

## Day 2

### Node.js

- Node.js merupakan runtime untuk bahasa pemrograman JavaScript yang berjalan di operating system
- Core module merupakan sekumpulan module yang telah tersedia ketika memasang Node.js (contoh: os)
- External module merupakan sekumpulan module tambahan yang bersumber dari luar (contoh: eslint)
- Node.js memiliki module http yang dapat digunakan untuk membangun sebuah web server
- Contoh implementasi web server dengan module http:

```js
const host = "localhost";
const port = 8000;

const server = http.createServer(function (req, res) {
  res.writeHead(200);
  res.end("My first server!");
});
server.listen(port, host, () => {
  console.log(`Server is running on http://${host}:${port}`);
});
```

## Day 3

### Express JS

- Express merupakan salah satu framework untuk membangun web server dengan Node.js
- Handling request ditentukan berdasarkan HTTP method dan endpoint (route)
- Contoh implementasi route di Express:

```js
app.get("/", (request, response) => {
  response.send("response for GET request");
});
```

- Middleware merupakan suatu fungsi yang dapat disisipkan ke dalam sebuah route yang dapat memiliki kemampuan untuk melakukan sesuatu sebelum atau sesudah handler sesungguhnya dieksekusi
- Contoh implementasi middleware di Express:

```js
app.use((request, response, next) => {
  console.log(`${request.method} url:: ${request.url}`);
  next();
});
```

## Day 4 & 5

### Database Design MySQL

- Tools yang dapat digunakan untuk melakukan database design diantaranya adalah: ERD Plus, draw.io, Diagrams, dll
- Relasi dalam database diantaranya adalah: 1 to 1, 1 to m, dan m to n
- Relasi m to n akan menghasilkan sebuah tabel baru (cross reference, junction, atau apapun namanya) yang berisi primary key dari masing-masing tabel yang berelasi
- Contoh relasi 1 to 1: mahasiswa dengan kartu mahasiswa
- Contoh relasi 1 to m: mahasiswa dengan kontak
- Contoh relasi m to n: mahasiswa dengan mata kuliah
