# TUGAS MANDIRI 5 — SQL VS ORM

## 1. Pengertian SQL dan ORM

### SQL (Structured Query Language)

SQL adalah bahasa yang digunakan untuk berkomunikasi secara langsung dengan database. Dengan SQL, programmer dapat melakukan berbagai operasi seperti mengambil, menambahkan, mengubah, dan menghapus data.

Contoh SQL:

```sql
SELECT * FROM jadwal WHERE id = 1;
```

Perintah tersebut digunakan untuk mengambil data dari tabel `jadwal` dengan `id` bernilai 1.

### ORM (Object-Relational Mapping)

ORM adalah teknik yang memungkinkan programmer berinteraksi dengan database menggunakan objek atau kode pemrograman tanpa harus menulis SQL secara langsung.

Salah satu contoh ORM pada Node.js adalah **Prisma**.

Contoh menggunakan Prisma:

```javascript
const jadwal = await prisma.jadwal.findUnique({
  where: {
    id: 1
  }
});
```

Kode tersebut digunakan untuk mengambil satu data dari tabel `jadwal` berdasarkan `id`.

---

## 2. Contoh Operasi Menggunakan SQL

Misalnya terdapat tabel database bernama `jadwal` dengan struktur:

| id | mata_kuliah       | hari   | jam   |
| -- | ----------------- | ------ | ----- |
| 1  | Pemrograman Web   | Senin  | 08:00 |
| 2  | Basis Data        | Selasa | 10:00 |
| 3  | Kecerdasan Buatan | Rabu   | 13:00 |

Untuk mengambil data jadwal dengan `id = 1`, dapat digunakan query:

```sql
SELECT * FROM jadwal WHERE id = 1;
```

Hasil yang diperoleh:

```text
id: 1
mata_kuliah: Pemrograman Web
hari: Senin
jam: 08:00
```

SQL memberikan kontrol langsung terhadap query yang dijalankan pada database.

---

## 3. Contoh Operasi Menggunakan ORM

Jika menggunakan Prisma sebagai ORM, operasi yang sama dapat dilakukan dengan:

```javascript
const jadwal = await prisma.jadwal.findUnique({
  where: {
    id: 1
  }
});
```

Hasilnya sama dengan penggunaan SQL, yaitu mendapatkan data jadwal dengan `id = 1`.

Perbedaannya adalah programmer tidak perlu menulis query SQL secara langsung karena Prisma akan menerjemahkan kode tersebut menjadi query database.

---

## 4. Perbandingan SQL dan ORM

| Aspek                  | SQL                                | ORM                                              |
| ---------------------- | ---------------------------------- | ------------------------------------------------ |
| Cara penggunaan        | Menulis query SQL secara langsung  | Menggunakan objek dan kode pemrograman           |
| Kemudahan              | Membutuhkan pemahaman SQL          | Lebih mudah untuk programmer aplikasi            |
| Kontrol query          | Sangat tinggi                      | Sebagian besar ditangani ORM                     |
| Kecepatan pengembangan | Dapat lebih lama                   | Biasanya lebih cepat                             |
| Fleksibilitas          | Sangat fleksibel                   | Bergantung pada fitur ORM                        |
| Maintenance            | Query harus dikelola secara manual | Struktur kode lebih terintegrasi dengan aplikasi |
| Contoh                 | MySQL, PostgreSQL, SQL Server      | Prisma, Sequelize, TypeORM                       |

---

## 5. Kelebihan SQL

Beberapa kelebihan penggunaan SQL:

1. Memberikan kontrol langsung terhadap database.
2. Dapat membuat query yang kompleks.
3. Dapat mengoptimalkan query sesuai kebutuhan.
4. Cocok digunakan ketika membutuhkan kontrol penuh terhadap performa database.
5. Dapat digunakan pada berbagai jenis DBMS seperti MySQL dan PostgreSQL.

---

## 6. Kelebihan ORM

Beberapa kelebihan penggunaan ORM:

1. Mempermudah programmer dalam mengakses database.
2. Mengurangi kebutuhan untuk menulis SQL secara manual.
3. Struktur kode lebih mudah diintegrasikan dengan aplikasi.
4. Mempercepat proses pengembangan aplikasi.
5. Membantu mengurangi kesalahan dalam penulisan query.
6. Beberapa ORM menyediakan fitur migration dan schema management.

---

## 7. SQL Injection

SQL Injection adalah serangan yang terjadi ketika input dari pengguna dimasukkan ke dalam query SQL tanpa pengamanan yang baik.

Contoh query yang tidak aman:

```javascript
const query = "SELECT * FROM users WHERE username = '" + username + "'";
```

Jika input pengguna tidak divalidasi dengan benar, penyerang dapat memasukkan karakter atau perintah SQL tertentu yang dapat mengubah maksud query.

Untuk mengurangi risiko SQL Injection, programmer dapat menggunakan **parameterized query**.

Contoh:

```sql
SELECT * FROM jadwal WHERE id = ?;
```

Nilai `id` diberikan sebagai parameter secara terpisah sehingga input pengguna tidak langsung digabungkan ke dalam query SQL.

ORM juga dapat membantu mengurangi risiko SQL Injection karena sebagian besar ORM menggunakan mekanisme parameterisasi ketika menjalankan query.

---

## 8. Kesimpulan

SQL dan ORM sama-sama dapat digunakan untuk berinteraksi dengan database, tetapi memiliki pendekatan yang berbeda.

SQL memberikan kontrol langsung kepada programmer terhadap query database sehingga cocok untuk kebutuhan yang membutuhkan fleksibilitas dan optimasi query. Sementara itu, ORM memungkinkan programmer mengakses database menggunakan objek dan kode pemrograman sehingga proses pengembangan aplikasi menjadi lebih mudah dan terstruktur.

Penggunaan SQL maupun ORM harus tetap memperhatikan keamanan database, terutama terhadap SQL Injection. Penggunaan parameterized query dan fitur keamanan yang tersedia pada ORM dapat membantu meningkatkan keamanan aplikasi.

Dengan demikian, pemilihan antara SQL dan ORM dapat disesuaikan dengan kebutuhan proyek, kemampuan programmer, kompleksitas aplikasi, serta kebutuhan terhadap kontrol dan performa database.
