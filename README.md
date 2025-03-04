## **Praktikum Aplikasi Perkantoran: Pengolahan Data Transaksi dengan Microsoft Excel**

Ini adalah salah satu tugas praktikum pada mata kuliah **Aplikasi Perkantoran**, khususnya pada penggunaan **Microsoft Excel**. Dalam tugas ini, terdapat dua tabel utama:  

1. **Tabel Transaksi Penjualan (Utama)** → Berisi detail transaksi, seperti **kode barang, nama barang, harga, jumlah, total belanja, diskon, potongan, dan total bayar**.  
2. **Tabel Barang (Referensi)** → Berisi daftar barang dengan **kode barang, nama barang, dan harga** sebagai referensi data.  

### **Instruksi yang harus dikerjakan:**  
1️⃣ **Bagaimana cara mengambil data harga dari tabel referensi tanpa memasukkan nilainya secara manual?** Gunakan fungsi yang dapat mencari nilai berdasarkan kode barang secara otomatis.  

2️⃣ **Bagaimana cara menghitung total belanja secara dinamis tanpa harus mengalikan harga dan jumlah satu per satu?** Pastikan rumus yang digunakan dapat bekerja untuk semua baris transaksi.  

3️⃣ **Bagaimana menentukan besaran potongan harga berdasarkan diskon yang diberikan dalam bentuk persen?** Temukan cara agar potongan harga otomatis berubah sesuai dengan nilai diskon yang tertera.  

4️⃣ **Bagaimana menghitung total bayar dengan mempertimbangkan potongan harga?** Pastikan hasil akhir menunjukkan jumlah yang harus dibayar setelah diskon diterapkan.  

Tantangan ini menguji pemahaman tentang **fungsi lookup (HLOOKUP/VLOOKUP), operasi aritmatika, serta pemrosesan data transaksi secara otomatis di Excel**.

---
### **Jawaban:**  

**1️⃣ Mengisi Kolom Harga**  
Saya menggunakan fungsi **HLOOKUP** untuk mengambil harga barang dari **Tabel Barang** ke **Tabel Transaksi Penjualan**. Caranya, saya mencocokkan **Kode Barang** di kolom pertama tabel transaksi dengan **Kode Barang** di tabel referensi. Karena harga barang ada di baris kedua tabel referensi, saya menggunakan indeks baris **2** dalam rumus HLOOKUP. Dengan cara ini, setiap kode barang otomatis mendapatkan harga yang sesuai.  

**2️⃣ Menghitung Total Belanja**  
Setelah harga barang terisi, saya menghitung total belanja dengan cara **mengalikan jumlah barang yang dibeli dengan harga satuannya**. Rumusnya cukup sederhana, yaitu:  

                                            Total Belanja = Harga × Jumlah

Dengan cara ini, setiap transaksi langsung memiliki total harga tanpa perlu memasukkan secara manual.  

**3️⃣ Menghitung Potongan Harga**  
Karena setiap barang bisa mendapatkan diskon, saya menghitung potongan harga berdasarkan **persentase diskon yang diberikan**. Saya mengalikan total belanja dengan nilai diskon yang ada di tabel transaksi. Misalnya, jika total belanja Rp10.000 dan diskonnya 5%, maka potongan harganya adalah **5% × 10.000 = 500**.  

**4️⃣ Menghitung Total Bayar**  
Terakhir, untuk mendapatkan jumlah yang harus dibayar oleh pelanggan, saya mengurangi **Total Belanja dengan Potongan Harga**. Jadi rumusnya:  

                                       Total Bayar = Total Belanja − Potongan Harga

Dengan cara ini, setiap pelanggan langsung mendapatkan jumlah yang harus dibayarkan setelah diskon diterapkan.  


Dengan pendekatan ini, saya memastikan bahwa semua perhitungan otomatis dan tidak perlu dilakukan secara manual satu per satu. Hal ini juga **mengurangi risiko kesalahan input dan mempercepat proses pengolahan data transaksi**. 🚀
