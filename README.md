# Jarkom-Modul-1-F12-2022

## Penyelesaian Soal Praktikum Modul 1 Jaringan Komputer

* Muhammad Andi Akbar Ramadhan (5025201264)
* Natya Madya Marciola	(5025201238)
* Neisa Hibatillah Alif	(5025201170)

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
