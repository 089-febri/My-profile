Method
GET
URL
https://httpbin.org/get
Tujuan
Menguji request GET dan melihat informasi request
yang diterima oleh server HTTPBin.
Data yang dikirim

Untuk GET pertama ini:

Tidak ada request body.
Status
200 OK
Hasil

HTTPBin mengembalikan informasi request dalam bentuk JSON, seperti query parameter, header, alamat origin, dan URL yang digunakan.



######################################### HTTP Method GET #########################################

GET merupakan HTTP Method yang digunakan untuk mengambil atau meminta data dari server. Pada praktikum ini, pengujian dilakukan menggunakan Postman dengan URL `https://httpbin.org/get`.

Setelah request dikirim menggunakan method GET, server memberikan response dengan status **200 OK**. Status tersebut menunjukkan bahwa request berhasil diterima dan diproses oleh server.

Response dari HTTPBin berisi informasi mengenai request yang dikirim, seperti `args`, `headers`, `origin`, dan `url`. Bagian `args` digunakan untuk menampilkan query parameter yang dikirim melalui URL. Karena pada pengujian awal tidak terdapat query parameter, maka nilai `args` kosong.

GET umumnya digunakan untuk mengambil atau membaca data dan tidak digunakan untuk mengubah data pada server. Data pada GET dapat dikirim melalui query parameter, contohnya `https://httpbin.org/get?nama=Febri&kelas=Informatika`.

Dengan demikian, pengujian GET menunjukkan bahwa client dapat meminta informasi kepada server melalui HTTP Method GET dan server memberikan response sesuai dengan request yang diterima.



######################################### HTTP Method POST #########################################

POST merupakan HTTP Method yang digunakan untuk mengirim data dari client ke server. POST umumnya digunakan untuk membuat atau menambahkan data baru pada suatu sistem.

Pada praktikum ini, pengujian POST dilakukan menggunakan Postman dengan URL `https://httpbin.org/post`. Data dikirim melalui **Body → raw → JSON** dengan contoh data:

```json
{
  "nama": "Febri",
  "kelas": "Informatika"
}
```

Setelah request dikirim, HTTPBin memberikan response dengan status **200 OK**. Status tersebut menunjukkan bahwa request berhasil diterima dan diproses oleh server.

Data yang dikirim dapat dilihat kembali pada bagian `json` di response HTTPBin. Hal tersebut menunjukkan bahwa HTTPBin berhasil menerima data JSON yang dikirim melalui request body.

Berbeda dengan GET yang digunakan untuk mengambil data, POST digunakan untuk mengirim data ke server dan pada API sebenarnya dapat digunakan untuk membuat data baru. Namun, HTTPBin tidak menyimpan data tersebut ke dalam database karena HTTPBin merupakan layanan untuk pengujian HTTP request dan response.

Dengan demikian, pengujian POST menunjukkan bagaimana client dapat mengirim data dalam bentuk JSON melalui request body kepada server dan menerima response dari server.



######################################### HTTP Method POST #########################################

POST merupakan HTTP Method yang digunakan untuk mengirim data dari client ke server. POST umumnya digunakan untuk membuat atau menambahkan data baru pada suatu sistem.

Pada praktikum ini, pengujian POST dilakukan menggunakan Postman dengan URL `https://httpbin.org/post`. Data dikirim melalui **Body → raw → JSON** dengan contoh data:

```json
{
  "nama": "Febri",
  "kelas": "Informatika"
}
```

Setelah request dikirim, HTTPBin memberikan response dengan status **200 OK**. Status tersebut menunjukkan bahwa request berhasil diterima dan diproses oleh server.

Data yang dikirim dapat dilihat kembali pada bagian `json` di response HTTPBin. Hal tersebut menunjukkan bahwa HTTPBin berhasil menerima data JSON yang dikirim melalui request body.

Berbeda dengan GET yang digunakan untuk mengambil data, POST digunakan untuk mengirim data ke server dan pada API sebenarnya dapat digunakan untuk membuat data baru. Namun, HTTPBin tidak menyimpan data tersebut ke dalam database karena HTTPBin merupakan layanan untuk pengujian HTTP request dan response.

Dengan demikian, pengujian POST menunjukkan bagaimana client dapat mengirim data dalam bentuk JSON melalui request body kepada server dan menerima response dari server.



######################################### HTTP Method PATCH #########################################

PATCH merupakan HTTP Method yang digunakan untuk memperbarui sebagian data atau resource yang sudah ada pada server. PATCH disebut sebagai metode untuk melakukan **partial update**, karena client hanya perlu mengirimkan bagian data yang ingin diubah.

Pada praktikum ini, pengujian PATCH dilakukan menggunakan Postman dengan URL `https://httpbin.org/patch`. Data dikirim melalui **Body → raw → JSON**. Contoh data yang dikirim adalah:

```json
{
  "kelas": "Informatika"
}
```

Data tersebut hanya berisi atribut `kelas` karena tujuan pengujian adalah menunjukkan bahwa PATCH dapat digunakan untuk mengubah sebagian data tanpa harus mengirimkan seluruh data.

Setelah request dikirim, HTTPBin memberikan response dengan status **200 OK**. Status tersebut menunjukkan bahwa request PATCH berhasil diterima dan diproses oleh server. Data yang dikirim juga dapat dilihat kembali pada bagian `json` dalam response.

PATCH berbeda dengan PUT. PUT umumnya digunakan untuk memperbarui atau mengganti representasi resource secara keseluruhan, sedangkan PATCH digunakan untuk memperbarui sebagian data dari suatu resource.

Perlu diketahui bahwa HTTPBin tidak benar-benar menyimpan perubahan ke database. HTTPBin hanya digunakan untuk menguji dan melihat request serta response HTTP.

Dengan demikian, pengujian PATCH menunjukkan bagaimana client dapat mengirim perubahan sebagian data melalui request body menggunakan HTTP Method PATCH.



######################################### HTTP Method DELETE #########################################
DELETE merupakan HTTP Method yang digunakan untuk menghapus suatu data atau resource dari server. Method ini biasanya digunakan ketika client ingin menghapus data yang sudah tidak diperlukan.

Pada praktikum ini, pengujian DELETE dilakukan menggunakan Postman dengan URL `https://httpbin.org/delete`. Request dikirim tanpa menggunakan request body karena pada pengujian ini tidak diperlukan data tambahan.

Setelah request dikirim, HTTPBin memberikan response dengan status **200 OK**. Status tersebut menunjukkan bahwa request DELETE berhasil diterima dan diproses oleh server. Response dari HTTPBin berisi informasi mengenai request yang diterima, seperti URL, headers, dan informasi lainnya.

Pada API sebenarnya, DELETE dapat digunakan untuk menghapus data tertentu dari database, misalnya `DELETE /users/1` yang berarti menghapus user dengan ID 1. Namun, pada praktikum ini HTTPBin tidak benar-benar menghapus data karena HTTPBin merupakan layanan yang digunakan untuk menguji HTTP request dan response.

Dengan demikian, pengujian DELETE menunjukkan bagaimana client dapat mengirim request untuk melakukan proses penghapusan resource menggunakan HTTP Method DELETE.



| No | Method | Endpoint  | Data yang dikirim | Status | Hasil                                                              |
| -: | ------ | --------- | ----------------- | ------ | ------------------------------------------------------------------ |
|  1 | GET    | `/get`    | Query parameter   | 200    | Server mengembalikan informasi request                             |
|  2 | POST   | `/post`   | JSON/body         | 200    | Server menerima dan mengembalikan data JSON                        |
|  3 | PUT    | `/put`    | JSON/body         | 200    | Server menerima dan mengembalikan data PUT                         |
|  4 | PATCH  | `/patch`  | JSON/body         | 200    | Server menerima dan mengembalikan data PATCH                       |
|  5 | DELETE | `/delete` | -                 | 200    | Server menerima request DELETE dan mengembalikan informasi request |


######################################### (FOTO Screenshot) #########################################
<img width="1917" height="1198" alt="Cuplikan layar 2026-10-06 234325" src="https://github.com/user-attachments/assets/b8d79274-66a9-4cb4-a161-475ea858864b" />
<img width="1917" height="1197" alt="Cuplikan layar 2026-10-06 235355" src="https://github.com/user-attachments/assets/399a1297-d306-47dc-9014-92e138a7d8f0" />
<img width="1917" height="1197" alt="Cuplikan layar 2026-10-06 235355" src="https://github.com/user-attachments/assets/6f278151-74d2-4f42-a753-373d23ad2918" />
<img width="1917" height="1198" alt="Cuplikan layar 2026-10-06 235534" src="https://github.com/user-attachments/assets/ac183dc2-3d81-4b8d-8310-1f0644ba4e09" />
<img width="1917" height="1198" alt="Cuplikan layar 2026-10-07 000117" src="https://github.com/user-attachments/assets/af3954fc-40b0-4ebe-b095-317d323f5301" />
