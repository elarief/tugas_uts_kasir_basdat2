Sistem Kasir Sederhana (Implementasi Stored Procedure & Trigger) 🛒

Aplikasi kasir berbasis web sederhana yang dikembangkan menggunakan PHP dan MySQL. Proyek ini dibuat sebagai pemenuhan tugas Ujian Tengah Semester (UTS) mata kuliah Basis Data 2 di Universitas Darussalam (UNIDA).

Fokus utama dari proyek ini bukanlah pada tampilan antarmuka (UI), melainkan pada Business Logic di sisi Database 
Management System (DBMS) menggunakan fitur Stored Procedure dan Trigger untuk menjaga integritas data dan keamanan transaksi.

🚀 Fitur Utama

- **Antarmuka Web Sederhana**: Form input untuk ID Barang dan Jumlah Beli menggunakan HTML dan PHP murni.
- **Stored Procedure (sp_CheckoutBarang)**: Logika utama transaksi dibungkus dalam satu prosedur di MySQL untuk mengecek stok, menghitung subtotal, dan menyimpan record ke tabel Transaksi dan Detail_Transaksi.
- **Trigger Otomatis (trg_UpdateStok)**: Trigger dengan event AFTER INSERT yang akan secara otomatis mengurangi stok pada tabel Barang setiap kali ada record transaksi baru.

🛠️ Prasyarat (Prerequisites)

Pastikan perangkat lunak berikut sudah terinstal di komputermu:

- XAMPP (Untuk menjalankan server Apache dan MySQL)
- Web Browser (Chrome, Edge, Firefox, dll)

⚙️ Panduan Instalasi (Setup)

Ikuti langkah-langkah berikut untuk menjalankan proyek ini di komputer lokal (localhost):

- **Clone/Download Repositori**
  Unduh repositori ini dan letakkan foldernya (misalnya beri nama kasir_uts) di dalam direktori htdocs XAMPP:** C:\xampp\htdocs\kasir_uts**

- **Jalankan XAMPP**
  Buka aplikasi XAMPP Control Panel, lalu klik Start pada modul Apache dan MySQL.

- **Konfigurasi Database**
  1. Buka browser dan akses http://localhost/phpmyadmin
  2. Buat database baru dengan nama db_penjualan_uts
  3. Buka menu/tab SQL, lalu jalankan script tabel, data dummy, trigger, dan stored procedure 

- **Jalankan Aplikasi**
  Buka browser dan ketik alamat berikut di URL bar: **http://localhost/kasir_uts**


📝 Penggunaan (Cara Kerja)

1. Pada halaman utama aplikasi, masukkan ID Barang (contoh: 1 untuk Keyboard Mekanikal).
2. Masukkan Jumlah Beli yang diinginkan.
3. Klik tombol Proses Checkout.
4. Jika stok mencukupi, transaksi akan berhasil, dan stok di database akan otomatis berkurang. Jika tidak mencukupi, aplikasi akan menampilkan pesan error.

