Reconnaissance with Shodan

Shodan = Search Engine Internet Infrastructure

ssl.cert.subject.CN:”bni.co.id” 200

CN = KTP

KTP = Identitas Orang WNI
CN = Identitas IP Milik perusahaan mana / mengarah ke domain mana

CN = Common Name = KTP nya IP/server

Zeroquery -> Platform Internal BNI (External tidak bisa akses)
https://zeroquery.bni.co.id/ -> Kita gak bisa akses ini (Kemungkinan besar di blokir WAF)
https://136.110.203.207/signin -> Kita bisa bypass aksesnya

https://zeroquery.bni.co.id/  -> Protect WAF dari sisi Domain
https://136.110.203.207/signin -> Tidak di protect WAF

Proses aplikasi di deploy
 1. Programmer bikin app nya
 2. Hosting di server (IP 136.110.203.207) -> Tidak di protect WAF
 3. IP Servernya diubah jadi Domain biar mudah diakses (zeroquery.bni.co.id (http://zeroquery.bni.co.id/))
 4. Domain sudah di protect WAF
 5. WAF biasanya hanya protect di layer domain/DNS

https://support.apple.com (https://support.apple.com/) <-> https://17.47.166.10/

https://support.apple.com/.do -> Tidak bisa diakses
https://17.47.166.10/.do -> Bisa diakses

dirsearch -u https://136.110.203.207/ -i 200

-i 200 untuk ngefilter status code

========================

Default Credentials

Default Credentials
admin:admin
admin:12345678
admin:pass
admin:password
adninistrator:password
admin:default
user:user
user:pass
user:default
username:password
root:pass
root:password
root:root
root:default
default:default
'or 1=1 limit 1 -- -+
