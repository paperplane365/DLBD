# Build Debian DLBD using Jigdo Template and Jigsaw Tools
DLBD adalah singkatan dari Debian Live Bootable Disc. Ini adalah media instalasi Debian yang dapat di-boot dari CD, DVD, atau USB. DLBD memungkinkan pengguna untuk menginstal Debian pada komputer mereka tanpa perlu menggunakan CD atau DVD fisik. DLBD sendiri memungkinkan kita menggunakan Debian tanpa harus mengganti disc atau DVD untuk menginstall service yang akan kita gunakan.

Pada kesempatan kali kita akan lab mengenai cara download De.bian DLBD menggunakan jigdo.

Jigsaw download (Jigdo) adalah tools yang biasanya digunakan untuk mengunduh dan menyatukan file besar, seperti CD, DVD atau Blu-ray Disc, dari banyak file penyusun individu yang lebih kecil. File konstituen mungkin lokal dan/atau diambil dari satu atau lebih situs mirror.

Syarat-syarat mengikuti Lab Praktik

Sebelum memulai praktik ada beberapa hal yang harus di persiapkan diantarnya :
1.	OS Linux atau bisa juga WSL.
2.	Akses internet yang stabil.
3.	File dasar Debian-version-x-DLBD.Jigdo.
4.	Situs Miror/Repo Debian.

Tutorial menggunakan Jigdo untuk download Debian DLBD.

Berikut Langkah-langkah untuk memulai lab praktiknya :

## Langkah 1 : Install Jigdo-lite

Silahkan buka terminal masuk user root atau gunakan sudo command di user privilledge. Pastikan internet yang digunakan stabil dan tidak ada kendala.

Ketikan perintah
```
sudo apt-get update
```
lalu untuk install jigdo-lite
```
sudo apt-get install jigdo-lite -y
```

setelah selesai buat directory untuk menyimpan file Debian DLBD dan masuk ke directory yang telah dibuat. Pastikan penyimpanan dikrektory cukup untuk file ISO Debian DLBD. Untuk size Debian DLBD -+ 45 GB.

## Langkah 2 : File Debian DLBD dengan Ekstensi .Jigdo dan .Template
Buka browser dan cari situs yang menyediakan file Debian DLBD dengan ekstensi .jigdo, 

Komunitas Debian Langsung
```
https://cdimage.debian.org/debian-cd/current/amd64/jigdo-dlbd/
```

Miror Indonesia
```
https://ftp.unpad.ac.id/iso/debian/current/amd64/jigdo-dlbd/
```
 
(Opsional) Download file dengan ekstensi .jigdo dan untuk file dengan ekstensi .template.
Setelah selesai mendownload file tersebut pastikan file berada pada direktori dengan jumlah penyimpanan yang besar, karena untuk file iso DLBD sendiri akan menjadi sekitar 47-+ GB.

## Langkah 3 : Jigdo file download
Buka Kembali terminal ketikan perintah berikut untuk menjalankan tools jigdo.
```
Jigdo-lite
```

Setelah tools jigdo dijalankan jigdo akan meminta file dengan ekstensi .jigdo untuk menjalankan download. Jika kita download manual kita bisa memasukan nama filenya. jika belum, masukan url file jigdo yang terdapat pada web yang kalian pilih. Kita anggap kita belum mendownload filenya secara manual di web. Jadi kita akan download via jigdo.

Masukan url file downloadnya contoh :
```
https://ftp.unpad.ac.id/iso/debian/current/amd64/jigdo-dlbd/debian-12.2.0-amd64-DLBD-1.jigdo
```
lalu tekan enter dan jigdo akan mulai mendownloadnya.

Setelah itu jigdo akan meminta file yang telah di download untuk di scan, masukan nama filenya. Contoh :

debian-12.2.0-amd64-DLBD-1.jigdo
tekan enter maka file tersebut akan terscan dan jigdo akan mendownload file .template

setelah file .template terdownload, maka akan kembali kebagian scan file namun yang berbeda terdapat 1 list file yang tadi telah kita download dengan nama debian-12.2.0-amd64-DLBD-1.jigdo.  lalu tekan enter

setelah itu jigdo akan meminta Debian mirror url.
```
https://www.debian.org/mirror/list
```

silahkan pilih salah satu mirror Debian. Disini saya akan menggunakan mirror dari us. 
```
http://ftp.us.debian.org/debian/
```
lalu tekan enter dan jigdo akan mendownload semua package yang tersedia di mirror Debian dan dijadikan dalam satu file yang Bernama debian-12.2.0-amd64-DLBD-1.iso dengan menggunakan file .jigdo dan .template yang telah kita buat tadi.
Untuk proses download memakan waktu yang cukup lama tergantung dengan koneksi internet yang anda gunakan. Dari pengalaman saya sendiri menggunakan virtual machine dengan NAT memakan waktu sekitar 9 – 10 jam.

