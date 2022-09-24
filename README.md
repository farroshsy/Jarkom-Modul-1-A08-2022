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
Dan dapat dilihat bahwa judul TA yang sedang dibuka oleh ishaq adalah “Evaluasi unjuk kerja User Space Filesystem FUSE1 <br>

## **Nomor 3**
**Filter sehingga wireshark hanya menampilkan paket yang menuju port 80!** <br>
Menggunakan display filter tcp.dstport == 80 || udp.dstport == 80 untuk menampilkan semua paket yang menuju port 80 <br>
![alt text](https://github.com/farroshsy/Jarkom-Modul-1-A08-2022/blob/main/assets%20modul%201/No.3/3.png) <br>

## **Nomor 4**

## **Nomor 5**

## **Nomor 6**

## **Nomor 7**

## **Nomor 8**
**Telusuri aliran paket dalam file .pcap yang diberikan, cari informasi berguna berupa percakapan antara dua mahasiswa terkait tindakan kecurangan pada kegiatan praktikum. Percakapan tersebut dilaporkan menggunakan protokol jaringan dengan tingkat keandalan yang tinggi dalam pertukaran datanya sehingga kalian perlu menerapkan filter dengan protokol yang tersebut.**


## **Nomor 9**
**Terdapat laporan adanya pertukaran file yang dilakukan oleh kedua mahasiswa dalam percakapan yang diperoleh, carilah file yang dimaksud! Untuk memudahkan laporan kepada atasan, beri nama file yang ditemukan dengan format [nama_kelompok].des3 dan simpan output file dengan nama “flag.txt”.**


## **Nomor 10**
**Temukan password rahasia (flag) dari organisasi bawah tanah yang disebutkan di atas!**


# **Kendala**

Terdapat beberapa kendala saat dilakukannya pengerjaan praktikum, antara lain sebagai berikut:
1. Terjadi kegagalan dalam proses decryption, dikarenakan file yang kita extract bukan paket byte murni, isi file tersebut telah dikonversi ke ASCII sehingga sebagian besar jumlah karakter dalam file dirubah paksa menjadi tanda titik.







	
