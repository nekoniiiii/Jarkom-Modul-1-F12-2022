# Jarkom-Modul-1-F12-2022

## Penyelesaian Soal Praktikum Modul 1 Jaringan Komputer

* Muhammad Andi Akbar Ramadhan (5025201264)
* Natya Madya Marciola	(5025201238)
* Neisa Hibatillah Alif	(5025201170)

### Kendala pengerjaan?
* Terdapat keambiguan pada nomor 4 dan 5 mengenai perintah yang harus dilakukan sehingga pada laporan ini ditampilkan kedua cara.

### Nomor 1 (menggunakan soal1-2.pcapng)
Pertama, masukkan ```http.host == “monta.if.its.ac.id”``` pada display filter
![ss1](https://user-images.githubusercontent.com/91374949/192082566-dd62dd4f-65cd-4071-b03f-b0362064894c.jpg)
Kemudian, klik kanan pada salah satu paket lalu tekan ```Follow``` dan dilanjutkan dengan menekan ```TCP Stream``` sampai muncul seperti pada gambar
![ss2](https://user-images.githubusercontent.com/91374949/192082731-f8d4dd07-394f-4c43-add3-cf91913a8238.jpg)
Sehingga, diketahui bahwa web server yang digunakan adalah **nginx/1.10.3**.

### Nomor 2 
Sama seperti soal sebelumnya, pertama masukkan ```http.host == “monta.if.its.ac.id”``` pada display filter
![ss1](https://user-images.githubusercontent.com/91374949/192082566-dd62dd4f-65cd-4071-b03f-b0362064894c.jpg)
Kemudian cari kata kunci yang terdapat pada soal, yaitu **detail topik**. Pada salah satu paket terdapat info yang mengandung kata kunci pada soal, yaitu **detailTopik/194**. Lalu klik kanan pada salah satu paket lalu tekan ```Follow``` dan dilanjutkan dengan menekan ```HTTP Stream```<br>
![image](https://user-images.githubusercontent.com/91374949/192083183-05e350f7-199d-4a10-bad1-7b2660c90f17.png)
Selanjutnya, ketikkan **detailTopik/194**  pada bagian ```Find``` untuk mempermudah pencarian
![image](https://user-images.githubusercontent.com/91374949/192083220-3b4a2cd1-e541-409b-9ca8-9c31e7a93a36.png)
<br>Sehingga, akan ditemukan judul TA yang dibuka, yaitu **Evaluasi unjuk kerja User Space Filesystem**.


### Nomor 3
Untuk menampilkan paket yang hanya menuju port 80 bisa dilakukan dengan mengisi display filter dengan ```tcp.dstport == 80 || udp.dstport == 80```. Kemudian hasilnya akan muncul sebagai berikut.
![ss3](https://user-images.githubusercontent.com/91374949/192083386-36aeabd1-2c3b-4a1a-ae74-c963f759406e.jpg)


### Nomor 4
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 21!
#### Jawaban:
Karena perintah pada soal adalah "mengambil", maka perlu dilakukan perintah pada capture filter menggunakan ```src port 21```.<br>
![4 1](https://user-images.githubusercontent.com/72701806/192085176-2d2cc742-e784-4dfa-95d9-574f77d5df40.png)

#### Alternatif jawaban:
Karena telah diberikan file ```soal3-6.pcap```, maka asumsikan bahwa jawaban hanya bisa didapat dari file tersebut. Karena telah di-capture pada file, maka dilakukan perintah ```udp.srcport == 21 || tcp.srcport == 21``` pada display filter.<br>
![4 2](https://user-images.githubusercontent.com/72701806/192085187-3b6f2bd7-81ef-4df5-b1f8-13b1f415a7f5.jpg)


### Nomor 5
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 443!
#### Jawaban:
Karena perintah pada soal adalah "mengambil", maka perlu dilakukan perintah pada capture filter menggunakan ```src port 443```.<br>
![5 1](https://user-images.githubusercontent.com/72701806/192085194-eafce842-8954-4c2f-9e59-d16cba6db099.png)

#### Alternatif jawaban:
Sama seperti nomor sebelumnya, asumsikan bahwa jawaban hanya bisa didapat dari file tersebut. Karena telah di-capture pada file, maka dilakukan perintah ```udp.srcport == 443 || tcp.srcport == 443``` pada display filter.<br>
![5 2](https://user-images.githubusercontent.com/72701806/192085204-2071d9dd-6e95-4882-b6a3-2210bdb826e8.png)


### Nomor 6
Filter sehingga wireshark hanya menampilkan paket yang menuju ke lipi.go.id!
#### Jawaban:
Pertama, cari ip dari lipi.go.id pada cmd menggunakan ```ping lipi.go.id```.<br>
![6 1](https://user-images.githubusercontent.com/72701806/192085214-87ae95e3-08e6-44b4-bf31-3cd75a5c1be2.png)

Setelah ip address didapat, isi display filter dari file ```soal3-6.pcap``` dengan ```ip.dst == 203.160.128.158```.<br>
![6 2](https://user-images.githubusercontent.com/72701806/192085219-3333e819-8f76-4d40-a9bf-0f8ff1b8d400.png)


### Nomor 7
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
#### Jawaban:
Pertama, cari ip pada cmd menggunakan ```ipconfig```.<br>
![7 1](https://user-images.githubusercontent.com/72701806/192085499-4bb9d95e-3f3f-4eb5-bc24-9c8f3c90fc19.png)

Setelah ip address didapat, lakukan perintah ```src host 192.168.1.13``` pada capture filter.<br>
![7 2](https://user-images.githubusercontent.com/72701806/192085229-14f44073-2d8a-4a61-b0d5-06950a7b070b.png)

### Nomor 8 (menggunakan nomor8-10.pcapng)
Gunakan display filter dengan parameter berikut ini dan follow TCP stream yang berhubungan dengan percakapan yang ada.
* tcp.stream eq 12 (Percakapan pertama)
![image](https://user-images.githubusercontent.com/80830860/192101250-92804357-4880-4417-931e-06a7972c422c.png)


* tcp.stream eq 41 (Percakapan kedua)
![image](https://user-images.githubusercontent.com/80830860/192101266-ad5460a8-e9c9-427e-8414-5e3bcaaa4d76.png)


* tcp.stream eq 90 (Percakapan ketiga)
![image](https://user-images.githubusercontent.com/80830860/192101278-3ebc45f1-382f-4efd-84aa-823c01acaa0d.png)


### Nomor 9 (menggunakan nomor8-10.pcapng)
Pertama, isi display filter dengan parameter berikut
* tcp.port == 9002 || udp.port == 9002

Atau juga dapat menggunakan
* tcp.stream eq 29

Setelah itu, terdapat salah satu paket yang ter-capture yang jika di-follow TCP Stream-nya muncul sebagai berikut

![image](https://user-images.githubusercontent.com/80830860/192078698-82da0e6e-9d1e-426e-800c-8d1269e6cdf4.png)

Ganti "Show data as"-nya menjadi "Raw"

![image](https://user-images.githubusercontent.com/80830860/192078733-eaef8815-81c1-48bb-b0ba-6b37343d9e49.png)

Lakukan "Save as" dengan sesuai dengan format nama yang diinginkan

![image](https://user-images.githubusercontent.com/80830860/192078853-5900d126-7590-4f4c-b849-7e6a8f1bbb91.png)

Menggunakan wsl (di Windows, bila menggunakan Linux langsung bisa menggunaakn command window), masukkan command dibawah ini setelah cd ke folder tempat .des3 tadi berada
* openssl des3 -d -salt -in {isi ini dengan nama file}.des3 -out flag.txt -k nakano
* Menggunakan "-k nakano" yang berarti key-nya berupa nakano, didapatkan dari nomor 8 dimana salah satu percakapan menyinggung soal "anime kembar lima"
* Anime kembar 5 tersebut berjudul "Gotoubun no Hanayome" dimana marga dari kelima anak perempuan tersebut merupakan Nakano.


![image](https://user-images.githubusercontent.com/80830860/192078951-5a273eaf-ba22-4107-a4f5-71f8077a7008.png)

Source : https://stackoverflow.com/questions/71593315/how-do-i-extract-the-tcp-data-packet-from-wireshark


### Nomor 10
Dari output file yang didapat dari nomor 10 akan terdapat flag yang tertulis :
* JaRkOm2022{8uK4N_CtF_k0k_h3h3h3}

![image](https://user-images.githubusercontent.com/80830860/192079002-f9ae97e3-b296-4975-9b66-627d14452253.png)



