# Tugas1-BigData
# Scraping Data from News Articles and Converting to JSON
Panduan ini menjelaskan bagaimana cara mengambil data dari artikel berita menggunakan Python dan mengonversi informasi yang diekstraksi ke dalam format JSON. Menggunakan library seperti requests, BeautifulSoup, dan newspaper3k untuk melakukan web scraping, serta json untuk pemformatan JSON.

Persyaratan 
Pastikan  telah menginstal perpustakaan Python berikut:
1. requests
2. beautifulsoup4
3. newspaper3k
4. json

Langkah-Langkah
1. Mengambil Konten Halaman Web: Gunakan perpustakaan requests untuk mengambil konten dari URL artikel berita.
2. Mengurai Konten HTML: Manfaatkan BeautifulSoup untuk mengurai konten HTML halaman web.
3. Mengekstrak Judul, Penulis, dan Tanggal Publikasi: Buat objek Article menggunakan newspaper3k, unduh dan parse artikel tersebut, ekstrak judul, penulis, dan tanggal publikasi dari objek artikel.
4. Mengekstrak Konten Artikel: Dapatkan konten utama artikel dengan menggunakan objek artikel.
5. Membuat Representasi JSON: Bangun kamus Python yang berisi data yang telah diekstrak, termasuk judul, penulis, tanggal publikasi, dan konten.
6. Mengonversi ke Format JSON: Gunakan fungsi json.dumps untuk mengonversi kamus Python menjadi string JSON.
7. Mencetak Data JSON: Cetak data JSON yang berisi informasi yang telah diekstrak

Penggunaan
Jalankan skrip Python untuk mengambil data dari artikel berita tertentu.
Hasilnya akan berupa string JSON yang berisi informasi yang telah diekstrak, termasuk judul, penulis, tanggal publikasi, dan konten.

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

#### Mengkoneksikan kontainer dengan  aplikasi Studio 3t
Kita akan membuat koneksi baru

![image](https://github.com/AriqAqi/Tugas1-BigData/assets/115605338/d029c267-bf22-46aa-b7db-472ffd701866)



Kita dapat mengisi server dengan localhost dan portnya 8082

![image](https://github.com/AriqAqi/Tugas1-BigData/assets/115605338/8c2b9d8e-6134-47e0-a150-dbdbae6693e2)


#### Import hasil crawling data kedalam kontainer
Setelah kita mengkoneksikannya, kita akan mengiputkan data json kedalam kontainernya

![image](https://github.com/AriqAqi/Tugas1-BigData/assets/115605338/c1f17c3a-b33b-4ea4-8a47-3eb363ff81ed)

Kita dapat mengisi target connection, target Database dan target collection. berikutnya kita akan klik run dan file json sudah masuk kedalam kontainernya




  


