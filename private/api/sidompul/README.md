
<a name="module_Sidompul"></a>
## Sidompul

* [Sidompul](#module_Sidompul)
    * _);Service_
        * [./v2/trx/history](#module_Sidompul./v2/trx/history)
    * _AccountService_
        * [./v1/account/profile](#module_Sidompul./v1/account/profile)
        * [./v1/account/balance](#module_Sidompul./v1/account/balance)
        * [./v1/inbox](#module_Sidompul./v1/inbox)
        * [./v1/account/pin/:pin](#module_Sidompul./v1/account/pin/_pin)
    * _ContentService_
        * [./v1/content/api/loyaltyprogram](#module_Sidompul./v1/content/api/loyaltyprogram)
        * [./v1/content/personalhomepage](#module_Sidompul./v1/content/personalhomepage)
        * [./v1/content/api/denom](#module_Sidompul./v1/content/api/denom)
        * [./v1/content/api/productcategories](#module_Sidompul./v1/content/api/productcategories)
        * [./v1/content/api/productflashsale](#module_Sidompul./v1/content/api/productflashsale)
        * [./v1/content/api/productitemlist](#module_Sidompul./v1/content/api/productitemlist)
        * [./v1/content/api/productbestoffer](#module_Sidompul./v1/content/api/productbestoffer)
    * _LoginService_
        * [./v1/auth/otp/:msisdn](#module_Sidompul./v1/auth/otp/_msisdn)
        * [./v1/auth/otp/:msisdn/:otp/:imei](#module_Sidompul./v1/auth/otp/_msisdn/_otp/_imei)
        * [./v1/login/token/firebase](#module_Sidompul./v1/login/token/firebase)
        * [./v1/login/token/favicon](#module_Sidompul./v1/login/token/favicon)
    * _LoyaltyService_
        * [./v1/loyalty/class](#module_Sidompul./v1/loyalty/class)
        * [./v1/loyalty/reward](#module_Sidompul./v1/loyalty/reward)
    * _TransactionService_
        * [./v1/trx/w2p](#module_Sidompul./v1/trx/w2p)
        * [./v1/trx/package](#module_Sidompul./v1/trx/package)
        * [./v1/trx/redeem-voucher-sa](#module_Sidompul./v1/trx/redeem-voucher-sa)
        * [./v1/trx/package-transfer](#module_Sidompul./v1/trx/package-transfer)
    * _UtilityService_
        * [./v1/common/prefix/:phonePrefix](#module_Sidompul./v1/common/prefix/_phonePrefix)
        * [./v1/sp/registration](#module_Sidompul./v1/sp/registration)
        * [./v1/package/check/:phone](#module_Sidompul./v1/package/check/_phone)
        * [./v1/package/eligibility/:msisdn/A](#module_Sidompul./v1/package/eligibility/_msisdn/A)
        * [./v1/package/eligibility/:msisdn/B](#module_Sidompul./v1/package/eligibility/_msisdn/B)
        * [./v1/package/validity/:msisdn/:voucherCode/:cgis](#module_Sidompul./v1/package/validity/_msisdn/_voucherCode/_cgis)



<a name="module_Sidompul./v2/trx/history"></a>
### Sidompul./v2/trx/history
**Request**```GET /v2/trx/history ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v2/trx/history?_id=```


<a name="module_Sidompul./v1/account/profile"></a>
### Sidompul./v1/account/profile
**Request**```GET /v1/account/profile ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v1/account/profile?_id=```


<a name="module_Sidompul./v1/account/balance"></a>
### Sidompul./v1/account/balance
**Request**```GET /v1/account/balance ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v1/account/balance?_id=```


<a name="module_Sidompul./v1/inbox"></a>
### Sidompul./v1/inbox
**Request**```GET /v1/inbox ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v1/inbox?_id=```


<a name="module_Sidompul./v1/account/pin/_pin"></a>
### Sidompul./v1/account/pin/:pin
**Request**```GET /v1/account/pin/:pin ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v1/account/pin/:pin?_id=```


<a name="module_Sidompul./v1/content/api/loyaltyprogram"></a>
### Sidompul./v1/content/api/loyaltyprogram
**Request**```GET /v1/content/api/loyaltyprogram ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v1/content/api/loyaltyprogram?_id=```


<a name="module_Sidompul./v1/content/personalhomepage"></a>
### Sidompul./v1/content/personalhomepage
**Request**```GET /v1/content/personalhomepage ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v1/content/personalhomepage?_id=```


<a name="module_Sidompul./v1/content/api/denom"></a>
### Sidompul./v1/content/api/denom
**Request**```GET /v1/content/api/denom ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v1/content/api/denom?_id=```


<a name="module_Sidompul./v1/content/api/productcategories"></a>
### Sidompul./v1/content/api/productcategories
**Request**```GET /v1/content/api/productcategories ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v1/content/api/productcategories?_id=```


<a name="module_Sidompul./v1/content/api/productflashsale"></a>
### Sidompul./v1/content/api/productflashsale
**Request**```GET /v1/content/api/productflashsale ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v1/content/api/productflashsale?_id=```


<a name="module_Sidompul./v1/content/api/productitemlist"></a>
### Sidompul./v1/content/api/productitemlist
**Request**```GET /v1/content/api/productitemlist ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v1/content/api/productitemlist?_id=```


<a name="module_Sidompul./v1/content/api/productbestoffer"></a>
### Sidompul./v1/content/api/productbestoffer
**Request**```GET /v1/content/api/productbestoffer ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v1/content/api/productbestoffer?_id=```


<a name="module_Sidompul./v1/auth/otp/_msisdn"></a>
### Sidompul./v1/auth/otp/:msisdn
**Request**```GET /v1/auth/otp/:msisdn ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v1/auth/otp/:msisdn?_id=```


<a name="module_Sidompul./v1/auth/otp/_msisdn/_otp/_imei"></a>
### Sidompul./v1/auth/otp/:msisdn/:otp/:imei
**Request**```GET /v1/auth/otp/:msisdn/:otp/:imei ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v1/auth/otp/:msisdn/:otp/:imei?_id=```


<a name="module_Sidompul./v1/login/token/firebase"></a>
### Sidompul./v1/login/token/firebase
**Request**```GET /v1/login/token/firebase ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v1/login/token/firebase?_id=```


<a name="module_Sidompul./v1/login/token/favicon"></a>
### Sidompul./v1/login/token/favicon
**Request**```GET /v1/login/token/favicon ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v1/login/token/favicon?_id=```


<a name="module_Sidompul./v1/loyalty/class"></a>
### Sidompul./v1/loyalty/class
**Request**```GET /v1/loyalty/class ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v1/loyalty/class?_id=```


<a name="module_Sidompul./v1/loyalty/reward"></a>
### Sidompul./v1/loyalty/reward
**Request**```GET /v1/loyalty/reward ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v1/loyalty/reward?_id=```


<a name="module_Sidompul./v1/trx/w2p"></a>
### Sidompul./v1/trx/w2p
**Request**```GET /v1/trx/w2p ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v1/trx/w2p?_id=```


<a name="module_Sidompul./v1/trx/package"></a>
### Sidompul./v1/trx/package
**Request**```GET /v1/trx/package ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v1/trx/package?_id=```


<a name="module_Sidompul./v1/trx/redeem-voucher-sa"></a>
### Sidompul./v1/trx/redeem-voucher-sa
**Request**```GET /v1/trx/redeem-voucher-sa ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v1/trx/redeem-voucher-sa?_id=```


<a name="module_Sidompul./v1/trx/package-transfer"></a>
### Sidompul./v1/trx/package-transfer
**Request**```GET /v1/trx/package-transfer ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v1/trx/package-transfer?_id=```


<a name="module_Sidompul./v1/common/prefix/_phonePrefix"></a>
### Sidompul./v1/common/prefix/:phonePrefix
**Request**```GET /v1/common/prefix/:phonePrefix ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v1/common/prefix/:phonePrefix?_id=```


<a name="module_Sidompul./v1/sp/registration"></a>
### Sidompul./v1/sp/registration
**Request**```GET /v1/sp/registration ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v1/sp/registration?_id=```


<a name="module_Sidompul./v1/package/check/_phone"></a>
### Sidompul./v1/package/check/:phone
**Request**```GET /v1/package/check/:phone ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v1/package/check/:phone?_id=```


<a name="module_Sidompul./v1/package/eligibility/_msisdn/A"></a>
### Sidompul./v1/package/eligibility/:msisdn/A
**Request**```GET /v1/package/eligibility/:msisdn/A ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v1/package/eligibility/:msisdn/A?_id=```


<a name="module_Sidompul./v1/package/eligibility/_msisdn/B"></a>
### Sidompul./v1/package/eligibility/:msisdn/B
**Request**```GET /v1/package/eligibility/:msisdn/B ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v1/package/eligibility/:msisdn/B?_id=```


<a name="module_Sidompul./v1/package/validity/_msisdn/_voucherCode/_cgis"></a>
### Sidompul./v1/package/validity/:msisdn/:voucherCode/:cgis
**Request**```GET /v1/package/validity/:msisdn/:voucherCode/:cgis ```


| Param | Type | Description |
| --- | --- | --- |
| _id | <code>String</code> | prefix `sidompul-`, wajib diisi, digunakan untuk multi akun |

**Example**  
```CURL http://localhost:9999/api/sidompul/v1/package/validity/:msisdn/:voucherCode/:cgis?_id=```

