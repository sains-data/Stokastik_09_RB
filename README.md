# Analisis Rantai Markov — Brand Switching Smartphone
### Studi Kasus: Mahasiswa Sains Data ITERA (130 Responden)

![status](https://img.shields.io/badge/Status-Finished-brightgreen)
![language](https://img.shields.io/badge/Language-R-blue)
![license](https://img.shields.io/badge/License-ITERA-orange)
![last-update](https://img.shields.io/badge/Update-2025-important)

---

## Deskripsi Singkat
Project ini menganalisis **pola perpindahan merek (brand switching) smartphone** di kalangan **130 mahasiswa Program Studi Sains Data ITERA (terkhusus hanya angkatan 2022)**, menggunakan **pemodelan stokastik Rantai Markov**.  
Hasil analisis menghasilkan:
- **Matriks probabilitas transisi (P¹)**
- **Probabilitas perpindahan 2 langkah (P²)**
- **Distribusi stasioner (steady state)** untuk memproyeksikan pangsa pasar smartphone jangka panjang

**Kesimpulan utama**:  
**Samsung, iPhone, dan Xiaomi** diproyeksikan menjadi **merek dominan jangka panjang**, sedangkan **Oppo & Vivo menunjukkan loyalitas rendah** karena seluruh pengguna mereka berpindah ke merek lain.

---

## Struktur Project
```text
📁 Markov-BrandSwitching-Smartphone
│
├── code.Rmd
├── dataset_responden.xlsx
├── 📂 outputs
│   └── laporan.pdf
│   └── poster.png
│   └── video.mp4
└── README.md
```
---

## Instalasi & Dependensi
```Pastikan R sudah terpasang (versi ≥ 4.3.0) bersama library berikut:
install.packages(c("readxl", "dplyr", "ggplot2", "igraph", "ggraph", "stringr"))
```
---
## Cara Menjalankan Analisis
```Clone repository:
git clone https://github.com/<username>/Markov-BrandSwitching-Smartphone.git
cd Markov-BrandSwitching-Smartphone
```
```Jalankan script utama:
source("main.R")
```
- Output yang dihasilkan:
- Matriks transisi P¹
- Probabilitas P²
- Vektor distribusi stasioner
- Diagram transisi probabilitas (network graph)
- Grafik perbandingan jumlah pengguna setiap merek

## Hasil Utama
Probabilitas Retensi (P¹)
| Merek   | Prob   |
| ------- | ------ |
| iPhone  | 0.6667 |
| Samsung | 0.5000 |
| Oppo    | 0.0000 |
| Vivo    | 0.0000 |


Distribusi Stasioner (Steady State)
| Merek   | Prob   |
| ------- | ------ |
| Samsung | 0.3779 |
| iPhone  | 0.2664 |
| Xiaomi  | 0.1804 |
| Lainnya | < 0.07 |

## Interpretasi
- Samsung & iPhone → retensi tertinggi & tujuan perpindahan utama
- Xiaomi → posisi transisi value-for-money
- Oppo & Vivo → loyalitas rendah; seluruh pengguna berpindah
- Pasar smartphone mahasiswa menunjukkan pola oligopolistik

## Peneliti / Developer
| Nama                       | Role                        |
| -------------------------- | --------------------------- |
| **Danang Hilal Kurniawan** | Data Scientist              |
| Rut Junita Sari Siburian   | Data Scientist              |
| Izza Lutfia                | Data Scientist              |
| Try Yani Rizki Nur Rohmah  | Data Scientist              |
