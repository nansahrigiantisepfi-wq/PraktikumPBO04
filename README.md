# Program Sistem Kasir Sederhana (PBO)

Repository ini berisi implementasi program **Sistem Kasir Sederhana** dalam bahasa pemrograman Java yang menerapkan konsep dasar **Pemrograman Berbasis Objek (Object-Oriented Programming / OOP)**.

---

## 📄 Struktur Kelas (Classes)

Program ini terdiri dari 2 kelas utama:

### 1. `Produk.java`
Kelas ini berfungsi sebagai *model data* untuk merepresentasikan produk/barang yang dijual.
- **Atribut/Variabel**:
  - `kodeProduk` (`String`): Menyimpan kode unik barang.
  - `namaProduk` (`String`): Menyimpan nama barang.
  - `harga` (`double`): Menyimpan harga satuan barang.
  - `stok` (`int`): Menyimpan jumlah stok barang yang tersedia.
  - `PAJAK` (`static final double`): Konstanta nilai pajak (misalnya 11% / `0.11`).
- **Method/Fungsi**:
  - **Constructor**: Menerima parameter untuk menginisialisasi atribut produk saat objek dibuat.
  - **Menghitung Subtotal & Pajak**: Menghitung total harga barang berdasarkan jumlah pembelian beserta nominal pajaknya.

### 2. `SistemKasir.java`
Kelas ini bertindak sebagai *sistem utama* yang mengelola alur transaksi pembelian barang.
- **Fungsi Utama**:
  - Mengelola daftar barang yang dibeli oleh pelanggan.
  - Menerima masukan (*input*) jumlah barang dari kasir/pengguna.
  - Menghitung total belanja, potongan harga/diskon (jika ada), pajak, dan total pembayaran akhir.
  - Menghitung uang kembalian berdasarkan pembayaran dari pelanggan.
  - Mencetak struk/nota transaksi penjualan.

---

## 🔄 Sistem Kerja Program

1. **Inisialisasi Produk**:
   - Sistem membuat objek `Produk` dengan menentukan `kodeProduk`, `namaProduk`, `harga`, dan jumlah `stok`.

2. **Input Transaksi**:
   - Kasir/pengguna memilih produk dan memasukkan jumlah (*quantity*) item yang dibeli oleh pelanggan.

3. **Kalkulasi & Perhitungan**:
   - Program menghitung total belanja dasar (`harga × jumlah`).
   - Program menambahkan nilai pajak berdasarkan konstanta `PAJAK` yang diset pada `Produk`.
   - Program menghitung total akhir yang harus dibayar.

4. **Pembayaran & Kembalian**:
   - Pelanggan memasukkan jumlah uang pembayaran.
   - Program memverifikasi apakah uang mencukupi, lalu menghitung nominal kembalian.

5. **Output Struk Transaksi**:
   - Sistem menampilkan rincian akhir transaksi (Nama Barang, Jumlah, Harga Satuan, Pajak, Total Bayar, Uang Pembayaran, dan Kembalian) pada konsol.

---

## 🛠️ Cara Menjalankan Program

1. Pastikan komputer Anda telah terinstal **Java Development Kit (JDK)**.
2. Download atau *clone* repository ini:
   ```bash
   git clone [https://github.com/nansahrigiantisepfi-wq/Praktikum-PBO.git](https://github.com/nansahrigiantisepfi-wq/Praktikum-PBO.git)
