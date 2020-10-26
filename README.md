[![GitHub release (latest SemVer including pre-releases)](https://img.shields.io/github/v/release/ndiing/dingklik?include_prereleases)](https://github.com/ndiing/dingklik/releases/latest)
[![GitHub All Releases](https://img.shields.io/github/downloads/ndiing/dingklik/total)](https://github.com/ndiing/dingklik/releases/latest)
[![GitHub Releases](https://img.shields.io/github/downloads/ndiing/dingklik/latest/total)](https://github.com/ndiing/dingklik/releases/latest)
[![GitHub Release Date](https://img.shields.io/github/release-date/ndiing/dingklik)](https://github.com/ndiing/dingklik/releases/latest)
[![GitHub last commit](https://img.shields.io/github/last-commit/ndiing/dingklik)](https://github.com/ndiing/dingklik/releases/latest)
[![GitHub issues](https://img.shields.io/github/issues/ndiing/dingklik)](https://github.com/ndiing/dingklik/issues/new/choose)
[![Discord](https://img.shields.io/discord/769894286484832288)](https://discord.gg/8BsAv5b)

# Dingklik

AIO (All In One) `Gateway API` dan `Addon OtomaX`

## Informasi

### Dokumentasi

-   [![](https://img.shields.io/badge/Baca-DigiposAja@com.telkomsel.digiposaja@5.1.6-brightgreen)](https://github.com/ndiing/dingklik/blob/main/private/api/digiposaja/README.md)
-   [![](https://img.shields.io/badge/Baca-GriyaBayar@https://griyabayar.com@5.0.0-brightgreen)](https://github.com/ndiing/dingklik/blob/main/private/api/griyabayar/README.md)
-   [![](https://img.shields.io/badge/Baca-RITA@com.hutchison.rita@1.2.9-brightgreen)](https://github.com/ndiing/dingklik/blob/main/private/api/rita/README.md)
-   [![](https://img.shields.io/badge/Baca-SRIS@https://sris.smartfren.com@1.2.42-yellow)](https://github.com/ndiing/dingklik/blob/main/private/api/sris/README.md)
-   [![](https://img.shields.io/badge/Baca-SiDOMPUL@com.toko.xl@2.2.5-brightgreen)](https://github.com/ndiing/dingklik/blob/main/private/api/sidompul/README.md)
-   [![](https://img.shields.io/badge/Baca-MyTelkomsel@com.telkomsel.telkomselcm@5.6.0-blue)](https://github.com/ndiing/dingklik/blob/main/private/api/mytelkomsel/README.md)
-   [![](https://img.shields.io/badge/Baca-LinkAja@com.telkom.mwallet@4.12.0-blue)](https://github.com/ndiing/dingklik/blob/main/private/api/linkaja/README.md)
-   [![](https://img.shields.io/badge/Baca-SIMPEL@com.digital.indosat.dealerapp@1.3.5-blue)](https://github.com/ndiing/dingklik/blob/main/private/api/simpel/README.md)
-   [![](https://img.shields.io/badge/Baca-MitraShopee@com.shopee.mitra.id@1.19.1-blue)](https://github.com/ndiing/dingklik/blob/main/private/api/mitrashopee/README.md)
-   [![](https://img.shields.io/badge/Baca-MitraTokopedia@com.tokopedia.kelontongapp@1.4.19.2-blue)](https://github.com/ndiing/dingklik/blob/main/private/api/mitratokopedia/README.md)
-   [![](https://img.shields.io/badge/Baca-MitraBukalapak@com.bukalapak.mitra@1.43.5-blue)](https://github.com/ndiing/dingklik/blob/main/private/api/mitrabukalapak/README.md)

### Status

-   [![](https://img.shields.io/badge/Status-Development-yellow)](https://github.com/ndiing/dingklik/issues/new/choose)
-   [![](https://img.shields.io/badge/Status-Soon-blueviolet)](https://github.com/ndiing/dingklik/issues/new/choose)
-   [![](https://img.shields.io/badge/Status-Release-brightgreen)](https://github.com/ndiing/dingklik/issues/new/choose)
-   [![](https://img.shields.io/badge/Status-Schedule-blue)](https://github.com/ndiing/dingklik/issues/new/choose)
-   [![](https://img.shields.io/badge/Status-Error-red)](https://github.com/ndiing/dingklik/issues/new/choose)
-   [![](https://img.shields.io/badge/Status-Obsolete-lightgrey)](https://github.com/ndiing/dingklik/issues/new/choose)

## Environment

Default port `9999`, jika port sudah digunakan oleh aplikasi lain,
sesuaikan port pada file `dingklik.env`, di lokasi `%localappdata%/Dingklik`

```js
// Buka `run` dengan cara takan `ctrl + r`
// lalu ketik %localappdata%/Dingklik
// selanjutnya buka file `dingklik.env`
// dan sesuaikan port yang ingin digunakan

// Keterangan
{
    // PORT Server
    // dibutuhkan untuk menjalankan service API
    // melalui jalur http, contoh:
    // http://localhost:9999/api/griyabayar
    "PORT": "9999",

    // Browser
    // dibutuhkan untuk melakukan otentikasi dan otoriasai
    // beberapa gateway API dibutuhkan by pass login, captcha, dan pengaturan sesi
    // dijalankan pada background service / mode headless
    "EXECUTABLE_PATH": "C:\\Users\\DELL\\AppData\\Local\\Google\\Chrome\\Application\\chrome.exe",

    // Database
    // dikarenakan banyak akun bersifat bisnis dan pribadi
    // kami tidak menyimpan data apapun, semua data disimpan
    // pada local komputer masing, demi kenyamanan penggunaan
    // dapat di cek menggunakan aplikasi network monitoring
    // untuk mengetahui data keluar masuk pada jaringan
    "DATABASE_PATH": "C:\\Users\\DELL\\AppData\\Local\\Dingklik\\Database",

    // Userdata
    // semua sesi browser disimpan pada folder ini
    // kami memisahkan semua identitas yang digunakan pada jalur API
    // sehingga dapat digunakan untuk multi / banyak akun dalam jalur API
    "USERDATA_PATH": "C:\\Users\\DELL\\AppData\\Local\\Dingklik\\Data",

    // Serial Number
    "KEY": "INPUT-REGISTERED-KEY"
}

// simpan dan jalankan aplikasi,
// selamat mencoba
```

## Note

-   User interface dalam aplikasi belum tersedia
-   Default access API di `http://localhost:9999/`
-   Cek status & Cek Update pada aplikasi, `bukan error`, keterangan masih sama dengan poin 1 interface sedang dikerjakan
-   Download update secara otomatis, butuh tindakan update seletah ada pemberitahuan, mengantisipasi adanya transaksi yang sedang berjalan
-   Boleh tidak melakukan update selama `2v` sebelumnya, tetapi wajib update jika terdapat perubahan API dari vendor, sifat `penting`

# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

<!-- ## [Unreleased] -->

## [0.5.1] - 2020-10-26

### Fixed

-   Kesalahan `path` system instalasi, kami temukan aplikasi terinstal pada 2 path yaitu `program files` dan `program data`

### Note

-   Perlu tindakan manual untuk ini, uninstall aplikasi `dingklik` terlebih dahulu sebelum update terbaru
-   `Database`/`Userdata`/`Sesi`/`SN` tidak hilang saat uninstall, dan dapat melanjutkan kembali saat menggunakan update terbaru

## [0.5.0] - 2020-10-26

### Added

-   sidompul@com.toko.xl@2.2.5

### Note

-   API FIX/Normal, kecuali penanganan sesi, yang akan kita kerjakan next update
-   API refresh token belum kami dapatkan
-   Mungkin terjadi logout dalam 1 hari penggunaan
-   Akan kita update setelah didapatkan `segera`

## [0.4.2] - 2020-10-26

### Fixed

-   Response server status, with UUID

## [0.4.1] - 2020-10-25

### Fixed

-   Update downloaded pending - issue by `AnggiFauzi@085793712632`

## [0.4.0] - 2020-10-25

### Added

-   Security added, hanya UUID yang terdaftar dapat mengakses aplikasi, minta KEY di WA lihat informasi

## [0.3.2] - 2020-10-24

### Fixed

-   System crash running instance - issue by `AnggiFauzi@085793712632`

## [0.3.1] - 2020-10-24

### Fixed

-   Failed request with API worker - issue by `AnggiFauzi@085793712632`

## [0.3.0] - 2020-10-24

### Fixed

-   ENOENT dingklik.env file/path

### Changed

-   Semantic Versioning

## [0.0.11] - 2020-10-23

### Added

-   rita@com.hutchison.rita@1.2.9

## v0.0.10 [0.0.10] - 2020-10-22

### Added

-   griyabayar@https://griyabayar.com@5.0.0

## v0.0.9 [0.0.9] - 2020-10-21

### Added

-   digiposaja@com.telkomsel.digiposaja@5.1.6

## v0.0.8 [0.0.8] - 2020-10-20

### Added

-   `Pre Release`
