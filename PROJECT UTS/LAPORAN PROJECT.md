## LAPORAN-PROJECT-UTS-STRUKTUR-DATA

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

4.implementasi array
    Program ini mengimplementasikan Array (Python List) sebagai fondasi struktur data Stack dengan prinsip Last In First Out (LIFO). Array bertindak sebagai wadah linear dinamis di mana operasi Push dijalankan melalui fungsi .append untuk menambah data ke indeks terakhir (paling atas). Operasi Pop menggunakan fungsi .pop untuk mengambil sekaligus menghapus elemen terakhir saat fitur Back dipanggil. Sementara itu, operasi Peek diterapkan menggunakan indeks guna mengakses data teratas tanpa mengubah struktur tumpukan. Penggunaan Array menjamin efisiensi memori dan kecepatan akses optimal dalam mengelola riwayat penjelajahan.

# SUMBER ILMIAH
Amaylia, S., Setiabudi, V. A., Alvianino, R., Saputra, R. N., Wardhani, H. K., & Suroni, A. (2025). Application of Stack Data Structure in Application Development. State University of Surabaya, Indonesia.

Saragiih, R. A., Surya, S., Syahrozi, H., & Gunawan, I. (Tidak terdapat tahun terbit). Data dan Struktur Data. Program Studi Teknik Informatika, STIKOM Tunas Bangsa Pematangsiantar.

Rahmatuloh, M., Kalyana, A. F., & Kusumah, P. P. (2024). Sistem ERP Modul Persediaan dengan Menggunakan Metode LIFO (Last In First Out) Berbasis Web (Studi Kasus: Distro Insulting Arrogant).

