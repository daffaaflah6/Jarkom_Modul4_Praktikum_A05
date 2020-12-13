# Jarkom_Modul4_Praktikum_A05
- 05111840000030 MUHAMMMAD DAFFA’ AFLAH SYARIF
- 05111840000163 PUTU PUTRI NATIH DEVAYANTI

![Soal Shift Modul 4](https://user-images.githubusercontent.com/52326074/101480977-027c4980-3987-11eb-8719-54e8c565ee5c.png)

# Catatan
- Soal shift dikerjakan pada `Cisco Packet Tracer` dan `UML` menggunakan metode perhitungan CLASSLESS yang `berbeda`

Keterangan : Bila di `CPT menggunakan VLSM`, maka di `UML menggunakan CIDR` atau `sebaliknya`

- `CLOUD` diberikan IP TUNTAP
- `Server` diberikan IP DMZ
- Setiap UML memiliki memori 64MB
- Pembagian IP dan Routing se efisien mungkin
- Pastikan semua UML dapat melakukan ping ke its.ac.id

# Yang Perlu di Perhatikan !
### 1. Hasil perhitungan subnetting dan pohon pembagian IP serta file .pkt dikirim ke email asisten penguji (Daftar asisten penguji keluar hari Rabu, 9 Desember 2020 pukul 12.00 WIB)
### 2. File yang didemokan adalah file .pkt yang telah dikirim ke asisten
### 3. Maksimal menghubungi asisten untuk demo hari Kamis, 10 Desember 2020 pukul 20.00 WIB
### 4. Pengurangan nilai
- Melanggar salah satu dari tulisan diatas
- Hasil perhitungan untuk VLSM / CIDR, berbeda dengan di CPT / UML
- Pembagian IP kurang efisien
- Routing kurang efisien
- Tidak bisa menjelaskan cara perhitungan VLSM dan CIDR

# Selamat Mengerjakan :)

![tabel-subnetting](https://user-images.githubusercontent.com/52326074/101975317-3f3d8e80-3c6e-11eb-8a57-8f1d4b2b920b.jpg)

# VLSM (Menggunakan CPT)
![vlsm](https://user-images.githubusercontent.com/52326074/101973431-a48f8080-3c6a-11eb-80d6-961858b58d4a.jpg)

- Menentukan jumlah alamat IP yang dibutuhkan oleh tiap subnet dan melakukan labelling netmask berdasarkan jumlah IP yang dibutuhkan

![tabel-vlsm](https://user-images.githubusercontent.com/52326074/101973438-bbce6e00-3c6a-11eb-9007-563abb154619.jpg)

Berdasarkan total IP dan netmask yang dibutuhkan, maka kita dapat menggunakan netmask /19 untuk memberikan pengalamatan IP pada subnet.

- Membuat pohon untuk perhitungan dan pembagian IP

![pembagian-pohon-vlsm](https://user-images.githubusercontent.com/52326074/101973456-de608700-3c6a-11eb-8846-46c1c6dd514a.jpg)

- Pembagian IP server menggunakan IP DMZ adalah sebagai berikut

![pembagian-dmz](https://user-images.githubusercontent.com/52326074/102003916-3ddb9700-3d3e-11eb-9dad-268a53ce64f5.jpg)

- Topologi pada CPT

![topologi-cpt](https://user-images.githubusercontent.com/52326074/101975189-2f717a80-3c6d-11eb-9021-f9134ea7344c.jpg)

# CIDR (Menggunakana UML)
![cidr](https://user-images.githubusercontent.com/52326074/101973469-f3d5b100-3c6a-11eb-8054-f4a0db6b30b6.png)

- Pembagian IP dengan pohon berdasarkan penggabungan subnet yang telah dilakukan

![pembagian-pohon-cidr](https://user-images.githubusercontent.com/52326074/102002943-07991a00-3d34-11eb-8800-9a5074a110be.jpg)
