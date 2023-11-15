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

# Perbedaan Antara `Navigator.push()` dan `Navigator.pushReplacement()` dan Contoh Penggunaanya
`Navigator.push()` dan `Navigator.pushReplacement()` adalah dua metode yang digunakan untuk menavigasi antara layar (atau rute) yang berbeda dalam aplikasi Flutter. Perbedaan utama antara keduanya adalah:

- `Navigator.push()` menambahkan rute baru ke tumpukan rute yang dikelola oleh widget Navigator. Ini berarti bahwa rute sebelumnya masih ada di bawah rute baru, dan kita dapat kembali ke rute sebelumnya dengan menggunakan `Navigator.pop().`
- `Navigator.pushReplacement()` menggantikan rute saat ini dengan rute baru di tumpukan rute. Ini berarti bahwa rute sebelumnya dihapus dari tumpukan rute, dan kita tidak dapat kembali ke rute sebelumnya dengan menggunakan `Navigator.pop()`.

Contoh penggunaan `Navigator.push()` adalah ketika kita ingin menampilkan detail dari suatu item di layar baru, dan kemudian kembali ke layar sebelumnya dengan menekan tombol kembali. Contoh penggunaan `Navigator.pushReplacement()` adalah ketika kita ingin mengarahkan pengguna ke layar utama setelah proses _login_ atau _logout_, dan kemudian mencegah pengguna untuk kembali ke layar _login_ atau _logout_ dengan menekan tombol kembali.

Berikut adalah contoh kode yang menunjukkan perbedaan antara `Navigator.push()` dan `Navigator.pushReplacement()`:
```// Layar pertama
class FirstScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Layar Pertama'),
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
            Text('Ini adalah layar pertama'),
            ElevatedButton(
              child: Text('Pindah ke layar kedua dengan push'),
              onPressed: () {
                // Pindah ke layar kedua dengan push
                Navigator.push(
                  context,
                  MaterialPageRoute(builder: (context) => SecondScreen()),
                );
              },
            ),
            ElevatedButton(
              child: Text('Pindah ke layar kedua dengan pushReplacement'),
              onPressed: () {
                // Pindah ke layar kedua dengan pushReplacement
                Navigator.pushReplacement(
                  context,
                  MaterialPageRoute(builder: (context) => SecondScreen()),
                );
              },
            ),
          ],
        ),
      ),
    );
  }
}

// Layar kedua
class SecondScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Layar Kedua'),
      ),
      body: Center(
        child: Text('Ini adalah layar kedua'),
      ),
    );
  }
}`
```

# Penjelasan _Layout_ Widget Pada Flutter dan Konteks Penggunaannya
Layout widget pada Flutter adalah widget yang digunakan untuk mengatur posisi, ukuran, dan tata letak dari widget lainnya. Ada beberapa jenis layout widget pada Flutter, antara lain:
- **Row** adalah widget yang menyusun widget anaknya secara horizontal, dari kiri ke kanan. Row dapat digunakan untuk membuat layout seperti menu, toolbar, atau status bar.
- **Column** adalah widget yang menyusun widget anaknya secara vertikal, dari atas ke bawah. Column dapat digunakan untuk membuat layout seperti daftar, form, atau card.
- **Wrap** adalah widget yang menyusun widget anaknya secara horizontal atau vertikal, tetapi dapat mengganti arah jika tidak ada ruang yang cukup. Wrap dapat digunakan untuk membuat layout yang responsif, seperti tag, chip, atau galeri.
- **Stack** adalah widget yang menyusun widget anaknya secara tumpang tindih, dengan widget pertama di bawah dan widget terakhir di atas. Stack dapat digunakan untuk membuat layout yang kompleks, seperti overlay, dialog, atau animasi.
- **Center** adalah widget yang menempatkan widget anaknya di tengah-tengah dari widget induknya. Center dapat digunakan untuk membuat layout yang sederhana, seperti judul, logo, atau ikon.
- **Align** adalah widget yang menempatkan widget anaknya di posisi tertentu dari widget induknya, berdasarkan alignment dan factor. Align dapat digunakan untuk membuat layout yang fleksibel, seperti banner, badge, atau watermark.
- **Padding** adalah widget yang memberikan jarak antara widget anaknya dengan tepi dari widget induknya. Padding dapat digunakan untuk membuat layout yang nyaman, seperti margin, border, atau spacing.
- **SizedBox** adalah widget yang memiliki ukuran tetap, baik lebar maupun tinggi. SizedBox dapat digunakan untuk membuat layout yang konsisten, seperti grid, button, atau separator.
- **Expanded** adalah widget yang memperluas widget anaknya untuk mengisi ruang kosong yang tersedia di dalam Row, Column, atau Flex. Expanded dapat digunakan untuk membuat layout yang dinamis, seperti progress bar, slider, atau rating.

# Elemen Input yang Digunakan Pada Tugas Ini dan Alasan Menggunakannya
Pada tugas ini saya menggunakan elemen input yang terdiri dari:
1. Nama untuk nama produk yang dijual
2. Harga untuk harga produk yang dijual
3. Deskripsi untuk menjelaskan detail produk yang dijual tersebut
4. Jenis untuk mengkategorikan produk-produk yang dijual
5. Jumlah untuk menjelaskan stok produk yang dijual

# Penerapan _Clean Architecture_ Pada Aplikasi Flutter
Penerapan _clean architecture_ pada aplikasi Flutter adalah suatu cara untuk menyusun kode yang bersih dan terstruktur, dengan memisahkan lapisan presentasi, lapisan domain, dan lapisan data. _Clean architecture_ dapat memberikan beberapa keuntungan, seperti fleksibilitas, keterawatan, dan skalabilitas, tetapi juga memiliki beberapa tantangan, seperti kompleksitas awal, over-engineering, dan kurva belajar.

Untuk menerapkan clean architecture pada aplikasi Flutter, berikut adalah langkah-langkahnya:
1. Buat proyek Firebase di Google Firebase console.
2. Buat aplikasi Flutter baru dan atur folder dan file yang dibutuhkan.
3. Implementasikan lapisan domain, yang berisi model data dan use case.
4. Sambungkan Firebase Firestore ke aplikasi Anda sebagai database.
5. Implementasikan lapisan data, yang berisi repository dan data source.
6. Implementasikan lapisan presentasi, yang berisi widget, state, dan bloc.
7. Tambahkan fitur CRUD untuk item toko

# Cara Saya Mengimplementasikan _Checklist_ Tugas ini
### Tahap menambahkan Drawer Menu untuk Navigasi Halaman
1. Membuat direktori baru bernama `widgets` di `tropische/lib` dan mengisinya dengan file `left_drawer.dart`.
2. Mengisi file `left_drawer.dart` dengan Widget build yang di dalamnya ada _drawer header_, _routing_. Selain itu, mengimport `flutter/material.dart`, `tropische/menu.dart`, dan `tropische/screens/shoplist_form.dart`.

### Tahap menambahkan Form dan Elemen Input
1. Membuat file baru, yaitu `shoplist_form.dart` dan mengimport drawer yang telah dibuat sebelumnya, dengan cara `import 'package:tropische/widgets/left_drawer.dart'`
2. Menambahkan `class ShopFormPage extends StatefulWidget` dan `class _ShopFormPageState extends State<ShopFormPage>`
3. Mengubah widget Placeholder dan menambahkan drawer, seperti berikut: 
```Scaffold(
  appBar: AppBar(
    title: const Center(
      child: Text(
        'Form Tambah Produk',
      ),
    ),
    backgroundColor: Colors.indigo,
    foregroundColor: Colors.white,
  ),
  // [kode drawer disini] 
  body: Form(
    child: SingleChildScrollView(),
  ),
);
```
4. Membuat handler dari form state, validasi form, dan penyimpanan form dengan membuat variabel baru `_formKey` dan menambahkannya ke atribut `key` milik widget `Form`.
5. Mengisi widget `Form` dengan _field_, antara lain ada nama, harga, deskripsi, jenis, dan jumlah pada tugas ini.
6. Setelah membuat _field_ tersebut, buat widget `Column` sebagai child dari `SingleChildScrollView`.
7. Selanjutnya, membuat widget `TextFormField` yang dibungkus Padding sebagai salah satu widget `Column` untuk _field_ nama, harga, dan deskripsi.
8. Membuat tombol sebagai child selanjutnya dari `Column`. Tombol ini dibungkus oleh widget `Padding` dan `Align`. Pop-up akan muncul jika tombol ditekan. Pesan yang muncul pada pop-up adalah bentuk konfirmasi dari input yang telah dimasukkan.

### Memunculkan Data
1. Menambahkan fungsi `showDialog()` pada bagian `onPressed()` dan memunculkan widet `AlertDialog` pada fungsi tersebut, serta fungsi _reset_ form.

### Menambahkan Fitur Navigasi pada Tombol
1. Pada menu.dart, di widget `ShopItem` dimodifikasi agar dapat melakukan navigasi ke _route_ lain. Disinilah `Navigator.push()` dan `Navigator.pop()` digunakan.

### Refactoring File
1. Membuat `shoplist_form.dart` dan memasukkannya ke direktori `screens` yang baru dibuat pada `tropische/lib`. Pindahkan juga `menu.dart` ke direktori ini.
2. Membuat file `shop_card.dart` pada direktori `widgets`.
3. Menyesuaikan path import file-file yang dipindahkan ini pada file lain yang menggunakannya.

**End of Tugas 2**

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

# Cara Saya Mengimplementasikan _Checklist_ Tugas Secara
1. Membuat proyek flutter dengan mengetikan `flutter create tropische` kemudian menjalankannya melalui Chrome.
2. Membuat file baru bernama `menu.dart` pada direktori tropische/lib. Mengisi file ini dengan mengimport package material.dart dari Flutter.
3. Memindahkan `class MyHomePage` dan `_MyHomePageState` dari main.dart ke menu.dart. Tidak lupa juga untuk mengimport tropische/menu.dart ke main.dart untuk mengatasi error karena ketidakberadaan class MyHomePage.

### Memulai membuat widget sederhana.
1. Mengubah warna menjadi indigo dengan cara mengetikkan `colorScheme: ColorScheme.fromSeed(seedColor: Colors.indigo),` pada main.dart. Ini menjadikan halaman bersifat stateless.
2. Mengubah `MyHomePage(title: 'Flutter Demo Home Page')` menjadi `MyHomePage()` pada main.dart.
3. Mengubah sifat widget halaman daru stateful menjadi stateless melalui file menu.dart. dengan cara mengubah bagian class MyHomePage menjadi:
```class MyHomePage extends StatelessWidget {
    MyHomePage({Key? key}) : super(key: key);

    @override
    Widget build(BuildContext context) {
        return Scaffold(
            ...
        );
    }
}
```
4. Setelah mengubah halaman menjadi stateless, selanjutnya menambahkan teks dan card untuk display barang yang dijual. Tambahan kodenya sebagai berikut:
```class ShopItem {
  final String name;
  final IconData icon;

  ShopItem(this.name, this.icon);
}
```
Dibawah `MyHomePage({Key? key}) : super(key: key);` menambahkan kode:
```final List<ShopItem> items = [
    ShopItem("Lihat Produk", Icons.checklist),
    ShopItem("Tambah Produk", Icons.add_shopping_cart),
    ShopItem("Logout", Icons.logout),
];
```
Selanjutnya, menambahkan widget-widget lain di dalam Widget build.
5. Mengextend `class ShopCard` dengan `StatelessWidget`.
