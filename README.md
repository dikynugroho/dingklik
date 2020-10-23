# Dingklik

AIO (All In One) `Gateway API` dan `Addon OtomaX`

## Informasi

-   [![GitHub release (latest SemVer including pre-releases)](https://img.shields.io/github/v/release/ndiing/dingklik?include_prereleases)](https://github.com/ndiing/dingklik/releases/latest)
-   [![GitHub All Releases](https://img.shields.io/github/downloads/ndiing/dingklik/total)](https://github.com/ndiing/dingklik/releases/latest)
-   [![](https://img.shields.io/badge/readme-changelog-blue)](https://github.com/ndiing/dingklik/blob/main/CHANGELOG.md)
-   [![GitHub Release Date](https://img.shields.io/github/release-date/ndiing/dingklik)](https://github.com/ndiing/dingklik/releases/latest)
-   [![GitHub last commit](https://img.shields.io/github/last-commit/ndiing/dingklik)](https://github.com/ndiing/dingklik/releases/latest)
-   [![GitHub issues](https://img.shields.io/github/issues/ndiing/dingklik)](https://github.com/ndiing/dingklik/issues/new/choose)
-   [![](https://img.shields.io/badge/whatsapp-ndiing-green)](https://web.whatsapp.com/send?phone=6281935155404&text=)
-   [![](https://img.shields.io/badge/whatsapp-anis@winarno-green)](https://web.whatsapp.com/send?phone=6281556880910&text=)

## Dokumentasi

-   [x] [![](https://img.shields.io/badge/dokumentasi-digiposaja@com.telkomsel.digiposaja@5.1.6-brightgreen)](https://github.com/ndiing/dingklik/blob/main/private/api/digiposaja/README.md)
-   [x] [![](https://img.shields.io/badge/dokumentasi-griyabayar@https://griyabayar.com@5.0.0-brightgreen)](https://github.com/ndiing/dingklik/blob/main/private/api/griyabayar/README.md)
-   [x] [![](https://img.shields.io/badge/dokumentasi-rita@com.hutchison.rita@1.2.9-brightgreen)](https://github.com/ndiing/dingklik/blob/main/private/api/rita/README.md)
-   [ ] [![](https://img.shields.io/badge/dokumentasi-sris@https://sris.smartfren.com@1.2.42-yellow)](https://github.com/ndiing/dingklik/blob/main/private/api/sris/README.md)
-   [ ] [![](https://img.shields.io/badge/dokumentasi-sidompul@com.toko.xl@2.2.5-blue)](https://github.com/ndiing/dingklik/blob/main/private/api/sidompul/README.md)
-   [ ] [![](https://img.shields.io/badge/dokumentasi-myim3@https://myim3.indosatooredoo.com@latest-blue)](https://github.com/ndiing/dingklik/blob/main/private/api/myim3/README.md)
-   [ ] [![](https://img.shields.io/badge/dokumentasi-whatsapp@https://web.whatsapp.com@2.2043.8-blue)](https://github.com/ndiing/dingklik/blob/main/private/api/whatsapp/README.md)

## Status

-   [![](https://img.shields.io/badge/status-maintenance-red)](https://github.com/ndiing/dingklik/issues/new/choose)
-   [![](https://img.shields.io/badge/status-development-yellow)](https://github.com/ndiing/dingklik/issues/new/choose)
-   [![](https://img.shields.io/badge/status-production-brightgreen)](https://github.com/ndiing/dingklik/issues/new/choose)
-   [![](https://img.shields.io/badge/status-schedule-blue)](https://github.com/ndiing/dingklik/issues/new/choose)
-   [![](https://img.shields.io/badge/status-deprecated-lightgrey)](https://github.com/ndiing/dingklik/issues/new/choose)

## Environment

Jika dibutuhkan penyesuaian pada aplikasi, dapat diatur pada file `dingklik.env`, di `%localappdata%/Dingklik`

```js
{
    // PORT Server
    // Default 9999
    // http://localhost:9999/api/setting
    "PORT": "9999",

    // Chrome Browser
    // Sebagaian gateway API menggunakan browser dengan mode headless
    // Seperti griyabayar dibutuhkan by pass captcha
    "EXECUTABLE_PATH": "C:\\Users\\QWERTY\\AppData\\Local\\Google\\Chrome\\Application\\chrome.exe",

    // Database Server
    // Digunakan untuk menyimpan informasi pengguna
    // Seperti akun griyabayar dibutuhkan penyimpanan ke database
    // yang nantinya digunakan untuk by pass login 
    "DATABASE_PATH": "C:\\Users\\QWERTY\\AppData\\Local\\Dingklik\\Database",

    // User Data Browser
    // Digunakan untuk menyimpan cookies dan storage
    // Digunakan untuk menyimpan session agan tidak perlu login berulang
    "USERDATA_PATH": "C:\\Users\\QWERTY\\AppData\\Local\\Dingklik\\Data"
}
```

# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

-   sris@https://sris.smartfren.com@1.2.42
-   sidompul@com.toko.xl@2.2.5
-   myim3@https://myim3.indosatooredoo.com@latest
-   whatsapp@https://web.whatsapp.com@2.2043.8

## [0.3.0] - 2020-10-24

### Fixed

-   ENOENT dingklik.env file/path

### Changed

-   Semantic Versioning

## [0.0.11] - 2020-10-23

### Added

-   rita@com.hutchison.rita@1.2.9

## v0.0.10 [0.0.10]

### Added

-   griyabayar@https://griyabayar.com@5.0.0

## v0.0.9 [0.0.9]

### Added

-   digiposaja@com.telkomsel.digiposaja@5.1.6

## v0.0.8 [0.0.8]

### Added

-   Released
