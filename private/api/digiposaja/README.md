
<a name="module_Digiposaja"></a>
## Digiposaja

* [Digiposaja](#module_Digiposaja)
    * _@_
        * [.@](#module_Digiposaja.@)
    * _AuthService_
        * [./user/auth/v2](#module_Digiposaja./user/auth/v2)
        * [./auth/otp](#module_Digiposaja./auth/otp)
    * _DetailOrderService_
        * [./recharge/v2](#module_Digiposaja./recharge/v2)
        * [./package-activation/v5](#module_Digiposaja./package-activation/v5)
    * _DigistarService_
        * [./redeem/detail](#module_Digiposaja./redeem/detail)
        * [./redeem/id](#module_Digiposaja./redeem/id)
    * _KonfirmasiPinService_
        * [./recharge/confirm](#module_Digiposaja./recharge/confirm)
        * [./package-activation/confirm/v2](#module_Digiposaja./package-activation/confirm/v2)
        * [./voucher-fisik/v2](#module_Digiposaja./voucher-fisik/v2)
    * _PulsaElektronikService_
        * [./recharge/denom](#module_Digiposaja./recharge/denom)
    * _TransactionService_
        * [./transactions/detail](#module_Digiposaja./transactions/detail)
        * [./transactions/history](#module_Digiposaja./transactions/history)
    * _UserService_
        * [./balance/v2/ngrs](#module_Digiposaja./balance/v2/ngrs)
        * [./outlet/linkaja](#module_Digiposaja./outlet/linkaja)
        * [./outlet/linkaja/list](#module_Digiposaja./outlet/linkaja/list)
        * [./linkaja/account](#module_Digiposaja./linkaja/account)
        * [./user/payment](#module_Digiposaja./user/payment)
        * [./product/v3](#module_Digiposaja./product/v3)
        * [./balance/v2/linkaja](#module_Digiposaja./balance/v2/linkaja)
        * [./reward/summary](#module_Digiposaja./reward/summary)
        * [./user/profile](#module_Digiposaja./user/profile)
    * _ZDingklikService_
        * [./recharge](#module_Digiposaja./recharge)
        * [./package-activation](#module_Digiposaja./package-activation)
        * [./voucher-fisik](#module_Digiposaja./voucher-fisik)



<a name="module_Digiposaja.@"></a>
### Digiposaja.@
**Akses lebih dari 1 Akun**query `_id` digunakan untuk identifikasi lebih akun yang berbeda```GET api/digiposaja?_id=digiposaja-YOUR_ID```**Example**```:: Contoh akun 1CURL http://localhost:9999/api/digiposaja/user/auth/v2?_id=digiposaja-akun1:: Contoh akun 2CURL http://localhost:9999/api/digiposaja/user/auth/v2?_id=digiposaja-akun2```**Cluster transaksi**jika `_id` tidak diatur, akan dikirimkan ke terminal secara bergantian**Example**```:: Contoh 10 transaksi, dikirim ke 3 akunCURL http://localhost:9999/api/digiposaja/recharge:: Terminal Akun1 -> Transaksi 1:: Terminal Akun2 -> Transaksi 2:: Terminal Akun3 -> Transaksi 3:: Terminal Akun1 -> Transaksi 4:: Terminal Akun2 -> Transaksi 5:: Terminal Akun3 -> Transaksi 6:: Terminal Akun1 -> Transaksi 7:: Terminal Akun2 -> Transaksi 8:: Terminal Akun3 -> Transaksi 9:: Terminal Akun1 -> Transaksi 10```



<a name="module_Digiposaja./user/auth/v2"></a>
### Digiposaja./user/auth/v2
**Request**```bashGET /user/auth/v2?_id=digiposaja-YOUR_ID&username=YOUR_USERNAME&password=YOUR_PASSWORD```


| Param | Type | Description |
| --- | --- | --- |
| username | <code>String</code> | di `query`, dibutuhkan `true` |
| password | <code>String</code> | di `query`, dibutuhkan `true` |
| _id | <code>String</code> | di `query`, dibutuhkan `true`, awalan `digiposaja-`, digunakan untuk akses lebih dari 1 akun |

**Example**  
```bashCURL http://localhost:9999/api/digiposaja/user/auth/v2?_id=digiposaja-YOUR_USERNAME&username=YOUR_USERNAME&password=YOUR_PASSWORD```**Response**```js{}```


<a name="module_Digiposaja./auth/otp"></a>
### Digiposaja./auth/otp
**Request**```bashGET /auth/otp?_id=digiposaja-YOUR_ID&otp=YOUR_OTP```


| Param | Type | Description |
| --- | --- | --- |
| otp | <code>String</code> | di `query`, dibutuhkan `true` |
| _id | <code>String</code> | di `query`, dibutuhkan `true`, awalan `digiposaja-`, digunakan untuk akses lebih dari 1 akun |

**Example**  
```bashCURL http://localhost:9999/api/digiposaja/auth/otp?_id=digiposaja-YOUR_USERNAME&otp=773344```**Response**```js{    "status": 0,    "message": "ok",    "data": {...},}```


<a name="module_Digiposaja./recharge/v2"></a>
### Digiposaja./recharge/v2
**Request**```bashGET /recharge/v2?_id=digiposaja-YOUR_ID&denomRecharge=YOUR_DENOMRECHARGE&price=YOUR_PRICE&rechargeType=YOUR_RECHARGETYPE&msisdn=YOUR_MSISDN&paymentMethod=YOUR_PAYMENTMETHOD```


| Param | Type | Description |
| --- | --- | --- |
| denomRecharge | <code>String</code> | di `query`, dibutuhkan `true` |
| price | <code>String</code> | di `query`, dibutuhkan `true` |
| rechargeType | <code>String</code> | di `query`, dibutuhkan `true`, nilai `BULK`/`FIX` |
| msisdn | <code>String</code> | di `query`, dibutuhkan `true` |
| paymentMethod | <code>String</code> | di `query`, dibutuhkan `true`, nilai `NGRS`/`LINKAJA` |
| _id | <code>String</code> | di `query`, dibutuhkan `true`, awalan `digiposaja-`, digunakan untuk akses lebih dari 1 akun |

**Example**  
```bashCURL http://localhost:9999/api/digiposaja/recharge/v2?_id=digiposaja-YOUR_USERNAME&denomRecharge=1000&price=1400&rechargeType=BULK&msisdn=085220878457&paymentMethod=LINKAJA```**Response**```js{    "status": 0,    "message": "ok",    "data": {...},}```


<a name="module_Digiposaja./package-activation/v5"></a>
### Digiposaja./package-activation/v5
**Request**```bashGET /package-activation/v5?_id=digiposaja-YOUR_ID&packageId=YOUR_PACKAGEID&price=YOUR_PRICE&msisdn=YOUR_MSISDN&trxType=YOUR_TRXTYPE&paymentMethod=YOUR_PAYMENTMETHOD```


| Param | Type | Description |
| --- | --- | --- |
| packageId | <code>String</code> | di `query`, dibutuhkan `true` |
| price | <code>String</code> | di `query`, dibutuhkan `true` |
| msisdn | <code>String</code> | di `query`, dibutuhkan `true` |
| trxType | <code>String</code> | di `query`, dibutuhkan `true`, nilai `HVC`/`DATA`/`DIGITAL`/`ROAMING`/`VOICE_SMS`/`VF` |
| paymentMethod | <code>String</code> | di `query`, dibutuhkan `true`, nilai `NGRS`/`LINKAJA` |
| _id | <code>String</code> | di `query`, dibutuhkan `true`, awalan `digiposaja-`, digunakan untuk akses lebih dari 1 akun |

**Example**  
```bashCURL http://localhost:9999/api/digiposaja/package-activation/v5?_id=digiposaja-YOUR_USERNAME&packageId=00017507&price=2500&msisdn=085220878457&trxType=DATA&paymentMethod=LINKAJA```**Response**```js{    "status": 0,    "message": "ok",    "data": {...},}```


<a name="module_Digiposaja./redeem/detail"></a>
### Digiposaja./redeem/detail
**Request**```bashGET /redeem/detail?_id=digiposaja-YOUR_ID&redeemId=YOUR_REDEEMID```


| Param | Type | Description |
| --- | --- | --- |
| redeemId | <code>String</code> | di `query`, dibutuhkan `true` |
| _id | <code>String</code> | di `query`, dibutuhkan `true`, awalan `digiposaja-`, digunakan untuk akses lebih dari 1 akun |

**Example**  
```bashCURL http://localhost:9999/api/digiposaja/redeem/detail?_id=digiposaja-YOUR_USERNAME&redeemId=123461```**Response**```js{    "status": 0,    "message": "ok",    "data": {...},}```


<a name="module_Digiposaja./redeem/id"></a>
### Digiposaja./redeem/id
**Request**```bashGET /redeem/id?_id=digiposaja-YOUR_ID```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | di `query`, dibutuhkan `true`, awalan `digiposaja-`, digunakan untuk akses lebih dari 1 akun |

**Example**  
```bashCURL http://localhost:9999/api/digiposaja/redeem/id?_id=digiposaja-YOUR_USERNAME```**Response**```js{    "status": 0,    "message": "ok",    "data": {...},}```


<a name="module_Digiposaja./recharge/confirm"></a>
### Digiposaja./recharge/confirm
**Request**```bashGET /recharge/confirm?_id=digiposaja-YOUR_ID&pin=YOUR_PIN&token=YOUR_TOKEN```


| Param | Type | Description |
| --- | --- | --- |
| pin | <code>String</code> | di `query`, dibutuhkan `true` |
| token | <code>String</code> | di `query`, dibutuhkan `true` |
| _id | <code>String</code> | di `query`, dibutuhkan `true`, awalan `digiposaja-`, digunakan untuk akses lebih dari 1 akun |

**Example**  
```bashCURL http://localhost:9999/api/digiposaja/recharge/confirm?_id=digiposaja-YOUR_USERNAME&pin=123456&token=qwertyuiopasdfghjklzxcvbnm123456789```**Response**```js{    "status": 0,    "message": "ok",    "data": {...},}```


<a name="module_Digiposaja./package-activation/confirm/v2"></a>
### Digiposaja./package-activation/confirm/v2
**Request**```bashGET /package-activation/confirm/v2?_id=digiposaja-YOUR_ID&pin=YOUR_PIN&token=YOUR_TOKEN```


| Param | Type | Description |
| --- | --- | --- |
| pin | <code>String</code> | di `query`, dibutuhkan `true` |
| token | <code>String</code> | di `query`, dibutuhkan `true` |
| _id | <code>String</code> | di `query`, dibutuhkan `true`, awalan `digiposaja-`, digunakan untuk akses lebih dari 1 akun |

**Example**  
```bashCURL http://localhost:9999/api/digiposaja/package-activation/confirm/v2?_id=digiposaja-YOUR_USERNAME&pin=123456&token=qwertyuiopasdfghjklzxcvbnm123456789```**Response**```js{    "status": 0,    "message": "ok",    "data": {...},}```


<a name="module_Digiposaja./voucher-fisik/v2"></a>
### Digiposaja./voucher-fisik/v2
**Request**```bashGET /voucher-fisik/v2?_id=digiposaja-YOUR_ID&serialNumber=YOUR_SERIALNUMBER&pin=YOUR_PIN&productId=YOUR_PRODUCTID&price=YOUR_PRICE&paymentMethod=YOUR_PAYMENTMETHOD```


| Param | Type | Description |
| --- | --- | --- |
| serialNumber | <code>String</code> | di `query`, dibutuhkan `true`, equal `msisdn` |
| pin | <code>String</code> | di `query`, dibutuhkan `true` |
| productId | <code>String</code> | di `query`, dibutuhkan `true` |
| price | <code>String</code> | di `query`, dibutuhkan `true` |
| paymentMethod | <code>String</code> | di `query`, dibutuhkan `true`, nilai `NGRS`/`LINKAJA` |
| _id | <code>String</code> | di `query`, dibutuhkan `true`, awalan `digiposaja-`, digunakan untuk akses lebih dari 1 akun |

**Example**  
```bashCURL http://localhost:9999/api/digiposaja/voucher-fisik/v2?_id=digiposaja-YOUR_USERNAME&serialNumber=085220878457&pin=142536&productId=00022541&price=8500&paymentMethod=LINKAJA```**Response**```js{    "status": 0,    "message": "ok",    "data": {...},}```


<a name="module_Digiposaja./recharge/denom"></a>
### Digiposaja./recharge/denom
**Request**```bashGET /recharge/denom?_id=digiposaja-YOUR_ID&msisdn=YOUR_MSISDN&paymentMethod=YOUR_PAYMENTMETHOD&categoryCode=YOUR_CATEGORYCODE```


| Param | Type | Description |
| --- | --- | --- |
| msisdn | <code>String</code> | di `query`, dibutuhkan `true` |
| paymentMethod | <code>String</code> | di `query`, dibutuhkan `true`, nilai `NGRS`/`LINKAJA` |
| categoryCode | <code>String</code> | di `query`, nilai `NSB` |
| _id | <code>String</code> | di `query`, dibutuhkan `true`, awalan `digiposaja-`, digunakan untuk akses lebih dari 1 akun |

**Example**  
```bash:: Contoh 1CURL http://localhost:9999/api/digiposaja/recharge/denom?_id=digiposaja-YOUR_USERNAME&msisdn=085220878457&paymentMethod=LINKAJA:: Contoh 2, ISPCURL http://localhost:9999/api/digiposaja/recharge/denom?_id=digiposaja-YOUR_USERNAME&msisdn=085220878457&paymentMethod=LINKAJA&categoryCode=NSB```**Response**```js{    "status": 0,    "message": "ok",    "data": {...},}```


<a name="module_Digiposaja./transactions/detail"></a>
### Digiposaja./transactions/detail
**Request**```bashGET /transactions/detail?_id=digiposaja-YOUR_ID&id=YOUR_ID&trxType=YOUR_TRXTYPE```


| Param | Type | Default | Description |
| --- | --- | --- | --- |
| id | <code>String</code> |  | di `query`, dibutuhkan `true` |
| trxType | <code>String</code> | <code>RECHARGE</code> | di `query`, dibutuhkan `true`, nilai `RECHARGE` |
| _id | <code>String</code> |  | di `query`, dibutuhkan `true`, awalan `digiposaja-`, digunakan untuk akses lebih dari 1 akun |

**Example**  
```bash:: Contoh 1CURL http://localhost:9999/api/digiposaja/transactions/detail?_id=digiposaja-YOUR_USERNAME&id=604040123&trxType=RECHARGE:: Contoh 2CURL http://localhost:9999/api/digiposaja/transactions/detail?_id=digiposaja-YOUR_USERNAME&id=604040123```**Response**```js{    "status": 0,    "message": "ok",    "data": {...},}```


<a name="module_Digiposaja./transactions/history"></a>
### Digiposaja./transactions/history
**Request**```bashGET /transactions/history?_id=digiposaja-YOUR_ID&startDate=YOUR_STARTDATE&endDate=YOUR_ENDDATE&page=YOUR_PAGE&pageSize=YOUR_PAGESIZE&trxType=YOUR_TRXTYPE&status=YOUR_STATUS```


| Param | Type | Default | Description |
| --- | --- | --- | --- |
| startDate | <code>String</code> | <code>CURRENT_DATE</code> | di `query`, dibutuhkan `true`, format `YYYYMMDD` example `20201201` |
| endDate | <code>String</code> | <code>CURRENT_DATE</code> | di `query`, dibutuhkan `true`, format `YYYYMMDD` example `20201201` |
| page | <code>String</code> | <code>0</code> | di `query`, dibutuhkan `true` |
| pageSize | <code>String</code> | <code>20</code> | di `query`, dibutuhkan `true` |
| trxType | <code>String</code> |  | di `query` |
| status | <code>String</code> |  | di `query` |
| _id | <code>String</code> |  | di `query`, dibutuhkan `true`, awalan `digiposaja-`, digunakan untuk akses lebih dari 1 akun |

**Example**  
```bash:: Contoh 1CURL http://localhost:9999/api/digiposaja/transactions/history?_id=digiposaja-YOUR_USERNAME&startDate=20201010&endDate=20201010&page=0&pageSize=20&trxType=&status=:: Contoh 2CURL http://localhost:9999/api/digiposaja/transactions/history?_id=digiposaja-YOUR_USERNAME```**Response**```js{    "status": 0,    "message": "ok",    "data": {...},}```


<a name="module_Digiposaja./balance/v2/ngrs"></a>
### Digiposaja./balance/v2/ngrs
**Request**```bashGET /balance/v2/ngrs?_id=digiposaja-YOUR_ID```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | di `query`, dibutuhkan `true`, awalan `digiposaja-`, digunakan untuk akses lebih dari 1 akun |

**Example**  
```bashCURL http://localhost:9999/api/digiposaja/balance/v2/ngrs?_id=digiposaja-YOUR_USERNAME```**Response**```js{    "status": 0,    "message": "ok",    "data": {...},}```


<a name="module_Digiposaja./outlet/linkaja"></a>
### Digiposaja./outlet/linkaja
**Request**```bashGET /outlet/linkaja?_id=digiposaja-YOUR_ID```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | di `query`, dibutuhkan `true`, awalan `digiposaja-`, digunakan untuk akses lebih dari 1 akun |

**Example**  
```bashCURL http://localhost:9999/api/digiposaja/outlet/linkaja?_id=digiposaja-YOUR_USERNAME```**Response**```js{    "status": 0,    "message": "ok",    "data": {...},}```


<a name="module_Digiposaja./outlet/linkaja/list"></a>
### Digiposaja./outlet/linkaja/list
**Request**```bashGET /outlet/linkaja/list?_id=digiposaja-YOUR_ID```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | di `query`, dibutuhkan `true`, awalan `digiposaja-`, digunakan untuk akses lebih dari 1 akun |

**Example**  
```bashCURL http://localhost:9999/api/digiposaja/outlet/linkaja/list?_id=digiposaja-YOUR_USERNAME```**Response**```js{    "status": 0,    "message": "ok",    "data": {...},}```


<a name="module_Digiposaja./linkaja/account"></a>
### Digiposaja./linkaja/account
**Request**```bashGET /linkaja/account?_id=digiposaja-YOUR_ID```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | di `query`, dibutuhkan `true`, awalan `digiposaja-`, digunakan untuk akses lebih dari 1 akun |

**Example**  
```bashCURL http://localhost:9999/api/digiposaja/linkaja/account?_id=digiposaja-YOUR_USERNAME```**Response**```js{    "status": 0,    "message": "ok",    "data": {...},}```


<a name="module_Digiposaja./user/payment"></a>
### Digiposaja./user/payment
**Request**```bashGET /user/payment?_id=digiposaja-YOUR_ID```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | di `query`, dibutuhkan `true`, awalan `digiposaja-`, digunakan untuk akses lebih dari 1 akun |

**Example**  
```bashCURL http://localhost:9999/api/digiposaja/user/payment?_id=digiposaja-YOUR_USERNAME```**Response**```js{    "status": 0,    "message": "ok",    "data": {...},}```


<a name="module_Digiposaja./product/v3"></a>
### Digiposaja./product/v3
**Request**```bashGET /product/v3?_id=digiposaja-YOUR_ID&categoryCode=YOUR_CATEGORYCODE&msisdn=YOUR_MSISDN&paymentMethod=YOUR_PAYMENTMETHOD```


| Param | Type | Description |
| --- | --- | --- |
| categoryCode | <code>String</code> | di `query`, dibutuhkan `true`, nilai `HVC`/`DATA`/`DIGITAL`/`ROAMING`/`VOICE_SMS`/`VF` |
| msisdn | <code>String</code> | di `query` |
| paymentMethod | <code>String</code> | di `query`, dibutuhkan `true`, nilai `NGRS`/`LINKAJA` |
| _id | <code>String</code> | di `query`, dibutuhkan `true`, awalan `digiposaja-`, digunakan untuk akses lebih dari 1 akun |

**Example**  
```bash:: Contoh 1CURL http://localhost:9999/api/digiposaja/product/v3?_id=digiposaja-YOUR_USERNAME&categoryCode=VF&msisdn=085220878457&paymentMethod=LINKAJA:: Contoh 2, HVCCURL http://localhost:9999/api/digiposaja/product/v3?_id=digiposaja-YOUR_USERNAME&categoryCode=HVC&paymentMethod=LINKAJA:: Contoh 2, DATACURL http://localhost:9999/api/digiposaja/product/v3?_id=digiposaja-YOUR_USERNAME&categoryCode=DATA&paymentMethod=LINKAJA:: Contoh 2, DIGITALCURL http://localhost:9999/api/digiposaja/product/v3?_id=digiposaja-YOUR_USERNAME&categoryCode=DIGITAL&paymentMethod=LINKAJA:: Contoh 2, ROAMINGCURL http://localhost:9999/api/digiposaja/product/v3?_id=digiposaja-YOUR_USERNAME&categoryCode=ROAMING&paymentMethod=LINKAJA:: Contoh 2, VOICE_SMSCURL http://localhost:9999/api/digiposaja/product/v3?_id=digiposaja-YOUR_USERNAME&categoryCode=VOICE_SMS&paymentMethod=LINKAJA:: Contoh 2, VFCURL http://localhost:9999/api/digiposaja/product/v3?_id=digiposaja-YOUR_USERNAME&categoryCode=VF&paymentMethod=LINKAJA```**Response**```js{    "status": 0,    "message": "ok",    "data": {...},}```


<a name="module_Digiposaja./balance/v2/linkaja"></a>
### Digiposaja./balance/v2/linkaja
**Request**```bashGET /balance/v2/linkaja?_id=digiposaja-YOUR_ID```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | di `query`, dibutuhkan `true`, awalan `digiposaja-`, digunakan untuk akses lebih dari 1 akun |

**Example**  
```bashCURL http://localhost:9999/api/digiposaja/balance/v2/linkaja?_id=digiposaja-YOUR_USERNAME```**Response**```js{    "status": 0,    "message": "ok",    "data": {...},}```


<a name="module_Digiposaja./reward/summary"></a>
### Digiposaja./reward/summary
**Request**```bashGET /reward/summary?_id=digiposaja-YOUR_ID```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | di `query`, dibutuhkan `true`, awalan `digiposaja-`, digunakan untuk akses lebih dari 1 akun |

**Example**  
```bashCURL http://localhost:9999/api/digiposaja/reward/summary?_id=digiposaja-YOUR_USERNAME```**Response**```js{    "status": 0,    "message": "ok",    "data": {...},}```


<a name="module_Digiposaja./user/profile"></a>
### Digiposaja./user/profile
**Request**```bashGET /user/profile?code=YOUR_CODE&_id=digiposaja-YOUR_ID```


| Param | Type | Description |
| --- | --- | --- |
| code | <code>String</code> | di `query`, dibutuhkan `true` |
| _id | <code>String</code> | di `query`, dibutuhkan `true`, awalan `digiposaja-`, digunakan untuk akses lebih dari 1 akun |

**Example**  
```bashCURL http://localhost:9999/api/digiposaja/user/profile?code=NOV2988084&_id=digiposaja-YOUR_USERNAME```**Response**```js{    "status": 0,    "message": "ok",    "data": {...},}```


<a name="module_Digiposaja./recharge"></a>
### Digiposaja./recharge
**Request**```bashGET /recharge?code=YOUR_CODE&_id=digiposaja-YOUR_ID&jumlah=YOUR_JUMLAH&keuntungan=YOUR_KEUNTUNGAN&batas=YOUR_BATAS&msisdn=YOUR_MSISDN&paymentMethod=YOUR_PAYMENTMETHOD&rechargeType=YOUR_RECHARGETYPE&pin=YOUR_PIN```


| Param | Type | Description |
| --- | --- | --- |
| transactionId | <code>String</code> | di `query` |
| jumlah | <code>String</code> | di `query`, dibutuhkan `true`, nominal yang akan dibeli |
| keuntungan | <code>String</code> | di `query`, dibutuhkan `true`, penambahan pada harga modal |
| batas | <code>String</code> | di `query`, dibutuhkan `true`, batas harga penjualan |
| msisdn | <code>String</code> | di `query`, dibutuhkan `true`, nomer hp yang akan di isi |
| paymentMethod | <code>String</code> | di `query`, dibutuhkan `true`, nilai `LINKAJA`/`NGRS` |
| rechargeType | <code>String</code> | di `query`, dibutuhkan `true`, nilai `BULK`/`FIX` |
| pin | <code>String</code> | di `query`, dibutuhkan `true`, dibutuhkan untuk melanjutkan transaksi, dikosongkan untuk cek ketersediaan produk |
| _id | <code>String</code> | di `query`, dibutuhkan `true`, awalan `digiposaja-`, digunakan untuk akses lebih dari 1 akun |

**Example**  
```bash:: Contoh 1, Cek ketersedian, produk yang melebihi batas harga akan dibatalkanCURL http://localhost:9999/api/digiposaja/recharge?_id=digiposaja-YOUR_USERNAME&jumlah=1000&keuntungan=500&batas=2000&msisdn=085220878457&paymentMethod=LINKAJA&rechargeType=BULK:: Contoh 2, Untuk melanjutkan transaksi tambahkan pin pada query, dengan kondisi seperti Contoh 1CURL http://localhost:9999/api/digiposaja/recharge?_id=digiposaja-YOUR_USERNAME&jumlah=1000&keuntungan=500&batas=2000&msisdn=085220878457&paymentMethod=LINKAJA&rechargeType=BULK&pin=142536```**Response**```js// Contoh 1, Cek ketersediaan{  "_id": "digiposaja-YOUR_USERNAME",  "transactionId": "",  "jumlah": 1000,  "keuntungan": "500",  "batas": 2000,  "msisdn": "085220878457",  "paymentMethod": "LINKAJA",  "rechargeType": "BULK",  "fee": 400,  "denom_type": "BULK",  "business_model": "1",  "start_value": "1000",  "end_value": "1000",  "tariff_mode": "2",  "hpp": 1400,  "harga": 1900,  "batal": false}// Note: Property jumlah,hpp,harga,batas,batal adalah tambahan / bukan jawaban dari digiposaja// Contoh 2, Transaksi sukses{  "status": 0,  "message": "ok",  "data": {    "id": "605925351",    "trxType": "RECHARGE",    "trxId": "DGPS201011215619234049829",    "outletId": "3200014122",    "rsNumber": "82142365800",    "msisdn": "085220878457",    "paymentMethod": "LINKAJA",    "productId": null,    "productName": "BULK 1000",    "serialNumber": "02110700000406758877",    "price": 1400,    "status": "SUCCESS",    "statusCode": "SUKSES",    "statusDesc": null,    "createdAt": "2020-10-11T14:56:20.021+00:00",    "createdBy": "5556912283",    "updatedAt": "2020-10-11T14:56:20.021+00:00",    "updatedBy": null,    "starPoint": 0,    "customData": null  }}// Contoh 3, Permintaan dibatalkan, karena melebihi batas harga yang ditentukan{  "transactionId": "",  "status": 404,  "statusText": "Not Found",  "_id": "digiposaja-YOUR_USERNAME",  "jumlah": "1000",  "keuntungan": "500",  "batas": "1500",  "msisdn": "085220878457",  "paymentMethod": "LINKAJA",  "rechargeType": "BULK",  "message": "Denom ini tidak tersedia di lokasi Anda saat ini, silahkan pilih produk lain"}// Note: Jawaban diatas, adalah Custom, bukan jawaban dari digiposaja```


<a name="module_Digiposaja./package-activation"></a>
### Digiposaja./package-activation
**Request**```bashGET /package-activation?code=YOUR_CODE&_id=digiposaja-YOUR_ID&keuntungan=YOUR_KEUNTUNGAN&batas=YOUR_BATAS&categoryCode=YOUR_CATEGORYCODE&msisdn=YOUR_MSISDN&paymentMethod=YOUR_PAYMENTMETHOD&packageId=YOUR_PACKAGEID&pin=YOUR_PIN```


| Param | Type | Description |
| --- | --- | --- |
| transactionId | <code>String</code> | di `query` |
| keuntungan | <code>String</code> | di `query`, dibutuhkan `true`, penambahan pada harga modal |
| batas | <code>String</code> | di `query`, dibutuhkan `true`, batas harga penjualan |
| categoryCode | <code>String</code> | di `query`, dibutuhkan `true`, nilai `HVC`/`DATA`/`DIGITAL`/`ROAMING`/`VOICE_SMS` |
| msisdn | <code>String</code> | di `query`, dibutuhkan `true`, nomer hp yang akan di isi |
| paymentMethod | <code>String</code> | di `query`, dibutuhkan `true`, nilai `LINKAJA`/`NGRS` |
| packageId | <code>String</code> | di `query`, dibutuhkan `true` |
| pin | <code>String</code> | di `query`, dibutuhkan `true`, dibutuhkan untuk melanjutkan transaksi, dikosongkan untuk cek ketersediaan produk |
| _id | <code>String</code> | di `query`, dibutuhkan `true`, awalan `digiposaja-`, digunakan untuk akses lebih dari 1 akun |

**Example**  
```bash:: Contoh 1, Cek ketersedian, produk yang melebihi batas harga akan dibatalkanCURL http://localhost:9999/api/digiposaja/package-activation?_id=digiposaja-YOUR_USERNAME&keuntungan=500&batas=3000&categoryCode=DATA&msisdn=085220878457&paymentMethod=LINKAJA&packageId=00017507:: Contoh 2, Untuk melanjutkan transaksi tambahkan pin pada query, dengan kondisi seperti Contoh 1CURL http://localhost:9999/api/digiposaja/package-activation?_id=digiposaja-YOUR_USERNAME&keuntungan=500&batas=3000&categoryCode=DATA&msisdn=085220878457&paymentMethod=LINKAJA&packageId=00017507&pin=142536```**Response**```js// Contoh 1, Cek ketersediaan{  "_id": "digiposaja-YOUR_USERNAME",  "transactionId": "",  "keuntungan": "500",  "batas": 3000,  "categoryCode": "DATA",  "msisdn": "085220878457",  "paymentMethod": "LINKAJA",  "packageId": "00017507",  "price": [    {      "amount": 2000,      "transfer_price": 500,      "payment_method": "RSEMONEY",      "price_description": ""    }  ],  "productId": "00017507",  "menuId": "ML4_DR_1_250001",  "productName": "1 GB (00-07) / 1 Hari",  "productSubCategory": "Paket Malam",  "duration": [    {      "length": "2",      "unit": "Days"    }  ],  "quota": [    {      "subclass": "DATA MDS",      "name": "Internet Midnight 00-07",      "validity_period": "2 Days",      "quota": "1 GB",      "highlight": "true",      "class": "DATA"    }  ],  "hpp": 2500,  "harga": 3000,  "batal": false}// Note: Property hpp,harga,batas,batal adalah tambahan / bukan jawaban dari digiposaja// Contoh 2, Transaksi sukses{  "status": 0,  "message": "ok",  "data": {    "id": "444975653",    "trxType": "DATA",    "trxId": "DGPS201012003407737592930",    "outletId": "3200014122",    "rsNumber": "82142365800",    "msisdn": "085220878457",    "paymentMethod": "LINKAJA",    "productId": "00017507",    "productName": "1 GB (00-07) / 1 Hari",    "serialNumber": "02111100000407593271",    "price": 2500,    "status": "SUCCESS",    "statusCode": "SUKSES",    "statusDesc": "success",    "createdAt": "2020-10-11T17:34:08.432+00:00",    "createdBy": "5556912283",    "updatedAt": "2020-10-11T17:34:10.592+00:00",    "updatedBy": "SYSTEM",    "starPoint": 12,    "customData": {      "digistar_notification": {        "digistar_notification": "Potensi extra bintang 4% dari kenaikan jual paket, ayo tingkatkan transaksimu"      }    }  }}// Contoh 3, Permintaan dibatalkan, karena melebihi batas harga yang ditentukan{  "status": 404,  "transactionId": "",  "statusText": "Not Found",  "_id": "digiposaja-YOUR_USERNAME",  "keuntungan": "500",  "batas": "2500",  "categoryCode": "DATA",  "msisdn": "085220878457",  "paymentMethod": "LINKAJA",  "packageId": "00017507",  "message": "Denom ini tidak tersedia di lokasi Anda saat ini, silahkan pilih produk lain"}// Note: Jawaban diatas, adalah Custom, bukan jawaban dari digiposaja```


<a name="module_Digiposaja./voucher-fisik"></a>
### Digiposaja./voucher-fisik
**Request**```bashGET /voucher-fisik?code=YOUR_CODE&_id=digiposaja-YOUR_ID```


| Param | Type | Description |
| --- | --- | --- |
| transactionId | <code>String</code> | di `query` |
| keuntungan | <code>String</code> | di `query`, dibutuhkan `true`, penambahan pada harga modal |
| batas | <code>String</code> | di `query`, dibutuhkan `true`, batas harga penjualan |
| categoryCode | <code>String</code> | di `query`, dibutuhkan `true`, nilai `VF` |
| msisdn | <code>String</code> | di `query`, dibutuhkan `true`, nomer hp yang akan di isi |
| paymentMethod | <code>String</code> | di `query`, dibutuhkan `true`, nilai `LINKAJA`/`NGRS` |
| productId | <code>String</code> | di `query`, dibutuhkan `true` |
| pin | <code>String</code> | di `query`, dibutuhkan `true`, dibutuhkan untuk melanjutkan transaksi, dikosongkan untuk cek ketersediaan produk |
| _id | <code>String</code> | di `query`, dibutuhkan `true`, awalan `digiposaja-`, digunakan untuk akses lebih dari 1 akun |

**Example**  
```bash:: Contoh 1, Cek ketersedian, produk yang melebihi batas harga akan dibatalkanCURL http://localhost:9999/api/digiposaja/voucher-fisik?_id=digiposaja-YOUR_USERNAME&keuntungan=500&batas=9000&categoryCode=VF&msisdn=085220878457&paymentMethod=LINKAJA&productId=00022541:: Contoh 2, Untuk melanjutkan transaksi tambahkan pin pada query, dengan kondisi seperti Contoh 1CURL http://localhost:9999/api/digiposaja/voucher-fisik?_id=digiposaja-YOUR_USERNAME&keuntungan=500&batas=9000&categoryCode=VF&msisdn=085220878457&paymentMethod=LINKAJA&productId=00022541&pin=142536```**Response**```js{}```

