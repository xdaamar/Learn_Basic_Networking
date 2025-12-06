Tanggal: 6 Desember 2025
Topik: Networking 

---

## 🎯 Tujuan Belajar Hari Ini
- Memahami bagaimana sebuah perangkat bisa berkomunikasi melalui internet dan dimana titik serangan bisa terjadi.

---

## 🧠 Teori Inti (Versi Singkat + Padat)
- IP kita analogikan sebagai alamat rumah, dan DNS bisa kita analogikan seperti sebuah penerjemah atau 
penunjuk arah yang bisa membantu kita sampai ke alamat tujuan. Ping disini kita analogikan seperti mengetuk
pintu rumah sebelum bertamu untuk memastikan di dalamnya apakah ada orang atau untuk tes seberapa cepat responsenya.

- IP Address adalah alamat logis dari sebuah perangkat (host) dalam jaringan. 
DNS berfungsi sebagai penerjemah nama domain menjadi IP Address agar manusia tidak perlu menghafal alamat numerik.
Ping digunakan untuk menguji apakah sebuah host aktif dan mengukur respon waktunya menggunakan protokol ICMP.

---

## 🔧 Tools yang Digunakan
- Tool 1               : Terminal/Shell
- OS / VM yang dipakai : Linux Mint

---

## 🧪 Praktik / Lab
### 1. Setup
Langkah awal:
- OS        : Linux Mint
- Jaringan  : Wifi
- Tool      : nslookup, shell, basic linux comand

### 2. Eksekusi
- nslookup nmap.org
- ip a
- ping 127.0.0.1

### 3. Hasil yang Didapat

- ❯ nslookup nmap.org
Server:		127.0.0.53
Address:	127.0.0.53#53

Non-authoritative answer:
Name:	nmap.org
Address: 50.116.1.184
Name:	nmap.org
Address: 2600:3c01:e000:3e6::6d4e:7061

- ❯ ip a
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host noprefixroute 
       valid_lft forever preferred_lft forever
2: wlp2s0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc noqueue state UP group default qlen 1000
    link/ether 04:68:74:9a:0a:d1 brd ff:ff:ff:ff:ff:ff
    inet 192.168.0.109/24 brd 192.168.0.255 scope global dynamic noprefixroute wlp2s0
       valid_lft 82474sec preferred_lft 82474sec
    inet6 fe80::f1ee:c965:e5bd:b32e/64 scope link noprefixroute 
       valid_lft forever preferred_lft forever

- ❯ ping 127.0.0.1
PING 127.0.0.1 (127.0.0.1) 56(84) bytes of data.
64 bytes from 127.0.0.1: icmp_seq=1 ttl=64 time=0.036 ms
64 bytes from 127.0.0.1: icmp_seq=2 ttl=64 time=0.061 ms

---

## ❗Error & Masalah yang Ditemui
- Error apa                    : Tidak ditemukan error selama praktik. Semua command berjalan normal.
- Penyebab menurut analisismu  : -


---

## ✅ Solusi
- Langkah perbaikan            : -
- Kenapa solusi ini berhasil   : -

---

## 🔐 Security Insight (Wajib)

Public IP pada router merupakan titik masuk utama dari internet. Jika router memiliki:
- Port terbuka yang tidak perlu
- Firmware yang tidak diperbarui
- Kredensial login default

Maka dapat dilakukan serangan seperti:
- Brute-force login router
- Exploit CVE pada firmware router
- DNS hijacking melalui akses admin router

Dampaknya:
- Seluruh jaringan lokal dapat dimonitor (Man-in-the-Middle)
- Pengalihan DNS ke situs phishing
- Penyadapan lalu lintas internal


---

## 🧠 Catatan Pribadi
- Bagian yang masih membingungkan : -
- Hal paling penting hari ini     : Aku belajar bagaimana cara aku bisa melihat suatu IP addres dari suat domain, 
                                    dan aku juga belajar bahwa Ping dapat digunakan untuk menguji konektivitas jaringan, 
                                    namun tidak dapat dijadikan indikator mutlak bahwa sebuah website aktif karena 
                                    ICMP bisa diblok oleh firewall.
- Rencana besok                   : belajar TCP vs UDP, Three Way Handshake, Port & Service.