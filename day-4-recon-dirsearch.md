Reconnaissance with Dirsearch

Directory = Folder 
Endpoint = FIle

Folder = /home/documents/kuliah/2026/semester1/algoritma/
File = tugas.pdf

/home/documents/kuliah/2026/tugas.pdf -> Endpoint
/home/documents/kuliah/2026/ -> Directory

.pdf
.docx
.ppt
.xlsx

Directory:
https://google.com/folder/
https://google.com/folder/photo/2022/november/
https://youtube.com/account/meta4sec

Endpoint:
https://google.com/folder/photo/2022/november/gambar.jpg

https://meta4sec.com/home.php 
https://meta4sec.com/home.php
https://meta4sec.com/home/video/hacking/reconnaissance.mp4

https://web.com/home/page.html -> Access
https://web.com/logo/image.jpg -> Access
https://web.com/new/feature.html -> Access
https://web.com/.env -> Otomatis Deploy -> Lupa di private
https://web.com/backup.zip -> Otomatis Deploy -> Lupa di private

Framework Laravel:
Developer Mode -> Mode pengembangan -> Masih ada fitur2 yang membantu programmer -> backup.zip
Production Mode -> Mode final launch -> Fitur2 tersebut sudah di private


Data sensitif seringkali ditermukan di dalam endpoint
https://contoh.com/backup.zip
https://contoh.com/file.env 

https://google.com/folder/file/2025/backup/backup.zip 

Scan Dirsearch
dirsearch -u http://zero.webappsecurity.com/
dirsearch -u http://zero.webappsecurity.com/ -i 200 

HTTP Reponse Code
2xx = Success
3xx = Redirect
4xx = User/Client Error
5xx = Server Error

2xx = User Request <-> Server Respon
3xx = User Request akses meta4sec.com <-> Server merespon tapi di redirect ke redlimit.id
4xx = User Request <-> Server menolak untuk respon
5xx = User Request <-> Server tidak merespon


https://web.com/backup.zip [200] [10kb]
https://web.com/.env [200] [10kb]
https://web.com/database.sql [200] [10kb]

WAF - Web Application Firewall

P1 = Critical
P2 = High
P3 = Medium
P4 = Low
P5 = Informational
