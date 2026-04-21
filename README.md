# TUGAS UTS STRUKTUR DATA 

<img width="162" height="148" alt="image" src="https://github.com/user-attachments/assets/c30ffe31-564f-4bc0-b0af-28385c2b2c9b" />



NAMA : DAUD GALLU WOLA (2501010343)

NAMA : CLAUDYA FOLENTA BUNGA BA (2501010358)

NAMA : ACHMAD SANDY FARYOKO (2501010066)

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

# 3. Sistem dan Implementasi

  # Desain sistem menggunakan Flowchart

<img width="397" height="425" alt="Cuplikan layar 2026-04-01 185202" src="https://github.com/user-attachments/assets/dfb0b823-710a-4ae7-a5a4-2b38e9127923" />

  
  **Penjelasan Flowchart Sistem Parkir (Queue Berbasis Array)**

  Flowchart tersebut menggambarkan alur kerja sistem parkir yang menggunakan konsep Queue (antrian) dengan beberapa pilihan menu utama. Setiap langkah memiliki fungsi tertentu dalam mengelola kendaraan yang masuk dan keluar dari area parkir.

 **1. Mulai**

 Proses dimulai dari simbol “Mulai”, yang menandakan bahwa sistem parkir mulai dijalankan.

**2. Input Pilihan Menu**

Pengguna (operator parkir) diminta untuk memasukkan pilihan menu yang tersedia. Pilihan ini menentukan operasi apa yang akan dilakukan dalam sistem.

**3. Proses Keputusan (Pilih?)**

Pada bagian ini terdapat simbol decision (percabangan) yang berfungsi untuk mengecek pilihan yang dimasukkan oleh pengguna. Terdapat 5 kemungkinan:

**A. Enqueue (Tambah Kendaraan)**

Jika memilih 1, maka sistem akan:

*Menambahkan kendaraan (nomor polisi) ke dalam antrian parkir

*Kendaraan ditempatkan di posisi paling belakang  

**B. Dequeue (Hapus Kendaraan Depan)**

Jika memilih 2, maka sistem akan:

*Menghapus kendaraan yang berada di posisi paling depan 

*Kendaraan tersebut dianggap keluar dari area parkir

**C. Peek (Melihat Kendaraan Depan)**

Jika memilih 3, maka sistem akan:

*Menampilkan kendaraan yang berada di posisi paling depan

*Data tidak dihapus, hanya ditampilkan kembali

**D. Tampil Semua**

Jika memilih 4, maka sistem akan:

Menampilkan seluruh daftar kendaraan yang sedang berada dalam antrian parkir

# ---------------------------------- #

<img width="1366" height="599" alt="screencapture-programiz-cpp-programming-online-compiler-2026-04-04-13_00_37" src="https://github.com/user-attachments/assets/8270baf4-1ad7-4c4d-8d66-f1d01811d0ac" />

<img width="1366" height="599" alt="screencapture-programiz-cpp-programming-online-compiler-2026-04-04-13_01_11 (1)" src="https://github.com/user-attachments/assets/a4dd9879-0d86-45e2-b7bb-b5f36afec366" />

<img width="1366" height="599" alt="screencapture-programiz-cpp-programming-online-compiler-2026-04-04-13_01_53" src="https://github.com/user-attachments/assets/84f18261-1b55-4ac1-8536-d17d926c2100" />

<img width="1366" height="599" alt="screencapture-programiz-cpp-programming-online-compiler-2026-04-04-13_02_13" src="https://github.com/user-attachments/assets/1cf52dd8-dcdb-4ad8-bbc2-2df92d20e568" />

<img width="1366" height="599" alt="screencapture-programiz-cpp-programming-online-compiler-2026-04-04-13_02_45" src="https://github.com/user-attachments/assets/8fb5d6dc-5688-4e71-a0a2-fe66103cddce" />

**#include <iostream>**

**#include <string>**

**using namespace std;**

**const int MAX = 100;  // Kapasitas maksimal 100

class SistemParkir {
private:
    string nomor[MAX];
    int front, rear;
    int totalMasuk, totalKeluar, sisa;

public:
    SistemParkir() {
        front = 0;
        rear = -1;
        totalMasuk = 0;
        totalKeluar = 0;
        sisa = 0;
    }

    bool isFull() {
        return sisa == MAX;
    }

    bool isEmpty() {
        return sisa == 0;
    }

    void enqueue() {
        if (isFull()) {
            cout << "\nParkir penuh (100/100)" << endl;
            return;
        }

        int jumlah;
        cout << "Jumlah kendaraan masuk: ";
        cin >> jumlah;

        if (jumlah > (MAX - sisa)) {
            cout << "Melebihi kapasitas! Maksimal " << (MAX - sisa) << endl;
            return;
        }

        for (int i = 0; i < jumlah; i++) {
            cout << "Nomor polisi ke-" << (i+1) << ": ";
            cin >> nomor[++rear];
            sisa++;
            totalMasuk++;
        }
        cout << "Berhasil masuk " << jumlah << " kendaraan" << endl;
    }

    void dequeue() {
        if (isEmpty()) {
            cout << "\nParkir kosong" << endl;
            return;
        }

        int jumlah;
        cout << "Jumlah kendaraan keluar: ";
        cin >> jumlah;

        if (jumlah > sisa) {
            cout << "Hanya ada " << sisa << " kendaraan" << endl;
            jumlah = sisa;
        }

        cout << "\nKendaraan keluar:" << endl;
        for (int i = 0; i < jumlah; i++) {
            cout << (i+1) << ". " << nomor[front] << endl;
            front++;
            sisa--;
            totalKeluar++;
        }
        cout << "Keluar " << jumlah << " kendaraan" << endl;
    }
    
    void peek() {
        if (isEmpty()) {
            cout << "\nParkir kosong" << endl;
            return;
        }
        cout << "\nKendaraan di depan: " << nomor[front] << endl;
        cout << "Total di parkir: " << sisa << endl;
    }

    void tampil() {
        if (isEmpty()) {
            cout << "\nParkir kosong" << endl;
            return;
        }

        cout << "\nDaftar kendaraan di parkir (" << sisa << "/100):" << endl;
        for (int i = front, no = 1; i <= rear; i++, no++) {
            cout << no << ". " << nomor[i] << endl;
        }
        cout << "\nTotal keluar: " << totalKeluar << endl;
    }

    void laporanAkhir() {
        cout << "LAPORAN SISTEM PARKIR" << endl;
        cout << "Kendaraan masuk: " << totalMasuk << endl;
        cout << "Kendaraan keluar: " << totalKeluar << endl;
        cout << "Masih di parkir: " << sisa << endl;
        
        cout << "SELESAI" << endl;
    }
};

int main() {
    SistemParkir parkir;
    int pilihan;

    cout << "SISTEM PARKIR - Kapasitas 100" << endl;

    while (true) {
        cout << "\n1. Masukkan kendaraan" << endl;
        cout << "2. Keluarkan kendaraan" << endl;
        cout << "3. Cek depan" << endl;
        cout << "4. Tampilkan parkir" << endl;
        cout << "5. Laporan akhir & selesai" << endl;
        cout << "Pilih (1-5): ";
        cin >> pilihan;

        switch (pilihan) {
            case 1:
                parkir.enqueue();
                break;
            case 2:
                parkir.dequeue();
                break;
            case 3:
                parkir.peek();
                break;
            case 4:
                parkir.tampil();
                break;
            case 5:
                parkir.laporanAkhir();
                return 0;
            default:
                cout << "Pilihan salah" << endl;
        }
    }
}

# _________________________________________________________________________ #


# HASIL NYA
# SISTEM PARKIR - Kapasitas 100

# Langkah 1

1. Masukkan kendaraan
2. Keluarkan kendaraan
3. Cek depan
4. Tampilkan parkir
5. Laporan akhir & selesai
Pilih (1-5): 1
Jumlah kendaraan masuk: 10
Nomor polisi ke-1: 1

Nomor polisi ke-2: 2

Nomor polisi ke-3: 3

Nomor polisi ke-4: 4

Nomor polisi ke-5: 5

Nomor polisi ke-6: 6

Nomor polisi ke-7: 7

Nomor polisi ke-8: 8

Nomor polisi ke-9: 9

Nomor polisi ke-10: 10

Berhasil masuk 10 kendaraan

# Langkah 2

1. Masukkan kendaraan

2. Keluarkan kendaraan

3. Cek depan

4. Tampilkan parkir

5. Laporan akhir & selesai

Pilih (1-5): 2

Jumlah kendaraan keluar: 6

Kendaraan keluar:

1. 1

2. 2

3. 3

4. 4

5. 5

6. 6

Keluar 6 kendaraan

# Langkah 3

1. Masukkan kendaraan

2. Keluarkan kendaraan

3. Cek depan

4. Tampilkan parkir

5. Laporan akhir & selesai

Pilih (1-5): 3

Kendaraan di depan: 7

Total di parkir: 4

# Langkah 4

1. Masukkan kendaraan

2. Keluarkan kendaraan

3. Cek depan

4. Tampilkan parkir

5. Laporan akhir & selesai

Pilih (1-5): 4

Daftar kendaraan di parkir (4/100):

1. 7

2. 8

3. 9

4. 10

Total keluar: 6

# Langkah 5

1. Masukkan kendaraan

2. Keluarkan kendaraan

3. Cek depan

4. Tampilkan parkir

5. Laporan akhir & selesai

Pilih (1-5): 5

LAPORAN SISTEM PARKIR

Kendaraan masuk: 10



Kendaraan keluar: 6

Masih di parkir: 4

SELESAI

# ______________________________________ #


# KESIMPULAN

Berdasarkan hasil perancangan dan implementasi sistem parkir berbasis Queue (antrian) menggunakan array, dapat disimpulkan bahwa:

**1.Konsep Queue (FIFO) terbukti sangat efektif dalam mengelola antrian kendaraan pada sistem parkir. Kendaraan yang masuk terlebih dahulu akan keluar lebih dahulu, sehingga menciptakan sistem yang adil, teratur, dan mudah dipahami.**

**2.Implementasi menggunakan array mampu memberikan solusi yang sederhana, terstruktur, dan efisien untuk sistem parkir dengan kapasitas terbatas. Operasi dasar seperti enqueue, dequeue, dan peek dapat dijalankan dengan baik sesuai dengan prinsip queue.**

**3.Sistem yang dirancang berhasil mengatasi permasalahan nyata, seperti pengelolaan kendaraan masuk dan keluar, keteraturan antrian, serta pemantauan jumlah kendaraan di area parkir secara real-time.**

**4.Dari hasil pengujian program, sistem mampu menampilkan informasi secara akurat, seperti jumlah kendaraan masuk, keluar, dan sisa kendaraan, sehingga memudahkan dalam proses monitoring dan pengambilan keputusan.**

**5.Meskipun array memiliki keterbatasan dalam kapasitas yang bersifat tetap, sistem ini tetap efektif untuk skala kecil hingga menengah. Untuk pengembangan lebih lanjut, penggunaan linked list dapat dipertimbangkan agar sistem menjadi lebih fleksibel dan dinamis.**

  **Secara keseluruhan**, sistem parkir berbasis queue ini menunjukkan bahwa penerapan struktur data dalam kehidupan nyata sangat membantu dalam meningkatkan efisiensi, keteraturan, dan kemudahan pengelolaan suatu sistem.



# SARAN

Sistem ini masih dapat dikembangkan lebih lanjut agar lebih optimal. Misalnya dengan menggunakan struktur data yang lebih fleksibel seperti linked list, menambahkan fitur pencarian kendaraan, serta membuat tampilan yang lebih interaktif. Selain itu, sistem juga bisa dikembangkan menjadi berbasis aplikasi agar lebih mudah digunakan dalam kondisi nyata.


# PENUTUP

Demikian tugas ini disusun sebagai bentuk pemahaman terhadap penerapan struktur data queue dalam kehidupan sehari-hari. Diharapkan sistem yang dibuat dapat memberikan gambaran sederhana mengenai pengelolaan antrian parkir. Penulis menyadari bahwa masih terdapat kekurangan, sehingga kritik dan saran sangat diharapkan untuk perbaikan ke depannya.
