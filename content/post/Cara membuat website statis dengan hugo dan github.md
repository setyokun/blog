---
title: "Cara membuat website statis dengan hugo dan github"
date: 2019-07-10T06:12:35+07:00
draft: false
---


1 . Download dan Install Hugo versi terbaru disini [Hugo Release.](https://github.com/gohugoio/hugo/releases)  
2 . Gunakan perintah `hugo new site <direktori>` untuk membuat site baru yang akan digenerate oleh hugo  
3 . Ketikkan `git init` untuk menambahkan git pada direktori yang udah digenerate oleh hugo tadi  
4 . Buat Repositori di github dengan nama `blog`  
5 . Tambahkan remote dengan perintah `git remote add origin <urlRepositoriBlog>` di direktori yang udah digenerate oleh hugo tadi  
6 . Tambahkan theme sesuai dengan keinginanmu, kamu bisa mencarinya disini [Hugo Themes](https://themes.gohugo.io/)  
7 . Pilih salah satu theme, kemudian clone dengan perintah `git clone <urlRepoTheme>` di folder *themes*  
8 . Jalankan perintah `hugo server -t <namaTheme>` untuk menjalankan website statis yang digenerate oleh hugo dan dapat diakses di [http://localhost:1313/](http://localhost:1313/)  
9 . Gunakan ctrl + C untuk menghentikan server hugo  
10 . Pastikan semua berjalan lancar, Kemudian Langsung lanjut dengan perinta `hugo` untuk mengenerate direktori public  
11 . Gunakan perintah `rm -rf <namaDirektori>` untuk menghapus direktori tersebut  
12 . Push semua file yang ada di repo lokal kita ke github dengan cara >> `git add .` >> `git commit -m "message"` >> `git push origin master`. Saat melakukan perintah `git push origin master` pertama kali pasti akan reject, karena di lokal tidak sama dengan yang ada di repo github kita, maka gunakan perintah `git push origin master --force`  
13 . Ketikkan perintah `git submodule add -b master <urlSite.github.io> public` untuk menambahkan/menanamkan repository baru pada repository inti  
14 . Push to submodule repo dengan cara >> `hugo` >> `cd public` >> `git add .` >> `git commit -m "your message"` >> `git push origin master`   
15 . Tunggu beberapa menit, kemudian buka github-pages yang kam buat tadi daaaaan TADAA, udah jadi deh :)  
16 . Agar lebih mudah untuk post content kamu perlu menambahkan `deploy.sh` (file confignya menyusul), dan cara penggunaanya adalah dengan cara `./deploy.sh "your message"`. simple kan :)  

Thanks :)