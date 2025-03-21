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
- [Struktur Database](#struktur-database)
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
3. **Gunakan Voucher:** Pilih voucher yang tersedia untuk mendapatkan potongan harga eksklusif.
4. **Proses Pembayaran:** Pilih metode pembayaran yang sesuai, lalu selesaikan transaksi dengan aman.
5. **Pesanan Selesai!** Pesanaan Anda akan segera diproses oleh Dekirume. 🎉

---

## 📄 Tentang Proyek
Proyek ini dikembangkan sebagai bagian dari tugas akhir mata kuliah *Manajemen Data Statistik*. Tujuan utama dari sistem ini adalah untuk menganalisis pola penjualan, perilaku pelanggan, dan efektivitas voucher dalam transaksi e-commerce.

Dengan menggunakan **R** dan **Shiny**, proyek ini menciptakan dashboard interaktif untuk memudahkan visualisasi dan analisis data secara real-time.

---

## 📸 Tangkapan Layar

### - Home  
<p align="center">
  <img width="900" height="500" src="Images/Home.jpg">
</p>

### - Product  
<p align="center">
  <img width="900" height="500" src="Images/Product.jpg">
</p>

### - Transactions  
<p align="center">
  <img width="900" height="500" src="Images/Transaction.jpg">
</p>

### - Voucher  
<p align="center">
  <img width="900" height="500" src="Images/Voucher.jpg">
</p>

### - Payment Methods  
<p align="center">
  <img width="900" height="500" src="Images/Payment.jpg">
</p>
---

## 📌 Struktur Database

| **Entitas**        | **Atribut Utama** | **Relasi**                  |
| ------------------ | ----------------- | --------------------------- |
| **Customer**       | `customerid`      | Transaksi                   |
| **Product**        | `productid`       | Transaksi                   |
| **Voucher**        | `voucherid`       | Transaksi                   |
| **Payment Method** | `pmid`            | Transaksi                   |
| **Transaction**    | `transactionid`   | Menghubungkan semua entitas |

---

## 🔗 ERD

📊 **Entity-Relationship Diagram (ERD)**  
Dokumentasi ini menyajikan Entity-Relationship Diagram (ERD) yang digunakan untuk memodelkan struktur data dalam sistem. ERD merupakan representasi visual dari entitas, atribut, serta hubungan antar entitas dalam basis data, yang bertujuan untuk memberikan pemahaman yang jelas mengenai desain dan alur data.

![ERD](Images/ERD.png)

---

## 📊 Deskripsi Data
Repositori ini berisi data dan dokumentasi terkait Dekirume. Data ini dikumpulkan dan diproses untuk mendukung analisis serta pengembangan lebih lanjut dalam konteks penggunaannya. Struktur tabel yang digunakan dalam database Dekirume.

### Create Table Customer
Tabel customer berisi informasi penting mengenai data pelanggan, memungkinkan pengguna untuk mengakses berbagai detail terkait identitas pelanggan. Informasi yang tercakup dalam tabel ini meliputi Customer ID sebagai identitas unik setiap pelanggan, jenis kelamin, serta lokasi pelanggan yang mencakup empat wilayah utama, yaitu California, New York, Chicago, dan New Jersey. Selain itu, tabel ini juga mencatat rentang usia pelanggan, yang berada dalam kisaran 17 hingga 63 tahun.

| Attribute          | Type                  | Description                     |
|:-------------------|:----------------------|:--------------------------------|
| customerid         | integer               | Id Customer                     |
| gender             | varchar               | Jenis Kelamin                   |
| locations          | varchar		           | Lokasi                          |
| age		             | integer	 	           | Umur	                           |

dengan syntax SQL sebagai berikut : 

```sql
CREATE TABLE IF NOT EXISTS data_customer (
      CustomerID INT PRIMARY KEY,
      Gender VARCHAR(10),
      Locations VARCHAR(50),
      Age INT
    );
```
### Create Table Voucher
Tabel voucher menyajikan informasi mendetail mengenai voucher yang tersedia. Selain mengetahui jumlah produk yang memenuhi syarat untuk penggunaan voucher, pengguna juga dapat mengakses berbagai data penting terkait voucher yang dapat digunakan. Informasi yang disediakan mencakup nama voucher sebagai identitasnya serta nilai diskon yang diberikan melalui voucher tersebut.

| Attribute                  | Type                  | Description                     		       |
|:---------------------------|:----------------------|:------------------------------------------|
| voucherid                  | varchar               | Id Voucher                       	       |
| voucher_name               | varchar	      	     | Nama Voucher                  		         |
| discount                   | decimal(5,2)	         | Besaran Diskon dari Setiap Voucher        |	

dengan syntax SQL sebagai berikut :

```sql
CREATE TABLE IF NOT EXISTS data_voucher (
      VoucherID VARCHAR(10) PRIMARY KEY,
      Voucher_name VARCHAR(100),
      Discount DECIMAL(5,2)
    );
```
### Create Table Payment Method
Tabel payment method menyajikan informasi mengenai metode pembayaran yang tersedia bagi pengguna. Tabel ini mencakup empat jenis metode pembayaran utama, yaitu kartu, PayPal, dompet digital, serta metode lainnya. Setiap metode pembayaran diidentifikasi dengan PMID (Payment Method ID) sebagai kode unik, serta nama metode pembayaran yang sesuai dengan setiap ID.

| Attribute          | Type                  | Description                     |
|:-------------------|:----------------------|:--------------------------------|
| pmid               | varchar               | Id pay method                   |
| method_name        | varchar		           | nama metode pembayaran	         |

dengan syntax SQL sebagai berikut :

```sql
CREATE TABLE IF NOT EXISTS data_payment_method (
      PMID VARCHAR(10) PRIMARY KEY,
      Method_name VARCHAR(50)
    );
```
### Create Table Product
Tabel produk berfungsi sebagai sumber informasi utama bagi pengguna untuk mengetahui detail berbagai produk yang tersedia di pasar Dekirume. Melalui tabel ini, pengguna dapat mengakses data penting, termasuk ID produk sebagai identitas unik, nama produk, deskripsi yang menjelaskan karakteristiknya, kategori produk untuk klasifikasi yang lebih terstruktur, jumlah stok yang mencerminkan ketersediaan barang, serta harga yang menjadi acuan dalam transaksi.

| Attribute                  | Type                  | Description                     		       |
|:---------------------------|:----------------------|:------------------------------------------|
| productid                  | varchar               | Id Produk                       		       |
| product_name               | varchar		           | Nama Produk                   		         |
| product_description        | text		               | Deskripsi Produk                      	   |	
| product_category           | varchar		           | Kategori Produk                 		       |
| stock	                     | integer		           | Jumlah Stok dari Setiap Produk	           |
| price		    	             | decimal(10,2)         | Harga dari Masing-Masing Produk           |

dengan syntax SQL sebagai berikut :

```sql
CREATE TABLE IF NOT EXISTS data_product (
      ProductID VARCHAR(20) PRIMARY KEY,
      Product_name VARCHAR(100),
      Product_Description TEXT,
      Product_Category VARCHAR(50),
      Stock INT,
      Price DECIMAL(10,2)
    );
```
### Create Table Transaction
Tabel transaksi berfungsi sebagai wadah penyimpanan data yang mencatat seluruh aktivitas transaksi yang terjadi. Melalui tabel ini, pengguna dapat mengakses berbagai informasi penting terkait transaksi, termasuk ID transaksi sebagai identitas unik, tanggal transaksi untuk pencatatan waktu, serta total harga yang mencerminkan nilai keseluruhan dari setiap transaksi. Selain itu, tabel ini juga mencakup jumlah produk yang dibeli, ID pelanggan untuk mengidentifikasi pembeli, ID produk yang menunjukkan barang yang dibeli, ID metode pembayaran untuk mencatat cara pembayaran yang digunakan, serta ID voucher beserta status penggunaannya.

| Attribute                  | Type                  | Description                       		       |
|:---------------------------|:----------------------|:--------------------------------------------|
| transactionid              | integer               | Id Transaksi                       	       |
| transaction_date           | date		               | Tanggal Transaksi                  	       |
| total_price                | decimal	      	     | Total Harga dari Tiap Transaksi             |	
| quantity                   | integer		           | Jumlah Produk	                	           |
| customerid                 | integer               | Id Customer                                 |
| productid    	      	     | varchar               | Id Produk	                                 |
| pmid	                     | varchar               | Id Pay Method     			                     |
| voucherid		               | varchar               | Id Voucher				                           |
| voucher_status             | varchar		           | Status Voucher                     	       |

dengan syntax SQL sebagai berikut :

```sql
CREATE TABLE IF NOT EXISTS data_transaction (
      TransactionID INT PRIMARY KEY,
      Transaction_Date DATE,
      Price DECIMAL(10,2),
      Total_Price DECIMAL(10,2),
      Discount_Price DECIMAL(10,2),
      Quantity INT,
      CustomerID INT,
      ProductID VARCHAR(20),
      PMID VARCHAR(10),
      VoucherID VARCHAR(10) NULL,
      Voucher_status VARCHAR(20),
      Discount DECIMAL(5,2),
      FOREIGN KEY (CustomerID) REFERENCES data_customer(CustomerID) ON DELETE CASCADE ON UPDATE CASCADE,
      FOREIGN KEY (ProductID) REFERENCES data_product(ProductID) ON DELETE CASCADE ON UPDATE CASCADE,
      FOREIGN KEY (VoucherID) REFERENCES data_voucher(VoucherID) ON DELETE CASCADE ON UPDATE CASCADE,
      FOREIGN KEY (PMID) REFERENCES data_payment_method(PMID) ON DELETE CASCADE ON UPDATE CASCADE
    );
```

---

## 📂 Struktur Folder

📁 **Struktur direktori proyek**:

```
.
├── Data                                   # Data proyek
│   └── csv
├── Images
├── app                                    # Aplikasi Shiny
│   ├── ProjectMDS_FrontBackEnd.qmd
│   ├── ProjectMDS_FrontBackEnd_DELA.qmd
│   ├── Server.qmd
│   └── UI.qmd
├── conn
│   └── DBManager.qmd
├── .gitignore
├── PraktikumMDS.Rproj
└── README.md
```

---

## ❤️ Tim Kami
### Frontend & Backend Developer: [M0501241024][Dela Gustiara](https://github.com/delagustiara24)
![Dela Gustiara](Images/dela.jpg)

### Database Manager: [M0501241071][Rupmana Br Butar Butar](https://github.com/Rupmana03)
![Rupmana Br Butar Butar](Images/rupmana.jpg)

### Copy Writer: [M0501241061][Rizqi Annafi Muhadi](https://github.com/rizqiannafii)
![Rizqi Annafi Muhadi](Images/rizqi.jpg)

### Database Designer: [M0501241047][Mega Maulina](https://github.com/megaamln)
![Mega Maulina](Images/mega.jpg)

---

📢 **Terima kasih telah membaca dokumentasi ini!** Jika ada pertanyaan atau saran, jangan ragu untuk menghubungi tim kami. Selamat berbelanja dengan Dekirume! 🚀
