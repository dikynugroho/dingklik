
<a name="module_Griyabayar"></a>
## Griyabayar

* [Griyabayar](#module_Griyabayar)
    * _@_
        * [.@](#module_Griyabayar.@)
    * _Service_
        * [./page-login](#module_Griyabayar./page-login)
        * [./function-laporan](#module_Griyabayar./function-laporan)
        * [./products](#module_Griyabayar./products)
        * [./format](#module_Griyabayar./format)
        * [./function-preinq](#module_Griyabayar./function-preinq)
        * [./function-inq](#module_Griyabayar./function-inq)
        * [./function-pay](#module_Griyabayar./function-pay)



<a name="module_Griyabayar.@"></a>
### Griyabayar.@
**Akses lebih dari 1 Akun**query `_id` digunakan untuk identifikasi lebih akun yang berbeda```GET api/griyabayar?_id=griyabayar-YOUR_ID```**Example**```:: Contoh akun 1CURL http://localhost:9999/api/griyabayar/page-login?_id=griyabayar-akun1:: Contoh akun 2CURL http://localhost:9999/api/griyabayar/page-login?_id=griyabayar-akun2```**Cluster transaksi**jika `_id` tidak diatur, akan dikirimkan ke terminal secara bergantian**Example**```:: Contoh 10 transaksi, dikirim ke 3 akunCURL http://localhost:9999/api/griyabayar/function-inq:: Terminal Akun1 -> Transaksi 1:: Terminal Akun2 -> Transaksi 2:: Terminal Akun3 -> Transaksi 3:: Terminal Akun1 -> Transaksi 4:: Terminal Akun2 -> Transaksi 5:: Terminal Akun3 -> Transaksi 6:: Terminal Akun1 -> Transaksi 7:: Terminal Akun2 -> Transaksi 8:: Terminal Akun3 -> Transaksi 9:: Terminal Akun1 -> Transaksi 10```



<a name="module_Griyabayar./page-login"></a>
### Griyabayar./page-login
**Request**Copy MAC_ADD dari komputer dengan cara```:: ctrl + r untuk membuka window run:: ketik cmd dan enter:: ketik getmac dan enter:: hasilPhysical Address    Transport Name=================== ==========================================================E8-39-35-31-26-5C   Media disconnected18-5E-0F-4A-C2-25   \Device\Tcpip_{D0378E1D-7B76-474A-A89D-45306B6AFAEF}1A-5E-0F-4A-C2-25   \Device\Tcpip_{F9FDE298-5E5E-4014-8BC0-ADD294C36714}0A-00-27-00-00-04   \Device\Tcpip_{2536FBEE-5CA3-4167-9CC6-59EE90911CB9}0A-00-27-00-00-0B   \Device\Tcpip_{7E38EC38-F41F-48E8-BC85-CA807BD2B779}:: ambil Physical Address saja:: ubah tanda - dengan ::: tambahkan ~ diantara macE8:39:35:31:26:5C~18:5E:0F:4A:C2:25~1A:5E:0F:4A:C2:25~0A:00:27:00:00:04~0A:00:27:00:00:0B:: jadikan 1 barisE8:39:35:31:26:5C~18:5E:0F:4A:C2:25~1A:5E:0F:4A:C2:25~0A:00:27:00:00:04~0A:00:27:00:00:0B:: selesai``````GET /page-login?_id=griyabayar-YOUR_ID&user_id=YOUR_USER_ID&pass=YOUR_PASS&MAC_ADD=YOUR_MAC_ADD```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `griyabayar-`, wajib diisi |
| user_id | <code>String</code> | user_id/username, wajib diisi |
| pass | <code>String</code> | pass/password, wajib diisi |
| MAC_ADD | <code>String</code> | MAC_ADD/mac address terdaftar, wajib diisi |

**Example**  
```CURL http://localhost:9999/api/griyabayar/page-login?_id=griyabayar-YOUR_ID&user_id=YOUR_USER_ID&pass=YOUR_PASS&MAC_ADD=E8:39:35:31:26:5C~18:5E:0F:4A:C2:25~1A:5E:0F:4A:C2:25~0A:00:27:00:00:04~0A:00:27:00:00:0B```


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
**Request**1. Cek format transaksi di http://localhost:9999/api/griyabayar/format?_id=YOUR_ID2. Cek list produk di http://localhost:9999/api/griyabayar/products?_id=YOUR_ID3. Pastikan urutan parameter sesuai dengan format, griyabayar hanya mengambil nilai sesuai urutan pada format, nama parameter di format boleh menggunakan nama bebas4. `kode_produk`,`produk` atau parameter pertama pada format ganti dengan uid, lihat uid di list produk```GET /function-preinq?_id=YOUR_ID```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `griyabayar-`, wajib diisi |
| uid | <code>String</code> | wajib diisi |

**Example**  
```:: Contoh 1CURL http://localhost:9999/api/griyabayar/function-preinq?_id=griyabayar-617905NunoCell&uid=800.TSEL&nopel=085220878457&tipe=0```


<a name="module_Griyabayar./function-inq"></a>
### Griyabayar./function-inq
**Request**1. Cek format transaksi di http://localhost:9999/api/griyabayar/format?_id=YOUR_ID2. Cek list produk di http://localhost:9999/api/griyabayar/products?_id=YOUR_ID3. Pastikan urutan parameter sesuai dengan format, griyabayar hanya mengambil nilai sesuai urutan pada format, nama parameter di format boleh menggunakan nama bebas4. `kode_produk`,`produk` atau parameter pertama pada format ganti dengan uid, lihat uid di list produk```GET /function-inq?_id=YOUR_ID```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `griyabayar-`, wajib diisi |
| uid | <code>String</code> | wajib diisi |

**Example**  
```:: Contoh 1CURL http://localhost:9999/api/griyabayar/function-inq?_id=griyabayar-617905NunoCell&uid=800.TSEL&nopel=085220878457&source=1&kode=TSEL1&harga=1425&cetak=0```


<a name="module_Griyabayar./function-pay"></a>
### Griyabayar./function-pay
**Request**1. Cek format transaksi di http://localhost:9999/api/griyabayar/format?_id=YOUR_ID2. Cek list produk di http://localhost:9999/api/griyabayar/products?_id=YOUR_ID3. Pastikan urutan parameter sesuai dengan format, griyabayar hanya mengambil nilai sesuai urutan pada format, nama parameter di format boleh menggunakan nama bebas4. `kode_produk`,`produk` atau parameter pertama pada format ganti dengan uid, lihat uid di list produk```GET /function-pay?_id=YOUR_ID```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `griyabayar-`, wajib diisi |
| uid | <code>String</code> | wajib diisi |

**Example**  
```:: Contoh 1CURL http://localhost:9999/api/griyabayar/function-pay?_id=griyabayar-617905NunoCell&uid=800.TSEL&nopel=085220878457&source=1&kode=TSEL5&harga=5700&cetak=0```

