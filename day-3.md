Reconnaissance

CSIRT = Computer Security Incident Response Team 

Subdomain = Anak domain

meta4sec.com (http://meta4sec.com/)
google.com (http://google.com/)
apple.com (http://apple.com/)

Domain utama = google.com
Subdomain = drive.google.com

google.com -> Domain utama
drive.google.com -> Subdomain
docs.google.com -> Subdomain
maps.google.com
spreadsheets.google.com
forms.google.com
accounts.google.com
cloud.google.com (http://cloud.google.com/)

jakarta.go.id (http://jakarta.go.id/) -> domain utama
admin.jakarta.go.id (http://admin.jakarta.go.id/) -> subdomain
dashboard-admin.jakarta.go.id (http://dashboard-admin.jakarta.go.id/) -> subdomain

ui.ac.id (http://ui.ac.id/) -> domain utama
fasilkom.ui.ac.id (http://fasilkom.ui.ac.id/) -> subdomain
fk.ui.ac.id (http://fk.ui.ac.id/) -> subdomain
admin.ui.ac.id (http://admin.ui.ac.id/) -> subdomain
dosen.ui.ac.id (http://dosen.ui.ac.id/) -> subdomain

Wildcard:
*.ui.com (http://ui.com/) = kalo ada tanda * (wildcard), berarti semua subdomainnya ikut masuk scope bounty


subfinder -d jakarta.go.id 
subfinder -d jakarta.go.id -o subdomains.txt -> scan dengan output
httpx-toolkit -l subdomains.txt -mc 200 -o active.txt

HTTP ngeliat isi http-title
cat active.txt | httpx-toolkit -silent -status-code -title -ip -mc 200

subdomains.txt -> hasil scan subfinder
active.txt -> hasil scan httpx

subdomain aktif = subdomain yang bisa diakses
subdomain pasif = subdomain yang tidak bisa kita akses (hanya bisa diakses tim internal)


HTTP Response Code
2xx = Respon berhasil diterima
3xx = Respon di redirect
4xx = Respon ditolak karena kita tidak memiliki akses
5xx = Respon ditolak karena server error

User -> auth.meta4sec.com (http://auth.meta4sec.com/) (302)
auth.meta4sec.com (http://auth.meta4sec.com/) -> login.google.com (http://login.google.com/) 
meta4sec.com/admin (http://meta4sec.com/admin) -> meta4sec.com/error (http://meta4sec.com/error)

admin.meta4sec.com/dashboard (http://admin.meta4sec.com/dashboard)  -> 4xx
403 forbidden
404 not found

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
