# LAPORAN-PROJECT-UTS-STRUKTUR-DATA
Mata Kuliah: Struktur Data
Semester: 2025/2026
Jenis Tugas: Tugas Kelompok
Tema: Penerapan Stack menggunakann Array

# IDENTITAS KELOMPOK
1. I Gede Winasa Edy Purnama | NIM: [2501010082] | Akun Github: [winasagntgbgt]
2. I Kadek Dwi Andika | NIM: [2501010085] | Akun Github: [dwiandika15]
3. Kristian Putra Santosa | [2501010348] | Akun Github: [TiannPtra]

# RUMUSAN MASALAH
1. Bagaimana cara mengimplementasikan struktur data stack untuk menyimpan riwayat halaman web yang telah dibuka?
2. Bagaimana cara kerja fitur undo (kembali ke halaman sebelumnya) menggunakan stack?
3. Bagaimana sistem menangani perintah membuka halaman web baru dan menyimpannya ke dalam stack?
4. Bagaimana menangani kondisi ketika pengguna melakukan undo tetapi data pada stack kosong?
5. Bagaimana cara merancang program agar dapat menjalankan perintah membuka web, undo, dan exit dengan baik dan terstruktur?

# LANDASAN TEORI
1. PENGERTIAN STRUKTUR DATA
   Struktur Data merupakan metode penyimpanan, penyususan, pengorganisasian, pengelompokan dan pengaturan berbagai data dalam suatu media penyimpanan dalam sistem komputer sehingga dapat dimanfaatkan secara efektif dan efisien.
   
2. KONSEP STACK
   Stack adalah struktur data linier yang berjalan berdasarkan prinsip Last In, First Out (LIFO). Ini berarti elemen terakhir yang ditambahkan ke stack adalah elemen      pertama yang dihapus. Meskipun prinsip ini tampak sederhana, prinsip ini sangat ampuh dan memiliki banyak aplikasi praktis dalam pemrograman.
   
   Stack menyediakan dua operasi utama: push, yang menambahkan elemen ke bagian atas stack, dan pop, yang menghapus elemen dari bagian atas stack. Meskipun hanya memiliki dua operasi inti ini, stack merupakan komponen penting dalam berbagai algoritma dan mekanisme sistem komputer.

3. KONSEP LIFO
   LIFO (Last In, First Out) adalah suatu metode yang mengasumsikan bahwa data yang terakhir masuk ke dalam stack akan dianggap sebagai yang pertama kali keluar. Dalam program yang kami buat, kami menggunakan konsep ini, jadi halaman website terakhir yang diakses oleh pengguna akan dianggap sebagai halaman pertama yang akan dihapus jika pengguna memberikan perintah back.

4. implementasi array
   Program ini mengimplementasikan Array (Python List) sebagai fondasi struktur data Stack dengan prinsip Last In First Out (LIFO). Array bertindak sebagai wadah linear dinamis di mana operasi Push dijalankan melalui fungsi .append untuk menambah data ke indeks terakhir (paling atas). Operasi Pop menggunakan fungsi .pop untuk mengambil sekaligus menghapus elemen terakhir saat fitur Back dipanggil. Sementara itu, operasi Peek diterapkan menggunakan indeks guna mengakses data teratas tanpa mengubah struktur tumpukan. Penggunaan Array menjamin efisiensi memori dan kecepatan akses optimal dalam mengelola riwayat penjelajahan.

# SUMBER ILMIAH
Amaylia, S., Setiabudi, V. A., Alvianino, R., Saputra, R. N., Wardhani, H. K., & Suroni, A. (2025). Application of Stack Data Structure in Application Development. State University of Surabaya, Indonesia.

Saragiih, R. A., Surya, S., Syahrozi, H., & Gunawan, I. (Tidak terdapat tahun terbit). Data dan Struktur Data. Program Studi Teknik Informatika, STIKOM Tunas Bangsa Pematangsiantar.

Rahmatuloh, M., Kalyana, A. F., & Kusumah, P. P. (2024). Sistem ERP Modul Persediaan dengan Menggunakan Metode LIFO (Last In First Out) Berbasis Web (Studi Kasus: Distro Insulting Arrogant).

# DESAIN SISTEM DAN IMPLEMENTASI 

<img width="857" height="1180" alt="ChatGPT Image 15 Apr 2026, 19 55 16" src="https://github.com/user-attachments/assets/adae17cc-ed72-4a62-b7cb-2e4cb3784665" />

# ALUR

Flowchart dimulai dari proses “Mulai”, kemudian sistem menampilkan halaman saat ini. Setelah itu, pengguna diminta untuk memasukkan perintah pada bagian input (Masukkan Perintah). Pada tahap ini terjadi percabangan (decision) berdasarkan perintah yang dimasukkan, yaitu push, pop, peek, atau exit.

Jika pengguna memilih push, maka sistem akan membuka halaman baru dan menambahkan URL ke dalam stack. Jika memilih pop, sistem akan menghapus halaman teratas dari stack (kembali ke halaman sebelumnya). Jika memilih peek, sistem akan menampilkan halaman yang sedang aktif (halaman teratas pada stack). Jika pengguna memasukkan perintah lain yang tidak valid, maka sistem akan menampilkan pesan error dan meminta input ulang.

Setelah setiap proses dijalankan, alur akan kembali ke tampilan halaman saat ini dan terus berulang sampai pengguna memilih exit, yang akan mengakhiri program dan menuju ke proses “Selesai”

# IMPLEMENTASI

-ARRAY


<img width="401" height="96" alt="Screenshot 2026-04-15 201337" src="https://github.com/user-attachments/assets/e6ff56fa-8ba4-4b90-a48f-7464f1970c6c" />


Dalam Python, Array diimplementasikan menggunakan List. Pada kode ini, Array didefinisikan di dalam konstruktor sebagai self.stack = []. Ini berfungsi sebagai wadah linear yang menyimpan data secara berurutan. Semua operasi Stack dilakukan pada ujung akhir (indeks terakhir) dari Array ini.



-PUSH


<img width="419" height="105" alt="Screenshot 2026-04-15 203005" src="https://github.com/user-attachments/assets/97697a31-94ee-4181-964a-11ee8da19388" />


Operasi Push adalah proses menambahkan data ke puncak tumpukan. Dalam kode ini, ini diterapkan pada fungsi buka_halaman(url).
Logika: Menggunakan perintah self.stack.append(url).
Cara Kerja: Data baru (URL) dimasukkan ke indeks terakhir Array, sehingga otomatis menjadi elemen teratas yang akan diakses pertama kali saat proses kembali (back).



-POP


<img width="625" height="180" alt="Screenshot 2026-04-15 203238" src="https://github.com/user-attachments/assets/0b6a8dec-c60c-4ecb-8ab2-4ee96e900973" />



Operasi Pop adalah proses mengambil sekaligus menghapus data dari puncak tumpukan. Ini diterapkan pada fungsi klik_back().
Logika: Menggunakan perintah self.stack.pop().
Cara Kerja: Program mengambil elemen di indeks terakhir Array dan menghapusnya dari memori tumpukan. Hal ini sesuai dengan prinsip LIFO (Last In First Out), di mana halaman terakhir yang dibuka adalah yang pertama kali ditutup.



-PEEK


<img width="345" height="134" alt="Screenshot 2026-04-15 203522" src="https://github.com/user-attachments/assets/27385a56-9b41-41cf-920d-f91ea2dad30f" />



Operasi Peek digunakan untuk melihat data teratas tanpa mengubah atau menghapus isi tumpukan. Ini diterapkan pada fungsi lihat_halaman_sekarang().
Logika: Menggunakan akses indeks self.stack[-1].
Cara Kerja: Indeks [-1] merujuk pada elemen terakhir dalam Array. Fungsi ini hanya mengembalikan nilai tersebut agar user tahu posisi halaman saat ini tanpa merusak riwayat yang ada.



-DISPLAY


<img width="678" height="880" alt="Screenshot 2026-04-15 204012" src="https://github.com/user-attachments/assets/ab35b9c6-7bcd-4efa-aee9-c153e29622fb" />



Penerapan Display pada kode tersebut berfungsi untuk memvisualisasikan seluruh isi Array riwayat secara transparan kepada pengguna. Operasi ini bekerja dengan melakukan Iterasi atau perulangan melalui fungsi enumerate(self.stack, 1), yang secara sistematis menelusuri elemen dari indeks awal hingga indeks terakhir (elemen teratas). Dalam laporan, bagian ini menunjukkan kemampuan program untuk membongkar tumpukan data dan menyajikannya dalam format daftar bernomor tanpa mengubah struktur asli Stack tersebut. Hal ini membuktikan bahwa meskipun Stack adalah struktur data akses terbatas (LIFO), seluruh elemen di dalam Array tetap dapat diakses untuk keperluan pelaporan atau pemeriksaan riwayat secara kronologis.

# KESIMPULAN

Berikut kesimpulan dari laporan tersebut:

**Kesimpulan:**

Berdasarkan hasil perancangan dan implementasi program, dapat disimpulkan bahwa struktur data **stack** dengan konsep **LIFO (Last In First Out)** sangat efektif digunakan untuk mengelola riwayat halaman web. Program yang dibuat mampu menjalankan fungsi utama seperti membuka halaman (push), kembali ke halaman sebelumnya (pop/undo), melihat halaman saat ini (peek), serta keluar dari program (exit) dengan baik dan terstruktur.

Penggunaan array (list Python) sebagai dasar implementasi stack terbukti sederhana namun efisien dalam mengelola data secara dinamis. Setiap operasi pada stack berjalan sesuai dengan prinsip LIFO, sehingga halaman terakhir yang dibuka akan menjadi yang pertama diakses kembali saat pengguna melakukan undo.

Selain itu, program juga mampu menangani kondisi khusus seperti stack kosong dengan memberikan respon yang sesuai. Dengan adanya fitur tambahan seperti display, pengguna dapat melihat seluruh riwayat halaman tanpa mengubah isi stack.

Secara keseluruhan, implementasi ini menunjukkan bahwa stack merupakan solusi yang tepat dan praktis untuk kasus pengelolaan riwayat navigasi, khususnya dalam aplikasi sederhana seperti simulasi browser.


