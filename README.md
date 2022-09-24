# Jarkom-Modul-1-F12-2022

## Penyelesaian Soal Praktikum Modul 1 Jaringan Komputer

* Muhammad Andi Akbar Ramadhan (5025201264)
* Natya Madya Marciola	(5025201238)
* Neisa Hibatillah Alif	(5025201170)

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

![image](https://user-images.githubusercontent.com/80830860/192078951-5a273eaf-ba22-4107-a4f5-71f8077a7008.png)

Source : https://stackoverflow.com/questions/71593315/how-do-i-extract-the-tcp-data-packet-from-wireshark

### Nomor 10
Dari output file yang didapat dari nomor 10 akan terdapat flag yang tertulis :
* JaRkOm2022{8uK4N_CtF_k0k_h3h3h3}

![image](https://user-images.githubusercontent.com/80830860/192079002-f9ae97e3-b296-4975-9b66-627d14452253.png)
