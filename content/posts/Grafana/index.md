---
title: "Grafana - OpenSource software untuk monitoring dan analisis data "

date: 2020-10-22T23:42:33+07:00
Author : "rot"
featuredImage: "graff.png"
lightgallery: true
draft: false
categories: ["FOSS"]
tags : ["foss", "Blog"]
---

 ## Apa itu Grafana ??? 
[**Grafana**](https://grafana.com/)  adalah sebuah software opensource yang membaca sebuah data matrics untuk dibuat menjadi sebuah grafik atau sebuah data tertulis.
  <!--more-->
 **Grafana** banyak sekali digunakan untuk melakukan analisis data dan monitoring. Grafana mendukung banyak storage backends yang berbeda untuk data time series (Source Data), seperti Prometheus,InfluxDB, Graphite,ElasticSearch,Google Big Query dan lain lain masih banyak lagi.
Setiap source data memiliki Query Editor tertentu yang disesuaikan untuk fitur dan kemampuan tertentu.
{{< image src_s="graf2.png" >}}

 Grafana telah menjadi teknologi paling populer di dunia yang digunakan untuk menyusun dashbor observabilitas dengan segala hal mulai dari metrik, log , data aplikasi dan lain-lain.






## Install & Run 


Jika teman teman tertarik ingin menggunakan grafana ,anda bisa mendownloadnya [disini](https://grafana.com/grafana/download) ,pilih sesaui OS yang digunakan.

atau denga

### Docker
Sebelum itu pastikan anda sudah menginstall docker terlebih dahulu. Jika sudah lalu masukkan command berikut untuk menjalankan grafana :
``` bash
docker run -d --name=grafana -p 3000:3000 grafana/grafana
``` 

###  Linux

 ##### Arch Linux

``` bash
 sudo pacman -S grafana
 ```

 ##### Debian/Ubuntu
 ```bash
 sudo apt-get install -y adduser libfontconfig1
wget https://dl.grafana.com/oss/release/grafana_7.3.0~beta2_amd64.deb
sudo dpkg -i grafana_7.3.0~beta2_amd64.deb
 ```
 
 ##### RHEL ,CentOs ,Fedora
``` bash
wget https://dl.grafana.com/oss/release/grafana-7.2.2-1.x86_64.rpm
sudo yum install grafana-7.2.2-1.x86_64.rpm
```
##### OpenSUSE dan SUSE
```bash
wget https://dl.grafana.com/oss/release/grafana-7.3.0~beta2-1.x86_64.rpm
sudo rpm -i --nodeps grafana-7.3.0~beta2-1.x86_64.rpm
```

### Dari Binnary file

Download latest .tar.gz [file](https://grafana.com/grafana/download?platform=linux) kemudian extract atau :
 ```bash
wget https://dl.grafana.com/oss/release/grafana-7.3.0-beta2.linux-amd64.tar.gz
tar -zxvf grafana-7.3.0-beta2.linux-amd64.tar.gz
``` 
Berikut contoh custom dashbord

{{< image src_s="graf1.png" >}}
