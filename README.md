# 🚀 Easy-RealESRGAN-Image-Upscaler

[![Open In Kaggle](https://img.shields.io/badge/Open%20in-Kaggle-blue?logo=kaggle)](https://www.kaggle.com/)
[![Python 3.12+](https://img.shields.io/badge/python-3.12+-blue.svg)](https://www.python.org/downloads/)
[![Real-ESRGAN](https://img.shields.io/badge/Real--ESRGAN-v0.3.0-brightgreen)](https://github.com/xinntao/Real-ESRGAN)

Proyek ini menyediakan antarmuka sederhana untuk melakukan **upscaling gambar** menggunakan **Real-ESRGAN** di lingkungan Kaggle. Dengan berbagai pilihan kualitas, model, dan faktor pembesaran, Anda dapat meningkatkan resolusi gambar umum maupun anime dengan hasil yang memuaskan.

## ✨ Fitur Utama

- **3 tingkat kualitas**: `ultra`, `high`, `balanced`, `fast` – dari kualitas terbaik hingga paling cepat.
- **2 mode gambar**: `general` (foto/umum) dan `anime` (ilustrasi/animasi).
- **Faktor pembesaran**: 2x atau 4x.
- **Upload**: dukungan untuk gambar tunggal maupun banyak gambar dalam folder.
- **Face enhancement** (khusus mode `ultra`): memperbaiki detail wajah menggunakan GFPGAN.
- **Automatis men-download model** yang diperlukan dan memverifikasi integritasnya.
- **Kompatibel dengan Python 3.12+** (patch otomatis untuk masalah `rgb_to_grayscale`).

## 📋 Daftar Isi

- [Persyaratan Sistem](#persyaratan-sistem)
- [Instalasi & Persiapan](#instalasi--persiapan)
- [Struktur Kode](#struktur-kode)
- [Penggunaan](#penggunaan)
  - [Upscale Gambar Tunggal](#upscale-gambar-tunggal)
  - [Upscale Banyak Gambar (Batch)](#upscale-banyak-gambar-batch)
- [Penjelasan Parameter](#penjelasan-parameter)
  - [image_type (Mode Gambar)](#image_type-mode-gambar)
  - [scale (Faktor Pembesaran)](#scale-faktor-pembesaran)
  - [quality (Tingkat Kualitas)](#quality-tingkat-kualitas)
- [Contoh Lengkap](#contoh-lengkap)
- [Mengatasi Masalah Umum](#mengatasi-masalah-umum)
- [Referensi](#referensi)
- [Kontribusi](#kontribusi)
- [Lisensi](#lisensi)

## 💻 Persyaratan Sistem

- **Kaggle Notebook** dengan akses GPU (disarankan GPU P100 atau T4).
- **Internet** aktif untuk mengunduh model (hanya sekali).
- **RAM/VRAM** yang cukup (untuk gambar besar, gunakan mode dengan `tile`).

## ⚙️ Instalasi & Persiapan

Jalankan seluruh sel di notebook secara berurutan. Bagian pertama akan:

1. Meng-clone repository Real-ESRGAN.
2. Menginstal dependensi (`basicsr`, `gfpgan`, `facexlib`, dll).
3. Menerapkan patch kompatibilitas Python 3.12+.
4. Mengunduh model-model yang diperlukan dengan verifikasi ukuran.

Setelah proses instalasi selesai, Anda akan melihat pesan **✅ SEMUA MODEL WAJIB BERHASIL DIUNDUH!** jika semuanya berjalan lancar.

## 📁 Struktur Kode

- **`QualityConfig`** – kelas konfigurasi yang menyimpan daftar model dan preset kualitas.
- **`RealESRGANUpscaler`** – kelas utama untuk mengatur proses upscaling.
- **`upscale_single`** – fungsi pembantu untuk memproses satu gambar.
- **`upscale_batch`** – fungsi pembantu untuk memproses banyak gambar dalam folder.
- **Bagian eksekusi** – contoh pemanggilan fungsi dengan parameter pilihan.

## 🛠️ Penggunaan

### Upscale Gambar Tunggal

```python
result = upscale_single(
    image_path='/path/to/image.jpg',
    image_type='general',   # atau 'anime'
    scale=4,                # 2 atau 4
    quality='high',         # 'ultra', 'high', 'balanced', 'fast'
    output_name='hasil'     # (opsional) nama file output
)
print(f"Hasil tersimpan di: {result}")
```

### Upscale Banyak Gambar

```python
results = upscale_batch(
    input_folder='/path/to/folder',   # folder berisi gambar
    image_type='anime',
    scale=4,
    quality='balanced',
    output_folder='/path/to/output'   # (opsional) folder tujuan
)
print(f"{len(results)} gambar berhasil diproses.")
```

## 📌 Penjelasan Parameter
soon

## 🌟 Contoh Lengkap
soon

## ⚠️ Mengatasi Masalah Umum
soon

## 📚 Referensi
soon

## 🤝 Kontribusi

Kontribusi sangat diterima! Jika Anda menemukan bug atau memiliki saran fitur, silakan buka issue atau kirim pull request. Pastikan untuk mengikuti pedoman kontribusi yang berlaku.

## 📄 Lisensi

Proyek ini dilisensikan di bawah MIT License – lihat file LICENSE untuk detail lebih lanjut.

<hr>

Dibuat dengan ❤️ untuk komunitas Kaggle dan open source.
