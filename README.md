<!-- # tropische

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference. -->

Nama  : Indira Arifia Rahmah
NPM   : 2206811846
Kelas : PBP B

# Perbedaan Utama Antara Stateless dan Stateful Widget dalam Konteks Pengembangan Aplikasi Flutter
- _Stateless widget_ adalah _widget_ yang tidak memiliki keadaan (_state_) yang dapat berubah, sedangkan _stateful widget_ adalah _widget_ yang memiliki keadaan (_state_) yang dapat berubah. Keadaan (_state_) adalah kumpulan nilai atau informasi yang menentukan tampilan dan perilaku _widget_.
- _Stateless widget_ hanya memiliki satu objek yang mewakili _widget_ tersebut, sedangkan _stateful widget_ memiliki dua objek, yaitu objek _stateful widget_ itu sendiri dan objek _state_ yang mengelola keadaan _widget_ tersebut. Objek _stateful widget_ bersifat tetap dan tidak berubah, sedangkan objek _state_ bersifat dinamis dan dapat berubah.
- _Stateless widget_ hanya memanggil metode _build_ sekali ketika widget tersebut dibuat, sedangkan _stateful widget_ dapat memanggil metode _build_ ulang kapan saja ketika terjadi perubahan keadaan. Metode _build_ adalah fungsi yang mengembalikan _widget_ yang akan ditampilkan di layar.
- _Stateless widget_ cocok digunakan untuk _widget_ yang sifatnya statis atau tidak memerlukan perubahan, seperti teks, ikon, tombol, dan sebagainya. _Stateful widget_ cocok digunakan untuk _widget_ yang sifatnya dinamis atau memerlukan perubahan, seperti formulir, animasi, jam, dan sebagainya.

# Berbagai Widget yang Saya Gunakan dalam Tugas Ini dan Fungsinya
1. *MyApp*: Ini adalah widget utama yang mewakili aplikasi ini. Ini adalah titik awal aplikasi dan mengatur tema dan halaman utama.
2. *MaterialApp*: widget yang menginisialisasi aplikasi dengan tema dan konfigurasi tertentu. Melalui widget ini dapat diatur berbagai atribut seperti judul, tema, dan halaman beranda.
3. *MyHomePage*: widget yang mewakili halaman beranda aplikasi. Ini adalah turunan dari `StatelessWidget` dan berisi widget-widget lainnya.
4. *Scaffold*: widget yang menyediakan kerangka kerja dasar untuk tampilan aplikasi, termasuk `AppBar` dan body. Bisa juga berisi drawer, bottom navigation, dan lain-lain.
5. *AppBar*: elemen atas halaman yang menampilkan judul aplikasi dan dapat mengkonfigurasi tampilan dan warna AppBar.
6. *SingleChildScrollView*: widget wrapper yang memungkinkan kontennya dapat discroll. Ini digunakan untuk mengatasi masalah overflow saat kontennya besar.
7. *Padding*: digunakan untuk memberikan jarak antara elemen-elemen dalam widgetnya.
8. *Column*: widget yang digunakan untuk menampilkan children secara vertikal. Ini adalah salah satu dari beberapa jenis layout widgets yang digunakan dalam program ini.
9. *Text*: untuk menampilkan teks pada layar. Di sini, digunakan untuk menampilkan judul toko.
10. *GridView.count*: widget yang digunakan untuk membuat tampilan grid dengan jumlah kolom yang sudah ditentukan. Ini mengatur tata letak grid untuk item-item dalam daftar items.
11. *ShopItem*: kelas yang merepresentasikan item dalam daftar menu. Setiap item memiliki nama dan ikon (IconData).
12. *ShopCard*: widget yang mewakili kartu individual dalam grid. Menerima ShopItem sebagai argumen dan menampilkan ikon dan teks. Ketika diklik, muncul SnackBar untuk memberi tahu pengguna tindakan yang dilakukan.

# Cara Saya Mengimplementasikan _Checklist_ Tugas Secara _Step-By-Step_

