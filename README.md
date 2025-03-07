# Dekirume Online Shop

## *"Belanja Mudah, Pilihan Lengkap!"*

---

## 📌 Daftar Isi

- [Tentang Dekirume](#tentang-dekirume)
  - [Apa itu Dekirume?](#apa-itu-dekirume)
  - [Fitur Utama](#fitur-utama)
  - [Keunggulan Dekirume](#keunggulan-dekirume)
- [Cara Menggunakan](#cara-menggunakan)
- [Tentang Proyek](#tentang-proyek)
- [Tangkapan Layar](#tangkapan-layar)
- [Demo](#demo)
- [Persyaratan](#persyaratan)
- [Skema Database](#skema-database)
- [ERD](#erd)
- [Deskripsi Data](#deskripsi-data)
- [Struktur Folder](#struktur-folder)
- [Tim Kami](#tim-kami)

---

## 📢 Tentang Dekirume

### Apa itu Dekirume?

**Dekirume** adalah platform e-commerce inovatif yang menyediakan kemudahan dalam berbelanja secara online dengan fitur yang lengkap dan canggih. Menggunakan teknologi modern, Dekirume memungkinkan pengguna untuk melakukan transaksi dengan aman, cepat, dan efisien.

Dekirume juga dirancang untuk membantu analisis tren penjualan melalui sistem database yang kuat, memungkinkan bisnis untuk memahami perilaku pelanggan dan meningkatkan strategi pemasaran.

### ✨ Fitur Utama

✔️ **Pencarian Produk Cepat:** Temukan barang yang diinginkan dengan fitur pencarian yang responsif.  
✔️ **Kategori Produk Lengkap:** Produk dikelompokkan berdasarkan kategori untuk kemudahan navigasi.  
✔️ **Manajemen Voucher & Promo:** Nikmati berbagai promo eksklusif untuk pengguna terdaftar.  
✔️ **Metode Pembayaran Fleksibel:** Mendukung berbagai metode pembayaran seperti kartu kredit, e-wallet, dan transfer bank.  
✔️ **Dashboard Interaktif:** Pantau transaksi, histori belanja, dan tren penjualan dalam satu tampilan.

### ⭐ Keunggulan Dekirume

1. **Sistem Terintegrasi:** Semua data produk, transaksi, dan pelanggan tersimpan secara terpusat dan aman.
2. **User-Friendly Interface:** Tampilan antarmuka yang sederhana dan mudah digunakan oleh semua pengguna.
3. **Keamanan Data:** Informasi pelanggan dan transaksi dilindungi dengan sistem enkripsi terkini.
4. **Analisis Data Real-Time:** Menyediakan wawasan mendalam tentang tren penjualan dan preferensi pelanggan.

---

## 🚀 Cara Menggunakan Dekirume

1. **Jelajahi Produk:** Gunakan menu navigasi atau fitur pencarian untuk menemukan barang yang Anda inginkan.
2. **Detail Produk:** Lihat deskripsi, harga, stok, dan diskon sebelum melakukan pembelian.
3. **Tambahkan ke Keranjang:** Klik tombol **"Tambahkan ke Keranjang"** untuk menyimpan produk pilihan.
4. **Gunakan Voucher:** Pilih voucher yang tersedia untuk mendapatkan potongan harga eksklusif.
5. **Proses Pembayaran:** Pilih metode pembayaran yang sesuai, lalu selesaikan transaksi dengan aman.
6. **Pesanan Selesai!** Anda akan menerima konfirmasi dan dapat melacak pesanan melalui akun Dekirume. 🎉

---

## 📄 Tentang Proyek

Proyek ini dikembangkan sebagai bagian dari tugas akhir mata kuliah *Manajemen Data Statistik*. Tujuan utama dari sistem ini adalah untuk menganalisis pola penjualan, perilaku pelanggan, dan efektivitas voucher dalam transaksi e-commerce.

Dengan menggunakan **R**, **PostgreSQL**, dan **Shiny**, proyek ini menciptakan dashboard interaktif untuk memudahkan visualisasi dan analisis data secara real-time.

---

## 📸 Tangkapan Layar

**Tampilan Beranda**  
![Beranda](Image/Screenshot_Home.png)

**Galeri Produk**  
![Produk](Image/Screenshot_Gallery_Product.png)

**Detail Transaksi**  
![Transaksi](Image/Screenshot_Transaction.png)

**Voucher & Promo**  
![Voucher](Image/Screenshot_Voucher.png)

**Metode Pembayaran**  
![Pembayaran](Image/Screenshot_Payment.png)

---

## 🎥 Demo

🔗 **Lihat demo proyek kami di:** [Dekirume Dashboard](https://yudheeet1991.shinyapps.io/mdskel4app/#)

---

## ⚠️ Persyaratan

- **Bahasa Pemrograman & Tools:** R (`rvest`, `tidyverse`, `rio`, `kableExtra`, `stringr`)
- **Database:** PostgreSQL & ElephantSQL
- **Framework Dashboard:** `shiny`, `shinythemes`, `bs4Dash`, `DT`, `dplyr`

---

## 🗂️ Skema Database

📌 **Diagram Relasi Antar Entitas**  
![Skema Database](Image/skema.png)

### 📌 Struktur Database

| **Entitas**        | **Atribut Utama** | **Relasi**                  |
| ------------------ | ----------------- | --------------------------- |
| **Customer**       | `customerid`      | -                           |
| **Product**        | `productid`       | Transaksi                   |
| **Voucher**        | `voucherid`       | Transaksi                   |
| **Payment Method** | `pmid`            | Transaksi                   |
| **Transaction**    | `transactionid`   | Menghubungkan semua entitas |

---

## 🔗 ERD

📊 **Entity-Relationship Diagram (ERD)**  
![ERD](Image/online_shop_erd.png)

---

## 📊 Deskripsi Data

Struktur tabel yang digunakan dalam database Dekirume.

**Contoh pembuatan tabel `Product`**:

```sql
CREATE TABLE Product (
    ProductID VARCHAR(20) PRIMARY KEY,
    Product_name TEXT NOT NULL,
    Product_Description TEXT NOT NULL,
    Product_Category TEXT NOT NULL,
    Stock INTEGER NOT NULL,
    Price NUMERIC NOT NULL
);
```

---

## 📂 Struktur Folder

📁 **Struktur direktori proyek**:

```
.
├── Image
├── app           # Aplikasi Shiny
│   ├── css
│   ├── server.R
│   └── ui.R
├── data          # Data proyek
│   ├── csv
│   └── sql
│       └── db.sql
├── doc           # Dokumentasi proyek
├── src           # Kode sumber proyek
├── .gitignore
└── README.md
```

---

## ❤️ Tim Kami
### Backend Developer: [nama](https://github.com/nama)
![nama](Image/nama)

### Database Manager: [nama](https://github.com/nama)
![nama](Image/nama.png)

### Technical Writer: [nama](https://github.com/nama)
![nama](Image/nama.png)

### Frontend Developer: [nama](https://github.com/nama)
![nama](Image/nama.png)

---

📢 **Terima kasih telah membaca dokumentasi ini!** Jika ada pertanyaan atau saran, jangan ragu untuk menghubungi tim kami. Selamat berbelanja dengan Dekirume! 🚀
