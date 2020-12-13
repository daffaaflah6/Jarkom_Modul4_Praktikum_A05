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

![tabel-vlsm](https://user-images.githubusercontent.com/52326074/102013439-cbd97100-3d82-11eb-904a-b9e95396dca4.jpg)

Berdasarkan total IP dan netmask yang dibutuhkan, maka kita dapat menggunakan netmask /19 untuk memberikan pengalamatan IP pada subnet.

- Membuat pohon untuk perhitungan dan pembagian IP

![pembagian-pohon-vlsm](https://user-images.githubusercontent.com/52326074/102013437-c9771700-3d82-11eb-98bc-ccb3f941b62e.jpg)

- Topologi pada CPT

![topologi-cpt](https://user-images.githubusercontent.com/52326074/101975189-2f717a80-3c6d-11eb-9021-f9134ea7344c.jpg)

- Melakukan Testing

Untuk pembuktian bahwa routing dapat berjalan semestinya, maka kami melakukan `testing` sebagai berikut. 

```
ping dari KEDIRI ke JEMBER

ping dari BONDOWOSO ke MADIUN

ping dari KEDIRI ke PROBOLINGGO

ping dari BOJONEGORO ke TULUNGAGUNG

ping dari JOMBANG ke JEMBER

ping dari SAMPANG ke BANYUWANGI

ping dari LUMAJANG ke BONDOWOSO

ping dari NGANJUK ke LUMAJANG

ping dari SIDOARJO ke BOJONEGORO
```

![messageImage_1607866076158](https://user-images.githubusercontent.com/56763600/102013983-74410280-3d8e-11eb-8e54-dd8aa7572c9c.jpg)

![messageImage_1607866498616](https://user-images.githubusercontent.com/56763600/102013984-76a35c80-3d8e-11eb-93e4-a61259ab4945.jpg)

# CIDR (Menggunakan UML)
![cidr](https://user-images.githubusercontent.com/52326074/101973469-f3d5b100-3c6a-11eb-8054-f4a0db6b30b6.png)

- Pembagian IP dengan pohon berdasarkan penggabungan subnet yang telah dilakukan

![pembagian-pohon-cidr](https://user-images.githubusercontent.com/52326074/102002943-07991a00-3d34-11eb-8800-9a5074a110be.jpg)

- Pembagian IP server menggunakan IP DMZ adalah sebagai berikut

![pembagian-dmz](https://user-images.githubusercontent.com/52326074/102003916-3ddb9700-3d3e-11eb-9dad-268a53ce64f5.jpg)

- Pembagian IP dan penentuan broadcast address berdasarkan subnet dalam pembagian pohon

![tabel-cidr](https://user-images.githubusercontent.com/52326074/102012541-aac25180-3d7d-11eb-9a45-0a8bf3f7a13f.jpg)

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

Kita tidak perlu menambahkan default routing pada router di UML karena sudah ada. Sehingga kita hanya menambahkan routing pada router `SURABAYA`, `PASURUAN`, `BATU`, dan `KEDIRI` disimpan dalam sebuah file bash `route.sh` untuk ke empat UML

![route-SURABAYA](https://user-images.githubusercontent.com/52326074/102011390-4780f100-3d76-11eb-9395-811891484d1d.jpg)

![route-PASURUAN](https://user-images.githubusercontent.com/52326074/102011389-464fc400-3d76-11eb-8d7a-3bceca398c15.jpg)

![route-BATU](https://user-images.githubusercontent.com/52326074/102011392-48198780-3d76-11eb-92f6-7ae21be9df4d.jpg)

![route-KEDIRI](https://user-images.githubusercontent.com/52326074/102011393-48b21e00-3d76-11eb-9b65-257ed8ec95b5.jpg)

- Restart network dengan mengetikkan `service networking restart` pada setiap UML
- Pada semua router jalankan `iptables –t nat –A POSTROUTING –o eth0 –j MASQUERADE –s 192.168.0.0/16` agar UML dapat mengakses internet
- Karena di UML setiap ada restart, route akan hilang, maka menjalankan bash script pada UML, menggunakan perintah `source`, sehingga untuk menjalankan route.sh dengan perintah `source route.sh`
- Selanjutnya tes di setiap UML dengan menjalankan perintah `ping its.ac.id`

##### PING its.ac.id
- SURABAYA

![ping-SURABAYA](https://user-images.githubusercontent.com/52326074/102012089-fd4e3e80-3d7a-11eb-825c-dca1840b34dc.jpg)

- PASURUAN
- PROBOLINGGO
- BATU

![ping-BATU](https://user-images.githubusercontent.com/52326074/102012095-ff180200-3d7a-11eb-980a-69adf2b8fd7d.jpg)

- KEDIRI

![ping-KEDIRI](https://user-images.githubusercontent.com/52326074/102012092-fde6d500-3d7a-11eb-9d26-955c68ae2c99.jpg)

- BLITAR

![ping-BLITAR](https://user-images.githubusercontent.com/52326074/102012094-fe7f6b80-3d7a-11eb-8767-ec4eb023ec81.jpg)

- MADIUN

![ping-MADIUN](https://user-images.githubusercontent.com/52326074/102012093-fde6d500-3d7a-11eb-8e11-f01b6559a034.jpg)

- MALANG

![ping-MALANG](https://user-images.githubusercontent.com/52326074/102012096-ffb09880-3d7a-11eb-8500-d3d86d5436c0.jpg)

- MOJOKERTO
- SAMPANG

![ping-SAMPANG](https://user-images.githubusercontent.com/52326074/102012088-fcb5a800-3d7a-11eb-974f-ab77e0a1034f.jpg)

- BONDOWOSO
- JEMBER
- BANYUWANGI
- SIDOARJO
- LUMAJANG

![ping-LUMAJANG](https://user-images.githubusercontent.com/52326074/102012097-00492f00-3d7b-11eb-9056-5628e9b6b395.jpg)

- TULUNGAGUNG

![ping-TULUNGAGUNG](https://user-images.githubusercontent.com/52326074/102012086-fb847b00-3d7a-11eb-9f73-39a545d57040.jpg)

- NGANJUK

![ping-NGANJUK](https://user-images.githubusercontent.com/52326074/102012084-fa534e00-3d7a-11eb-94d9-5728ce365645.jpg)

- BOJONEGORO

![ping-BOJONEGORO](https://user-images.githubusercontent.com/52326074/102012083-f8898a80-3d7a-11eb-8f59-be18623d80d7.jpg)

- JOMBANG

![ping-JOMBANG](https://user-images.githubusercontent.com/52326074/102012087-fc1d1180-3d7a-11eb-8deb-434b103a1d38.jpg)

- Setelah itu, lakukan update pada setiap UML dengan mengetikkan `apt-get update`
- Terakhir, untuk mematikan UML JANGAN langsung di close. Ketikkan `halt` pada setiap UML untuk mematikannya. Alternatif lain adalah dengan membuat script dengan ekstensi .sh supaya mempermudah serta mempercepat kalian untuk mematikannya. Sebagai contoh buat file bernama `bye.sh` kemudian simpan script yang sudah dibuat kemudian jalankan dengan mengetikkan `bash bye.sh`

![halt-uml](https://user-images.githubusercontent.com/52326074/102012652-363be280-3d7e-11eb-90a0-ab8d638e32eb.jpg)
