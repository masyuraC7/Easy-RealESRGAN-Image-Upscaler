# 🚀 Easy-RealESRGAN-Image-Upscaler

[![Open In Kaggle](https://img.shields.io/badge/Open%20in-Kaggle-blue?logo=kaggle)](https://www.kaggle.com/code/pyrisforge/easy-realesrgan-image-upscaler)
[![Python 3.12+](https://img.shields.io/badge/python-3.12+-blue.svg)](https://www.python.org/downloads/)
[![Real-ESRGAN](https://img.shields.io/badge/Real--ESRGAN-v0.3.0-brightgreen)](https://github.com/xinntao/Real-ESRGAN)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Proyek ini menyediakan antarmuka sederhana untuk melakukan **upscaling gambar** menggunakan **Real-ESRGAN** di lingkungan Kaggle. Dengan berbagai pilihan kualitas, model, dan faktor pembesaran, Anda dapat meningkatkan resolusi gambar umum maupun anime dengan hasil yang memuaskan.

---

## ✨ Fitur Utama

* **4 Tingkat Kualitas**: Tersedia opsi `ultra`, `high`, `balanced`, dan `fast` untuk menyesuaikan antara kecepatan dan detail hasil.
* **2 Mode Gambar**: Mendukung mode `general` untuk foto/umum dan `anime` untuk ilustrasi/animasi.
* **Faktor Pembesaran**: Pilihan skala perbesaran 2x atau 4x.
* **Manajemen Data**: Dukungan upload gambar tunggal maupun banyak gambar sekaligus melalui interface interaktif.
* **Face Enhancement**: Perbaikan detail wajah secara otomatis menggunakan integrasi GFPGAN pada mode kualitas tertinggi.
* **Otomasi Model**: Sistem otomatis mengunduh model yang diperlukan dan memverifikasi integritas file sebelum dijalankan.
* **Kompatibilitas Modern**: Sudah menyertakan patch otomatis untuk berjalan mulus di Python 3.12+.

---

## 📋 Daftar Isi

- [Persyaratan Sistem](#persyaratan-sistem)
- [Instalasi & Persiapan](#instalasi--persiapan)
- [Struktur Kode](#struktur-kode)
- [Penjelasan Parameter](#penjelasan-parameter)
- [Mengatasi Masalah Umum](#mengatasi-masalah-umum)
- [☕ Support Me](#-support-me)
- [📚 Referensi](#-referensi)
- [⚖️ Lisensi](#-lisensi)

---

## 💻 Persyaratan Sistem

* **Kaggle Notebook**: Wajib menggunakan lingkungan Kaggle dengan akses GPU aktif (P100 atau T4).
* **Koneksi Internet**: Diperlukan untuk mengunduh model dan dependensi pada saat inisialisasi awal.
* **Alokasi VRAM**: Untuk gambar beresolusi sangat besar, disarankan menggunakan mode kualitas dengan mekanisme `tile`.

---

## ⚙️ Instalasi & Persiapan

Proses persiapan dilakukan secara otomatis melalui sel-sel notebook yang mencakup:
1. **Repository Cloning**: Mengambil source code resmi Real-ESRGAN.
2. **Dependency Install**: Pemasangan paket `basicsr`, `gfpgan`, `facexlib`, dan pustaka pendukung lainnya.
3. **Compatibility Patch**: Perbaikan otomatis pada library BasicSR agar kompatibel dengan versi Python terbaru.
4. **Model Verification**: Pengunduhan bobot model (weights) secara otomatis ke folder yang ditentukan.

---

## 📁 Struktur Kode

Proyek ini dirancang secara modular agar mudah dipelajari atau dikembangkan kembali:
* **`QualityConfig`**: Kelas sentral yang menyimpan preset konfigurasi, daftar model, dan ukuran tile untuk setiap tingkat kualitas.
* **`RealESRGANUpscaler`**: Engine utama yang menangani inisialisasi model, pemrosesan gambar, dan penanganan memori GPU.
* **`Data Manager Interface`**: Komponen UI interaktif menggunakan `ipywidgets` untuk memudahkan pengguna mengelola file input tanpa menyentuh kode.
* **Visualisasi**: Sistem perbandingan berdampingan (side-by-side) untuk melihat perbedaan sebelum dan sesudah proses upscale.

---

## 📌 Penjelasan Parameter

| Parameter | Opsi | Deskripsi |
| :--- | :--- | :--- |
| **image_type** | `general`, `anime` | Tentukan kategori gambar untuk hasil optimal (mode `anime` menjaga garis tetap halus). |
| **scale** | `2`, `4` | Target perbesaran resolusi dari ukuran asli. |
| **quality** | `ultra`, `high`, `balanced`, `fast` | Mengatur keseimbangan antara detail tekstur, perbaikan wajah, dan kecepatan proses. |

---

## ⚠️ Mengatasi Masalah Umum

* **`[Errno 2] No such file or directory`**: Pastikan Anda telah mengunggah gambar di bagian Data Manager atau memasukkan path dataset Kaggle dengan benar.
* **Out of Memory (OOM)**: Jika GPU kehabisan memori saat memproses gambar besar, coba turunkan tingkat kualitas ke `balanced` atau `fast`.
* **Proses Terhenti**: Pastikan sesi Kaggle Anda memiliki koneksi internet dan GPU Accelerator sudah dinyalakan pada menu *Settings* notebook.

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

## 📚 Referensi

* **Real-ESRGAN Core**: [xinntao/Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN)
* **Face Restoration**: [TencentARC/GFPGAN](https://github.com/TencentARC/GFPGAN)
* **Framework**: [XPixelGroup/BasicSR](https://github.com/XPixelGroup/BasicSR)

---

## ⚖️ Lisensi

Project ini dilisensikan di bawah **MIT License**. Anda bebas menggunakan, mengubah, dan mendistribusikan kode ini untuk keperluan pribadi maupun komersial.

Copyright (c) 2026 **PyForge**

---
Dibuat dengan ❤️ oleh **PyForge** – Full Stack Programmer & Creative Content Creator.
