# 🖼️ ImageForge - PNG to JPG Converter

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1PjLz6x7v4LYImHYauHyOzTcTPXDsBuMV?usp=sharing)
![Python](https://img.shields.io/badge/python-3.10+-blue.svg)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Version](https://img.shields.io/badge/version-v1.0-green)
![Status](https://img.shields.io/badge/status-active-success)

---

Batch image converter untuk mengubah file **PNG → JPG/JPEG** secara otomatis.

Dirancang khusus untuk workflow batch processing sebelum proses **image upscaling** atau **AI pipeline** lainnya yang membutuhkan format JPG tanpa transparansi.

--- 

## ✨ Features

-   📂 **Batch PNG Conversion**: Konversi banyak file PNG sekaligus ke JPG atau kembali ke PNG.
-   🎯 **Preserve Filename**: Nama file asli dipertahankan, hanya ekstensinya yang diubah.
-   ⚙️ **Adjustable JPEG Quality**: Kontrol kualitas kompresi untuk output JPG (10-100).
-   📦 **Automatic Output Folder**: Hasil konversi disimpan dalam folder terpisah untuk menjaga kerapian.
-   🚀 **Fast Processing**: Dioptimalkan untuk pemrosesan gambar yang cepat.
-   🖼️ **Transparent PNG to JPG Handling**: Secara otomatis mengisi latar belakang transparan (alpha channel) PNG dengan warna putih saat dikonversi ke JPG, cocok untuk workflow AI.
-   🌐 **Gradio Interface**: Antarmuka pengguna yang intuitif dan mudah digunakan melalui Gradio.
-   ☁️ **Colab Optimized**: Dirancang untuk berjalan mulus di Google Colab dengan tunneling Cloudflare untuk akses publik.

---

## 🚀 Cara Menggunakan (Google Colab)

1.  **Buka di Google Colab**: Klik tombol "Open in Colab" di atas (atau di file `ImageForge.ipynb`).
2.  **Jalankan Semua Sel**: Jalankan semua sel kode secara berurutan. Anda bisa melakukannya dengan `Runtime` -> `Run all`.
3.  **Instalasi Dependensi**: Sel pertama akan menginstal pustaka yang diperlukan (`gradio`).
4.  **Aplikasi Berjalan**: Setelah semua sel dijalankan, Anda akan melihat link Cloudflare di bagian output sel terakhir (biasanya dimulai dengan `https://....trycloudflare.com`).
5.  **Akses Aplikasi**: Klik link tersebut untuk membuka antarmuka ImageForge di browser Anda.
6.  **Unggah & Konversi**: Unggah gambar PNG atau JPG Anda, pilih format target dan kualitas (untuk JPG), lalu klik "Mulai Konversi 🚀".
7.  **Unduh Hasil**: Hasil konversi akan tersedia untuk diunduh sebagai file tunggal atau file ZIP jika Anda mengunggah banyak gambar.

---

## ☕ Support Me

Dukungan Anda sangat berarti untuk membantu keberlanjutan riset teknologi dan pengembangan project kreatif lainnya di masa depan.

| Platform | Link Dukungan |
| :--- | :--- |
| **Trakteer** | [trakteer.id/pyforge](https://trakteer.id/pyforge) |
| **Saweria** | [saweria.co/pyforge](https://saweria.co/pyforge) |
| **SociaBuzz** | [sociabuzz.com/pyforge](https://sociabuzz.com/pyforge) |
| **PayPal** | [paypal.me/Masyura](https://www.paypal.com/paypalme/Masyura) |

---

## ⚖️ Lisensi

Project ini dilisensikan di bawah **MIT License**. Anda bebas menggunakan, mengubah, dan mendistribusikan kode ini untuk keperluan pribadi maupun komersial.

Copyright (c) 2026 **masyuraC7**

---
Dibuat dengan ❤️ oleh **masyuraC7** – Full Stack Programmer & Creative Content Creator.
