# Sistem Arsip Budaya Lokal Berbasis Linux Bash Shell
**Perlindungan Arsip Digital Budaya Lokal Menggunakan Bash Shell Linux untuk Keamanan dan Pelestarian Warisan**
Skrip bash ini berfungsi untuk mengelola arsip budaya lokal dengan fitur otentikasi pengguna, verifikasi, penambahan, dan penghapusan data budaya menggunakan *digital signature* berbasis algoritma DSA. Skrip ini menggunakan *Zenity* untuk antarmuka grafis dan *OpenSSL* untuk keamanan. Skrip ini hanya dapat dijalankan pada sistem operasi Linux.

Skrip ini dibuat untuk memenuhi tugas kelompok proyek mata kuliah **Sistem Operasi Jaringan** Semester 2, Departemen Teknik Elektro dan Informatika, Sekolah Vokasi, Universitas Gadjah Mada di bawah pengawasan Dosen Pengampu **Ir. Yuris Mulya Saputra, S.T., M.Sc., Ph.D.**

## Prosedur Penggunaan
1. Install `zenity` dan `openssl`
   ```bash
   sudo apt-get install zenity openssl
   ```
2. Pindah *working directory* ke [folder]
   ```bash
   cd [folder]
   ```
3. Tambahkan izin eksekusi file `arsipbudaya.sh`:
   ```bash
   chmod +x arsipbudaya.sh
   ```
4. Jalankan skrip dengan perintah:
   ```bash
   ./arsipbudaya.sh
   ```

## Fitur Utama
- **Otentikasi Pengguna**: Pendaftaran dan login akun dengan hashing password menggunakan SHA-256.
- **Manajemen Arsip Budaya**: Menambah, menampilkan, dan menghapus data budaya (nama, deskripsi, daerah, sejarah, jenis).
- **Digital Signature (DSA)**: Setiap entri budaya ditandatangani dengan kunci DSA (1024-bit) dan disimpan dalam format *base64* di `signaturebudaya.txt`.
- **Verifikasi dan Keamanan**: Validasi *digital signature* untuk penghapusan data, memastikan integritas dan otentikasi.
- **Antarmuka Pengguna**: Menggunakan *Zenity* untuk input dan output grafis yang ramah pengguna.

## Struktur File
- `arsipbudaya.csv`: Menyimpan data budaya dalam format CSV (nama, deskripsi, daerah, sejarah, jenis).
- `signaturebudaya.txt`: Menyimpan *digital signature* untuk setiap entri budaya.
- `akun.txt`: Menyimpan username dan password yang di-hash (SHA-256).
- `private_key.pem`: Kunci privat DSA untuk menandatangani data.
- `public_key.pem`: Kunci publik DSA untuk verifikasi *signature*.

## Prasyarat
- Sistem operasi Linux *desktop environment*.
- Dependensi:
  - `zenity`: Untuk antarmuka grafis.
  - `openssl`: Untuk pembuatan kunci DSA dan *digital signature*.
  - `sha256sum`: Untuk hashing password.
- Instal dependensi:
  ```bash
  sudo apt-get install zenity openssl
  ```

## Kontributor
Skrip ini dibuat dengan kontribusi dari semua anggota kelompok dan bimbingan dosen pengampu mata kuliah **Sistem Operasi Jaringan** Semester Genap Tahun Ajaran 2024/2025.

### Anggota Kelompok:
1. [Rahma Dinara Safia Ardianti](mailto:rahmadinarasafiaardianti@mail.ugm.ac.id)
2. [Iqro Septendi](mailto:iqroseptendi@mail.ugm.ac.id)
3. [M. Farhan Wijayanto](mailto:mfarhanwijayanto@mail.ugm.ac.id)
4. [Muhammad Fayyadhh Muslih](mailto:muhammadfayyadhmuslih@mail.ugm.ac.id)
5. [Maria Oktaviani Tirta Kumala Dewi](mailto:mariaoktavianitirtakumaladewi@mail.ugm.ac.id)

