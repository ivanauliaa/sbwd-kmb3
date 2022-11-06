# Week 7

## Day 1
### MySQL Dasar
Data type:
- Number (int, float, decimal)
- Text (char, varchar, text, enum)
- Boolean
- Datetime (date, datetime, time, timestamp)
- Other (default, null)

DDL
- CREATE DATABASE 
- DROP DATABASE
- CREATE TABLE
- DROP TABLE
- ALTER TABLE

DML
- SELECT (mengambil data)
- INSERT (menambah data)
- UPDATE (mengubah data)
- DELETE (menghapus data)

Query
- WHERE (pengondisian)
- AND, OR, NOT (operator logika)
- ORDER BY (pengurutan)
- GROUP BY (pengelompokan)
- LIMIT (batas jumlah data)

## Day 2
### MySQL Lanjutan

Join (menggabungkan kolom dari banyak tabel):
- INNER JOIN (kedua tabel memenuhi persyaratan)
- LEFT JOIN (tabel pertama memenuhi persyaratan, jika tidak ada di tabel kedua maka diisi null)
- RIGHT JOIN (tabel kedua memenuhi persyaratan, jika tidak ada di tabel pertama maka diisi null)

Agregasi (mencari nilai baru dari sekumpulan nilai):
- MAX (nilai maksimum dari suatu kolom)
- MIN (nilai minimum dari suatu kolom)
- SUM (total nilai dari suatu kolom)
- COUNT (jumlah baris suatu kolom)
- AVG (nilai rata-rata dari suatu kolom)

Union (menggabungkan baris dari banyak tabel)

Having (pengondisian untuk data agregasi)

Like & wildcard (digunakan untuk mencari nilai yang mengadung suatu nilai yang sedang dipertimbangkan)

## Day 3
### Authentication & Authorization
Authentication: sebuah tindakan terhadap user untuk melakukan otentikasi terhadap data yang dianggap sebagai kredensial

Authorization: sebuah tindakan terhadap user untuk melakukan pengecekan hak akses terhadap suatu resource  

JWT: 
- JSON Web Token (JWT) merupakan salah satu alat untuk membantu mengimplementasikan token based authentication
- JWT memiliki 3 artifact yang dipisahkan dengan tanda titik, yaitu metadata, payload, dan signature

## Day 5
### Sequelize
ORM: Object Relational Mapper (ORM) adalah sebuah alat yang dapat membantu melakukan mapping data dari database ke suatu bahasa pemrograman atau sebaliknya

Sequelize query:
- Insert data: `Model.create()`
- Get all data: `Model.findAll()`
- Update data: `Model.update()`
- Delete data: `Model.delete()`
