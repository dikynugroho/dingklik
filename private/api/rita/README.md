
<a name="module_Rita"></a>
## Rita


<a name="module_Rita.@"></a>
### Rita.@
**Akses lebih dari 1 Akun**query `_id` digunakan untuk identifikasi lebih akun yang berbeda```GET api/rita?_id=rita-YOUR_ID```**Example**```:: Contoh akun 1CURL http://localhost:9999/api/rita/user/auth/v2?_id=rita-akun1:: Contoh akun 2CURL http://localhost:9999/api/rita/user/auth/v2?_id=rita-akun2```**Cluster transaksi**jika `_id` tidak diatur, akan dikirimkan ke terminal secara bergantian**Example**```:: Contoh 10 transaksi, dikirim ke 3 akunCURL http://localhost:9999/api/rita/recharge:: Terminal Akun1 -> Transaksi 1:: Terminal Akun2 -> Transaksi 2:: Terminal Akun3 -> Transaksi 3:: Terminal Akun1 -> Transaksi 4:: Terminal Akun2 -> Transaksi 5:: Terminal Akun3 -> Transaksi 6:: Terminal Akun1 -> Transaksi 7:: Terminal Akun2 -> Transaksi 8:: Terminal Akun3 -> Transaksi 9:: Terminal Akun1 -> Transaksi 10```


