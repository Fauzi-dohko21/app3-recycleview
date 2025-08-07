<img width="812" height="207" alt="image" src="https://github.com/user-attachments/assets/25829029-d173-48c8-90df-aa0794723976" />## 📱 Aplikasi RecyclerView – Data Siswa
Pembuatan project ini bertujuan untuk menampilkan daftar siswa dengan menggunakan komponen RecyclerView pada Android Studio. Aplikasi ini merupakan tugas praktikum yang dirancang untuk memahami cara kerja dari RecyclerView, model data, dan adapter dalam menampilkan data secara dinamis

## 👥 Daftar Anggota Tim
- M Alfian Fauzi ( 21 )
- Meutya Candra Dewi ( 26 )
- Sabila Zahrani ( 35 )
 
## Penjelasan RecyclerView
RecyclerView adalah sebuah komponen UI canggih yang diperkenalkan dalam Android Lollipop (API 21) sebagai pengganti metode ListView dan GridView, penggantian dilakukan karena Recycleview dapat menghasilkan performa yang jauh lebih baik dan fleksibilitas tinggi. RecyclerView digunakan untuk menampilkan kumpulan data yang besar secara efisien dengan cara mendaur ulang tampilan item yang tidak terlihat agar menghemat memori dan meningkatkan performa dan RecyclerView memungkinkan pengembang untuk mengatur tata letak item menggunakan LayoutManager seperti LinearLayoutManager, GridLayoutManager, atau StaggeredGridLayoutManager

## Penjelasan Alur Data
1. Student.kt (Model)

Student adalah sebuah data class yang berisi dan menyimpan properti dari siswa, seperti nama, NIS, kelas, dan foto. Model yang digunakan ini merupakan acuan untuk membangun struktur data yang akan ditampilkan di RecycleView


2. StudentAdapter.kt (Adapter) 

Berfungsi sebagai penghubung antara data siswa dan tampilan di RecyclerView. Adapter ini mengatur dan menangani aksi data siswa dimasukkan ke dalam layout item yang sudah dibuat dengan berdasarkan item_student.xml


3. item_student.xml (Layout Item) 

Merupakan layout yang digunakan untuk menampilkan satu item siswa dalam daftar RecyclerView. Layout ini biasanya berisi elemen gambar siswa, nama, NIS, dan kelas.


4. MainActivity.kt

MainActivity.kt bertanggung jawab untuk menampilkan data siswa ke dalam RecyclerView. Pada bagian ini, data siswa akan diinisialisasi dan kemudian dimasukkan ke dalam adapter. Setelah itu, RecyclerView akan dikonfigurasi menggunakan LayoutManager agar data ditampilkan dalam bentuk daftar (list) yang rapi dan terstruktur


5. DetailActivity.kt

Activity ini digunakan untuk menampilkan detail lengkap dari siswa yang dipilih. Data dikirim melalui Intent dari MainActivity

## ⚙️ Fitur Aplikasi
- Fitur Pertama yakni menampilkan 10 data siswa, yang memiliki code seperti ini :

<img width="500" height="420" alt="image" src="https://github.com/user-attachments/assets/8afc615e-4e32-4821-92e9-1c43f61b44a7" />

Kode ini berlokasikan di dalam fungsi onCreate() pada MainActivity, dan berfungsi untuk menampilkan daftar siswa menggunakan RecyclerView. Pertama, layout activity_main.xml dipasang, lalu RecyclerView dihubungkan menggunakan findViewById dan diatur tampil secara vertikal dengan LinearLayoutManager. Selanjutnya, data siswa dimasukkan secara manual ke dalam studentList menggunakan addAll(), berisi objek Student yang memiliki nama, NIS, dan kelas. Setelah data dimasukkan, adapter StudentAdapter dibuat dengan membawa context dan data tersebut, lalu disambungkan ke RecyclerView dengan recyclerView.adapter = studentAdapter.Setelah terjadi proses tersebut data siswa akan tampil secara otomatis di layar dalam bentuk list yang menghasilkan tampilan daftar siswa seperti ini

<img src="https://github.com/user-attachments/assets/c181ba1a-676b-4b79-b4dc-62e624f936f3" alt="WhatsApp Image" width="300"/>

- Fitur Kedua yakni fitur untuk melihat lebih lanjut data dari siswa, yang memiliki code seperti ini :

<img width="500" height="300" alt="Screenshot 2025-08-07 181149" src="https://github.com/user-attachments/assets/831eabe9-a2e5-4a08-9530-76d95dd4c4a1" />

Kode ini memiliki fungsi untuk menampilkan dialog konfirmasi saat item siswa di-klik di dalam RecyclerView. Saat pengguna menekan salah satu item, muncul dialog dengan pertanyaan "Lihat Detail?" dan pesan yang menyebutkan nama siswa tersebut. Jika tombol "Lihat" ditekan, maka aplikasi akan membuka DetailActivity sambil mengirimkan data siswa berupa nama, NIS, dan kelas melalui Intent. Data ini kemudian bisa ditampilkan lebih lanjut di halaman detail. Jika pengguna memilih "Batal", dialog akan ditutup tanpa melakukan apa-apa
- Contoh dari hasil code jika data siswa ditekan maka akan muncul notifikasi seperti ini :

<img src="https://github.com/user-attachments/assets/f4b224ee-44c3-4516-bc6d-5bbf2cfdae13" alt="WhatsApp Image" width="300"/>

- Contoh jika user memilih melihat data siswa :

<img src="https://github.com/user-attachments/assets/52b5c72e-3564-444a-be83-6bc3f78fb76c" alt="WhatsApp Image" width="300" />

- Fitur Ketiga yakni fitur untuk menambahan data siswa, yang memiliki code sepeti ini :
- 
<img width="500" height="170" alt="image" src="https://github.com/user-attachments/assets/365ff635-dc13-4eba-9061-47a6f7a7bf87" />

Kode ini berfungsi untuk membuka halaman tambah data siswa saat tombol Tambah ditekan. Ketika tombol tersebut diklik, aplikasi membuat Intent yang mengarah ke AddEditActivity. Selanjutnya, aktivitas tersebut dijalankan dengan startActivityForResult() menggunakan kode permintaan REQUEST_ADD agar data baru yang dimasukkan bisa diterima dan ditampilkan kembali di halaman utama.


Contoh dari hasil code tambah :

- Fitur Keempat yakni fitur edit yang memungkinkan untuk memperbarui data lama siswa dengan data yang baru, yang memiliki code seperti ini :

<img width="500" height="200" alt="image" src="https://github.com/user-attachments/assets/17ba6518-a99d-4773-87ab-f5f51b9ca6ec" />

Kode ini digunakan untuk mengarahkan pengguna ke halaman edit data siswa saat tombol Edit ditekan pada item RecyclerView. Data siswa seperti nama, NIS, kelas, dan posisi datanya dikirim ke AddEditActivity menggunakan Intent. Setelah itu, halaman edit dibuka dengan startActivityForResult() agar hasil perubahan bisa dikembalikan dan diperbarui di tampilan utama

- Contoh dari hasil dari code edit :


## Kesimpulan
Melalui proyek ini, kami belajar bagaimana mengembangkan aplikasi Android sederhana yang mampu menampilkan data siswa secara dinamis menggunakan RecyclerView. Proyek ini juga memberikan pemahaman mengenai penerapan fitur CRUD, seperti menambah, mengedit, menghapus, dan melihat detail data, dengan memanfaatkan adapter dan intent antar activity. Seluruh proses pengembangan dilakukan menggunakan Android Studio, yang membantu kami memahami alur kerja dalam membangun aplikasi yang fungsional dan terstruktur. Dengan demikian, proyek ini menambah wawasan serta keterampilan kami dalam pengembangan aplikasi berbasis Android.
