# **Tutorial Install EPrints pada Linux Mint**

1. `apt update && apt upgrade -y` *perintah ini berfungsi untuk menghapus versi lama dari paket yang diinstal atau yang dapat ditingkatkan pada sistem yang tidak lagi diperlukan saat melakukan peningkatan.*
2. `sudo apt-get install build-essential libarchive-tar-perl libwww-perl libxml-parser-perl libcrypt-ssleay-perl libapache2-mod-perl2 libdbd-mysql-perl mysql-server ` *Perintah ini berfungsi untuk mengunduh paket-paket yang dibutuhkan ke dalam sistem.*
3. `sudo tar -xzf '/home/user/Downloads/eprints-x.x.x.tar.gz'` *Perintah ini berfungsi untuk mengekstrak Versi terbaru eprints yang telah diunduh ke dalam direktori /opt.*
4. `cd /opt/eprints-x.x.x` *Perintah ini berfungsi untuk mengubah direktori ke folder EPrints yang telah diekstrak.*
5. `ls /opt`
6. `ls ~/Downloads`
7. `cd ~/Downloads tar -xzf eprints-x.x.x.tar.gz`
8. `cd ~Downloads`
9. `tar -xzf ~/Downloads/eprints-x.x.x.tar.gz -C ~/Downloads`
10. `ls ~/Downloads`
11. `sudo mv ~/Downloads/eprints-x.x.x /opt/`
12. `cd /opt/eprints-3.4.5`
13. `sudo ./configure` *Perintah ini berfungsi untuk menginstall EPrints>*
14. `sudo apt install libncurses-dev`
15. `apt install perl libselinux1 apache2 libapache2-mod-perl2 libxml-libxml-perl \`
16. `libunicode-string-perl libterm-readkey-perl libmime-lite-perl libmime-types-perl libdigest-sha-perl \` *Pada user root perintah ini berfungsi untuk menginstall dependencies yang dibutuhkan untuk EPrints.*
17. `sudo apt install libunicode-string-perl`
18. `sudo apt install libterm-readkey-perl`
19. `sudo apt install libmime-lite-perl`
20. `sudo apt install libdigest-sha-perl \`
21. `sudo apt install libdbd-mysql-perl libxml-parser-perl libxml2-dev libxml-twig-perl libarchive-any-perl libjson-perl`
22. `sudo apt install liblwp-protocol-https-perl libtext-unidecode-perl lynx wget ghostscript poppler-utils antiword elinks`
23. `sudo apt install texlive-base texlive-binaries psutils imagemagick adduser tar gzip unzip libsearch-xapian-perl`
24. `sudo apt install libtex-encode-perl libio-string-perl python3-html2text make libexpat1-dev libxslt1-dev`
25. `adduser eprints` *Perintah ini berfungsi untuk menambahkan user eprints.*
26. `sudo nano /etc/apache2/sites-available/eprints.conf` *Perintah ini berfungsi untuk mengkonfigurasi Apache web server untuk melayani Eprints.*
27. Masukkan configurasi berikut : `<VirtualHost *:80> ServerAdmin webmaster@your_domain.com DocumentRoot /opt/eprints-x.x.x/archives/ ServerName your_domain.com ServerAlias www.your_domain.com <Directory /opt/eprints-x.x.x/archives/> Options FollowSymLinks AllowOverride All Order allow,deny allow from all </Directory> ErrorLog ${APACHE_LOG_DIR}/error.log CustomLog ${APACHE_LOG_DIR}/access.log combined </VirtualHost>` *ubah `your_domain.com` dengan nama domain anda. Simpan file konfigurasi tersebut, lalu jalankan perintah selanjutnya.*
28. `sudo a2ensite eprints.conf`
29. `sudo systemctl restart apache2` *perintah ini berfungsi untuk memulai ulang web Apache sehingga dapat memakai perubahan yang diberikan.*
30. **Acces EPrints** menggunakan domain yang dimasukkan sebelumnya. 
