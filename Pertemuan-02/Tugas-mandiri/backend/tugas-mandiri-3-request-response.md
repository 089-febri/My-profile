# TUGAS MANDIRI 3 — MEMAHAMI REQUEST DAN RESPONSE

## 1. Pengujian GET /get

Pengujian pertama dilakukan menggunakan Postman dengan method GET dan URL:

```text
https://httpbin.org/get
```

Hasil pengujian menunjukkan status **200 OK**, yang berarti request berhasil diterima dan diproses oleh server. Response dari HTTPBin menampilkan informasi mengenai request yang dikirim, seperti `args`, `headers`, `origin`, dan `url`.

Pada pengujian ini, bagian `args` bernilai kosong karena tidak terdapat query parameter pada URL.

**Screenshot:** hasil pengujian GET `/get`.

---

## 2. Pengujian GET dengan Query Parameter

Pengujian kedua menggunakan URL:

```text
https://httpbin.org/get?nama=Umar&kelas=TI
```

Hasil pengujian menunjukkan status **200 OK**. Pada response terdapat bagian `args` yang menampilkan:

```json
{
  "nama": "Umar",
  "kelas": "TI"
}
```

Data tersebut merupakan query parameter yang dikirim melalui URL.

Query parameter adalah data yang ditambahkan pada URL setelah tanda `?`. Jika terdapat lebih dari satu parameter, setiap parameter dipisahkan menggunakan tanda `&`.

---

## 3. Pengujian HTTP Header

Pengujian ketiga dilakukan menggunakan:

```text
GET https://httpbin.org/headers
```

Hasil pengujian menunjukkan status **200 OK** dan response menampilkan berbagai informasi HTTP Header yang diterima oleh HTTPBin.

Contoh header yang dapat ditampilkan adalah `User-Agent`, `Accept`, dan `Host`.

**Screenshot:** hasil pengujian `/headers`.

---

## 4. Pengertian Request

Request adalah permintaan yang dikirim oleh client kepada server untuk meminta atau melakukan suatu proses. Dalam praktikum ini, Postman bertindak sebagai client yang mengirimkan request kepada HTTPBin.

Contohnya:

```text
GET https://httpbin.org/get
```

merupakan sebuah HTTP request.

---

## 5. Pengertian Response

Response adalah balasan yang diberikan oleh server setelah menerima dan memproses request dari client.

Contohnya adalah:

```text
200 OK
```

yang menunjukkan bahwa request berhasil diproses. Response juga dapat berisi data dalam bentuk JSON.

---

## 6. Pengertian Query Parameter

Query parameter adalah data yang dikirimkan melalui URL. Query parameter ditulis setelah tanda `?` dan jika terdapat beberapa parameter, setiap parameter dipisahkan dengan tanda `&`.

Contohnya:

```text
https://httpbin.org/get?nama=Umar&kelas=TI
```

Pada URL tersebut terdapat dua query parameter, yaitu:

```text
nama = Umar
kelas = TI
```

---

## 7. Pengertian HTTP Header

HTTP Header merupakan informasi tambahan yang dikirim bersama HTTP request atau response. Header dapat digunakan untuk memberikan informasi mengenai request, client, format data, autentikasi, dan informasi lainnya.

Contohnya:

```text
User-Agent
Accept
Host
Content-Type
Authorization
```

---

## 8. Perbedaan Data pada URL dan Request Body

Data yang dikirim melalui URL biasanya menggunakan query parameter. Contohnya:

```text
https://httpbin.org/get?nama=Umar&kelas=TI
```

Sedangkan data pada request body dikirim di dalam isi request, seperti ketika menggunakan POST dengan format JSON:

```json
{
  "nama": "Febri",
  "kelas": "Informatika"
}
```

Perbedaannya adalah query parameter berada pada URL, sedangkan request body berada pada isi request. Query parameter sering digunakan untuk memberikan parameter pencarian atau penyaringan data, sedangkan request body umumnya digunakan untuk mengirim data yang akan diproses atau dibuat oleh server.

########################################## FOTO SCRENSOOT #########################################
UNTUK YG GET:
<img width="1916" height="1198" alt="Cuplikan layar 2026-10-07 013158" src="https://github.com/user-attachments/assets/0ba50991-e709-4918-9af5-2353624e4702" />

UNTUK YG HEADEARS:
<img width="1917" height="1198" alt="Cuplikan layar 2026-10-07 013400" src="https://github.com/user-attachments/assets/1730a81d-87fc-4d89-8643-8be4d62c47b6" />

