# Tugas Besar Algoritma dan Pemrograman dengan topik Sistem Toko Top Up Mobile Legends (JeMLBBStore.id)

## Deskripsi Program

JeMLBBStore.id merupakan program simulasi toko top up Diamond Mobile Legends berbasis CLI (Command Line Interface). Program ini dirancang untuk membantu pengguna melakukan simulasi pembelian Diamond, melihat daftar transaksi, menambahkan pesanan, serta menghapus pesanan yang telah dibuat.

Program ini menerapkan beberapa konsep dasar algoritma dan pemrograman, seperti **CRUD (Create, Read, Update, Delete)**, struktur data List dan Dictionary, percabangan, perulangan, validasi input, serta operasi aritmatika.

## Algoritma dan Konsep yang Digunakan

### 1. Algoritma CRUD (Create, Read, Update, Delete)

Program menggunakan konsep CRUD sebagai dasar pengelolaan data transaksi pembelian Diamond.

- **Create:** Digunakan untuk membuat transaksi baru dengan memilih nominal Diamond yang tersedia. Data pembelian disimpan ke dalam daftar transaksi, meliputi jenis item, jumlah Diamond, harga awal, pajak, dan total pembayaran.
- **Read:** Digunakan untuk menampilkan seluruh data transaksi atau mencari transaksi tertentu berdasarkan kata kunci yang dimasukkan pengguna.
- **Update:** Digunakan untuk menambahkan pembelian baru ke dalam daftar transaksi yang sudah ada.
- **Delete:** Digunakan untuk menghapus transaksi tertentu berdasarkan nomor urut item yang dipilih pengguna.

### 2. Struktur Data List dan Dictionary

Program memanfaatkan dua jenis struktur data utama:

- **List:** Digunakan sebagai tempat penyimpanan seluruh transaksi pembelian selama program berjalan. Struktur ini memungkinkan data ditambahkan maupun dihapus secara dinamis.
- **Dictionary:** Digunakan untuk menyimpan detail setiap transaksi dalam bentuk pasangan key-value. Informasi yang disimpan meliputi jenis item, jumlah Diamond, harga, pajak, dan total pembayaran.

Kombinasi keduanya memudahkan pengelolaan transaksi karena setiap pembelian dapat memiliki beberapa atribut yang saling berkaitan.

### 3. Algoritma Pencarian Data (Linear Search)

Pada fitur pencarian transaksi, program menggunakan algoritma **Linear Search** atau pencarian berurutan.

Algoritma ini bekerja dengan memeriksa setiap elemen dalam daftar transaksi satu per satu, kemudian mencocokkan kata kunci yang dimasukkan pengguna dengan jenis item yang tersimpan.

Pencarian dilakukan tanpa membedakan huruf besar dan kecil (*case-insensitive*), sehingga pengguna dapat mencari data dengan lebih fleksibel.

Jika ditemukan kecocokan, program akan menampilkan informasi transaksi tersebut. Sebaliknya, jika tidak ditemukan, program memberikan informasi bahwa item yang dicari tidak tersedia.

### 4. Algoritma Penghapusan Data

Penghapusan transaksi dilakukan dengan memanfaatkan posisi atau indeks elemen pada List.

Program menampilkan seluruh transaksi beserta nomor urutnya. Pengguna kemudian memasukkan nomor transaksi yang ingin dihapus.

Setelah nomor tersebut divalidasi, program menghapus elemen yang berada pada indeks terkait. Dengan demikian, data transaksi yang tidak lagi diperlukan dapat dihilangkan dari daftar.

### 5. Validasi Input (Input Validation)

Program menerapkan validasi input untuk memastikan data yang dimasukkan pengguna sesuai dengan ketentuan sistem.

Beberapa bentuk validasi yang digunakan meliputi:

- **Validasi tipe data:** Memastikan input yang membutuhkan angka dapat dikonversi menjadi integer.
- **Validasi rentang nilai:** Memastikan pilihan nominal Diamond dan menu berada dalam rentang yang tersedia.
- **Validasi panjang karakter:** Memastikan ID Mobile Legends terdiri dari 8–9 digit dan server terdiri dari 4–5 digit.
- **Validasi karakter:** Memastikan ID dan server hanya berisi angka.
- **Validasi pilihan menu:** Memastikan pengguna hanya memasukkan opsi yang telah disediakan.
- **Penanganan kesalahan:** Menggunakan mekanisme exception handling untuk menangani kesalahan input, khususnya ketika pengguna memasukkan nilai yang tidak dapat dikonversi menjadi integer.

Validasi ini bertujuan mengurangi kesalahan input dan menjaga agar alur program tetap berjalan sesuai aturan.

### 6. Algoritma Perhitungan Harga dan Pajak

Perhitungan transaksi menggunakan operasi aritmatika dasar.

Setiap nominal Diamond memiliki harga yang telah ditentukan. Setelah pengguna memilih nominal pembelian, sistem menghitung pajak sebesar 10% dari harga awal.

Rumus perhitungan yang digunakan:

**Perhitungan Pajak:**

Pajak = Harga Diamond × 10%

**Perhitungan Total Pembayaran:**

Total Pembayaran = Harga Diamond + Pajak

Hasil perhitungan tersebut kemudian disimpan sebagai bagian dari data transaksi sehingga dapat ditampilkan kembali ketika pengguna melihat daftar pesanan.

### 7. Algoritma Penjumlahan Data (Summation)

Program menggunakan konsep penjumlahan atau *summation* untuk menghitung keseluruhan jumlah Diamond dan total pembayaran dari transaksi yang tersimpan.

Terdapat dua komponen perhitungan:

- **Total Diamond:** Menjumlahkan seluruh nominal Diamond dari transaksi yang memiliki jenis item Diamond.
- **Total Harga:** Menjumlahkan seluruh total pembayaran transaksi Diamond, termasuk pajak.

Perhitungan dilakukan dengan mengambil nilai dari setiap transaksi yang memenuhi kondisi tertentu, kemudian menjumlahkannya menggunakan operasi agregasi.

### 8. Perulangan dan Percabangan

Program menggunakan perulangan dan percabangan untuk mengatur alur interaksi dengan pengguna.

- **Perulangan (Looping):** Digunakan untuk mengulang tampilan menu, meminta input kembali ketika terjadi kesalahan, serta memberikan kesempatan kepada pengguna untuk melakukan beberapa transaksi.
- **Percabangan (Conditional):** Digunakan untuk menentukan tindakan berdasarkan pilihan pengguna, seperti melakukan pembelian, melihat transaksi, menambahkan pesanan, menghapus pesanan, atau keluar dari program.

Kedua konsep ini memungkinkan program berjalan secara interaktif dan menyesuaikan proses berdasarkan keputusan pengguna.

## Fungsi-Fungsi Utama

| Fungsi | Kegunaan |
|---|---|
| `profile()` | Memvalidasi dan menerima ID serta server Mobile Legends. |
| `list_harga_diamond()` | Menyediakan daftar nominal Diamond beserta harga masing-masing. |
| `create()` | Membuat transaksi pembelian Diamond dan menghitung pajak serta total pembayaran. |
| `read()` | Menampilkan seluruh transaksi atau mencari transaksi berdasarkan kata kunci. |
| `update()` | Menambahkan transaksi pembelian baru ke daftar transaksi. |
| `delete()` | Menghapus transaksi berdasarkan nomor urut yang dipilih. |
| `perhitungan()` | Menghitung total Diamond dan keseluruhan pembayaran dari transaksi yang tersimpan. |
| `tampilan()` | Menampilkan menu utama dan mengatur navigasi antarfitur program. |

## Alur Kerja Program

1. Program menampilkan halaman utama JeMLBBStore.id.
2. Pengguna memilih salah satu menu yang tersedia.
3. Jika memilih pembelian Diamond, pengguna diminta memasukkan ID dan server Mobile Legends.
4. Setelah data profil divalidasi, pengguna memilih nominal Diamond yang ingin dibeli.
5. Sistem mengambil harga berdasarkan nominal yang dipilih, kemudian menghitung pajak 10% dan total pembayaran.
6. Data transaksi disimpan ke dalam List dalam bentuk Dictionary.
7. Pengguna dapat melihat seluruh transaksi, mencari transaksi tertentu, menambahkan pembelian, atau menghapus transaksi.
8. Program berakhir ketika pengguna memilih menu keluar atau proses transaksi dihentikan.

## Konsep Pemrograman yang Diterapkan

Secara keseluruhan, program ini menerapkan beberapa konsep dasar pemrograman:

- **Modular Programming:** Membagi program menjadi beberapa fungsi berdasarkan tanggung jawab masing-masing agar pengelolaan program lebih terstruktur.
- **CRUD:** Mengelola data transaksi melalui proses penambahan, pembacaan, pembaruan, dan penghapusan.
- **Linear Search:** Melakukan pencarian data transaksi secara berurutan.
- **List dan Dictionary:** Mengelola serta menyimpan data transaksi.
- **Conditional Statement:** Mengatur pengambilan keputusan berdasarkan kondisi dan pilihan pengguna.
- **Looping:** Mengatur pengulangan proses dan interaksi pengguna.
- **Exception Handling:** Menangani kesalahan input agar program tidak langsung berhenti akibat kesalahan konversi tipe data.
- **Arithmetic Operations:** Melakukan perhitungan harga, pajak, dan total pembayaran.

## Tujuan Pembuatan

Program ini dibuat sebagai penerapan konsep dasar Algoritma dan Pemrograman menggunakan Python. Melalui simulasi sistem toko top up Diamond Mobile Legends, program ini mengimplementasikan pengelolaan data transaksi, algoritma pencarian, operasi perhitungan, validasi input, serta penggunaan fungsi untuk membangun sebuah sistem sederhana yang interaktif.
