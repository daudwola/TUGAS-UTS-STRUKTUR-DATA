# TUGAS-UTS-STRUKTUR-DATA
/*
 * ================================================================
 *  SISTEM ANTRIAN PARKIR KENDARAAN - BERBASIS ARRAY (QUEUE)
 *  Studi Kasus : Manajemen Antrian Masuk Parkir
 *  Struktur Data : Queue (FIFO) dengan Circular Array
 *  Bahasa       : C++
 * ================================================================
 */

#include <iostream>
#include <string>
#include <iomanip>
using namespace std;

// ================================================================
//  KONSTANTA
// ================================================================
const int MAX_KAPASITAS = 8;   // Kapasitas lahan parkir
const int MAX_ANTRIAN   = 10;  // Kapasitas maksimum antrian masuk

// ================================================================
//  STRUKTUR DATA KENDARAAN
// ================================================================
struct Kendaraan {
    int    nomorUrut;
    string platNomor;
    string jenisKendaraan;   // Motor / Mobil
    string waktuTiba;
    string status;           // Menunggu / Parkir / Keluar
};

// ================================================================
//  IMPLEMENTASI QUEUE BERBASIS CIRCULAR ARRAY
// ================================================================
struct QueueAntrian {
    Kendaraan data[MAX_ANTRIAN];
    int front;
    int rear;
    int ukuran;
    int counter;

    // --- Inisialisasi ---
    QueueAntrian() : front(0), rear(-1), ukuran(0), counter(0) {}

    bool isEmpty() { return ukuran == 0; }
    bool isFull()  { return ukuran == MAX_ANTRIAN; }

    // ---- ENQUEUE: Kendaraan masuk ke antrian ----
    bool enqueue(string plat, string jenis, string waktu) {
        if (isFull()) {
            cout << "\n  [!] Antrian penuh! Kendaraan tidak dapat mendaftar.\n";
            return false;
        }
        rear = (rear + 1) % MAX_ANTRIAN;
        counter++;
        data[rear] = { counter, plat, jenis, waktu, "Menunggu" };
        ukuran++;
        cout << "\n  [+] Kendaraan berhasil masuk antrian!\n";
        cout << "  +--------------------------------------------+\n";
        cout << "  | Nomor Urut     : " << setw(4) << left << counter << "                       |\n";
        cout << "  | Plat Nomor     : " << setw(22) << left << plat << "       |\n";
        cout << "  | Jenis          : " << setw(22) << left << jenis << "       |\n";
        cout << "  | Waktu Tiba     : " << setw(22) << left << waktu << "       |\n";
        cout << "  | Status         : Menunggu                   |\n";
        cout << "  +--------------------------------------------+\n";
        return true;
    }

    // ---- DEQUEUE: Kendaraan terdepan masuk area parkir ----
    bool dequeue(int &slotTersisa) {
        if (isEmpty()) {
            cout << "\n  [!] Antrian kosong. Tidak ada kendaraan yang menunggu.\n";
            return false;
        }
        if (slotTersisa <= 0) {
            cout << "\n  [!] Lahan parkir penuh! Kendaraan tetap mengantri.\n";
            return false;
        }
        Kendaraan k = data[front];
        front = (front + 1) % MAX_ANTRIAN;
        ukuran--;
        slotTersisa--;
        cout << "\n  [>>] Kendaraan dipersilakan masuk lahan parkir:\n";
        cout << "  +--------------------------------------------+\n";
        cout << "  | Plat Nomor     : " << setw(22) << left << k.platNomor  << "       |\n";
        cout << "  | Jenis          : " << setw(22) << left << k.jenisKendaraan << "       |\n";
        cout << "  | Waktu Tiba     : " << setw(22) << left << k.waktuTiba   << "       |\n";
        cout << "  | Status         : PARKIR                     |\n";
        cout << "  | Slot Tersisa   : " << setw(4) << left << slotTersisa << "                       |\n";
        cout << "  +--------------------------------------------+\n";
        return true;
    }

    // ---- PEEK: Lihat kendaraan terdepan antrian ----
    void peek() {
        if (isEmpty()) {
            cout << "\n  [!] Antrian kosong.\n";
            return;
        }
        Kendaraan k = data[front];
        cout << "\n  [~] Kendaraan terdepan antrian:\n";
        cout << "  +--------------------------------------------+\n";
        cout << "  | Nomor Urut     : " << setw(22) << left << k.nomorUrut    << "       |\n";
        cout << "  | Plat Nomor     : " << setw(22) << left << k.platNomor    << "       |\n";
        cout << "  | Jenis          : " << setw(22) << left << k.jenisKendaraan << "       |\n";
        cout << "  | Waktu Tiba     : " << setw(22) << left << k.waktuTiba    << "       |\n";
        cout << "  | Status         : " << setw(22) << left << k.status       << "       |\n";
        cout << "  +--------------------------------------------+\n";
    }

    // ---- DISPLAY: Tampilkan seluruh kendaraan dalam antrian ----
    void display() {
        if (isEmpty()) {
            cout << "\n  [!] Antrian kosong.\n";
            return;
        }
        cout << "\n  +---------+-------------+--------+-----------+-----------+\n";
        cout << "  | No.Urut | Plat        | Jenis  | Tiba      | Status    |\n";
        cout << "  +---------+-------------+--------+-----------+-----------+\n";
        for (int i = 0; i < ukuran; i++) {
            int idx = (front + i) % MAX_ANTRIAN;
            cout << "  | " << setw(7) << left << data[idx].nomorUrut
                 << " | " << setw(11) << left << data[idx].platNomor
                 << " | " << setw(6)  << left << data[idx].jenisKendaraan
                 << " | " << setw(9)  << left << data[idx].waktuTiba
                 << " | " << setw(9)  << left << data[idx].status
                 << " |\n";
        }
        cout << "  +---------+-------------+--------+-----------+-----------+\n";
        cout << "  Jumlah antrian: " << ukuran << " kendaraan\n";
    }

    void infoAntrian(int slotTersisa) {
        cout << "\n  [i] Informasi Sistem Parkir:\n";
        cout << "      Kapasitas Antrian  : " << MAX_ANTRIAN << " kendaraan\n";
        cout << "      Antrian Sekarang   : " << ukuran << " kendaraan\n";
        cout << "      Kapasitas Lahan    : " << MAX_KAPASITAS << " slot\n";
        cout << "      Slot Tersisa       : " << slotTersisa << " slot\n";
        cout << "      Total Terdaftar    : " << counter << " kendaraan\n";
        string st = isEmpty() ? "KOSONG" : (isFull() ? "PENUH" : "AKTIF");
        cout << "      Status Antrian     : " << st << "\n";
    }
};

// ================================================================
//  UTILITAS
// ================================================================
void cetakHeader() {
    cout << "\n";
    cout << "  +==============================================+\n";
    cout << "  |     SISTEM ANTRIAN PARKIR KENDARAAN         |\n";
    cout << "  |     Queue Array (FIFO) - C++                |\n";
    cout << "  +==============================================+\n";
}

void cetakMenu() {
    cout << "\n";
    cout << "  +----------------------------------------------+\n";
    cout << "  |               MENU UTAMA                     |\n";
    cout << "  +----------------------------------------------+\n";
    cout << "  |  1. Kendaraan Masuk Antrian   (Enqueue)      |\n";
    cout << "  |  2. Proses Masuk Lahan Parkir (Dequeue)      |\n";
    cout << "  |  3. Lihat Kendaraan Terdepan  (Peek)         |\n";
    cout << "  |  4. Lihat Semua Antrian       (Display)      |\n";
    cout << "  |  5. Info Sistem Parkir                        |\n";
    cout << "  |  0. Keluar                                    |\n";
    cout << "  +----------------------------------------------+\n";
    cout << "  Pilihan Anda: ";
}

// Simulasi waktu sederhana
string simulasiWaktu() {
    static int jam = 7, menit = 55;
    menit += 7;
    if (menit >= 60) { menit -= 60; jam++; }
    string j = (jam   < 10 ? "0" : "") + to_string(jam);
    string m = (menit < 10 ? "0" : "") + to_string(menit);
    return j + ":" + m + " WIB";
}

// ================================================================
//  FUNGSI MAIN
// ================================================================
int main() {
    QueueAntrian antrian;
    int slotParkir = MAX_KAPASITAS;
    int pilihan;

    cetakHeader();
    cout << "\n  [*] Memuat data demo awal...\n";

    // Isi data awal
    antrian.enqueue("B 1234 ABC", "Mobil", "08:02 WIB");
    antrian.enqueue("D 5678 XYZ", "Motor", "08:09 WIB");
    antrian.enqueue("F 9999 QRS", "Mobil", "08:16 WIB");

    do {
        cetakMenu();
        cin >> pilihan;
        cin.ignore();

        switch (pilihan) {
            case 1: {
                string plat, jenis;
                int pil;
                cout << "\n  -- KENDARAAN MASUK ANTRIAN --\n";
                cout << "  Plat Nomor     : ";
                getline(cin, plat);
                cout << "  Jenis [1=Mobil / 2=Motor]: ";
                cin >> pil; cin.ignore();
                jenis = (pil == 1) ? "Mobil" : "Motor";
                antrian.enqueue(plat, jenis, simulasiWaktu());
                break;
            }
            case 2:
                antrian.dequeue(slotParkir);
                break;
            case 3:
                antrian.peek();
                break;
            case 4:
                antrian.display();
                break;
            case 5:
                antrian.infoAntrian(slotParkir);
                break;
            case 0:
                cout << "\n  Terima kasih. Sistem Parkir ditutup.\n\n";
                break;
            default:
                cout << "\n  [!] Pilihan tidak valid.\n";
        }
    } while (pilihan != 0);

    return 0;
}
