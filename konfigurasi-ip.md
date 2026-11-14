# Konfigurasi IP Address pada Debian 12

## 1. Pengertian IP Address

IP Address (Internet Protocol Address) adalah alamat berupa angka yang digunakan untuk mengidentifikasi perangkat dalam suatu jaringan komputer.

IP Address memungkinkan komputer atau server saling berkomunikasi melalui jaringan.

## 2. Tujuan Konfigurasi IP Address

- Memberikan alamat jaringan kepada server Debian.
- Menghubungkan server dengan jaringan lokal.
- Memungkinkan server berkomunikasi dengan perangkat lain.
- Mengatur alamat gateway untuk akses ke jaringan lain.

## 3. Jenis IP Address

### A. DHCP (Dynamic Host Configuration Protocol)

DHCP merupakan metode pemberian IP Address secara otomatis dari server DHCP atau router.

### B. Static IP Address

Static IP Address merupakan alamat IP yang ditentukan secara manual dan biasanya digunakan pada server agar alamatnya tetap.

## 4. Contoh Konfigurasi IP Address

Contoh informasi jaringan:

- IP Address: `192.168.1.10`
- Subnet Mask: `255.255.255.0`
- Gateway: `192.168.1.1`

Contoh konfigurasi menggunakan ifupdown pada Debian 12:

Buka file konfigurasi:

```bash
sudo nano /etc/network/interfaces
```

Contoh isi konfigurasi:

```text
auto enp0s3
iface enp0s3 inet static
    address 192.168.1.10/24
    gateway 192.168.1.1
```

Keterangan:
- `enp0s3`: nama interface jaringan.
- `address`: alamat IP server.
- `/24`: prefix jaringan.
- `gateway`: alamat router.

Terapkan konfigurasi:

```bash
sudo systemctl restart networking
```

Periksa alamat IP:

```bash
ip a
```

Periksa gateway:

```bash
ip route
```

**Catatan:** IP Address, gateway, dan nama interface di atas hanya contoh. Semuanya harus disesuaikan dengan jaringan yang digunakan. Konfigurasi ini berlaku jika sistem menggunakan ifupdown dan interface tersebut dikelola olehnya.

## 5. Kesimpulan

Konfigurasi IP Address merupakan salah satu tahap penting dalam pengaturan server Debian 12. Dengan IP Address yang benar, server dapat terhubung dan berkomunikasi dengan perangkat lain dalam jaringan.
