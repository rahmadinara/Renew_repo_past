# Sistem Arsip Budaya Lokal
**Pemanfaatan Bash Script untuk Pengarsipan dan Perlindungan Data Budaya Lokal dengan Digital Signature di Sistem Operasi Linux**
Skrip bash ini berfungsi untuk mengelola arsip budaya lokal dengan fitur otentikasi pengguna, penambahan, verifikasi, dan penghapusan data budaya menggunakan *digital signature* berbasis algoritma DSA. Skrip ini menggunakan *Zenity* untuk antarmuka grafis dan *OpenSSL* untuk keamanan. Skrip ini hanya dapat dijalankan pada sistem operasi Linux berbasis Debian (seperti Ubuntu) yang memiliki *desktop environment* (non-headless).

Skrip ini dibuat untuk memenuhi tugas kelompok proyek mata kuliah **Sistem Operasi Jaringan** Semester 2, Departemen Teknik Elektro dan Informatika, Sekolah Vokasi, Universitas Gadjah Mada.

## Prosedur Penggunaan
1. Kloning branch `main` repositori ini ke komputer dengan sistem operasi berbasis Debian:
   ```bash
   git clone https://github.com/username/sistem-arsip-budaya.git --branch=main
   ```
2. Pindah *working directory* ke folder skrip:
   ```bash
   cd sistem-arsip-budaya
   ```
3. Tambahkan izin eksekusi file `arsip_budaya.sh`:
   ```bash
   chmod +x arsip_budaya.sh
   ```
4. Jalankan skrip dengan perintah:
   ```bash
   ./arsip_budaya.sh
   ```
   atau
   ```bash
   bash arsip_budaya.sh
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
- Sistem operasi Linux berbasis Debian (contoh: Ubuntu) dengan *desktop environment*.
- Dependensi:
  - `zenity`: Untuk antarmuka grafis.
  - `openssl`: Untuk pembuatan kunci DSA dan *digital signature*.
  - `sha256sum`: Untuk hashing password.
- Instal dependensi:
  ```bash
  sudo apt install zenity openssl
  ```

## Catatan
- File kunci (`private_key.pem`, `public_key.pem`) dan data sensitif (`akun.txt`) dibuat otomatis saat skrip pertama kali dijalankan.
- Lindungi file sensitif dari akses tidak sah.
- Contoh format data di `arsipbudaya.csv`:
  ```
  Tari Saman,Tarian tradisional dari Aceh,Aceh,Dibawakan dalam acara adat,Seni Tari
  ```
- Contoh *signature* di `signaturebudaya.txt`:
  ```
  MEUCIQDqN... (base64 digital signature)
  ```

## Kontributor
Skrip ini dibuat dengan kontribusi dari semua anggota kelompok dan bimbingan dosen pengampu mata kuliah **Sistem Operasi Jaringan** Semester Genap Tahun Ajaran 2024/2025.

### Anggota Kelompok:
1. [Rahma Dinara Safia Ardianti](mailto:rahmadinarasafiaardianti@mail.ugm.ac.id)
2. [Iqro Septendi](mailto:iqroseptendi@mail.ugm.ac.id)
3. [M. Farhan Wijayanto](mailto:mfarhanwijayanto@mail.ugm.ac.id)
4. [Muhammad Fayyadhh Muslih](mailto:muhammadfayyadhmuslih@mail.ugm.ac.id)
5. [Maria Oktaviani Tirta Kumala Dewi](mailto:mariaoktavianitirtakumaladewi@mail.ugm.ac.id)

