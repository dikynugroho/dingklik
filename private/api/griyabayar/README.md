
<a name="module_Griyabayar"></a>
## Griyabayar

* [Griyabayar](#module_Griyabayar)
    * [./page-login](#module_Griyabayar./page-login)
    * [./function-laporan](#module_Griyabayar./function-laporan)



<a name="module_Griyabayar./page-login"></a>
### Griyabayar./page-login
**Request**```GET /page-login?_id=griyabayar-YOUR_ID&user_id=YOUR_USER_ID&pass=YOUR_PASS&MAC_ADD=YOUR_MAC_ADD```**Example**```CURL http://localhost:9999/api/griyabayar/page-login?_id=griyabayar-YOUR_ID&user_id=YOUR_USER_ID&pass=YOUR_PASS&MAC_ADD=YOUR_MAC_ADD```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `griyabayar-`, wajib diisi |
| user_id | <code>String</code> | user_id/username, wajib diisi |
| pass | <code>String</code> | pass/password, wajib diisi |
| MAC_ADD | <code>String</code> | MAC_ADD/mac address terdaftar, wajib diisi |



<a name="module_Griyabayar./function-laporan"></a>
### Griyabayar./function-laporan
**Request**```GET /function-laporan?_id=YOUR_ID&tgl=YOUR_TGL&tgl2=YOUR_TGL2&type=YOUR_TYPE&order=YOUR_ORDER&waktu=YOUR_WAKTU&waktu2=YOUR_WAKTU2```**Example**```:: Contoh 1CURL http://localhost:9999/api/griyabayar/function-laporan?_id=YOUR_ID:: Contoh 2CURL http://localhost:9999/api/griyabayar/function-laporan?_id=YOUR_ID&tgl=21102020:: Contoh 3CURL http://localhost:9999/api/griyabayar/function-laporan?_id=YOUR_ID&tgl=YOUR_TGL&tgl2=YOUR_TGL2&type=YOUR_TYPE&order=YOUR_ORDER&waktu=YOUR_WAKTU&waktu2=YOUR_WAKTU2```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `griyabayar-`, wajib diisi |
| tgl | <code>String</code> | tgl, tanggal awal, format `DDMMYYYY` |
| tgl2 | <code>String</code> | tgl2, tanggal akhir, format `DDMMYYYY` |
| type | <code>String</code> | type, `0`,`1`,`2`,`3`, untuk `lengkap`,`sederhana`,`harian`,`mutasi` |
| order | <code>String</code> | order, `0`,`1`, untuk `asc`,`desc` |
| waktu | <code>String</code> | waktu, waktu awal, format `MMHH` |
| waktu2 | <code>String</code> | waktu2, waktu akhir, format `MMHH` |


