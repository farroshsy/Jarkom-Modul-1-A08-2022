# Jarkom-Modul-1-A08-2022

| **No** | **Nama**                   | **NRP**    |
| ------ | -------------------------- | ---------- |
| 1      | Dhani Rizki A. C. T. P.    | 5025201226 |
| 2      | Khariza Azmi Alfajira H.   | 5025201044 |
| 3      | Farros Hilmi Syafei        | 5025201012 |


## **Nomor 1**
**Sebutkan web server yang digunakan pada "monta.if.its.ac.id"!** <br>
Mencari paket dengan filter http.host == monta.if.its.ac.id <br>
![alt text](https://github.com/farroshsy/Jarkom-Modul-1-A08-2022/blob/main/assets%20modul%201/No.1/1a.png) <br>

Klik kanan salah satu paket → follow → tcp stream <br>
Setelah itu muncul dialog box sebagai berikut, dan dapat dilihat bahwa server yang digunakan adalah nginx/1.10.3 <br>
![alt text](https://github.com/farroshsy/Jarkom-Modul-1-A08-2022/blob/main/assets%20modul%201/No.1/1b.png) <br>


## **Nomor 2**
**Ishaq sedang bingung mencari topik ta untuk semester ini , lalu ia datang ke website monta dan menemukan detail topik pada website “monta.if.its.ac.id” , judul TA apa yang dibuka oleh ishaq ?** <br>

Pertama kita cari tahu paket apa yang berisi data yang berkaitan dengan menggunakan (http.request.uri contains “detail”) atau “topik”, <br>
![alt text](https://github.com/farroshsy/Jarkom-Modul-1-A08-2022/blob/main/assets%20modul%201/No.2/2a.png) <br>
![alt text](https://github.com/farroshsy/Jarkom-Modul-1-A08-2022/blob/main/assets%20modul%201/No.2/2b.png) <br>

Jika kita follow http stream dari paket tersebut, kita dapat mencari sesuai uri yang ditinjau pada paket, <br>
![alt text](https://github.com/farroshsy/Jarkom-Modul-1-A08-2022/blob/main/assets%20modul%201/No.2/2c.png) <br>
![alt text](https://github.com/farroshsy/Jarkom-Modul-1-A08-2022/blob/main/assets%20modul%201/No.2/2d.png) <br>
Juga dapat kita lihat dalam file html [di sini](https://github.com/farroshsy/Jarkom-Modul-1-A08-2022/blob/main/194.html) <br>
Dan dapat dilihat bahwa judul TA yang sedang dibuka oleh ishaq adalah "Evaluasi unjuk kerja User Space Filesystem (FUSE)". <br>

## **Nomor 3**
**Filter sehingga wireshark hanya menampilkan paket yang menuju port 80!** <br>
Menggunakan display filter tcp.dstport == 80 || udp.dstport == 80 untuk menampilkan semua paket yang menuju port 80 <br>
![alt text](https://github.com/farroshsy/Jarkom-Modul-1-A08-2022/blob/main/assets%20modul%201/No.3/3.png) <br>

## **Nomor 4**
**Filter sehingga wireshark hanya mengambil paket yang berasal dari port 21!** <br>
Menggunakan display filter tcp.srccport == 21 || udp.srcport == 21 untuk menangkap semua paket yang berasal dari port 21 <br>
![alt text](https://github.com/farroshsy/Jarkom-Modul-1-A08-2022/blob/main/assets%20modul%201/No.4/4.png) <br>

## **Nomor 5**
**Filter sehingga wireshark hanya mengambil paket yang berasal dari port 443!** <br>
Menggunakan display filter tcp.srcport == 443 || udp.srcport == 443 untuk menangkap semua paket yang berasal dari port 443 <br>
![alt text](https://github.com/farroshsy/Jarkom-Modul-1-A08-2022/blob/main/assets%20modul%201/No.5/5.png) <br>


## **Nomor 6**
**Filter sehingga wireshark hanya menampilkan paket yang menuju ke lipi.go.id** <br>
Kita pertama harus mencari tahu ip dari lipi.go.id, untungnya ada packet http yang tertuju pada alamat ip lipi.go.id, <br>
![alt text](https://github.com/farroshsy/Jarkom-Modul-1-A08-2022/blob/main/assets%20modul%201/No.6/6a.png) <br>
Kemudian kita hanya perlu menggunakan ip pada destinasi paket sebelumnya pada ip.dst untuk mencari paket mana saja yang destinasinya tertuju pada alamat yang sama. <br>
![alt text](https://github.com/farroshsy/Jarkom-Modul-1-A08-2022/blob/main/assets%20modul%201/No.6/6b.png) <br>

## **Nomor 7**
**Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!** <br>
Mengecek IP address: <br>
Membuka command prompt, <br>
Mengetikkan perintah ipconfig, <br>
Lihat IP address pada perangkat(192.168.198.1). <br>
<br>Menggunakan filter capture src host, <br>
![alt text](https://github.com/farroshsy/Jarkom-Modul-1-A08-2022/blob/main/assets%20modul%201/No.7/7.png) <br>

## **Nomor 8**
**Telusuri aliran paket dalam file .pcap yang diberikan, cari informasi berguna berupa percakapan antara dua mahasiswa terkait tindakan kecurangan pada kegiatan praktikum. Percakapan tersebut dilaporkan menggunakan protokol jaringan dengan tingkat keandalan yang tinggi dalam pertukaran datanya sehingga kalian perlu menerapkan filter dengan protokol yang tersebut.** <br>
Di sini kami sedikit kebingungan apakah menggunakan filter ssh atau tcp, jika dengan filter ssh, kita dapat mengikuti ip lain untuk mendapatkan pesan yang tepat. tetapi dengan tcp.stream, kita dapat melihat paket, kemudian mengecek ulang pada flag push, <br>
![alt text](https://github.com/farroshsy/Jarkom-Modul-1-A08-2022/blob/main/assets%20modul%201/No.8/8a.png) <br>
![alt text](https://github.com/farroshsy/Jarkom-Modul-1-A08-2022/blob/main/assets%20modul%201/No.8/8b.png) <br>
Terdapat beberapa percakapan lanjutan dari percakapan di atas, tapi hanya membahas password sehingga tidak perlu ditampilkan juga. <br>

## **Nomor 9**
**Terdapat laporan adanya pertukaran file yang dilakukan oleh kedua mahasiswa dalam percakapan yang diperoleh, carilah file yang dimaksud! Untuk memudahkan laporan kepada atasan, beri nama file yang ditemukan dengan format [nama_kelompok].des3 dan simpan output file dengan nama “flag.txt”.** <br>
Berikut file salt yang ditemukan setelah mencari packet tcp yang berasal atau menuju port 9002, <br>
![alt text](https://github.com/farroshsy/Jarkom-Modul-1-A08-2022/blob/main/assets%20modul%201/No.9/9a.png) <br>
Setelah itu file tersebut kami simpan menggunakan opsi “Save as…” dengan nama A08.des3. Sayangnya setelah berulang kali usaha decryption menggunakan openssl dan dengan password “nakano”, semua hasilnya mengembalikan error bad decrypt dan file flag.txt yang berisi sampah, <br>
![alt text](https://github.com/farroshsy/Jarkom-Modul-1-A08-2022/blob/main/assets%20modul%201/No.9/9b.png) <br>
Ternyata proses decryption tersebut gagal karena file yang kita extract bukan paket byte murni, isi file tersebut telah dikonversi ke ASCII sehingga sebagian besar jumlah karakter dalam file dirubah paksa menjadi tanda titik. Kemudian kita menggunakan opsi File > Export Packet Bytes untuk mengekstrak ulang file tersebut dan berikut hasil decryption menggunakan openssl dengan password sebelumnya, <br>
![alt text](https://github.com/farroshsy/Jarkom-Modul-1-A08-2022/blob/main/assets%20modul%201/No.9/9c.png) <br>

## **Nomor 10**
**Temukan password rahasia (flag) dari organisasi bawah tanah yang disebutkan di atas!** <br>
Berikut flag yang kami temukan dari decryption openssl sebelumnya, <br>
![alt text](https://github.com/farroshsy/Jarkom-Modul-1-A08-2022/blob/main/assets%20modul%201/No.10/10.png) <br>

# **Kendala**

Terdapat beberapa kendala saat dilakukannya pengerjaan praktikum, antara lain sebagai berikut:
1. Terjadi kegagalan dalam proses decryption, dikarenakan file yang kita extract bukan paket byte murni, isi file tersebut telah dikonversi ke ASCII sehingga sebagian besar jumlah karakter dalam file dirubah paksa menjadi tanda titik.
