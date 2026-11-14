# Konfigurasi SSH pada Debian 12

## 1. Pengertian SSH

SSH (Secure Shell) adalah protokol jaringan yang digunakan untuk mengakses dan mengendalikan komputer atau server dari jarak jauh dengan aman melalui jaringan.

SSH menggunakan sistem enkripsi agar komunikasi antara komputer client dan server lebih terlindungi.

## 2. Fungsi SSH

Beberapa fungsi SSH, yaitu:

- Mengakses server dari jarak jauh.
- Mengelola server melalui terminal.
- Menjalankan perintah pada komputer lain.
- Mengirim dan memindahkan file secara aman.
- Melindungi komunikasi menggunakan enkripsi.

## 3. Instalasi SSH pada Debian 12

Untuk menggunakan SSH Server, Debian 12 memerlukan paket OpenSSH Server.

Perintah instalasi:

```bash
sudo apt update
sudo apt install openssh-server
```

## 4. Memeriksa Status SSH

Setelah instalasi selesai, periksa apakah layanan SSH sudah berjalan dengan perintah:

```bash
sudo systemctl status ssh
```

Jika layanan berjalan, status akan menunjukkan `active (running)`.

## 5. Mengaktifkan SSH

Untuk mengaktifkan layanan SSH secara otomatis ketika komputer dinyalakan, gunakan perintah:

```bash
sudo systemctl enable ssh
```

Untuk menjalankan layanan SSH:

```bash
sudo systemctl start ssh
```

## 6. Port SSH

SSH secara default menggunakan port:

```text
22
```

Port tersebut digunakan sebagai jalur komunikasi antara client dan server.

## 7. Contoh Koneksi SSH

Untuk mengakses server Debian 12 dari komputer lain, gunakan perintah:

```bash
ssh username@alamat-ip-server
```

Contoh:

```bash
ssh user@192.168.1.10
```

Alamat IP dan username di atas hanya contoh. Keduanya harus disesuaikan dengan konfigurasi server yang digunakan.

## 8. Kesimpulan

SSH merupakan layanan penting dalam administrasi server karena memungkinkan pengguna mengakses dan mengelola komputer dari jarak jauh secara aman. Dengan SSH, pengelolaan server Debian 12 dapat dilakukan melalui koneksi jaringan.
