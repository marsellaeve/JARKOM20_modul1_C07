# JARKOM20_modul1_C07

Laporan Resmi Praktikum Modul 1 Jaringan Komputer 2020

Kelompok C07 (0099 &amp; 0157)

# Pembahasan Jawaban

### No 1 Sebutkan webserver yang digunakan pada "testing.mekanis.me"!

`http.host contains "testing.mekanis.me" lalu follow tcp stream`

![alt text](https://github.com/marsellaeve/JARKOM20_modul1_C07/blob/main/img/1.png)

### No 2 Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!

`File -> export object -> http ->filter->Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg`

`http contains Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg`

![alt text](https://github.com/marsellaeve/JARKOM20_modul1_C07/blob/main/img/2.png)

![alt text](https://github.com/marsellaeve/JARKOM20_modul1_C07/blob/main/img/2b.png)

### No 3 Cari username dan password ketika login di "ppid.dpr.go.id"!

`http.host contains "ppid.dpr.go.id" && http.request.method == POST`

![alt text](https://github.com/marsellaeve/JARKOM20_modul1_C07/blob/main/img/3.png)

### No 4 Temukan paket dari web-web yang menggunakan basic authentication method!

`Http.authbasic`

![alt text](https://github.com/marsellaeve/JARKOM20_modul1_C07/blob/main/img/4.png)

### No 5 Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!

`http.authbasic && http.host contains aku.pengen.pw`

![alt text](https://github.com/marsellaeve/JARKOM20_modul1_C07/blob/main/img/5a.png)

![alt text](https://github.com/marsellaeve/JARKOM20_modul1_C07/blob/main/img/5b.png)

### No 6 Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut).

`ftp-data.command=="STOR Answer.zip"`

![alt text](https://github.com/marsellaeve/JARKOM20_modul1_C07/blob/main/img/6a.png)

`ftp-data.command=="STOR zipkey.txt"`

![alt text](https://github.com/marsellaeve/JARKOM20_modul1_C07/blob/main/img/6b.png)

Isi "Open This.pdf":

![alt text](https://github.com/marsellaeve/JARKOM20_modul1_C07/blob/main/img/6c.png)

### No 7 Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut. Your Super Mega Ultra Rare Hint = nama pdf-nya "Yes.pdf"

`frame contains "Yes.pdf"`

![alt text](https://github.com/marsellaeve/JARKOM20_modul1_C07/blob/main/img/7a.png)

Isi Yes.pdf:

![alt text](https://github.com/marsellaeve/JARKOM20_modul1_C07/blob/main/img/7b.png)

### No 8 Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!

`ftp.request.command=="RETR"`

![alt text](https://github.com/marsellaeve/JARKOM20_modul1_C07/blob/main/img/8a.png)

Isi TCP Stream dari file Readme:

![alt text](https://github.com/marsellaeve/JARKOM20_modul1_C07/blob/main/img/8b.png)

Isi TCP Stream dari license.txt:

![alt text](https://github.com/marsellaeve/JARKOM20_modul1_C07/blob/main/img/8c.png)

Karena Follow -> TCP Stream melihatkan Microsoft FTP Service pada RETR Readme maka objek yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service adalah Readme

### No 9 Cari username dan password ketika login FTP pada localhost!

`ftp.request.command=="PASS"`

![alt text](https://github.com/marsellaeve/JARKOM20_modul1_C07/blob/main/img/9a.png)

`ftp.request.command=="USER"`

![alt text](https://github.com/marsellaeve/JARKOM20_modul1_C07/blob/main/img/9b.png)

### No 10 Cari file .pdf di wireshark lalu download dan buka file tersebut! clue: "25 50 44 46"

`frame contains "application/pdf"`

![alt text](https://github.com/marsellaeve/JARKOM20_modul1_C07/blob/main/img/10a.png)

Potongan isi dari file .pdf dengan hex code 25504446 sebagai berikut:

![alt text](https://github.com/marsellaeve/JARKOM20_modul1_C07/blob/main/img/10b.png)

### No 11 Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!

`port 21`

![alt text](https://github.com/marsellaeve/JARKOM20_modul1_C07/blob/main/img/11.png)

### No 12 Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!

`Src port 80`

![alt text](https://github.com/marsellaeve/JARKOM20_modul1_C07/blob/main/img/12.png)

### No 13 Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!

`dst port 443`

![alt text](https://github.com/marsellaeve/JARKOM20_modul1_C07/blob/main/img/13.png)

### No 14 Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

Ip addr: 192.168.0.9

![alt text](https://github.com/marsellaeve/JARKOM20_modul1_C07/blob/main/img/14a.png)

`Src net 192.168.0.9`

![alt text](https://github.com/marsellaeve/JARKOM20_modul1_C07/blob/main/img/14b.png)

### No 15 Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!

`dst "monta.if.its.ac.id"`

![alt text](https://github.com/marsellaeve/JARKOM20_modul1_C07/blob/main/img/15.png)


## Authors

Created by:

[Evelyn Tjitrodjojo 99](https://github.com/marsellaeve)

[Naufal Rafi Akbar Harahap 157](https://github.com/NaufalRafi-hub)
