# android-helloworld-kotlin

## PRAKTIK

1. Membuat project baru<br/>
<img src="images/project&#32;config.png" width="500" alt="Pengaturan project baru"/><br/>
3. Tampilan awal setelah membuat project baru<br/>
<img src="images/main&#32;activity.png" width="800" alt="Tampilan awal project baru"/><br/>
4. Pada kelas MainActivity seperti berikut<br/>
```kotlin
class MainActivity : AppCompatActivity() {
    // apa saja
}
```
5. Berarti kelas MainActivity adalah turunan dari kelas AppCompatActivity
6. Sedangkan AppCompatActivity sendiri adalah subkelas dari kelas Activity yang mendukung semua fitur Android modern sambil memberikan kompatibilitas dengan versi Android yang lebih lama. Untuk membuat aplikasi kita tersedia untuk sejumlah besar perangkat dan pengguna mungkin, selalu gunakan AppCompatActivity.<br/>
7. Perhatikan metode ```onCreate()```. Activity tidak menggunakan konstruktor untuk menginisialisasi objek. Sebagai gantinya, serangkaian metode yang telah ditentukan (disebut "metode siklus hidup") disebut sebagai bagian dari pengaturan aktivitas. Salah satu metode siklus hidup tersebut adalah ```onCreate()```, yang selalu ditimpa di aplikasi kita sendiri.<br/>
8. Di ```onCreate()```, kita menentukan layout mana yang dikaitkan dengan aktivitas, dan Anda mengembang tata letak. Metode setContentView () melakukan kedua hal itu.<br/>
```kotlin
override fun onCreate(savedInstanceState: Bundle?) {
    super.onCreate(savedInstanceState)
    setContentView(R.layout.activity_main)
}
```
10. Metode ```setContentView()``` mereferensikan layout menggunakan ```R.layout.activity_main```, yang sebenarnya merupakan referensi integer. Kelas R dihasilkan ketika kita membangun aplikasi kita. Kelas R mencakup semua aset aplikasi, termasuk konten direktori res.<br/>
11. ```R.layout.activity_main``` merujuk ke kelas R yang dihasilkan, folder layout, dan file layout ```activity_main.xml```. (Sumber daya tidak termasuk ekstensi file) Kita akan merujuk ke banyak sumber daya aplikasi (termasuk gambar, string, dan elemen dalam file layout) menggunakan referensi serupa di kelas R.<br/>
<img src="images/activity&#32;main&#32;layout.png" width="800" alt="Tampilan file activity_main.xml"/><br/>
12. Untuk menjalankan aplikasi atau debugging, dapat dilakukan dengan dua cara.<br/>
    - [ ] Emulator \(Tidak terinstall)
    - [x] Mobile device \(Sudah siap)<br/>
      - Siapkan smartphone dan kabel data. Smartphone dengan OS Mobile Android, sedangkan kabel data adalah kabel yang dapat membaca data dari smartphone ke laptop (karena beberapa kasus terdapat kabel data yang hanya dapat digunakan untuk mengisi power atau baterai).
      - Penggunaan physical device dalam melakukan debug memerlukan beberapa pengaturan pada smartphone yaitu mengaktifkan developer option pada smartphone.<br/>
         - Pada perangkat mobile masuk ke **Pengaturan > Tentang telepon**
         - Klik beberapa kali pada bagian **Versi MIUI** dengan cepat sampai ada popup pesan bahwa **Anda sudah menjadi pengembang**
         - Kembali ke tampilan awal **Pengaturan** lalu masuk ke **Setelan tambahan > Opsi pengembang**
         - Scroll kebawah dan aktifkan **Debugging USB**<br/>
13. Setelah konfigurasi di langkah sebelumnya selesai, maka kita bisa melakukan debugging pada aplikasi kita menggunakan media emulator atau mobile device.
