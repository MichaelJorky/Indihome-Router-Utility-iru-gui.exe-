# Indihome Router Utility

> **Peringatan:** :red_circle: Alat ini dibuat khusus untuk keperluan pendidikan dan penelitian. Penulis tidak bertanggung jawab atas segala bentuk penyalahgunaan atau kerusakan yang mungkin timbul dari penggunaan skrip ini. Harap gunakan dengan bijak dan hanya di lingkungan di mana Anda memiliki izin eksplisit.

Indihome Router Utility adalah alat Decoder dan Encoder config pada router seperti zte, huawei, tp-link, d-link, tenda, fiberhome dll dan alat ini baru disempurnakan untuk router zte, dengan alat ini Anda tidak perlu bersusah payah untuk mencari seputar isi konfigurasi pada router Indihome di rumah Anda.

#
Fitur yang ada pada Aplikasi Indihome Router Utility.exe 
- Decoder & Decryption Tools
- Encoder & Encryption Tools
- Decoder Generator
- Encoder Generator
- Router ADC (Auto Download Configuration)
- Ping & Trace Route
- Open Port Checker
- FTP Utility
- Telnet Utility
- SSH Utility
- Grab Proxy List Server
- Mac Address Generator
- Hash Type Identifier
- MD5 Password Generator
- HTTP Header Checker
- Compare Text Utility

~ (v1.0.0.1) Sabtu 6 April 2024 - First Release Decoder Utility

~ (v1.0.0.2) Senin 8 April 2024 - Penambahan fitur Router ADC (Auto Download Configuration)

~ (v1.0.0.3) Selasa 9 April 2024 - Penambahan fitur Mac Address Generator

~ (v1.0.0.4) Selasa 9 April 2024 - Penambahan fitur MD5 Password Generator

~ (v1.0.0.5) Rabu 10 April 2024 - Penambahan fitur Grab Proxy List Server

~ (v1.0.0.6) Rabu 10 April 2024 - Penambahan fitur HTTP Header Checker

~ (v1.0.0.7) Rabu 10 April 2024 - Penambahan fitur Telnet Utility

~ (v1.0.0.8) Rabu 10 April 2024 - Penambahan fitur Multi Open Port Checker

~ (v1.0.0.9) Kamis 11 April 2024 - Penambahan fitur Decoder Generator

~ (v1.0.1.0) Kamis 11 April 2024 - Penambahan fitur Encoder Generator

~ (v1.0.1.1) Sabtu 13 April 2024 - Penambahan fitur Encoder Utility

~ (v1.0.1.2) Sabtu 13 April 2024 - Penambahan fitur Ping Tracert Utility

~ (v1.0.1.3) Sabtu 20 April 2024 - Perbaikan fitur Auto Save Configuration

~ (v1.0.1.4) Senin 22 April 2024 - Penambahan fitur Compare Text Utility

~ (v1.0.1.5) Senin 16 Desember 2024 - Perbaikan Bug API Windows
#
<b>Panduan Cara Penggunaan:</b>
1. Pastikan sebelumnya sudah menginstal "Indihome Decoder Utility" yang pernah dibahas disini https://github.com/MichaelJorky/indihome-router-decoder
2. Download "Indihome Router Utility" caranya arahkan cursor pada bagian "code" pada "local" pilih "download zip".
3. Lalu ekstrak filenya kemudian copy isi file yang ada didalam folder "Indihome-Router-Utility-main" lalu pastekan pada folder ```.zte-decoder``` (point 1).
4. Untuk default script decodingnya maupun encodingnya menggunakan script seperti yang sudah dibahas pada (point 1) atau seperti yang tercantum dibawah ini:

<b>Default Decoder List (12 List):</b>
```
decoder1.py config/config.bin config/config.xml
decoder2.py config/config.bin config/config.xml
decoder3.py config/config.bin config/config.xml
decoder1.py --model "F670L" config/config.bin config/config.xml
decoder2.py --model "F670L" config/config.bin config/config.xml
decoder3.py --model "F670L" config/config.bin config/config.xml
decoder1.py --serial ZTE123456789 config/config.bin config/config.xml
decoder2.py --serial ZTE123456789 config/config.bin config/config.xml
decoder3.py --serial ZTE123456789 config/config.bin config/config.xml
decoder1.py --mac AA:BB:CC:DD:EE:FF --serial ZTE123456789 config/config.bin config/config.xml
decoder2.py --mac AA:BB:CC:DD:EE:FF --serial ZTE123456789 config/config.bin config/config.xml
decoder3.py --mac AA:BB:CC:DD:EE:FF --serial ZTE123456789 config/config.bin config/config.xml
```
<b>Default Encoder List (6 List):</b>
```
encoder1.py --key 'isi_key' --signature 'F670L' --include-header config/config.xml config/new.config.bin
encoder1.py --key 'isi_key' --signature 'F670L' --version 1 --include-header config/config.xml config/new.config.bin
encoder1.py --signature F670L --payload-type 6 config/config.xml config/new.config.bin 
encoder1.py --model "F670L" config/config.xml config/new.config.bin
encoder1.py --serial ZTE123456789 --signature 'F670L' config/config.xml config/new.config.bin
encoder1.py --signature 'F670L' --use-signature-encryption config/config.xml config/new.config.bin
```
5. Untuk decoding support penggunaan perintah seperti contoh yang tercantum dibawah ini:
```
--key 2bf3525fd2dcc7fe
--model F670L
--serial ZTE123456789
--mac AA:BB:CC:DD:EE:FF
--longpass Telkomdso123
--signature ZXHN F670L V9.0
--key-prefix CEFD0000000000174654
--iv-prefix ZTE%FN$GponNJ025
--key-suffix 574ffbb30a488a9e2d583a86719400a7
--iv-suffix dedb7b84041d5f10bfe84bca2a165e39
--try-all-known-keys
```
6. Decoder yang dihasilkan dari "Decoder Generator" Total ada 0-11 Kombinasi:

~ 0 Kombinasi (3 List)
```
decoder1.py config/config.bin config/config.xml
decoder2.py config/config.bin config/config.xml
decoder3.py config/config.bin config/config.xml
```
~ 1 Kombinasi (33 List)
```
decoder1.py --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder1.py --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder1.py --try-all-known-keys config/config.bin config/config.xml
decoder1.py --model F670L config/config.bin config/config.xml
decoder1.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder1.py --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder1.py --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder1.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder1.py --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder1.py --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder1.py --longpass Telkomdso123 config/config.bin config/config.xml
decoder2.py --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder2.py --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder2.py --try-all-known-keys config/config.bin config/config.xml
decoder2.py --model F670L config/config.bin config/config.xml
decoder2.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder2.py --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder2.py --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder2.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder2.py --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder2.py --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder2.py --longpass Telkomdso123 config/config.bin config/config.xml
decoder3.py --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder3.py --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder3.py --try-all-known-keys config/config.bin config/config.xml
decoder3.py --model F670L config/config.bin config/config.xml
decoder3.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder3.py --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder3.py --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder3.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder3.py --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder3.py --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder3.py --longpass Telkomdso123 config/config.bin config/config.xml
```
~ 2 Kombinasi (327 List)
```
decoder1.py --signature ZXHN F670L V9.0 --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder1.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder1.py --key 2bf3525fd2dcc7fe --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder1.py --mac 60:E5:D8:00:00:00 --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder1.py --signature ZXHN F670L V9.0 --longpass Telkomdso123 config/config.bin config/config.xml
decoder1.py --try-all-known-keys --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder1.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder1.py --signature ZXHN F670L V9.0 --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder1.py --try-all-known-keys --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder1.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --longpass Telkomdso123 config/config.bin config/config.xml
decoder1.py --try-all-known-keys --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder1.py --serial ZTEGCEFD0000 --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder1.py --longpass Telkomdso123 --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder1.py --longpass Telkomdso123 --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder1.py --mac 60:E5:D8:00:00:00 --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder1.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder1.py --longpass Telkomdso123 --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder1.py --model F670L --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder1.py --serial ZTEGCEFD0000 --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder1.py --longpass Telkomdso123 --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder1.py --mac 60:E5:D8:00:00:00 --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder1.py --mac 60:E5:D8:00:00:00 --try-all-known-keys config/config.bin config/config.xml
decoder1.py --key-prefix CEFD0000000000174654 --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder1.py --key 2bf3525fd2dcc7fe --try-all-known-keys config/config.bin config/config.xml
decoder1.py --longpass Telkomdso123 --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder1.py --longpass Telkomdso123 --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder1.py --key-prefix CEFD0000000000174654 --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder1.py --longpass Telkomdso123 --try-all-known-keys config/config.bin config/config.xml
decoder1.py --model F670L --try-all-known-keys config/config.bin config/config.xml
decoder1.py --iv-prefix ZTE%FN$GponNJ025 --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder1.py --key 2bf3525fd2dcc7fe --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder1.py --key-prefix CEFD0000000000174654 --try-all-known-keys config/config.bin config/config.xml
decoder1.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder1.py --iv-prefix ZTE%FN$GponNJ025 --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder1.py --serial ZTEGCEFD0000 --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder1.py --key 2bf3525fd2dcc7fe --longpass Telkomdso123 config/config.bin config/config.xml
decoder1.py --try-all-known-keys --model F670L config/config.bin config/config.xml
decoder1.py --model F670L --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder1.py --longpass Telkomdso123 --model F670L config/config.bin config/config.xml
decoder1.py --key-prefix CEFD0000000000174654 --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder1.py --serial ZTEGCEFD0000 --longpass Telkomdso123 config/config.bin config/config.xml
decoder1.py --iv-prefix ZTE%FN$GponNJ025 --try-all-known-keys config/config.bin config/config.xml
decoder1.py --try-all-known-keys --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder1.py --try-all-known-keys --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder1.py --serial ZTEGCEFD0000 --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder1.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder1.py --serial ZTEGCEFD0000 --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder1.py --key 2bf3525fd2dcc7fe --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder1.py --key 2bf3525fd2dcc7fe --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder1.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --try-all-known-keys config/config.bin config/config.xml
decoder1.py --iv-prefix ZTE%FN$GponNJ025 --model F670L config/config.bin config/config.xml
decoder1.py --key-prefix CEFD0000000000174654 --longpass Telkomdso123 config/config.bin config/config.xml
decoder1.py --iv-prefix ZTE%FN$GponNJ025 --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder1.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder1.py --signature ZXHN F670L V9.0 --model F670L config/config.bin config/config.xml
decoder1.py --iv-prefix ZTE%FN$GponNJ025 --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder1.py --key-prefix CEFD0000000000174654 --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder1.py --serial ZTEGCEFD0000 --try-all-known-keys config/config.bin config/config.xml
decoder1.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --model F670L config/config.bin config/config.xml
decoder1.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --try-all-known-keys config/config.bin config/config.xml
decoder1.py --iv-prefix ZTE%FN$GponNJ025 --longpass Telkomdso123 config/config.bin config/config.xml
decoder1.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder1.py --mac 60:E5:D8:00:00:00 --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder1.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder1.py --key 2bf3525fd2dcc7fe --model F670L config/config.bin config/config.xml
decoder1.py --model F670L --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder1.py --try-all-known-keys --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder1.py --mac 60:E5:D8:00:00:00 --model F670L config/config.bin config/config.xml
decoder1.py --try-all-known-keys --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder1.py --signature ZXHN F670L V9.0 --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder1.py --model F670L --longpass Telkomdso123 config/config.bin config/config.xml
decoder1.py --serial ZTEGCEFD0000 --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder1.py --try-all-known-keys --longpass Telkomdso123 config/config.bin config/config.xml
decoder1.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --model F670L config/config.bin config/config.xml
decoder1.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder1.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder1.py --model F670L --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder1.py --signature ZXHN F670L V9.0 --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder1.py --iv-prefix ZTE%FN$GponNJ025 --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder1.py --serial ZTEGCEFD0000 --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder1.py --mac 60:E5:D8:00:00:00 --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder1.py --try-all-known-keys --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder1.py --signature ZXHN F670L V9.0 --try-all-known-keys config/config.bin config/config.xml
decoder1.py --key-prefix CEFD0000000000174654 --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder1.py --mac 60:E5:D8:00:00:00 --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder1.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder1.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder1.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder1.py --key 2bf3525fd2dcc7fe --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder1.py --key-prefix CEFD0000000000174654 --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder1.py --key-prefix CEFD0000000000174654 --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder1.py --signature ZXHN F670L V9.0 --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder1.py --key 2bf3525fd2dcc7fe --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder1.py --model F670L --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder1.py --iv-prefix ZTE%FN$GponNJ025 --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder1.py --model F670L --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder1.py --key-prefix CEFD0000000000174654 --model F670L config/config.bin config/config.xml
decoder1.py --mac 60:E5:D8:00:00:00 --longpass Telkomdso123 config/config.bin config/config.xml
decoder1.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --longpass Telkomdso123 config/config.bin config/config.xml
decoder1.py --model F670L --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder1.py --serial ZTEGCEFD0000 --model F670L config/config.bin config/config.xml
decoder1.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder1.py --signature ZXHN F670L V9.0 --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder1.py --signature ZXHN F670L V9.0 --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder1.py --iv-prefix ZTE%FN$GponNJ025 --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder1.py --longpass Telkomdso123 --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder1.py --model F670L --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder1.py --key 2bf3525fd2dcc7fe --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder1.py --longpass Telkomdso123 --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder2.py --signature ZXHN F670L V9.0 --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder2.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder2.py --key 2bf3525fd2dcc7fe --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder2.py --mac 60:E5:D8:00:00:00 --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder2.py --signature ZXHN F670L V9.0 --longpass Telkomdso123 config/config.bin config/config.xml
decoder2.py --try-all-known-keys --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder2.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder2.py --signature ZXHN F670L V9.0 --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder2.py --try-all-known-keys --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder2.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --longpass Telkomdso123 config/config.bin config/config.xml
decoder2.py --try-all-known-keys --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder2.py --serial ZTEGCEFD0000 --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder2.py --longpass Telkomdso123 --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder2.py --longpass Telkomdso123 --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder2.py --mac 60:E5:D8:00:00:00 --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder2.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder2.py --longpass Telkomdso123 --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder2.py --model F670L --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder2.py --serial ZTEGCEFD0000 --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder2.py --longpass Telkomdso123 --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder2.py --mac 60:E5:D8:00:00:00 --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder2.py --mac 60:E5:D8:00:00:00 --try-all-known-keys config/config.bin config/config.xml
decoder2.py --key-prefix CEFD0000000000174654 --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder2.py --key 2bf3525fd2dcc7fe --try-all-known-keys config/config.bin config/config.xml
decoder2.py --longpass Telkomdso123 --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder2.py --longpass Telkomdso123 --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder2.py --key-prefix CEFD0000000000174654 --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder2.py --longpass Telkomdso123 --try-all-known-keys config/config.bin config/config.xml
decoder2.py --model F670L --try-all-known-keys config/config.bin config/config.xml
decoder2.py --iv-prefix ZTE%FN$GponNJ025 --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder2.py --key 2bf3525fd2dcc7fe --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder2.py --key-prefix CEFD0000000000174654 --try-all-known-keys config/config.bin config/config.xml
decoder2.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder2.py --iv-prefix ZTE%FN$GponNJ025 --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder2.py --serial ZTEGCEFD0000 --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder2.py --key 2bf3525fd2dcc7fe --longpass Telkomdso123 config/config.bin config/config.xml
decoder2.py --try-all-known-keys --model F670L config/config.bin config/config.xml
decoder2.py --model F670L --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder2.py --longpass Telkomdso123 --model F670L config/config.bin config/config.xml
decoder2.py --key-prefix CEFD0000000000174654 --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder2.py --serial ZTEGCEFD0000 --longpass Telkomdso123 config/config.bin config/config.xml
decoder2.py --iv-prefix ZTE%FN$GponNJ025 --try-all-known-keys config/config.bin config/config.xml
decoder2.py --try-all-known-keys --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder2.py --try-all-known-keys --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder2.py --serial ZTEGCEFD0000 --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder2.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder2.py --serial ZTEGCEFD0000 --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder2.py --key 2bf3525fd2dcc7fe --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder2.py --key 2bf3525fd2dcc7fe --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder2.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --try-all-known-keys config/config.bin config/config.xml
decoder2.py --iv-prefix ZTE%FN$GponNJ025 --model F670L config/config.bin config/config.xml
decoder2.py --key-prefix CEFD0000000000174654 --longpass Telkomdso123 config/config.bin config/config.xml
decoder2.py --iv-prefix ZTE%FN$GponNJ025 --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder2.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder2.py --signature ZXHN F670L V9.0 --model F670L config/config.bin config/config.xml
decoder2.py --iv-prefix ZTE%FN$GponNJ025 --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder2.py --key-prefix CEFD0000000000174654 --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder2.py --serial ZTEGCEFD0000 --try-all-known-keys config/config.bin config/config.xml
decoder2.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --model F670L config/config.bin config/config.xml
decoder2.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --try-all-known-keys config/config.bin config/config.xml
decoder2.py --iv-prefix ZTE%FN$GponNJ025 --longpass Telkomdso123 config/config.bin config/config.xml
decoder2.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder2.py --mac 60:E5:D8:00:00:00 --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder2.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder2.py --key 2bf3525fd2dcc7fe --model F670L config/config.bin config/config.xml
decoder2.py --model F670L --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder2.py --try-all-known-keys --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder2.py --mac 60:E5:D8:00:00:00 --model F670L config/config.bin config/config.xml
decoder2.py --try-all-known-keys --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder2.py --signature ZXHN F670L V9.0 --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder2.py --model F670L --longpass Telkomdso123 config/config.bin config/config.xml
decoder2.py --serial ZTEGCEFD0000 --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder2.py --try-all-known-keys --longpass Telkomdso123 config/config.bin config/config.xml
decoder2.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --model F670L config/config.bin config/config.xml
decoder2.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder2.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder2.py --model F670L --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder2.py --signature ZXHN F670L V9.0 --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder2.py --iv-prefix ZTE%FN$GponNJ025 --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder2.py --serial ZTEGCEFD0000 --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder2.py --mac 60:E5:D8:00:00:00 --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder2.py --try-all-known-keys --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder2.py --signature ZXHN F670L V9.0 --try-all-known-keys config/config.bin config/config.xml
decoder2.py --key-prefix CEFD0000000000174654 --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder2.py --mac 60:E5:D8:00:00:00 --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder2.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder2.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder2.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder2.py --key 2bf3525fd2dcc7fe --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder2.py --key-prefix CEFD0000000000174654 --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder2.py --key-prefix CEFD0000000000174654 --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder2.py --signature ZXHN F670L V9.0 --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder2.py --key 2bf3525fd2dcc7fe --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder2.py --model F670L --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder2.py --iv-prefix ZTE%FN$GponNJ025 --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder2.py --model F670L --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder2.py --key-prefix CEFD0000000000174654 --model F670L config/config.bin config/config.xml
decoder2.py --mac 60:E5:D8:00:00:00 --longpass Telkomdso123 config/config.bin config/config.xml
decoder2.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --longpass Telkomdso123 config/config.bin config/config.xml
decoder2.py --model F670L --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder2.py --serial ZTEGCEFD0000 --model F670L config/config.bin config/config.xml
decoder2.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder2.py --signature ZXHN F670L V9.0 --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder2.py --signature ZXHN F670L V9.0 --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder2.py --iv-prefix ZTE%FN$GponNJ025 --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder2.py --longpass Telkomdso123 --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder2.py --model F670L --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder2.py --key 2bf3525fd2dcc7fe --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder2.py --longpass Telkomdso123 --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder3.py --signature ZXHN F670L V9.0 --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder3.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder3.py --key 2bf3525fd2dcc7fe --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder3.py --mac 60:E5:D8:00:00:00 --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder3.py --signature ZXHN F670L V9.0 --longpass Telkomdso123 config/config.bin config/config.xml
decoder3.py --try-all-known-keys --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder3.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder3.py --signature ZXHN F670L V9.0 --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder3.py --try-all-known-keys --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder3.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --longpass Telkomdso123 config/config.bin config/config.xml
decoder3.py --try-all-known-keys --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder3.py --serial ZTEGCEFD0000 --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder3.py --longpass Telkomdso123 --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder3.py --longpass Telkomdso123 --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder3.py --mac 60:E5:D8:00:00:00 --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder3.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder3.py --longpass Telkomdso123 --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder3.py --model F670L --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder3.py --serial ZTEGCEFD0000 --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder3.py --longpass Telkomdso123 --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder3.py --mac 60:E5:D8:00:00:00 --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder3.py --mac 60:E5:D8:00:00:00 --try-all-known-keys config/config.bin config/config.xml
decoder3.py --key-prefix CEFD0000000000174654 --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder3.py --key 2bf3525fd2dcc7fe --try-all-known-keys config/config.bin config/config.xml
decoder3.py --longpass Telkomdso123 --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder3.py --longpass Telkomdso123 --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder3.py --key-prefix CEFD0000000000174654 --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder3.py --longpass Telkomdso123 --try-all-known-keys config/config.bin config/config.xml
decoder3.py --model F670L --try-all-known-keys config/config.bin config/config.xml
decoder3.py --iv-prefix ZTE%FN$GponNJ025 --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder3.py --key 2bf3525fd2dcc7fe --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder3.py --key-prefix CEFD0000000000174654 --try-all-known-keys config/config.bin config/config.xml
decoder3.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder3.py --iv-prefix ZTE%FN$GponNJ025 --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder3.py --serial ZTEGCEFD0000 --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder3.py --key 2bf3525fd2dcc7fe --longpass Telkomdso123 config/config.bin config/config.xml
decoder3.py --try-all-known-keys --model F670L config/config.bin config/config.xml
decoder3.py --model F670L --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder3.py --longpass Telkomdso123 --model F670L config/config.bin config/config.xml
decoder3.py --key-prefix CEFD0000000000174654 --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder3.py --serial ZTEGCEFD0000 --longpass Telkomdso123 config/config.bin config/config.xml
decoder3.py --iv-prefix ZTE%FN$GponNJ025 --try-all-known-keys config/config.bin config/config.xml
decoder3.py --try-all-known-keys --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder3.py --try-all-known-keys --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder3.py --serial ZTEGCEFD0000 --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder3.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder3.py --serial ZTEGCEFD0000 --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder3.py --key 2bf3525fd2dcc7fe --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder3.py --key 2bf3525fd2dcc7fe --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder3.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --try-all-known-keys config/config.bin config/config.xml
decoder3.py --iv-prefix ZTE%FN$GponNJ025 --model F670L config/config.bin config/config.xml
decoder3.py --key-prefix CEFD0000000000174654 --longpass Telkomdso123 config/config.bin config/config.xml
decoder3.py --iv-prefix ZTE%FN$GponNJ025 --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder3.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder3.py --signature ZXHN F670L V9.0 --model F670L config/config.bin config/config.xml
decoder3.py --iv-prefix ZTE%FN$GponNJ025 --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder3.py --key-prefix CEFD0000000000174654 --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder3.py --serial ZTEGCEFD0000 --try-all-known-keys config/config.bin config/config.xml
decoder3.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --model F670L config/config.bin config/config.xml
decoder3.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --try-all-known-keys config/config.bin config/config.xml
decoder3.py --iv-prefix ZTE%FN$GponNJ025 --longpass Telkomdso123 config/config.bin config/config.xml
decoder3.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder3.py --mac 60:E5:D8:00:00:00 --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder3.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder3.py --key 2bf3525fd2dcc7fe --model F670L config/config.bin config/config.xml
decoder3.py --model F670L --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder3.py --try-all-known-keys --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder3.py --mac 60:E5:D8:00:00:00 --model F670L config/config.bin config/config.xml
decoder3.py --try-all-known-keys --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder3.py --signature ZXHN F670L V9.0 --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder3.py --model F670L --longpass Telkomdso123 config/config.bin config/config.xml
decoder3.py --serial ZTEGCEFD0000 --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder3.py --try-all-known-keys --longpass Telkomdso123 config/config.bin config/config.xml
decoder3.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --model F670L config/config.bin config/config.xml
decoder3.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder3.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder3.py --model F670L --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 config/config.bin config/config.xml
decoder3.py --signature ZXHN F670L V9.0 --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder3.py --iv-prefix ZTE%FN$GponNJ025 --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder3.py --serial ZTEGCEFD0000 --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder3.py --mac 60:E5:D8:00:00:00 --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder3.py --try-all-known-keys --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder3.py --signature ZXHN F670L V9.0 --try-all-known-keys config/config.bin config/config.xml
decoder3.py --key-prefix CEFD0000000000174654 --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder3.py --mac 60:E5:D8:00:00:00 --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder3.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder3.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder3.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder3.py --key 2bf3525fd2dcc7fe --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder3.py --key-prefix CEFD0000000000174654 --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder3.py --key-prefix CEFD0000000000174654 --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder3.py --signature ZXHN F670L V9.0 --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder3.py --key 2bf3525fd2dcc7fe --serial ZTEGCEFD0000 config/config.bin config/config.xml
decoder3.py --model F670L --iv-prefix ZTE%FN$GponNJ025 config/config.bin config/config.xml
decoder3.py --iv-prefix ZTE%FN$GponNJ025 --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder3.py --model F670L --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder3.py --key-prefix CEFD0000000000174654 --model F670L config/config.bin config/config.xml
decoder3.py --mac 60:E5:D8:00:00:00 --longpass Telkomdso123 config/config.bin config/config.xml
decoder3.py --key-suffix 574ffbb30a488a9e2d583a86719400a7 --longpass Telkomdso123 config/config.bin config/config.xml
decoder3.py --model F670L --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder3.py --serial ZTEGCEFD0000 --model F670L config/config.bin config/config.xml
decoder3.py --iv-suffix dedb7b84041d5f10bfe84bca2a165e39 --signature ZXHN F670L V9.0 config/config.bin config/config.xml
decoder3.py --signature ZXHN F670L V9.0 --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
decoder3.py --signature ZXHN F670L V9.0 --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder3.py --iv-prefix ZTE%FN$GponNJ025 --key 2bf3525fd2dcc7fe config/config.bin config/config.xml
decoder3.py --longpass Telkomdso123 --key-prefix CEFD0000000000174654 config/config.bin config/config.xml
decoder3.py --model F670L --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder3.py --key 2bf3525fd2dcc7fe --key-suffix 574ffbb30a488a9e2d583a86719400a7 config/config.bin config/config.xml
decoder3.py --longpass Telkomdso123 --mac 60:E5:D8:00:00:00 config/config.bin config/config.xml
```
7. Untuk Encoding support penggunaan perintah seperti contoh yang tercantum dibawah ini:
```
--key 2bf3525fd2dcc7fe
--model F670L
--serial ZTE123456789
--mac AA:BB:CC:DD:EE:FF
--longpass Telkomdso123
--signature ZXHN F670L V9.0
--iv {iv_key}
--use-signature-encryption
--chunk-size 65536
--payload-type {0/1/2/3/4/5/6}
--version {1/2}
--include-header
--little-endian-header
--include-unencrypted-length
--key-prefix CEFD0000000000174654
--iv-prefix ZTE%FN$GponNJ025
--key-suffix 574ffbb30a488a9e2d583a86719400a7
--iv-suffix dedb7b84041d5f10bfe84bca2a165e39
```

