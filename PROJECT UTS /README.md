# TUGAS UTS STRUKTUR DATA 

<img width="162" height="148" alt="image" src="https://github.com/user-attachments/assets/c30ffe31-564f-4bc0-b0af-28385c2b2c9b" />



NAMA : DAUD GALLU WOLA (2501010343)

NAMA : 

# STUDI KASUS SISTEM PARKIR (QUEUE BERBASIS ARRAY)
# 1. Rumusan Masalah dan Solusi

Rumusan Masalah
1.  Bagaimana konsep struktur data queue dapat digunakan untuk mengelola antrian kendaraan pada sistem parkir secara efisien dan terstruktur?
    Permasalahan ini muncul karena dalam kehidupan sehari-hari, kendaraan yang masuk ke area parkir harus dilayani berdasarkan urutan kedatangan agar tidak terjadi kekacauan atau ketidakadilan dalam pelayanan.

2.  Bagaimana penggunaan struktur data lain seperti linked list dapat meningkatkan fleksibilitas dibandingkan array dalam implementasi sistem antrian parkir?
    Hal ini menjadi penting karena jumlah kendaraan yang datang tidak selalu tetap, sehingga diperlukan struktur data yang mampu menyesuaikan kapasitas secara dinamis.

3.  Bagaimana sistem parkir berbasis queue yang dirancang mampu menyelesaikan permasalahan nyata seperti keterbatasan lahan parkir, penumpukan kendaraan, dan pengelolaan keluar-masuk kendaraan secara tertib?
    Permasalahan ini sering terjadi di pusat perbelanjaan, kampus, maupun perkantoran yang memiliki kapasitas parkir terbatas.

# Solusi yang Ditawarkan

**1**.Penggunaan Queue (FIFO)
Sistem menggunakan konsep First In First Out (FIFO), di mana kendaraan yang datang terlebih dahulu akan keluar terlebih dahulu. Hal ini menciptakan sistem yang adil dan teratur.

**2**.Implementasi Menggunakan Array
Array digunakan sebagai struktur penyimpanan data kendaraan karena mudah diimplementasikan dan efisien untuk sistem sederhana dengan kapasitas tetap.

**3**.Pengelolaan Operasi Queue
    Sistem menyediakan operasi:

   Enqueue → menambahkan kendaraan ke antrian
  
   Dequeue → mengeluarkan kendaraan dari antrian
  
   Peek → melihat kendaraan paling depan

**4**.Efisiensi dan Keteraturan Sistem
Sistem ini membantu mengurangi kemacetan, mengatur kendaraan dengan rapi, serta memudahkan pengelolaan parkir secara otomatis.

# 2. Landasan Teori

**Pengertian Struktur Data**

Struktur data adalah cara untuk menyimpan, mengatur, dan mengelola data dalam komputer sehingga dapat digunakan secara efisien. Struktur data sangat penting dalam pengembangan sistem karena menentukan bagaimana data diproses dan diakses.

**Konsep Queue dan Stack**

Queue adalah struktur data yang bekerja berdasarkan prinsip antrian (FIFO), sedangkan stack menggunakan prinsip tumpukan (LIFO). Dalam queue, elemen pertama yang masuk akan menjadi elemen pertama yang keluar. Sedangkan dalam stack, elemen terakhir yang masuk akan menjadi yang pertama keluar.

**Konsep FIFO dan LIFO**

FIFO (First In First Out) digunakan dalam queue, seperti antrian parkir.
LIFO (Last In First Out) digunakan dalam stack, seperti tumpukan buku.
Dalam sistem parkir, FIFO lebih relevan karena kendaraan harus keluar sesuai urutan masuk

**Implementasi Array dan Linked List**

* Array: memiliki ukuran tetap, mudah digunakan, dan efisien untuk data kecil.

* Linked List: lebih fleksibel karena dapat bertambah atau berkurang secara dinamis, tetapi lebih kompleks.

Dalam tugas ini digunakan array karena sesuai untuk sistem sederhana dengan kapasitas terbatas.

**Sumber Ilmiah**

1.Weiss, Mark Allen. Data Structures and Algorithm Analysis in C++.

2.Cormen, Thomas H. Introduction to Algorithms.

3.Artikel Jurnal: “Implementation of Queue Data Structure in Real Life Applications”
