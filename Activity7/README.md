# 🏭 Activity 7: Simulasi Sistem Manufaktur Sederhana

Proyek ini merupakan implementasi tugas **Activity 7** dari mata kuliah Pemodelan dan Simulasi. Studi kasus ini berfokus pada pemodelan sistem manufaktur yang terdiri dari *conveyor* dan satu mesin pemrosesan untuk menganalisis metrik kinerja sistem.

**Perangkat Lunak yang Digunakan:**
* **JaamSim**: Digunakan untuk membangun dan menjalankan model simulasi kejadian diskrit.
* **Microsoft Excel**: Digunakan untuk mencatat dan menganalisis hasil output simulasi.

---

## 📝 Soal Tugas (Tasks)

Berikut adalah deskripsi masalah dan tugas yang harus diselesaikan sesuai dengan soal yang diberikan.

### Deskripsi Sistem
Sebuah sistem manufaktur kecil terdiri dari sebuah *conveyor* dan satu alat pemrosesan (mesin). Benda kerja mentah (*raw parts*) tiba di sistem, bergerak di sepanjang *conveyor*, diproses oleh satu mesin, dan kemudian dikirim keluar dari sistem.

**Data dan Asumsi:**
* **Pola Kedatangan Benda Kerja:** Deterministik, setiap **5 menit** sekali.
* **Waktu Tempuh Conveyor:** Deterministik, selama **1 menit**.
* **Waktu Proses Mesin:** Distribusi **Normal** dengan:
    * Rata-rata ($\mu$): **4 menit**
    * Standar Deviasi ($\sigma$): **1 menit**
* **Durasi Simulasi:** **12 jam**.
* **Aturan Sistem:**
    * Mesin hanya dapat memproses satu benda kerja pada satu waktu.
    * Jika mesin sedang sibuk, benda kerja yang tiba harus menunggu dalam antrian (*queue*) sebelum diproses.

### Tugas Pelaporan (Report Tasks)
Berdasarkan hasil simulasi selama 12 jam, laporkan metrik kinerja berikut:

1.  Rata-rata panjang antrian sebelum mesin (*average queue length*).
2.  Rata-rata waktu pemrosesan per benda kerja (*average processing time*).
3.  Jumlah benda kerja yang selesai diproses pada akhir simulasi (*number of parts completed*).

---

## 🛠️ Isi dan Implementasi Model

Repositori ini berisi file-file yang digunakan untuk memodelkan dan menyelesaikan tugas ini.

* **`Activity_7_Manufacturing.cfg`**:
    * Ini adalah file model utama yang dibuat menggunakan **JaamSim**.
    * Model ini berisi objek-objek simulasi seperti `EntityGenerator` (untuk kedatangan), `Server` (untuk *conveyor*), `EntityQueue` (untuk antrian mesin), dan `Server` (untuk mesin pemrosesan).
    * Semua parameter (waktu kedatangan, waktu tempuh, dan waktu proses) telah diatur sesuai spesifikasi soal.

* **`Hasil_Simulasi_Activity_7.xlsx`**:
    * File spreadsheet yang berisi rangkuman hasil output dari simulasi JaamSim.
    * File ini digunakan untuk menjawab tiga poin tugas pelaporan di atas.

---

## 📈 Hasil Simulasi (Results)

Setelah menjalankan model `Activity_7_Manufacturing.cfg` selama **12 jam (720 menit)**, berikut adalah metrik kinerja yang dilaporkan:

*(Catatan: Ganti angka di bawah ini dengan hasil aktual dari simulasi JaamSim Anda)*

1.  **Rata-rata Panjang Antrian (Average Queue Length):**
    * `Panjang antrian 0.02639048069 part dengan Rata-rata Waktu Tunggu 7.917144208 detik atau 0.1319524035 menit atau 0.002199206725 jam.`

2.  **Rata-rata Waktu Pemrosesan (Average Processing Time):**
    * `0.06450036123 jam atau 3.870021674 menit atau 232.2013004 detik`

3.  **Jumlah Benda Kerja Selesai (Parts Completed):**
    * `144 parts`
