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

- Topologi pada CPT

![topologi-cpt](https://user-images.githubusercontent.com/52326074/101975189-2f717a80-3c6d-11eb-9021-f9134ea7344c.jpg)

# CIDR (Menggunakana UML)
![cidr](https://user-images.githubusercontent.com/52326074/101973469-f3d5b100-3c6a-11eb-8054-f4a0db6b30b6.png)

- Pembagian IP dengan pohon berdasarkan penggabungan subnet yang telah dilakukan

![pembagian-pohon-cidr](https://user-images.githubusercontent.com/52326074/102002943-07991a00-3d34-11eb-8800-9a5074a110be.jpg)

- Pembagian IP server menggunakan IP DMZ adalah sebagai berikut

![pembagian-dmz](https://user-images.githubusercontent.com/52326074/102003916-3ddb9700-3d3e-11eb-9dad-268a53ce64f5.jpg)

### Topologi

![topologi-uml](https://user-images.githubusercontent.com/52326074/102011033-4949b500-3d74-11eb-8fb5-316bec1c66a0.jpg)

### Pengaturan UML

- Uncomment `net.ipv4.ip_forward=1` untuk setiap router
- Setting IP pada setiap UML dengan mengetikkan `nano /etc/network/interfaces`

##### ROUTER
- SURABAYA
![SURABAYA](https://user-images.githubusercontent.com/52326074/102011282-bdd12380-3d75-11eb-9c8b-66b50dba634a.jpg)

- PASURUAN
![PASURUAN](https://user-images.githubusercontent.com/52326074/102011278-bb6ec980-3d75-11eb-9416-ab6eb19b8be4.jpg)

- PROBOLINGGO
![PROBOLINGGO](https://user-images.githubusercontent.com/52326074/102011279-bc076000-3d75-11eb-9ea9-a42d14a96d55.jpg)

- BATU
![BATU](https://user-images.githubusercontent.com/52326074/102011264-b4e05200-3d75-11eb-950c-135ab8c6ca65.jpg)

- KEDIRI
![KEDIRI](https://user-images.githubusercontent.com/52326074/102011272-b873d900-3d75-11eb-9009-8e923d65d1bf.jpg)

- BLITAR
![BLITAR](https://user-images.githubusercontent.com/52326074/102011265-b6117f00-3d75-11eb-8c3e-702c96d2477d.jpg)

- MADIUN
![MADIUN](https://user-images.githubusercontent.com/52326074/102011274-b9a50600-3d75-11eb-97a6-8b7a3d0b6cbc.jpg)

##### SERVER
- MALANG
![MALANG](https://user-images.githubusercontent.com/52326074/102011275-b9a50600-3d75-11eb-804a-e4006acdb2b5.jpg)

- MOJOKERTO
![MOJOKERTO](https://user-images.githubusercontent.com/52326074/102011276-ba3d9c80-3d75-11eb-953e-9cff2e98af5c.jpg)

##### CLIENT
- SAMPANG
![SAMPANG](https://user-images.githubusercontent.com/52326074/102011280-bc9ff680-3d75-11eb-886c-458c640eba1e.jpg)

- BONDOWOSO
![BONDOWOSO](https://user-images.githubusercontent.com/52326074/102011268-b6aa1580-3d75-11eb-93bd-a8717dfb5f2d.jpg)

- JEMBER
![JEMBER](https://user-images.githubusercontent.com/52326074/102011270-b742ac00-3d75-11eb-9779-29050e2ee417.jpg)

- BANYUWANGI
![BANYUWANGI](https://user-images.githubusercontent.com/52326074/102011263-b3af2500-3d75-11eb-8c79-168fad67d2ee.jpg)

- SIDOARJO
![SIDOARJO](https://user-images.githubusercontent.com/52326074/102011281-bd388d00-3d75-11eb-9a99-f637b221fdfd.jpg)

- LUMAJANG
![LUMAJANG](https://user-images.githubusercontent.com/52326074/102011273-b90c6f80-3d75-11eb-9cbb-f2916e961aaf.jpg)

- TULUNGAGUNG
![TULUNGAGUNG](https://user-images.githubusercontent.com/52326074/102011262-b27df800-3d75-11eb-8f02-839f5cd05d15.jpg)

- NGANJUK
![NGANJUK](https://user-images.githubusercontent.com/52326074/102011277-bad63300-3d75-11eb-8092-99ff7f89aa82.jpg)

- BOJONEGORO
![BOJONEGORO](https://user-images.githubusercontent.com/52326074/102011266-b6117f00-3d75-11eb-8155-70e78e3260cc.jpg)

- JOMBANG
![JOMBANG](https://user-images.githubusercontent.com/52326074/102011271-b7db4280-3d75-11eb-8c51-edcad7ab4bb4.jpg)

##### ROUTING

Kita tidak perlu menambahkan default routing pada router di UML karena sudah ada. Sehingga kita hanya menambahkan routing pada router `SURABAYA`, `PASURUAN`, `BATU`, dan `KEDIRI`

![route-SURABAYA](https://user-images.githubusercontent.com/52326074/102011390-4780f100-3d76-11eb-9395-811891484d1d.jpg)
![route-PASURUAN](https://user-images.githubusercontent.com/52326074/102011389-464fc400-3d76-11eb-8d7a-3bceca398c15.jpg)
![route-BATU](https://user-images.githubusercontent.com/52326074/102011392-48198780-3d76-11eb-92f6-7ae21be9df4d.jpg)
![route-KEDIRI](https://user-images.githubusercontent.com/52326074/102011393-48b21e00-3d76-11eb-9b65-257ed8ec95b5.jpg)

- Restart network dengan mengetikkan `service networking restart` pada setiap UML
- Pada semua router jalankan `iptables –t nat –A POSTROUTING –o eth0 –j MASQUERADE –s 192.168.0.0/16`
