# 🚀 PromptForge — Batch Prompt Processing Toolkit

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1jCktX5ExxhJ8idt6VPET_Z5brElOYfD6?usp=sharing)
![Python](https://img.shields.io/badge/python-3.10+-blue.svg)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Version](https://img.shields.io/badge/version-v1.0-green)
![Status](https://img.shields.io/badge/status-active-success)

---

PromptForge adalah tool untuk membersihkan, mengelompokkan, dan mengekspor prompt secara otomatis berdasarkan **aspect ratio**.

Tool ini dirancang untuk mempercepat workflow batch generation pada berbagai AI image generator.

---

## ✨ Key Capabilities

- 📥 Multiple input modes  
  - Paste text  
  - Upload `.txt` file  

- 🧹 Prompt cleaning  
  - Remove duplicate prompts  
  - Normalize whitespace  

- ⚙️ Smart processing  
  - Auto suffix injection  
  - Ratio-based prompt grouping  

- 📦 Batch exporting  
  - Export per aspect ratio  
  - Optional ZIP packaging  
  - Automatic download  

---

## 🧩 Interface Setup

Bagian ini membangun **interactive interface** menggunakan `ipywidgets`.

Interface memungkinkan pengguna untuk:

- Memilih mode input
- Mengatur opsi pemrosesan
- Mengontrol output file

Komponen utama yang dibuat:

- Input mode selector  
- Text input area  
- File upload system  
- Processing options  
- Execution button  
- Status display

## 🧠 Core Processing Engine

Bagian ini berisi logika utama untuk memproses prompt.

Pipeline yang dijalankan:

1. Membaca input text
2. Mendeteksi **aspect ratio**
3. Membersihkan prompt
4. Menambahkan suffix (opsional)
5. Menghapus duplicate prompt
6. Mengelompokkan prompt berdasarkan ratio
7. Menyimpan hasil ke file

Parsing dilakukan menggunakan **regular expressions** untuk memastikan struktur prompt tetap konsisten.

## 📦 Export System

Prompt hasil pemrosesan akan diekspor secara otomatis.

Format output:

- Satu file per aspect ratio
- Nama file berbasis timestamp
- Folder batch otomatis dibuat

Opsional:

- Download otomatis
- ZIP packaging
- Blank line separation

## ▶️ Usage Guide

Ikuti langkah berikut untuk menggunakan PromptForge:

1️⃣ Pilih **Input Mode**

- `Paste Text`
atau  
- `Upload File`

---

2️⃣ Atur opsi pemrosesan

Opsional:

- Remove duplicate prompts
- Add suffix
- Separate with blank space
- Auto download
- Auto zip files

---

3️⃣ Klik tombol:

**PROCESS PROMPTS**

---

4️⃣ File hasil akan:

- Dibuat otomatis
- Diunduh otomatis (jika aktif)

## 📁 Output Structure

Setiap batch akan menghasilkan folder:
- Batch_YYYYMMDD_HHMMSS/
  - BatchPrompt_16x9_TIMESTAMP.txt
  - BatchPrompt_1x1_TIMESTAMP.txt
  - BatchPrompt_9x16_TIMESTAMP.txt
  - Batch_YYYYMMDD_HHMMSS.zip