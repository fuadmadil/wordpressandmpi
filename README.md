### Instalasi Apache dan WordPress di Ubuntu Server

#### Cara Install Apache

1. **Login ke Ubuntu Server**
   - ![Gambar: Login ke Ubuntu Server](https://github.com/fuadmadil/wordpressandmpi/assets/150570456/aa40d761-6dfe-411d-8ccc-9614c7d360ac)

2. **Install Apache dengan Sudo Apt Install apache2**
   - ![Gambar: Install Apache dengan Sudo Apt Install apache2](https://github.com/fuadmadil/wordpressandmpi/assets/150570456/aea81367-585d-4cc0-b722-5f9e6f7946cf)
   - *Di atas jika sudah terinstall Apache*

3. **Pastikan Apache Terpasang di Ubuntu**
   - Gunakan perintah `sudo ufw app list` untuk memeriksa instalasi Apache.
   - ![Gambar: Memastikan Apache Terpasang di Ubuntu](https://github.com/fuadmadil/wordpressandmpi/assets/150570456/d33f5d7e-9650-44a7-990a-38f0bc797159)

4. **Lihat IP Address yang Berjalan Saat Ini**
   - Gunakan perintah `ip a` untuk melihat alamat IP yang sedang berjalan saat ini.
   - ![Gambar: Melihat IP Address yang Berjalan Saat Ini](https://github.com/fuadmadil/wordpressandmpi/assets/150570456/4da8d909-f910-478d-b9f0-d118521dd3e8)

5. **Gunakan IP Utama untuk Login ke Server Apache**
   - Masukkan IP (contoh: 192.168.0.98) ke browser untuk login ke server Apache.
   - ![Gambar: Login ke Server Apache dengan IP Utama](https://github.com/fuadmadil/wordpressandmpi/assets/150570456/a0224e88-7fed-4c94-beb3-536225262492)

6. **Remote ke CMD dengan “ssh fuad@192.168.0.9”**
   - ![Gambar: Remote ke CMD dengan SSH](https://github.com/fuadmadil/wordpressandmpi/assets/150570456/e2919c25-32af-46e6-977b-b6eabed4c377)

7. **Remote ke PuTTY Config dengan IP Utama**
   - ![Gambar: Remote ke PuTTY Config dengan IP Utama](https://github.com/fuadmadil/wordpressandmpi/assets/150570456/d442fb3b-f963-4d67-9218-6ee87b9b0270)

8. **Login Kembali dengan Username dan Password**
   - ![Gambar: Login Kembali dengan Username dan Password](https://github.com/fuadmadil/wordpressandmpi/assets/150570456/3a4ce821-d50f-4ba9-bc7d-f740b209d8ce)

9. **Login ke Ubuntu Desktop dengan Cara yang Sama seperti PuTTY dan CMD**
   - ![Gambar: Login ke Ubuntu Desktop dengan Cara yang Sama](https://github.com/fuadmadil/wordpressandmpi/assets/150570456/6c7686cb-0197-4ea0-aa5c-d13115f9402c)

#### Install WordPress di Ubuntu Server

1. **Install MariaDB**
   - Gunakan perintah:
     ```bash
     sudo apt install mariadb-server mariadb-client
     ```
   - ![Gambar: Install MariaDB](https://github.com/fuadmadil/wordpress/assets/150570456/eadee46c-5fba-4424-b423-cca69075af3c)
   - *Jika sudah terinstal MariaDB*

2. **Install PHP**
   - Gunakan perintah:
     ```bash
     sudo apt install php php-mysql
     ```
   - ![Gambar: Install PHP](https://github.com/fuadmadil/wordpress/assets/150570456/b23bcd9a-5eae-4c2d-ae13-d539ee92792a)
   - *Jika sudah terinstal PHP*

3. **Check Instalasi PHP**
   - Buka browser dan periksa apakah PHP sudah terinstal dengan membuka:
     ```
     http://192.168.0.98/info.php
     ```
   - ![Gambar: Check Instalasi PHP](https://github.com/fuadmadil/wordpress/assets/150570456/33087ee2-1158-40a1-a5a1-d01b0ba7f4bc)

4. **Install PHP untuk Apache**
   - Gunakan perintah:
     ```bash
     sudo apt install php libapache2-mod-php php-mysql
     ```
   - ![Gambar: Install PHP untuk Apache](https://github.com/fuadmadil/wordpress/assets/150570456/ba1953f9-6613-49a2-8ffd-392d14b4a46c)
   - *Jika sudah diinstal*

5. **Buat Database WordPress**
   - Gunakan perintah:
     ```bash
     mysql -u root -p
     ```
   - ![Gambar: Buat Database](https://github.com/fuadmadil/wordpress/assets/150570456/4d69b64b-072b-4ec4-a633-787ed347bd1b)

6. **Buat Database**
   - ![Gambar: Buat Database](https://github.com/fuadmadil/wordpress/assets/150570456/136ffc2e-00c4-4dc9-a647-1a98874da6a5)

7. **Buat Pengguna Database**
   - ![Gambar: Buat Pengguna Database](https://github.com/fuadmadil/wordpress/assets/150570456/9f84c982-508c-468e-8f67-f10f3d4666c7)

8. **Install WordPress CMS**
   - Gunakan perintah:
     ```bash
     cd /tmp && wget https://wordpress.org/latest.tar.gz
     tar -xvf latest.tar.gz
     ```
   - ![Gambar: Install WordPress CMS](https://github.com/fuadmadil/wordpress/assets/150570456/bfb2e52d-d4b1-4af1-9758-ecbcccd25c60)
   - ![Gambar: Ekstraksi WordPress CMS](https://github.com/fuadmadil/wordpress/assets/150570456/e59f1d2f-e14d-4853-9437-9b391d99d4a1)

9. **Buat Direktori dapat Diakses**
   - ![Gambar: Buat Direktori dapat Diakses](https://github.com/fuadmadil/wordpress/assets/150570456/3f135aec-71c8-4320-8501-698fa03de9b3)

10. **Akses Browser dengan IP Utama dan /wordpress**
    - Buka browser dengan URL:
      ```
      http://192.168.0.98/wordpress
      ```
    - Ikuti langkah-langkah penginstalan dasar pada WordPress.
    - ![Gambar: Instalasi WordPress - Langkah 1](https://github.com/fuadmadil/wordpress/assets/150570456/dc2f8ca8-7c55-4914-9491-fb99dfd5bf18)
    - ![Gambar: Instalasi WordPress - Langkah 2](https://github.com/fuadmadil/wordpress/assets/150570456/86214e5a-174b-4f2b-8802-5bb135fb4979)
    - ![Gambar: Instalasi WordPress - Langkah 3](https://github.com/fuadmadil/wordpress/assets/150570456/4a58c25a-141b-4691-bdc7-c3601cb59126)
    - ![Gambar: Instalasi WordPress - Langkah 4](https://github.com/fuadmadil/wordpress/assets/150570456/2b86903d-a4d3-4bea-a7b1-257b5f44e4e0)

11. **Buka WordPress Setelah Proses Sign Up**
    - ![Gambar: Buka WordPress Setelah Proses Sign Up](https://github.com/fuadmadil/wordpress/assets/150570456/516164d3-100f-4acf-8adc-93c74ed98046)

12. **Upload WordPress - Gambar 1**
    - ![Gambar: Upload WordPress - Gambar 1](https://github.com/fuadmadil/wordpress/assets/150570456/c249407c-fb61-4ade-8321-29367e569755)

13. **Upload WordPress - Gambar 2**
    - ![Gambar: Upload WordPress - Gambar 2](https://github.com/fuadmadil/wordpress/assets/150570456/a2f8afab-7f6d-4ea1-a3bc-26c25f831ec3)

Dengan mengikuti langkah-langkah di atas, Anda dapat berhasil menginstal dan mengkonfigurasi Apache dan WordPress pada server Ubuntu.
