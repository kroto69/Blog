---
title: "Recovey RouterOs yang lupa user dan password "
date: 2020-09-06T01:42:55+07:00
draft: true
Author : "rot"
featuredImage: "shot.jpg"
lightgallery: true
draft: true
categories: ["Tips & Trick"]
tags : ["Tutorial", "Mikrotik"]
---


**Hallo teman teman -** Apa kabar?Kali ini saya akan berbagi sedikit pengalaman saya tentang bagaimana cara **merecovey** user atau password mikrotik **RouterOS** yang lupa menggunakan file .backup


## Persyaratan
### Yang perlu dipersiapkan
- Perangkat mikrotik
- File Backup
- Kopi & rokok buat penenang :

### Dependency
- Python,  terserah python2 atau python3 tapi bukan ular python yaa...
- Python Pip
- pycrypto

## How To
Pada case ini saya mempraktikanya menggunakan **Linux** , jika teman teman menggunakan **windows** mungkin caranya akan sedikit berbeda 

##### 1. Pertama,Clone repsository atau download dan ekstrak

``` zsh
    git clone  https://github.com/BigNerd95/RouterOS-Backup-Tools.git && cd RouterOS-Backup-Tools
```

##### 2. Kalau sudah di clone / download repositorynya dan Install dependencynya, langsung saja kita jalankan commandnya :


{{< admonition note "Note" >}}  
    - Sesuaikan (backupanmu.backup ) dengan nama hasil backupanmu dari mikrotik.
    -  sebelum jalankan commandnya Copy backupanmu ke directory RouterOS-Backup-Tools agar lebih mudah

{{< /admonition >}}

```zsh
    python ROSbackup.py unpack -i backupanmu.backup -d unpack1
```
Berikut contohnya
{{< image src="gambar1.png"  >}}

##### 3. Kalau sudah , lanjutkan dengan command selanjutnya
```zsh
python extract_user.py v-unpack1/user.dat

```
##### Taraaaa...
Berikut Hasilnya : 

{{< image src="gambar2.png"  caption=  **v.44.6** >}}

{{< image src="gambar3.png"  caption=  **v.45.7** >}}

 *note
 tidak semua versi RouterOS berhasil menampilkan user & password dg lengkap
jika sudah di enter tapi tidak menampilkan user & paswd coba dg cara ini

strings folder-extrakanmu/user.dat

