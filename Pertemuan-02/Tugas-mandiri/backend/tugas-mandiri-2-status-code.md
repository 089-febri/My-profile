| Status Code | Arti                  | Hasil Pengujian          | Kapan Digunakan                                    |
| ----------: | --------------------- | ------------------------ | -------------------------------------------------- |
|     **200** | OK                    | Request berhasil         | Saat request berhasil diproses                     |
|     **201** | Created               | Resource berhasil dibuat | Biasanya setelah POST berhasil membuat data        |
|     **400** | Bad Request           | Request tidak valid      | Format atau parameter request salah                |
|     **401** | Unauthorized          | Membutuhkan autentikasi  | User belum login atau kredensial/token tidak valid |
|     **403** | Forbidden             | Akses ditolak            | User tidak memiliki izin mengakses resource        |
|     **404** | Not Found             | Resource tidak ditemukan | URL/resource yang diminta tidak tersedia           |
|     **500** | Internal Server Error | Terjadi kesalahan server | Server mengalami masalah saat memproses request    |

1. Apa perbedaan 400 dan 404?

400 Bad Request berarti request yang dikirim oleh client tidak valid atau tidak dapat diproses oleh server.

Sedangkan 404 Not Found berarti request dapat dipahami, tetapi resource atau alamat yang diminta tidak ditemukan.

Singkatnya:
400 → Request-nya bermasalah          
404 → Resource-nya tidak ditemukan          

2. Apa perbedaan 401 dan 403?

401 Unauthorized berarti client belum memberikan autentikasi yang diperlukan atau kredensialnya tidak valid.
 
403 Forbidden berarti server sudah memahami identitas/request client, tetapi client tidak memiliki izin untuk mengakses resource tersebut.

Singkatnya:
401 → Belum berhasil autentikasi
403 → Tidak punya izin

3. Mengapa 500 menunjukkan masalah pada sisi server?

Karena status 500 Internal Server Error menunjukkan bahwa server mengalami kondisi atau kesalahan yang membuatnya tidak dapat menyelesaikan request dengan normal.

Contohnya bisa berupa error program, kegagalan database, atau masalah internal lainnya.

4. Apakah semua error HTTP berarti server mengalami kerusakan?

Tidak.

Tidak semua error HTTP berarti server rusak.

Contohnya:
400 → Kesalahan request dari client
401 → Masalah autentikasi
403 → Masalah izin akses
404 → Resource tidak ditemukan
500 → Kesalahan internal server

##################################### FOTO SCRENSOOT #####################################
<img width="1917" height="1198" alt="Cuplikan layar 2026-10-07 000844" src="https://github.com/user-attachments/assets/cd79b85d-daec-4dc9-96b5-51ab26ef6c5f" />
<img width="1917" height="1197" alt="Cuplikan layar 2026-10-07 000952" src="https://github.com/user-attachments/assets/72e40831-129a-4e31-afbf-011906a5dc9c" />
<img width="1917" height="1198" alt="Cuplikan layar 2026-10-07 001036" src="https://github.com/user-attachments/assets/8c8d2204-d6b7-4198-962d-116a55a731f4" />



 
 
