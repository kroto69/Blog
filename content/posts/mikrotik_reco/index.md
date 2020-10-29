---
title: "Recovery RouterOs yang lupa user dan password "
date: 2020-10-28T01:42:55+07:00
Author : "rot"
featuredImage: "gambar3.png"
lightgallery: true
draft: false
categories: ["Tips & Trick"]
tags : ["Tutorial", "Mikrotik"]
---


**Hallo teman teman -** Apa kabar?Kali ini saya akan berbagi sedikit pengalaman saya tentang bagaimana cara **merecovey** user atau password mikrotik **RouterOS** yang lupa dengan memanfaatkan file .backup


## Persyaratan
#### Yang perlu dipersiapkan
- Perangkat mikrotik
- File Backup
- Kopi & rokok buat penenang :

#### Dependensi
- Python3,  tapi bukan ular python yaa...
- Python Pip
- pycrypto

## How To
Pada case ini saya mempraktikanya menggunakan **Linux** , jika teman teman menggunakan **windows** mungkin caranya akan sedikit berbeda 

###### 1. Pertama,Clone repsository atau download dan ekstrak

``` bash
    git clone  https://github.com/BigNerd95/RouterOS-Backup-Tools.git && cd RouterOS-Backup-Tools
```

###### 2. Kalau sudah di clone / download repositorinya dan Install dependencsiya, langsung saja kita jalankan commandnya :


{{< admonition note "Note" >}}  
    - Sesuaikan (backupanmu.backup ) dengan nama hasil backupanmu dari mikrotik.
    -  sebelum jalankan commandnya Copy backupanmu ke directory RouterOS-Backup-Tools agar lebih mudah

{{< /admonition >}}

```bash
    python3 ROSbackup.py unpack -i backupanmu.backup -d unpack1
```

{{< image src="gambar1.png" caption= **contohnya**  >}}

###### 3. Kalau sudah , lanjutkan dengan command selanjutnya
```bash
python3 extract_user.py unpack1/user.dat

```
###### Taraaaa...
Berikut Hasilnya : 

{{< image src="gambar2.png"  caption=  **6.44.6** >}}

{{< image src="gambar3.png"  caption=  **6.45.7** >}}


{{< admonition note "Note" >}}  

 tidak semua versi RouterOS berhasil menampilkan user & password dengan lengkap.
jika sudah dijalankan tapi tidak menampilkan user & paswd, coba dengan cara ini

{{< /admonition >}}
```bash
strings folder-extrakanmu/user.dat
```


Selamat Mencoba dan Semoga berhasil :D


Share jika artikel ini bermanfaat untuk teman teman,kalau ada kesalahan mohon dikoreksi. Terima kasih :)

## Referensi

-  https://github.com/BigNerd95/RouterOS-Backup-Tools