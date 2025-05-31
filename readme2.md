
# Sistem Arsip Budaya Lokal  
**Pemanfaatan Bash Script Berbasis GUI (Zenity) untuk Perlindungan dan Verifikasi Arsip Digital Budaya di Sistem Operasi Linux**

Skrip bash ini dirancang untuk membantu pengguna dalam **mengelola, memverifikasi, dan melindungi arsip budaya lokal secara digital** menggunakan antarmuka grafis **Zenity**. Fitur utamanya meliputi sistem login, manajemen arsip budaya, serta penerapan tanda tangan digital (**Digital Signature Algorithm/DSA**) untuk memastikan keaslian dan integritas data.

Skrip ini hanya dapat dijalankan pada sistem operasi **Linux berbasis Debian** (seperti Ubuntu) yang memiliki **desktop environment** karena menggunakan komponen GUI berbasis **Zenity**.

Skrip ini dikembangkan sebagai bagian dari proyek mini mata kuliah **Sistem Operasi Jaringan** semester 2.

## Prosedur Penggunaan

1. Kloning repositori ini (misalnya):
```bash
git clone https://github.com/namakamu/arsip-budaya.git --branch=main
```

2. Pindah ke direktori skrip:
```bash
cd arsip-budaya
```

3. Tambahkan izin eksekusi pada file utama:
```bash
chmod +x script.sh
```

4. Jalankan skrip:
```bash
./script.sh
```
atau
```bash
bash script.sh
```

## Fitur Utama
- Login dan registrasi akun dengan hashing SHA-256
- Penambahan, penghapusan, dan pembacaan data budaya lokal
- Pembuatan digital signature untuk tiap arsip budaya
- Verifikasi keaslian arsip berdasarkan tanda tangan digital
- Antarmuka grafis ramah pengguna menggunakan Zenity

## Ketergantungan
Pastikan sistem Anda telah terinstal:
- `bash`
- `zenity`
- `openssl`
- `sha256sum`

Install dengan:
```bash
sudo apt install zenity openssl
```

## Kontributor  
Skrip ini dikembangkan dengan kontribusi seluruh anggota kelompok proyek mini dan didampingi oleh dosen pengampu mata kuliah **Sistem Operasi Jaringan kelas BB Semester Genap Tahun Ajaran 2024/2025**:  
**Ir. Yuris Mulya Saputra, S.T., M.Sc., Ph.D.**

#### Anggota Kelompok:
1. [Nama Anggota 1](https://github.com/username1)
2. [Nama Anggota 2](https://github.com/username2)
3. [Nama Anggota 3](https://github.com/username3)
4. [Nama Anggota 4](https://github.com/username4)
5. [Nama Anggota 5](https://github.com/username5)
