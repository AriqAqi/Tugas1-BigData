# Tugas1-BigData




Setelah melakukan Crawling data, kita bisa menyimpan hasil ke container yang sudah dibuat.

#### Install Docker
Sebelum itu kita dapat mengistall docker terlebih dahulu. Kalian dapat mengunduh Docker dari situs web resmi mereka: <a href="https://www.docker.com/products/docker-desktop/">Docker Website</a>
#### Pull MongoDB Image dari Docker Hub
Buka terminal atau command prompt dan jalankan perintah berikut untuk mengunduh gambar MongoDB dari Docker Hub:
```yaml
Docker pull 
```
#### Membuat Container MongoDB
Setelah unduhan selesai, kita dapat membuat container pada terminal atau command prompt dengan perintah berikut:
```yaml
docker container create --name mongoserver5 -p 8082:27017 mongo
```
Penjelasan perintah diatas:
- --name mongoserver5 : memberi nama kontainer 
- -p 8082:27017 : agar bisa diakses dengan port 8082 dan akan diforward requestnya ke port 27017
  
#### Verifikasi Kontainer Berjalan
Kita dapat memeriksa apakah kontainer MongoDB berjalan dengan baik menggunakan perintah:
```yaml
docker container ls
```
Ini akan menunjukkan daftar kontainer yang berjalan, pastikan kontainer MongoDB yang baru saja kita buat ada di sana

#### Mengakses Kontainer MongoDB
Kita dapat masuk ke kontainer MongoDB yang sudah dibuat dengan menggunakan perintah berikut:
```yaml
docker exec -it mongoserver5 bash
```

#### Mengkoneksikan kontainer dengan Studio 3t


  


