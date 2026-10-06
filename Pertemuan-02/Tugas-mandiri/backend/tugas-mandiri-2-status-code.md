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
| ---------- ---------- ---------- ----------| 
|400 → Request-nya bermasalah                |
| ---------- ---------- ---------- ----------|
|404 → Resource-nya tidak ditemukan          |

2. Apa perbedaan 401 dan 403?

401 Unauthorized berarti client belum memberikan autentikasi yang diperlukan atau kredensialnya tidak valid.
 
403 Forbidden berarti server sudah memahami identitas/request client, tetapi client tidak memiliki izin untuk mengakses resource tersebut.
 
 
