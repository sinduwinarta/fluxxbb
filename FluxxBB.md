# Web Aplikasi "FluxBB"

[About](#sekilas-tentang) | [Instalasi](#instalasi) | [Konfigurasi](#konfigurasi) | [Otomatisasi](#otomatisasi) | [Cara Pemakaian](#cara-pemakaian) | [Pembahasan](#pembahasan) | [Referensi](#referensi)

## About

FluxBB adalah aplikasi forum open source gratis yang dirancang untuk menjadi cepat, ringan dan user friendly.Kode FluxBB ini, ditulis dalam PHP, memiliki rekam jejak yang terbukti stabilitas dan keamanan. FluxBB sedang aktif dikembangkan.

## Instalasi

#### Software Requirement

-Install Apache
```
	# instal SSH
        sudo apt update
        sudo apt install ssh
```
-Install MySQL, PHP
```
        # instal Apache, MySQL, PHP
        sudo apt install apache2
        sudo apt install mysql-server
        sudo apt install php
        sudo apt install libapache2-mod-php
        sudo apt install php-mysql
        sudo apt install php-gd php-mcrypt php-mbstring php-xml php-ssh2
        sudo service apache2 restart
```
-Instal SQLite3
```
        wget http://www.sqlite.org/sqlite-autoconf-3070603.tar.gz
        tar xvfz sqlite-autoconf-3070603.tar.gz
        cd sqlite-autoconf-3070603
        ./configure
        make
        make install
```

#### Server Requirement :

- Apache 2.4
- MySQL Server 4.1+
- PHP versi 4.4+
- SQLite 3.
- PHP versi 7.0.25


#### Cara instalasi
1. Membuat database dan user untuk Wordpress
    ```
    mysql -u root -p -v -e "
        CREATE DATABASE fluxbb;
        CREATE USER fluxbb IDENTIFIED BY 'password';
        GRANT ALL PRIVILEGES ON fluxbb.* TO fluxbb;"
    ```
    
2. Unduh arsip ZIP untuk instalasi 
``$ wget https://fluxbb.org/download/releases/1.5.10/fluxxbb-1.5.10.zip``

3. Unzip arsip yang sudah terunduh
``$ unzip fluxxbb-1.5.10.zip``

4. Setting permission access
``$ sudo chmod -R 755 /var/www``

5. Pindahkan direktori pagekit ke var/www/html/(direktori sekarang “pagekit”)
``$ sudo mv fluxbb-1.5.10 /var/www/html/``

6. Selanjutnya buka http://localhost (localhost -> alamat IP atau URL anda). 

## Konfigurasi (opsional)

Langkah-langkah untuk konfigurasi :

        - Pengaturan Database
        - Pengaturan Administrasi
        - Pengaturan Board 
        - Selesai! (Tampilan halaman admin)

## Otomatisasi
(**_tidak ada_**)


## Cara Pemakaian

User baru:

	1. Buka website : https://fluxbb.org/forums/register.php untuk registrasi pengguna baru
	2. Click “agree” untuk melanjutkan proses registrasi
	3. Isi formulir pada halaman yang muncul dengan sebenar benarnya dan click “register”. Pastikan kembali isi dari form yang sudah diisi adalah benar agar dapat menerima email konfirmasi dari pihak fluxbb
	4. Konfirmasi email address dan aktivasi akun melalui email address yang tertera pada form pendaftaran tadi
	5. Setelah aktivasi, silahkan setup password lalu login dengan username dan password yang telah dibuat.
	6. done

User lama:

	1. buka website https://fluxbb.org/forums/login.php untuk login
	2. Isi form dengan username dan password yang telah dibuat
	3. Done.
	
Cara membuat Post:

	1. Login ke website FluxBB
	2. Sukses, lalu klik ke forum diskusi terkait
	3. Scroll page ke bawah dan temukan “Post a new Topic”
	4. Masukkan “Subject” dengan judul post dan isikan “Message” dengan isi yang ingin didiskusikan
	5. Klik “Preview” jika ingin melihat kembali postingan barunya
	6. Jika sudah yakin, ketik “Submit”
	7. Done


## Pembahasan

- Pendapat tentang aplikasi web ini
	- Kelebihan:
		- Situs My FluxBB merupakan sebuah aplikasi berbasis web yang ringan sehingga tidak berat saat me-load halaman, diskusi yang dilakukan pada my FluxBB juga terhindar dari spam, hal ini dikarenakan salah satu peraturan My FluxBB dimana user hanya post selama 30 menit sekali.		
	- Kekurangan:
		- Tidak ada validasi email ketika mengisi form registrasi user
		- Untuk Register, hanya dapat dilakukan 1 jam sekali dengan IP yang sama
		- Post hanya dapat dilakukan 30 menit sekali
		

## Referensi

https://fluxbb.org/docs/v1.4/installing

https://www.thegeekstuff.com/2011/07/install-sqlite3/

https://pushpullfork.com/installing-a-known-blog-on-a-private-server/

https://github.com/fluxbb/fluxbb

