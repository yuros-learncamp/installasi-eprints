# **Tutorial Install EPrints pada Linux Mint**

1. `apt update && apt upgrade -y`
2. `sudo apt-get install build-essential libarchive-tar-perl libwww-perl libxml-parser-perl libcrypt-ssleay-perl libapache2-mod-perl2 libdbd-mysql-perl mysql-server `
3. `sudo tar -xzf '/home/user/Downloads/eprints-x.x.x.tar.gz'`
4. `cd /opt/eprints-x.x.x`
5. `ls /opt`
6. `ls ~/Downloads`
7. `cd ~/Downloads tar -xzf eprints-x.x.x.tar.gz`
8. `cd ~Downloads`
9. `tar -xzf ~/Downloads/eprints-x.x.x.tar.gz -C ~/Downloads`
10. `ls ~/Downloads`
11. `sudo mv ~/Downloads/eprints-x.x.x /opt/`
12. `cd /opt/eprints-3.4.5`
13. `sudo ./configure`
14. `sudo apt install libncurses-dev`
15. `apt install perl libselinux1 apache2 libapache2-mod-perl2 libxml-libxml-perl \`
16. `libunicode-string-perl libterm-readkey-perl libmime-lite-perl libmime-types-perl libdigest-sha-perl \`
17. `sudo apt install libunicode-string-perl`
18. `sudo apt install libterm-readkey-perl`
19. `sudo apt install libmime-lite-perl`
18. `sudo apt install libdigest-sha-perl \`
19. `sudo apt install libdbd-mysql-perl libxml-parser-perl libxml2-dev libxml-twig-perl libarchive-any-perl libjson-perl`
20. `sudo apt install liblwp-protocol-https-perl libtext-unidecode-perl lynx wget ghostscript poppler-utils antiword elinks`
21. `sudo apt install texlive-base texlive-binaries psutils imagemagick adduser tar gzip unzip libsearch-xapian-perl`
22. `sudo apt install libtex-encode-perl libio-string-perl python3-html2text make libexpat1-dev libxslt1-dev`
23. `adduser eprints`
