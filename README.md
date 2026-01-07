# SmartSpense: AI-Powered Expense Tracker 📱💸

![Kotlin](https://img.shields.io/badge/Kotlin-2.0-purple?style=for-the-badge&logo=kotlin)
![Jetpack Compose](https://img.shields.io/badge/Jetpack%20Compose-Material3-green?style=for-the-badge&logo=android)
![Architecture](https://img.shields.io/badge/Clean%20Architecture-MVVM-orange?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active%20Development-blue?style=for-the-badge)

> **SmartScan** adalah aplikasi pencatat keuangan modern yang memanfaatkan **On-Device Machine Learning (ML Kit)** untuk mengotomatisasi input data. Cukup foto struk belanja, dan aplikasi akan mengekstrak total harga dan tanggal secara otomatis.

---

## 📸 Screenshots & Demo

| Dashboard (Home) | Camera Scanner (OCR) | Expense Detail | Analytics |
|:---:|:---:|:---:|:---:|
| ![Home](link-gambar-home.png) | ![Scan](link-gambar-scan.png) | ![Detail](link-gambar-detail.png) | ![Chart](link-gambar-chart.png) |

---

## ✨ Key Features

* **🧾 AI Receipt Scanner:** Menggunakan **Google ML Kit** dan **CameraX** untuk memindai struk belanja fisik dan melakukan ekstraksi teks (OCR) secara *real-time*.
* **📂 Offline-First Architecture:** Data tersimpan lokal menggunakan **Room Database**, aplikasi tetap berfungsi 100% tanpa koneksi internet.
* **📊 Insightful Analytics:** Visualisasi pengeluaran bulanan dengan grafik interaktif.
* **🎨 Modern UI/UX:** Dibangun sepenuhnya dengan **Jetpack Compose** (Material 3) mendukung Dark/Light mode.
* **🔍 Smart Parsing Logic:** Algoritma custom untuk mendeteksi pola harga dan tanggal dari teks mentah hasil OCR.

---

## 🛠 Tech Stack & Libraries

Project ini dibangun dengan standar **Modern Android Development (MAD)** terbaru:

* **Language:** Kotlin 100%
* **UI Toolkit:** Jetpack Compose (No XML)
* **Architecture Pattern:** Clean Architecture (Presentation, Domain, Data layers) + MVVM
* **Dependency Injection:** Dagger Hilt
* **Local Storage:** Room Database (SQLite)
* **Asynchronous:** Kotlin Coroutines & Flow
* **Hardware Integration:** CameraX
* **Machine Learning:** Google ML Kit (Text Recognition v2)
* **Image Loading:** Coil

---

## 🏗 Architecture Overview

Saya menerapkan prinsip **Clean Architecture** untuk memastikan kode yang *scalable*, *testable*, dan mudah dipelihara (Maintainable).

```text
com.example.smartscan
├── data                # Repository Impl, Room DB, API Sources
├── domain              # Use Cases, Repository Interface, Entity Models (Pure Kotlin)
├── presentation        # UI (Compose), ViewModels, State Holders
└── di                  # Dependency Injection Modules (Hilt)
