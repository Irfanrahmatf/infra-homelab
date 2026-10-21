# Infrastructure Home Lab

**Proyek pembelajaran mandiri | Oracle VirtualBox**

## Ringkasan

Home lab ini dibuat untuk praktik dasar administrasi infrastruktur IT menggunakan beberapa VM Windows dan Linux. Fokus latihan meliputi jaringan, administrasi server, berbagi file, keamanan dasar, serta pengelolaan pengguna melalui Active Directory.

## Lingkungan Lab

| Sistem | Peran | IP jaringan internal |
|---|---|---|
| Ubuntu Linux | Administrasi Linux dan file sharing | `192.168.50.10` |
| Windows 11 Pro | Client domain | `192.168.50.20` |
| Windows 10 Pro | Client domain | `192.168.50.30` |
| Windows Server 2025 | Domain Controller dan DNS Server | `192.168.50.40` |

VirtualBox menggunakan **Internal Network (`labnet`)** untuk komunikasi antarmesin. Adapter **NAT** digunakan saat diperlukan akses internet. Windows 11 juga digunakan dalam sebagian latihan konektivitas dan akses file.

## Praktik yang Dilakukan

- **Networking:** Mengatur IP statis, mengenali perbedaan NAT dan Internal Network, serta menguji koneksi menggunakan `ping`.
- **Linux Administration:** Menggunakan SSH, memeriksa status layanan dan log, serta mengelola permission file dan ACL.
- **File Sharing:** Mengonfigurasi Samba di Ubuntu dan menguji akses berbagi file dari Windows dengan hak akses berbeda.
- **Firewall:** Mengatur UFW untuk membatasi akses SSH dan Samba dari jaringan internal.
- **DNS dan DHCP:** Memeriksa konfigurasi DNS, resolusi nama, serta perbedaan alamat IP statis dan DHCP.
- **Backup dan Restore:** Membuat arsip backup, memulihkan file, dan memverifikasi integritasnya menggunakan perbandingan file dan SHA-256.
- **Windows Server dan Active Directory:** Menginstal AD DS dan DNS, membuat domain `corp.lab.test`, menggabungkan Windows 10 ke domain, serta membuat dan menggunakan akun domain untuk latihan login.

## Hasil Pengujian

- Komunikasi jaringan internal antar-VM berhasil diuji.
- Akses SSH dan Samba berhasil dipraktikkan.
- Pengaturan permission dan firewall berhasil diterapkan pada skenario lab.
- File backup berhasil dipulihkan dan diperiksa integritasnya.
- Layanan Active Directory dan DNS pada Windows Server berhasil diverifikasi.
- Windows 10 berhasil bergabung dengan domain `corp.lab.test`.

## Dokumentasi

- [Technical Notes](COMMAND.md)
- [Screenshots](./Screenshots/)
