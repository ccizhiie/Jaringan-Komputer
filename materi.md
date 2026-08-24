# JARINGAN KOMPUTER

## Apa itu Jaringan Komputer?
Jarkom adalah interaksi antara beberapa perangkat (komputer, router, switch, dll) yang saling terhubung untuk berbagi dan bertukar data.

### CIDR (Classless Inter-Domain Routing)
cidr adalah bilangan untuk menandai jumlah bit yang digunakan untuk subnet mask. CIDR ditulis dalam format IP address diikuti dengan garis miring dan angka desimal yang menunjukkan jumlah bit yang digunakan untuk subnet mask. Contoh: 192.168.1.0/24 (CIDR 24 berarti subnet mask menggunakan 24 bit). jadi cuma ubah angka di belakang garis miring untuk menentukan jumlah bit yang digunakan untuk subnet mask. hal ini mencegah pemborosan alamat IP.
### Network dan Host Portions
1. Network portion adalah bagian dari alamat IP yang digunakan untuk mengidentifikasi jaringan tertentu.
dianalogikan seperti nomor perumahan.
2. Host portion adalah bagian dari alamat IP yang digunakan untuk mengidentifikasi host tertentu dalam jaringan tersebut. dianalogikan seperti nomor rumah(id unique di srtiap jaringan) bisa disimpulkan seperti ini:
``` Network portion + Host portion = Alamat IP. Contoh: 192.168.1.10/24
```
### IPV4 dan Subnet Mask
3. IPV4 adalah alamat IP yang terdiri dari 32 bit, dibagi menjadi 4 oktet (8 bit per oktet) dan ditulis dalam format desimal bertitik. Contoh: 192.168.1.1

4. Subnet mask adalah filter wajib yang mendampingi alamat IP untuk menentukan network portion dan host portion. Subnet mask juga terdiri dari 32 bit, dibagi menjadi 4 oktet (8 bit per oktet) dan ditulis dalam format desimal bertitik. Contoh: 255.255.255.0

### Prefix Length
Cara penulisan subnet mask yang jauh lebih ringkas. Menulis 255.255.255.0 memakan waktu; prefix length menyingkatnya menjadi /24 (menandakan ada 24 bit angka 1 pada deret biner).

### Penentuan Jaringan dengan Logika AND
Komputer tidak membaca desimal. Proses ini adalah kalkulasi matematis (operasi boolean AND) yang dilakukan router atau PC antara IP Address dan Subnet Mask untuk menemukan Network Address (titik nol dari sebuah jaringan).

### VLSM: Efisiensi Tingkat Lanjut
1. Subnetting: Pemecahan jaringan konvensional (Fixed Length). Asumsi dasarnya adalah membagi blok IP menjadi ukuran yang sama rata. Ini adalah logika yang rentan cacat karena memicu pemborosan besar jika sebuah ruangan hanya butuh 2 PC, tapi tetap diberi jatah 30 IP.

2. Skema Subnetting VLSM: Subnetting dari sebuah subnet. Ini adalah koreksi analitis terhadap skema dasar. VLSM memotong jaringan secara asimetris sesuai dengan porsi kebutuhan absolut setiap divisi, sehingga tidak ada host IP yang menganggur secara percuma.

3. Penetapan Topologi VLSM Address: Tahap eksekusi akhir. Mengalokasikan Network Address, Range IP valid, dan Broadcast Address hasil perhitungan perhitungan VLSM ke dalam peta fisik/logis (titik interface router, switch, dan PC) agar jaringan berfungsi tanpa tumpang tindih
