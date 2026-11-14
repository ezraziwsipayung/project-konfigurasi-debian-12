# PROJECT KONFIGURASI DEBIAN 12

**Konfigurasi Server Dasar: IP Address, DNS, dan SSH**

## 1. Identitas Project

- Sistem Operasi: Debian 12 (Bookworm)
- Virtualisasi: VMware Workstation
- Jenis Jaringan: NAT
- Materi: Administrasi Server Linux

## 2. Tujuan Project

Project ini bertujuan mempelajari konfigurasi dasar server Linux menggunakan Debian 12, meliputi pengaturan jaringan, DNS, dan layanan SSH.

## 3. Tahapan Praktik

### A. Persiapan VMware
Mengatur Network Adapter VMware menggunakan mode NAT agar Debian dapat mengakses jaringan internet.

### B. Pemeriksaan IP Address
Menggunakan perintah:

```bash
ip a
```

### C. Pemeriksaan Gateway

```bash
ip route
```

### D. Pengujian Koneksi Internet

```bash
ping -c 4 8.8.8.8
```

### E. Pengujian DNS

```bash
ping -c 4 google.com
```

### F. Instalasi SSH Server

```bash
sudo apt update
sudo apt install openssh-server -y
```

### G. Mengaktifkan SSH

```bash
sudo systemctl enable --now ssh
```

### H. Memeriksa Status SSH

```bash
sudo systemctl status ssh
```

## 4. Dokumentasi Praktik

Screenshot hasil konfigurasi akan dimasukkan ke folder `images`.

1. Pengaturan Network Adapter VMware.
2. Hasil pemeriksaan IP Address.
3. Hasil pemeriksaan gateway.
4. Pengujian koneksi internet.
5. Pengujian DNS.
6. Status SSH Server.

## 5. Kesimpulan

Konfigurasi Debian 12 ini memberikan pemahaman dasar mengenai administrasi server Linux, khususnya pengaturan IP Address, DNS, dan SSH Server menggunakan VMware.

**Project ini dibuat sebagai dokumentasi pembelajaran administrasi jaringan dan server Linux.**
