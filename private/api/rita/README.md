
<a name="module_Rita"></a>
## Rita

* [Rita](#module_Rita)
    * _@_
        * [.@](#module_Rita.@)
    * _Service_
        * [./login/otp-request](#module_Rita./login/otp-request)
        * [./oauth/token](#module_Rita./oauth/token)
        * [./homescreen/profile](#module_Rita./homescreen/profile)
        * [./homescreen/home](#module_Rita./homescreen/home)
        * [./balloon](#module_Rita./balloon)
        * [./transaction/get](#module_Rita./transaction/get)
        * [./notification/get](#module_Rita./notification/get)
        * [./notification/read-update](#module_Rita./notification/read-update)
        * [./profile/home](#module_Rita./profile/home)
        * [./profile/profile](#module_Rita./profile/profile)
        * [./product/get-product/:path](#module_Rita./product/get-product/_path)
        * [./product/activation-product-frc](#module_Rita./product/activation-product-frc)
        * [./product/activation-product-spv](#module_Rita./product/activation-product-spv)
        * [./product/activation-product-recharges](#module_Rita./product/activation-product-recharges)
        * [./ligaSuper/checkKPK](#module_Rita./ligaSuper/checkKPK)
        * [./ligaSuper/checkSPV](#module_Rita./ligaSuper/checkSPV)



<a name="module_Rita.@"></a>
### Rita.@
**Akses lebih dari 1 Akun**query `_id` digunakan untuk identifikasi lebih akun yang berbeda```GET api/rita?_id=rita-YOUR_ID```**Example**```:: Contoh akun 1CURL http://localhost:9999/api/rita/user/auth/v2?_id=rita-akun1:: Contoh akun 2CURL http://localhost:9999/api/rita/user/auth/v2?_id=rita-akun2```**Cluster transaksi**jika `_id` tidak diatur, akan dikirimkan ke terminal secara bergantian**Example**```:: Contoh 10 transaksi, dikirim ke 3 akunCURL http://localhost:9999/api/rita/recharge:: Terminal Akun1 -> Transaksi 1:: Terminal Akun2 -> Transaksi 2:: Terminal Akun3 -> Transaksi 3:: Terminal Akun1 -> Transaksi 4:: Terminal Akun2 -> Transaksi 5:: Terminal Akun3 -> Transaksi 6:: Terminal Akun1 -> Transaksi 7:: Terminal Akun2 -> Transaksi 8:: Terminal Akun3 -> Transaksi 9:: Terminal Akun1 -> Transaksi 10```



<a name="module_Rita./login/otp-request"></a>
### Rita./login/otp-request
**Request**```GET /login/otp-request?_id=```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `rita-`, wajib diisi, digunakan untuk akses lebih dari 1 akun |
| msisdn | <code>String</code> | wajib diisi, MSISDN Pemilik Toko |
| qrCode | <code>String</code> | wajib diisi, ID Retailer |

**Example**  
```CURL http://localhost:9999/api/rita/login/otp-request?_id=rita-00037261&msisdn=&qrCode=```


<a name="module_Rita./oauth/token"></a>
### Rita./oauth/token
**Request**```GET /oauth/token?_id=```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `rita-`, wajib diisi, digunakan untuk akses lebih dari 1 akun |
| username | <code>String</code> | wajib diisi, MSISDN Pemilik Toko |
| password | <code>String</code> | wajib diisi, Kode OTP |
| qrCode | <code>String</code> | wajib diisi, ID Retailer |

**Example**  
```CURL http://localhost:9999/api/rita/oauth/token?_id=rita-00037261&username=&password=&qrCode=```


<a name="module_Rita./homescreen/profile"></a>
### Rita./homescreen/profile
**Request**```GET /homescreen/profile?_id=```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `rita-`, wajib diisi, digunakan untuk akses lebih dari 1 akun |

**Example**  
```CURL http://localhost:9999/api/rita/homescreen/profile?_id=rita-00037261```


<a name="module_Rita./homescreen/home"></a>
### Rita./homescreen/home
**Request**```GET /homescreen/home?_id=```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `rita-`, wajib diisi, digunakan untuk akses lebih dari 1 akun |

**Example**  
```CURL http://localhost:9999/api/rita/homescreen/home?_id=rita-00037261```


<a name="module_Rita./balloon"></a>
### Rita./balloon
**Request**```GET /balloon?_id=```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `rita-`, wajib diisi, digunakan untuk akses lebih dari 1 akun |

**Example**  
```CURL http://localhost:9999/api/rita/balloon?_id=rita-00037261```


<a name="module_Rita./transaction/get"></a>
### Rita./transaction/get
**Request**```GET /transaction/get?_id=```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `rita-`, wajib diisi, digunakan untuk akses lebih dari 1 akun |

**Example**  
```CURL http://localhost:9999/api/rita/transaction/get?_id=rita-00037261```


<a name="module_Rita./notification/get"></a>
### Rita./notification/get
**Request**```GET /notification/get?_id=```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `rita-`, wajib diisi, digunakan untuk akses lebih dari 1 akun |

**Example**  
```CURL http://localhost:9999/api/rita/notification/get?_id=rita-00037261```


<a name="module_Rita./notification/read-update"></a>
### Rita./notification/read-update
**Request**```GET /notification/read-update?_id=```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `rita-`, wajib diisi, digunakan untuk akses lebih dari 1 akun |
| id | <code>String</code> | wajib diisi |

**Example**  
```CURL http://localhost:9999/api/rita/notification/read-update?_id=rita-00037261```


<a name="module_Rita./profile/home"></a>
### Rita./profile/home
**Request**```GET /profile/home?_id=```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `rita-`, wajib diisi, digunakan untuk akses lebih dari 1 akun |

**Example**  
```CURL http://localhost:9999/api/rita/profile/home?_id=rita-00037261```


<a name="module_Rita./profile/profile"></a>
### Rita./profile/profile
**Request**```GET /profile/profile?_id=```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `rita-`, wajib diisi, digunakan untuk akses lebih dari 1 akun |

**Example**  
```CURL http://localhost:9999/api/rita/profile/profile?_id=rita-00037261```


<a name="module_Rita./product/get-product/_path"></a>
### Rita./product/get-product/:path
**Request**```GET /product/get-product/:path?_id=```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `rita-`, wajib diisi, digunakan untuk akses lebih dari 1 akun |

**Example**  
```:: param :path:: 0 = kpk produk:: 2 = mixmax:: 1 = spv blank produk:: 5 = spv 0:: 3 = pulsa/mobiledata/addonCURL http://localhost:9999/api/rita/product/get-product/0?_id=rita-00037261CURL http://localhost:9999/api/rita/product/get-product/2?_id=rita-00037261CURL http://localhost:9999/api/rita/product/get-product/1?_id=rita-00037261CURL http://localhost:9999/api/rita/product/get-product/5?_id=rita-00037261CURL http://localhost:9999/api/rita/product/get-product/3?_id=rita-00037261```


<a name="module_Rita./product/activation-product-frc"></a>
### Rita./product/activation-product-frc
**Request**```GET /product/activation-product-frc?_id=```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `rita-`, wajib diisi, digunakan untuk akses lebih dari 1 akun |
| code | <code>String</code> | boleh kosong, boleh diulang |
| price | <code>String</code> | boleh kosong, boleh diulang |
| msisdn | <code>String</code> | wajib diisi, boleh diulang |
| pin | <code>String</code> | wajib diisi |
| productCode | <code>String</code> | wajib diisi |
| productPrice | <code>String</code> | wajib diisi |
| trxMsisdn | <code>String</code> | wajib diisi |

**Example**  
```:: Contoh 1, tanpa addon &code=&price=CURL http://localhost:9999/api/rita/product/activation-product-frc?_id=rita-00037261&msisdn=&pin=&productCode=&productPrice=&trxMsisdn= :: Contoh 2, dengan addonCURL http://localhost:9999/api/rita/product/activation-product-frc?_id=rita-00037261&code=&price=&msisdn=&pin=&productCode=&productPrice=&trxMsisdn= :: Contoh 2, dengan addon, lebih dari 1 produk max 3CURL http://localhost:9999/api/rita/product/activation-product-frc?_id=rita-00037261&code=&price=&code=&price=&code=&price=&msisdn=&pin=&productCode=&productPrice=&trxMsisdn= ```


<a name="module_Rita./product/activation-product-spv"></a>
### Rita./product/activation-product-spv
**Request**```GET /product/activation-product-spv?_id=```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `rita-`, wajib diisi, digunakan untuk akses lebih dari 1 akun |
| pin | <code>String</code> | wajib diisi |
| productCode | <code>String</code> | wajib diisi, untuk `SPVBLANK` |
| productPrice | <code>String</code> | wajib diisi, untuk `SPVBLANK` |
| qrVoucher | <code>String</code> | wajib diisi, untuk `SPVBLANK`, boleh diulang |
| price | <code>String</code> | wajib diisi, untuk `SPV0`, boleh diulang |
| voucher | <code>String</code> | wajib diisi, untuk `SPV0`, boleh diulang |
| spvType | <code>String</code> | wajib diisi, `SPVBLANK`,`SPV0` |
| trxMsisdn | <code>String</code> | wajib diisi |

**Example**  
```CURL http://localhost:9999/api/rita/product/activation-product-spv?_id=rita-00037261```


<a name="module_Rita./product/activation-product-recharges"></a>
### Rita./product/activation-product-recharges
**Request**```GET /product/activation-product-recharges?_id=```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `rita-`, wajib diisi, digunakan untuk akses lebih dari 1 akun |
| groupFeature | <code>String</code> | wajib diisi, `RITATOPUP`,`RITAPACKAGE`,`VASPRODUCTS` |
| msisdn | <code>String</code> | wajib diisi |
| pin | <code>String</code> | wajib diisi |
| productCode | <code>String</code> | wajib diisi |
| productPrice | <code>String</code> | wajib diisi |
| trxMsisdn | <code>String</code> | wajib diisi |

**Example**  
```CURL http://localhost:9999/api/rita/product/activation-product-recharges?_id=rita-00037261```


<a name="module_Rita./ligaSuper/checkKPK"></a>
### Rita./ligaSuper/checkKPK
**Request**```GET /ligaSuper/checkKPK?_id=```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `rita-`, wajib diisi, digunakan untuk akses lebih dari 1 akun |
| subscriberMsisdn | <code>String</code> | waajib |

**Example**  
```CURL http://localhost:9999/api/rita/ligaSuper/checkKPK?_id=rita-00037261```


<a name="module_Rita./ligaSuper/checkSPV"></a>
### Rita./ligaSuper/checkSPV
**Request**```GET /ligaSuper/checkSPV?_id=```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | awalan `rita-`, wajib diisi, digunakan untuk akses lebih dari 1 akun |
| voucherQrCode | <code>String</code> | wajib |

**Example**  
```CURL http://localhost:9999/api/rita/ligaSuper/checkSPV?_id=rita-00037261```

