Tanggal: 7 Desember 2025
Topik: Networking 

---

## 🎯 Tujuan Belajar Hari Ini
- Memahami apa itu Enumeration, bisa membaca output dari nmap, mengetahui port mana yang berbahaya,
 dan bisa memiliki insting recon seperti seorang Pentester.

---

## 🧠 Teori Inti (Versi Singkat + Padat)
- Enumeration adalah proses pengumpulan informasi aktif secara mendalam terhadap service, sistem operasi, 
  user, dan resource yang berjalan pada target setelah tahap scanning, dengan tujuan untuk mengidentifikasi 
  potensi celah keamanan yang dapat dieksploitasi.
  Hal ini biasanya bertujuan untuk mengetahui informasi secara lengkap supaya nantinya kita bisa
  melakukan exploitasi secara ter arah dan tidak menembak di dalam kegelapan. `NMAP` disini
  berfungsi sebagai tools yang bisa menampilkan semua informasi yang bisa di ambil dari jaringan
  atau IP yang sebelumnya di scan, `NMAP` juga bisa melakukan script-based enumeration dengan NSE 
  (Nmap Scripting Engine) yang sudah masuk tahap semi-aktif eksploitasi ringan (bukan full exploit).

- Selai itu, tujuan dari enumeration adalah untuk mengetahui Port mana yang bisa kita jadikan sebagai
  sasaran exploitasi. Port disini kita asumsikan sebagai gerbang, yang dimana port ini bisa menjadi
  jalan keluar atau masuk nya suatu data melalui jaringan, dengan teknik enumeration kita dapat mengetahui
  apakah gerbang yang telah di temukan/dipetakan lemah atau terdapat celah yang dapat memberi kita jalan masuk.

---

## 🔧 Tools yang Digunakan
- `NMAP`
- OS : `Mint Linux`

---

## 🧪 Praktik / Lab
### 1. Setup
Langkah awal:
- OS : `Mint Linux`
- Jaringan : `WIFI`
- Tool : `NMAP`

### 2. Eksekusi
- `sudo nmap -sS 127.0.0.1`
- `ip route`
- `sudo nmap -sS -sV <IP_ROUTER>`

### 3. Hasil yang Didapat

- ![hasil comand : sudo nmap -sS 127.0.0.1](/images/sudo%20nmap%20-sS%20127.0.0.1.png)
  - Port 80 terbuka → kemungkinan web server

- ![hasil comand : ip route](/images/sstunlp-tools.png)

- ![hasil comand : sudo nmap -sS -sV <IP_ROUTER>](/images/sudo%20nmap.png)
  - Port 80 terbuka → kemungkinan web server

---

## ❗Error & Masalah yang Ditemui
- Selama praktik kali ini tidak ada eror atau kesulitan yanng aku temukan.

---

## 🔐 Security Insight (Wajib)
- NMAP tools secara teknis tidak digunakan untuk melakukan peretasan secara langsung,
  aka tetapi tools ini sangat berguna untuk kita bisa mendapatkan celah dari sebuah system
  pada jaringan terbua atau open port, denggan tools ini kita bisa mengetahui versi service
  yang digunakan oleh target, ya, kita bisa melakukan ini denggan comand `nmap -sV IP_TARGET`.
  Denggan mengetahui versi lengkap dari suatu service pada port yang terbuka di nmap kita dapat
  mencari CVE atau kerentanan yang telah ditemukan sebelumnya untuk melakukan exploitasi yang
  lebih ter arah dan profesional.

---

## 🧠 Catatan Pribadi
- Hariini aku belajar bahwa Firewall bukan jaminan keamanan mutlak. Banyak sistem memblokir 
  ICMP (ping) namun tetap membiarkan port database atau panel admin terbuka, yang berpotensi 
  menjadi entry point bagi attacker.
  Banyak server diluar sana yang memblokir ping akan tetapi lupa memfilter port Database.
  Dan dari materi hariini aku belajar pentingnya melakukan enumerasi atau mengenal target
  lebih dalam supaya exploitasi yang aku lakukan nantinya bisa ter arah dan tidak seperti
  membidik sasaran di tempat gelap.

  - Rencanaku selanjutnya adalah : Mempelajari `HTTP, Web Server, dan Dasar Web Exploitation`