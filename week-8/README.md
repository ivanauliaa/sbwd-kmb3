# Week 8

## Day 1
### Sequelize
ORM: Object Relational Mapper (ORM) adalah sebuah alat yang dapat membantu melakukan mapping data dari database ke suatu bahasa pemrograman atau sebaliknya

Sequelize query:
- Insert data: `Model.create()`
- Get all data: `Model.findAll()`
- Update data: `Model.update()`
- Delete data: `Model.delete()`

## Day 2
### MongoDB
MongoDB merupakan database NoSQL (non relasional)

Sama halnya dengan service-service lain, MongoDB dapat dipasang secara local ataupun di cloud, baik compute service maupun fully managed service

MongoDB data type:
- Float
- Double
- Integers
- Long
- Date
- RegExp
- String
- Binary class
- Code class
- ObjectID class
- DbRef class
- Symbol class

Membuat MongoDB connection
```js
const MongoClient = require('mongodb').MongoClient;
MongoClient.connect("mongodb://localhost:27017/exampleDb", function(err, db) {
  if(!err) {
    console.log("We are connected");
  }
});
```

Collection access
```js
const collection = db.collection('test');
```

Query
- Insert: `collection.insert({ data: 'some data' });`
- Find: `collection.find().toArray(function(err, items) {});`
- Update: `collection.update({mykey:1}, {$set:{fieldtoupdate:2}}, {w:1}, function(err, result) {});`
- Delete: `collection.remove({mykey:1});`

## Day 3
### Mongoose
Mongoose merupakan salah satu package Nodejs yang berfungsi sebagai ORM terhadap MongoDB

Connection
```js
mongoose.connect('mongodb://localhost:33333', {
useNewUrlParser:true, useUnifiedTopology:true,
dbName:'cars', user:'rootUser', pass:'pwd123'
})
```

Schema: mendefinisikan struktur dari sebuah collection
```js
client.createCollection('coll_name',{ validator:{} })
```

Model: sebuah instance dari schema dan sebagai data access object untuk melakukan operasi data di MongoDB
```js
const Car = mongoose.model('car_list',schema_obj)
```

Query
- Insert: `car_1.save()`
- Find: `Car.find(( err, results )=>{ console.log(results) }) `
- Update: `Car.findByIdAndUpdate(req.params.carId, req.body, {new: true}, (err, car) => {})`
- Delete: `Car.findByIdAndRemove(req.params.carId, (err, car) => {});`

## Day 4
### Docker
Docker merupakan salah satu container provider

Container adalah software yang secara virtual dapat mengemas dan mengisolasi aplikasi untuk deployment. Container dapat berbagi akses ke OS kernel tanpa kebutuhan tradisional untuk VM.

Dockerfile
- ADD menyalin file dari sumber di host ke sistem file container sendiri di tujuan yang ditetapkan.
- CMD dapat digunakan untuk menjalankan perintah tertentu di dalam wadah.
- ENTRYPOINT menetapkan aplikasi default untuk digunakan setiap kali wadah dibuat dengan gambar.
- ENV menetapkan variabel lingkungan.
- EXPOSE mengaitkan port tertentu untuk mengaktifkan jaringan antara wadah dan dunia luar.
- FROM mendefinisikan gambar dasar yang digunakan untuk memulai proses pembuatan.
- MAINTAINER mendefinisikan nama lengkap dan alamat email pembuat gambar.
- RUN adalah direktif pelaksana pusat untuk Dockerfiles.
- USER menetapkan UID (atau nama pengguna) yang akan menjalankan container.
- VOLUME digunakan untuk mengaktifkan akses dari wadah ke direktori pada mesin host.
- WORKDIR menetapkan jalur di mana perintah, yang didefinisikan dengan CMD, akan dieksekusi.
- LABEL memungkinkan Anda untuk menambahkan label ke gambar buruh pelabuhan Anda.

Membuat docker image
```shell
docker build -t <image_name:tag> <Dockerfile path>
```

Membuat dan menjalankan instance dari sebuah docker image (container)
- `--name`: nama container
- `--publish`: expose port
- `--environment`: environment variable
- `--detach`: run in background
```shell
docker run <image_name>
```