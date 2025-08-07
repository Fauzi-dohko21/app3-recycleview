## 📱 Aplikasi RecyclerView – Data Siswa
Pembuatan project ini bertujuan untuk menampilkan daftar siswa dengan menggunakan komponen RecyclerView pada Android Studio. Aplikasi ini merupakan tugas praktikum yang dirancang untuk memahami cara kerja dari RecyclerView, model data, dan adapter dalam menampilkan data secara dinamis

## 👥 Daftar Anggota Tim
- M Alfian Fauzi ( 21 )
- Meutya Candra Dewi ( 26 )
- Sabila Zahrani (35)
- 
## 📄 Penjelasan RecyclerView
RecyclerView adalah sebuah komponen UI canggih yang diperkenalkan dalam Android Lollipop (API 21) sebagai pengganti metode ListView dan GridView, penggantian dilakukan karena Recycleview dapat menghasilkan performa yang jauh lebih baik dan fleksibilitas tinggi. RecyclerView digunakan untuk menampilkan kumpulan data yang besar secara efisien dengan cara mendaur ulang tampilan item yang tidak terlihat agar menghemat memori dan meningkatkan performa dan RecyclerView memungkinkan pengembang untuk mengatur tata letak item menggunakan LayoutManager seperti LinearLayoutManager, GridLayoutManager, atau StaggeredGridLayoutManager

## 🔄 Penjelasan Alur Data
1.Student.kt (Model)
Student adalah sebuah data class yang berisi dan menyimpan properti dari siswa, seperti nama, NIS, kelas, dan foto. Model yang digunakan ini merupakan acuan untuk membangun struktur data yang akan ditampilkan di RecycleView

2.StudentAdapter.kt (Adapter) 
Berfungsi sebagai penghubung antara data siswa dan tampilan di RecyclerView. Adapter ini mengatur dan menangani aksi data siswa dimasukkan ke dalam layout item yang sudah dibuat dengan berdasarkan item_student.xml

3.item_student.xml (Layout Item) 
Merupakan layout yang digunakan untuk menampilkan satu item siswa dalam daftar RecyclerView. Layout ini biasanya berisi elemen gambar siswa, nama, NIS, dan kelas.

4.MainActivity.kt
MainActivity.kt bertanggung jawab untuk menampilkan data siswa ke dalam RecyclerView. Pada bagian ini, data siswa akan diinisialisasi dan kemudian dimasukkan ke dalam adapter. Setelah itu, RecyclerView akan dikonfigurasi menggunakan LayoutManager agar data ditampilkan dalam bentuk daftar (list) yang rapi dan terstruktur

5.DetailActivity.kt
Activity ini digunakan untuk menampilkan detail lengkap dari siswa yang dipilih. Data dikirim melalui Intent dari MainActivity

## ⚙️ Fitur Aplikasi

1.Menampilkan daftar siswa menggunakan RecyclerView dengan tata letak vertikal

2.Setiap item siswa berisi foto, nama, NIS, dan kelas.

3.Pengguna dapat melihat detail lengkap siswa melalui halaman DetailActivity.

4.Tersedia tombol Edit untuk mengubah data siswa.

5.Tersedia tombol Hapus untuk menghapus data siswa dari daftar.


💻 Penjelasan code penting

1.📄 Penjelasan Kode DetailActivity.kt
