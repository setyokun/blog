---
title: "Docker - command"
date: 2019-07-04T16:08:02+07:00
draft: false
---
##**Glosarium Perintah Docker Container** 
- **from @youtube (programmer zaman now)** #pakboi

  *Resume by Setyokun's* 

 **`docker pull mongo:4.1`**
- Perintah untuk mengambil images dari docker hub (mongo itu nama imagesnya dan 4.1 itu versionnya)
---
**`docker images`**
- Perintah untuk menampilkan images yang sudah terinstall/ter-pull di local/pc kita
---
**`docker container ls`** 
- Perintah untuk melihat container yang sedang berjalan/running
---
**`docker container ls --all`**
- Perintah untuk melihat semua container yang sedang berjalan/running ataupun yang tidak berjalan/running
---
**`docker container create mongo:4.1`**
- Perintah untuk membuat container dari image mongo dengan version 4.1 (image tersebut bisa kita ubah sesuai dengan yang kita mau/dibutuhkan)
- Perintah diatas akan menghasilkan container dengan nama acak dan sulit diingat (ex:36596432jdsgskgds)
- Solusinya kita kasih nama agar mudah diingat dan diketikkan ulang
---
**`docker container create --name mongoserver1 mongo:4.1`**
- Perintah untuk membuat container dengan nama yang sudah diset
- mongoserver1 adalah nama container yang kita set
- --name adalah perintah untuk memberi nama container
---
**`docker container create --name mongoserver1 -p 8080:27071 mongo:4.1`**
- Perintah untuk membuat container dengan nama yang sudah diset dan port yang udah diset
- mongoserver1 adalah nama container yang kita set
- --name adalah perintah untuk memberi nama container
- -p adalah perintah untuk expose port keluar (8080 adalah port untuk expose keluar, 27021 adalah port internal dari docker yang dibuat)
- Port 8080 bisa diganti2 ya
---
**`docker container start mongoserver1`**
- Perintah untuk menjalankan/running container
- mongoserver adalah nama container yang kita buat tadi (bisa diubah sesuai nama docker yang udah dibuat nanti)
 --- 
**`docker container stop mongoserver1 mongoserver2`**
- Perintah untuk meng-stop/memberhentikan container yang sedang berjalan
- mongoserver1 dan mongoserver2 adalah nama container, jadi kita bisa meng-stop lebih dari 1 container sekaligus
---
**`docker container rm mongoserver1 mongoserver2`**
- Perintah untuk menghapus/delete container
- rm : remove
- mongoserver1 dan mongoserver2 adalah nama container, jadi kita bisa menghapus lebih dari 1 container sekaligus
- dengan dihapusnya container bukan berarti images juga terhapus, images masih ada (coba cek dengan : docker images)
---
 **`docker image rm mongo:4.1`**
- perintah untuk menghapus images
- mongo itu nama imagenya, 4.1 itu versi imagenya
- rm itu perintah remove
---
**`dockerfile (bukan syntax/perintah , tapi file)`**
- dockerfile itu adalah suatu file yang berisi perintah-perintah untuk membuild sebuah images, biasanya perintah2 tersebut ga jauh beda dengan perintah yang biasa di pakai di ubuntu/docker/node dll
---
**`docker build --tag appnode-sty:1.0 .`**
- docker build : perintah untuk membuat/membuild image 
- --tag : untuk memberi nama image beserta versinya
- (.) : untuk membuat image pada direktori tersebut/saat ini 
---
**`docker tag appnode-sty:1.0 setyokun/appnode-sty:1.0`**
- perintah untuk menambahkan image dengan nama yang berbeda
- appnode-sty:1.0 adalah nama image di lokal kita
- setyokun/appnode-sty:1.0 adalah nama image yang akan dibuat berdasarkan image lokal (appnode-sty:1.0) yang ditulis tadi , penulisan nama images ini berdasarkan aturan dari dockerhub
---
**`docker push setyokun/appnode-sty:1.0`**
- perintah untuk push/upload to dockerhub
---
**`docker login`**
- perintah untuk login ke dockerhub lewat terminal




**Lanjutkan !**