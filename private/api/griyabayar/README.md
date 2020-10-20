
<a name="module_Griyabayar"></a>
## Griyabayar

* [Griyabayar](#module_Griyabayar)
    * [./page-login](#module_Griyabayar./page-login)
    * [./function-laporan](#module_Griyabayar./function-laporan)



<a name="module_Griyabayar./page-login"></a>
### Griyabayar./page-login
**Request**```GET /page-login?_id=griyabayar-YOUR_USER_ID&user_id=YOUR_USER_ID&pass=YOUR_PASS&MAC_ADD=YOUR_MAC_ADD```


| Param | Type | Description |
| --- | --- | --- |
| user_id | <code>String</code> | di `query`, required `true`, username |
| pass | <code>String</code> | di `query`, required `true`, password |
| MAC_ADD | <code>String</code> | di `query`, mac address komputer yang terdaftar di griyabayar |
| _id | <code>String</code> | di `query`, dibutuhkan `true`, awalan `griyabayar-`, digunakan untuk akses lebih dari 1 akun |

**Example**  
```:: LoginCURL http://localhost:9999/api/griyabayar/page-login?_id=griyabayar-YOUR_USER_ID&user_id=YOUR_USER_ID&pass=YOUR_PASSWORD:: Login dengan mac addressCURL http://localhost:9999/api/griyabayar/page-login?_id=griyabayar-YOUR_USER_ID&user_id=YOUR_USER_ID&pass=YOUR_PASSWORD&MAC_ADD=E8:39:35:31:26:5C~18:5E:0F:4A:C2:25~1A:5E:0F:4A:C2:25~0A:00:27:00:00:04~0A:00:27:00:00:0B```


<a name="module_Griyabayar./function-laporan"></a>
### Griyabayar./function-laporan
**Request**```GET /function-laporan?_id=griyabayar-YOUR_USER_ID```


| Param | Type | Description |
| --- | --- | --- |
| tgl | <code>String</code> | di `query`, format `DDMMYYYY`, tanggal awal |
| tgl2 | <code>String</code> | di `query`, format `DDMMYYYY`, tanggal akhir |
| type | <code>String</code> | di `query`, nilai `0`/`1`/`2`/`3`, untuk `lengkap`/`sederhana`/`harian`/`mutasi` |
| order | <code>String</code> | di `query`, nilai `0`/`1`, untuk `asc`/`desc` |
| waktu | <code>String</code> | di `query`, format `HHMM`, waktu awal |
| waktu2 | <code>String</code> | di `query`, format `HHMM`, waktu akhir |
| _id | <code>String</code> | di `query`, dibutuhkan `true`, awalan `griyabayar-`, digunakan untuk akses lebih dari 1 akun |

**Example**  
```CURL http://localhost:9999/api/griyabayar/function-laporan?_id=griyabayar-YOUR_USER_ID&tgl=01102020```

