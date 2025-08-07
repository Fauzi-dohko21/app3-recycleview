PROJECT REYCLERVIEW

PROJECT REYCLERVIEW biasanya merujuk pada pembuatan aplikasi Android yang menampilkan data dalam bentuk daftar atau grid menggunakan RecyclerView, yaitu salah satu komponen UI di Android yang lebih efisien dibandingkan komponen lama seperti ListView.

📱 Aplikasi RecyclerView – Data Siswa
Aplikasi ini merupakan hasil dari tugas praktikum yang bertujuan untuk memahami cara kerja komponen RecyclerView pada Android Studio.
Dalam aplikasi ini, RecyclerView digunakan untuk menampilkan daftar siswa dalam bentuk list yang rapi, efisien, dan mudah dikelola.
Komponen ini dipilih karena memiliki performa yang lebih baik dibandingkan ListView dalam menampilkan data jumlah banyak secara dinamis.

📄 Penjelasan RecyclerView

RecyclerView adalah salah satu komponen tampilan (view) yang disediakan oleh Android untuk 
menampilkan kumpulan data dalam jumlah besar secara efisien. Komponen ini bekerja dengan 
cara menampilkan hanya item yang terlihat di layar dan mendaur ulang (recycle) tampilan item yang sudah tidak terlihat agar dapat digunakan kembali untuk data berikutnya. 
Dengan metode ini, performa aplikasi menjadi lebih baik dan penggunaan memori menjadi lebih efisien.

Dibandingkan dengan ListView, RecyclerView memiliki fleksibilitas yang lebih tinggi. 
RecyclerView memungkinkan pengembang untuk mengatur tata letak item menggunakan LayoutManager seperti LinearLayoutManager, GridLayoutManager, atau StaggeredGridLayoutManager.
Selain itu, RecyclerView juga mendukung penggunaan dekorasi item (item decoration) dan animasi transisi data, sehingga tampilan daftar menjadi lebih menarik.

👥 Tim

-M.Alfian Fauzi (21)

-Meutya Candra Dewi (26)

-Sabila Zahrani (35)

🔄 Penjelasan Alur Data
1.Student.kt (Model) Berisi data class Student yang digunakan untuk menyimpan informasi setiap siswa, seperti nama, NIS, kelas, dan foto.
Model ini menjadi acuan struktur data yang akan ditampilkan di aplikasi.
2.StudentAdapter.kt (Adapter) Berfungsi sebagai penghubung antara data siswa dan tampilan di RecyclerView. 
Adapter ini mengatur bagaimana setiap data siswa akan dimasukkan ke dalam layout item yang sudah dibuat.
3.item_student.xml (Layout Item) Merupakan layout yang digunakan untuk menampilkan satu item siswa dalam daftar RecyclerView. 
Layout ini biasanya berisi elemen gambar siswa, nama, NIS, dan kelas.
4.MainActivity.kt Bertanggung jawab untuk menampilkan data siswa pada RecyclerView.
Di sini, data dimasukkan ke dalam adapter dan diatur menggunakan LayoutManager agar tampil dalam bentuk list.
5.DetailActivity.kt Menampilkan detail lengkap siswa yang dipilih dari daftar. 
Data dikirimkan dari MainActivity melalui Intent.

⚙️ Fitur Aplikasi
1.Menampilkan daftar siswa menggunakan RecyclerView dengan tata letak vertikal
2.Setiap item siswa berisi foto, nama, NIS, dan kelas.
3.Pengguna dapat melihat detail lengkap siswa melalui halaman DetailActivity.
4.Tersedia tombol Edit untuk mengubah data siswa.
5.Tersedia tombol Hapus untuk menghapus data siswa dari daftar.

🔧 Teknologi
Kotlin
Android Studio
Git + GitHub

💻 Penjelasan code penting
1.📄 Penjelasan Kode DetailActivity.kt
