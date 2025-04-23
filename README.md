# ROZ4NOM v1.0 - Cyber Toolkit by ANDIROZAS-SKD

**Stealth. Smart. Savage.**  
Tool serba bisa untuk pentesting & recon berbasis Python, dirancang untuk dijalankan dengan mudah di Termux (Android) maupun Linux.  

## Fitur Utama

ROZ4NOM mencakup berbagai modul penting untuk pengujian keamanan dan informasi intelijen:

| Fitur              | Deskripsi Singkat                                                                 |
|--------------------|-----------------------------------------------------------------------------------|
| `--port-scanner`   | Scan port terbuka dari domain/IP target                                           |
| `--subdomain-scan` | Mencari subdomain aktif menggunakan wordlist                                     |
| `--http-status`    | Mengecek status HTTP dari sebuah URL                                             |
| `--sql-inject`     | Melakukan deteksi dasar terhadap celah SQL Injection                             |
| `--xss-scan`       | Melakukan deteksi dasar terhadap XSS (Cross-site Scripting)                      |
| `--dns-lookup`     | Resolve DNS domain menjadi alamat IP                                             |
| `--whois`          | Mengambil data WHOIS dari sebuah domain                                          |
| `--geoip`          | Melihat lokasi geografis berdasarkan IP                                          |
| `--smtp-banner`    | Grab banner dari server SMTP                                                     |
| `--ftp-banner`     | Grab banner dari server FTP                                                      |
| `--ssl-cert`       | Menampilkan informasi sertifikat SSL dari domain                                 |
| `--traceroute`     | Melacak rute jaringan menuju target                                              |
| `--http-headers`   | Mengecek header keamanan dari HTTP response                                      |
| `--crawl`          | Melakukan crawling sederhana untuk menemukan URL/link dalam halaman              |

## Instalasi

### Di Termux (Android)

```bash
pkg update && pkg upgrade
pkg install python git
pip install requests dnspython
git clone https://github.com/andirozaS-SKD/roz4nom.git
cd roz4nom
python roz4nom.py --help
```

Di Linux (Debian/Ubuntu/Arch/etc.)

```bash
sudo apt update && sudo apt install python3 python3-pip git
pip3 install requests dnspython
git clone https://github.com/andirozaS-SKD/roz4nom.git
cd roz4nom
python3 roz4nom.py --help
```

## Contoh Penggunaan

python roz4nom.py --port-scanner example.com --port 443

python roz4nom.py --subdomain-scan example.com --wordlist wordlist.txt

python roz4nom.py --http-status http://target.com

python roz4nom.py --sql-inject http://target.com/page.php?id=1

python roz4nom.py --xss-scan http://target.com/search?q=

python roz4nom.py --dns-lookup example.com

python roz4nom.py --whois example.com

python roz4nom.py --geoip 8.8.8.8

python roz4nom.py --ssl-cert example.com

python roz4nom.py --crawl http://target.com

## Catatan

Semua fitur bekerja dengan baik di Termux & Linux.

Untuk fitur --subdomain-scan, kamu harus menyertakan file wordlist sendiri (.txt) berisi daftar subdomain.

Tool ini tidak menggunakan library berat dan ramah untuk device dengan resource rendah.


## Lisensi

Tool ini dibuat untuk edukasi dan pengujian keamanan secara etis.
Penggunaan untuk tujuan ilegal sepenuhnya menjadi tanggung jawab pengguna.
