# TUGAS MANDIRI 4 — POSTMAN DAN CURL

## 1. Pengujian GET Menggunakan Postman

Pengujian pertama dilakukan menggunakan Postman dengan method GET dan URL:

```text
https://httpbin.org/get
```

Setelah request dikirim, server memberikan status **200 OK**. Response berisi informasi mengenai request yang dikirim, seperti `args`, `headers`, `origin`, dan `url`.

Pengujian ini menunjukkan bahwa Postman dapat digunakan untuk mengirim HTTP request dan melihat response dari server.

**Screenshot:** hasil pengujian GET menggunakan Postman.

---

## 2. Pengujian POST Menggunakan Postman

Pengujian kedua dilakukan menggunakan method POST dengan URL:

```text
https://httpbin.org/post
```

Data dikirim melalui **Body → raw → JSON**:

```json
{
  "nama": "Umar",
  "kelas": "Informatika"
}
```

Setelah request dikirim, server memberikan status **200 OK**. Data yang dikirim dapat ditemukan kembali pada bagian `json` dalam response HTTPBin.

Hal ini menunjukkan bahwa Postman berhasil mengirim data JSON melalui request body dan HTTPBin berhasil menerima data tersebut.

**Screenshot:** hasil pengujian POST menggunakan Postman.

---

## 3. Pengujian curl dengan Parameter -i

Pengujian berikutnya dilakukan menggunakan curl melalui terminal dengan perintah:

```bash
curl -i https://httpbin.org/get
```

Parameter `-i` digunakan untuk menampilkan HTTP response header bersamaan dengan response body.

Hasil pengujian menunjukkan status **200 OK** dan menampilkan header serta data JSON dari HTTPBin.

**Screenshot:** hasil perintah `curl -i`.

---

## 4. Pengujian curl dengan Parameter -s

Pengujian selanjutnya dilakukan menggunakan:

```bash
curl -s https://httpbin.org/get
```

Parameter `-s` atau `--silent` digunakan agar curl tidak menampilkan progress meter selama proses request.

Response yang ditampilkan berisi data JSON dari HTTPBin tanpa tampilan progress meter.

**Screenshot:** hasil perintah `curl -s`.

---

## 5. Perbandingan Postman dan curl

Postman dan curl sama-sama dapat digunakan untuk mengirim HTTP request kepada server, tetapi memiliki cara penggunaan yang berbeda.

Postman merupakan aplikasi dengan antarmuka grafis atau GUI sehingga konfigurasi method, URL, header, dan body dapat dilakukan melalui menu. Postman lebih mudah digunakan untuk pemula dan cocok untuk melakukan pengujian API secara visual.

Sementara itu, curl merupakan command-line tool yang digunakan melalui terminal. Request dilakukan dengan mengetikkan perintah secara langsung. curl lebih ringan dan dapat digunakan dalam script maupun proses otomatisasi.

Contoh request GET menggunakan Postman:

```text
GET https://httpbin.org/get
```

Sedangkan menggunakan curl:

```bash
curl -i https://httpbin.org/get
```

Keduanya digunakan untuk mengirim request GET ke endpoint yang sama.

---

## 6. Kesimpulan

Berdasarkan pengujian yang dilakukan, Postman dan curl dapat digunakan untuk melakukan pengujian REST API. Postman lebih mudah digunakan karena memiliki antarmuka grafis, sedangkan curl lebih praktis untuk penggunaan melalui terminal dan otomatisasi.

Parameter `-i` pada curl digunakan untuk menampilkan response header dan body, sedangkan parameter `-s` digunakan untuk menjalankan curl dalam mode silent tanpa menampilkan progress meter.

########################################### FOTO SCRENSOOT ###########################################
UNTUK YG GET:
<img width="1916" height="1197" alt="Cuplikan layar 2026-10-07 014523" src="https://github.com/user-attachments/assets/f836e6b3-f451-4b23-bd37-89e7b3ba4c72" />
UNTUK YG POST:
<img width="1916" height="1196" alt="Cuplikan layar 2026-10-07 014640" src="https://github.com/user-attachments/assets/4c4df759-b336-4da9-b75e-a59d3ba9fe4c" />
UNTUK YG CRUL -i:
<img width="1917" height="1195" alt="Cuplikan layar 2026-10-07 014829" src="https://github.com/user-attachments/assets/77c16d0b-294a-4032-aa5c-8b8ff17e9a1f" />
UNTUK YG CRUL -S:
<img width="1917" height="1198" alt="Cuplikan layar 2026-10-07 015004" src="https://github.com/user-attachments/assets/5caa6a23-7f03-4411-9dc5-d3384073642a" />

