
<a name="module_Griyabayar"></a>
## Griyabayar

* [Griyabayar](#module_Griyabayar)
    * [./page-login](#module_Griyabayar./page-login)
    * [./function-laporan](#module_Griyabayar./function-laporan)
    * [./products](#module_Griyabayar./products)
    * [./format](#module_Griyabayar./format)
    * [./function-preinq](#module_Griyabayar./function-preinq)
    * [./function-inq](#module_Griyabayar./function-inq)



<a name="module_Griyabayar./page-login"></a>
### Griyabayar./page-login
**Request**```GET /page-login?_id=griyabayar-YOUR_ID&user_id=YOUR_USER_ID&pass=YOUR_PASS&MAC_ADD=YOUR_MAC_ADD```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `griyabayar-`, wajib diisi |
| user_id | <code>String</code> | user_id/username, wajib diisi |
| pass | <code>String</code> | pass/password, wajib diisi |
| MAC_ADD | <code>String</code> | MAC_ADD/mac address terdaftar, wajib diisi |

**Example**  
```CURL http://localhost:9999/api/griyabayar/page-login?_id=griyabayar-YOUR_ID&user_id=YOUR_USER_ID&pass=YOUR_PASS&MAC_ADD=YOUR_MAC_ADD```


<a name="module_Griyabayar./function-laporan"></a>
### Griyabayar./function-laporan
**Request**```GET /function-laporan?_id=YOUR_ID&tgl=YOUR_TGL&tgl2=YOUR_TGL2&type=YOUR_TYPE&order=YOUR_ORDER&waktu=YOUR_WAKTU&waktu2=YOUR_WAKTU2```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `griyabayar-`, wajib diisi |
| tgl | <code>String</code> | tgl, tanggal awal, format `DDMMYYYY` |
| tgl2 | <code>String</code> | tgl2, tanggal akhir, format `DDMMYYYY` |
| type | <code>String</code> | type, `0`,`1`,`2`,`3`, untuk `lengkap`,`sederhana`,`harian`,`mutasi` |
| order | <code>String</code> | order, `0`,`1`, untuk `asc`,`desc` |
| waktu | <code>String</code> | waktu, waktu awal, format `MMHH` |
| waktu2 | <code>String</code> | waktu2, waktu akhir, format `MMHH` |

**Example**  
```:: Contoh 1CURL http://localhost:9999/api/griyabayar/function-laporan?_id=YOUR_ID:: Contoh 2CURL http://localhost:9999/api/griyabayar/function-laporan?_id=YOUR_ID&tgl=21102020:: Contoh 3CURL http://localhost:9999/api/griyabayar/function-laporan?_id=YOUR_ID&tgl=YOUR_TGL&tgl2=YOUR_TGL2&type=YOUR_TYPE&order=YOUR_ORDER&waktu=YOUR_WAKTU&waktu2=YOUR_WAKTU2```


<a name="module_Griyabayar./products"></a>
### Griyabayar./products
**Request**```GET /products?_id=YOUR_ID```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `griyabayar-`, wajib diisi |

**Example**  
```:: Contoh 1CURL http://localhost:9999/api/griyabayar/products?_id=YOUR_ID```


<a name="module_Griyabayar./format"></a>
### Griyabayar./format
**Request**```GET /format?_id=YOUR_ID```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `griyabayar-`, wajib diisi |

**Example**  
```:: Contoh 1CURL http://localhost:9999/api/griyabayar/format?_id=YOUR_ID```


<a name="module_Griyabayar./function-preinq"></a>
### Griyabayar./function-preinq
**Request**1. Lihat list `produk` di http://localhost:9999/api/griyabayar/products?_id=YOUR_ID2. Lihat `format` transaksi di http://localhost:9999/api/griyabayar/format?_id=YOUR_ID3. Parameter pada modul ini bersifat dinamis, nama kunci boleh bebas, namun harus tetap sesuai urutan `format`, griyabayar hanya mengambil nilai pada parameter, contoh `key=value` nilai `value` saja yang digunakan, pada format terdapat keterangan `produk`/`kode_produk` ini contoh key yang sama, (biasanya kode produk ada tepat di bagian depan)4. Pada `preinq` `kode_produk`/`kode` yang terdapat pada penjelasan `nomer 3`, diganti dengan `uid````GET /function-preinq?_id=YOUR_ID```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `griyabayar-`, wajib diisi |

**Example**  
```:: Contoh 1CURL http://localhost:9999/api/griyabayar/function-preinq?_id=griyabayar-617905NunoCell&uid=800.XL&nopel=087758437457&tipe=0```


<a name="module_Griyabayar./function-inq"></a>
### Griyabayar./function-inq
**Request**1. Lihat list `produk` di http://localhost:9999/api/griyabayar/products?_id=YOUR_ID2. Lihat `format` transaksi di http://localhost:9999/api/griyabayar/format?_id=YOUR_ID3. Parameter pada modul ini bersifat dinamis, nama kunci boleh bebas, namun harus tetap sesuai urutan `format`, griyabayar hanya mengambil nilai pada parameter, contoh `key=value` nilai `value` saja yang digunakan, pada format terdapat keterangan `produk`/`kode_produk` ini contoh key yang sama, (biasanya kode produk ada tepat di bagian depan)```GET /function-inq?_id=YOUR_ID```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `griyabayar-`, wajib diisi |

**Example**  
```:: Contoh 1CURL http://localhost:9999/api/griyabayar/function-inq?_id=griyabayar-617905NunoCell&kode_produk=800&nopel=087758437457&source=&kode=&harga=6050&cetak=0```

