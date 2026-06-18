ERD Cafe: menunjukkan entitas seperti User, Admin, Ordering Area, Seating Area, dan Decor & Ambience, lengkap dengan atribut dan relasi antar entitas (misalnya relasi “memesan”, “mengelola”, dan “memiliki”).

DFD Level 0 (Context Diagram): menggambarkan aliran data antara Pengguna, Admin, dan System Cafe — termasuk proses pemesanan, penggunaan fasilitas, serta pembayaran digital.

Struktur ini cocok untuk dokumentasi proyek atau tugas analisis sistem informasi.
Kalau kamu mau, aku bisa bantu lanjutkan ke DFD Level 1 agar alur prosesnya lebih detail (misalnya pemesanan, pembayaran, dan feedback pelanggan). Mau aku buatkan juga?

DFD Level 0 (Context Diagram) menampilkan interaksi utama antara Pengguna (Mahasiswa, Karyawan, Pecinta Kopi) dan Admin dengan System Cafe.
Alur data mencakup:
Melakukan pemesanan
Menggunakan fasilitas
Pembayaran digital
Pengelolaan operasional cafe

DFD Level 1 (Detailed Processes) memecah sistem menjadi empat proses utama:
Pemesanan → Input, verifikasi, dan konfirmasi pesanan
Pembayaran → Proses dan validasi transaksi
Penyajian Pesanan → Persiapan dan penyajian minuman
Feedback & Rating → Input ulasan dan pencatatan review

Pemesanan

1.1 Input Pesanan → pelanggan memasukkan detail pesanan.
1.2 Verifikasi Pesanan → sistem memeriksa ketersediaan menu.
1.3 Konfirmasi Order → pesanan dikonfirmasi dan disimpan ke Data Pesanan.

Pembayaran

2.1 Proses Pembayaran → pelanggan memilih metode pembayaran.
2.2 Validasi Pembayaran → sistem memverifikasi transaksi dan menyimpan ke Data Pembayaran.

Penyajian Pesanan

3.1 Persiapan Minuman → barista menyiapkan pesanan berdasarkan data dapur.
3.2 Penyajian ke Pelanggan → pesanan disajikan dan status diperbarui.

Feedback & Rating

4.1 Ulasan Feedback → pelanggan memberikan ulasan setelah pesanan selesai.
4.2 Catat Rating & Review → sistem menyimpan data ke Data Feedback.

Pengguna → Memulai proses dengan memilih menu.
Pemesanan → Mengecek ketersediaan, input pesanan, dan menampilkan notifikasi jika menu tidak tersedia.
Pembayaran → Memilih metode pembayaran, verifikasi transaksi, dan menampilkan status berhasil/gagal.
Penyajian & Feedback → Menyiapkan minuman, mengantarkan pesanan ke meja, lalu pelanggan memberikan ulasan dan rating.

Alur berakhir di titik End, setelah sistem menyimpan Rating & Review.
Diagram ini cocok untuk dokumentasi analisis sistem atau laporan tugas perancangan sistem informasi.

Diagram ini memperlihatkan urutan interaksi antar entitas utama dalam sistem cafe:
User → memulai dengan Pesan Menu dan melakukan pembayaran.
System → memproses pesanan, memverifikasi pembayaran, dan mengelola data pesanan serta feedback.
Barista → menerima instruksi untuk menyiapkan dan mengantarkan pesanan.
Admin → memantau data pesanan dan menampilkan feedback pelanggan.

 Alur utama:
User mengirim Pesan Menu ke System.
System melakukan Cek Ketersediaan dan mengirim hasil ke User.
Jika tersedia, System memproses order dan meminta User melakukan pembayaran.
System memverifikasi pembayaran melalui Admin.
Setelah berhasil, System mengirim instruksi ke Barista untuk menyiapkan dan mengantarkan pesanan.
User memberikan ulasan, System menyimpan Rating & Review, lalu Admin memperbarui data pesanan dan menampilkan feedback.

Diagram ini berguna untuk memahami urutan komunikasi antar komponen dalam sistem cafe — dari pemesanan hingga feedback pelanggan.
Diagram ini menampilkan struktur kelas dan relasi antar objek utama dalam sistem:
Customer → atribut: customer_id, nama, kontak
Order → atribut: order_id, tanggal, total_harga
MenuItem → atribut: item_id, nama_item, harga
Payment → atribut: payment_id, metode, status
Staff → superclass dengan dua subclass:
Barista → atribut: jadwal, shift
Admin → atribut: username, password

Relasi utama:
Customer memesan → Order (1:N)
Order terdiri dari → MenuItem (N:M)
Order diproses oleh → Payment (1:1)
Staff mengelola → Order (1:N)
Staff memiliki subclass Barista dan Admin

Diagram ini membantu memahami struktur logis sistem cafe — bagaimana setiap kelas saling berhubungan untuk mendukung proses pemesanan, pembayaran, dan pengelolaan operasional.
Diagram ini menampilkan hubungan antara aktor utama dan fungsi sistem secara visual:
Di sisi kiri, Customer terhubung ke empat use case: Lihat Menu, Pesan Menu, Lakukan Pembayaran, dan Beri Feedback.
Ada relasi <<include>> dari Pesan Menu ke Lihat Menu.
Ada relasi <<extend>> dari Lakukan Pembayaran ke Verifikasi Pembayaran dan dari Beri Feedback ke Simpan Rating & Review.

Di sisi kanan, Barista terhubung ke Siapkan Pesanan dan Antar Pesanan.
Di bawahnya, Admin terhubung ke Kelola Menu, Kelola Transaksi, dan Lihat Feedback.
Semua use case berada di dalam kotak besar bertuliskan System Cafe, yang menjadi pusat interaksi seluruh aktor.

Diagram ini menggambarkan alur kerja lengkap dari pelanggan hingga pengelola cafe — mulai dari pemesanan hingga evaluasi layanan.
Diagram ini menampilkan instansiasi nyata dari kelas-kelas sistem cafe, menggambarkan bagaimana objek saling berhubungan dalam satu skenario transaksi:
Customer (Rina) → melakukan pemesanan dengan detail kontak dan ID pelanggan.
Order (2105) → berisi tanggal transaksi dan total harga Rp45.000.
MenuItem → terdiri dari dua objek: Latte (Rp25.000) dan Croissant (Rp20.000).
Payment (8801) → metode Gopay, status Berhasil.
Barista → jadwal Shift Pagi, jam kerja 08:00–14:00.
Admin → username admin123, bertugas mengelola data pesanan.
Feedback → rating 5, komentar “Layanan sangat memuaskan!”.

Relasi antar objek:
Customer → Order (pesanan)
Order → MenuItem (item)
Order → Payment (pembayaran)
Order → Feedback (review)
Staff (Barista & Admin) → Order (mengelola)

Diagram ini membantu memahami bagaimana setiap objek berinteraksi dalam sistem nyata — dari pemesanan hingga feedback pelanggan.

