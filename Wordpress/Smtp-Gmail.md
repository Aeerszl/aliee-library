# SMTP Gmail Ayarları

**Video Tutorial:** https://youtu.be/OLYxdbk2kbs?si=MIAvCIlJdHVpkbXl
📌 WordPress – Gmail SMTP (WP Mail SMTP)
✍️ NOT ALMAK İÇİN NET ADIMLAR
1️⃣ Gmail’de Uygulama Şifresi Alma

Google hesabına gir

Güvenlik → 2 Adımlı Doğrulama (Açık olmalı)

Direkt bu linke gir:
👉 https://myaccount.google.com/apppasswords

Telefonuna gelen doğrulama kodunu gir

App name alanına yaz:
WordPress SMTP

Create butonuna bas

Google’ın verdiği 16 haneli şifreyi kopyala
👉 Bu SMTP şifresidir

2️⃣ WordPress’te WP Mail SMTP Ayarları

WordPress Panel → Eklentiler

WP Mail SMTP eklentisini aç

Ayarlar (Settings) bölümüne gir

Mailer: Other SMTP seç

3️⃣ SMTP Bilgileri (Birebir Yaz)
SMTP Host: smtp.gmail.com
Encryption: TLS
SMTP Port: 587
Authentication: ON
Username: gmailadresin@gmail.com
Password: (Gmail’den aldığın 16 haneli uygulama şifresi)


⚠️ Normal Gmail şifresi ASLA yazılmaz

4️⃣ Test Mail Gönderme

WP Mail SMTP → Email Test

Kendi mail adresini yaz

Send Email de

“Success” yazısı gelirse → ✅ TAMAM
KISA ÖZET (1 Satır)

Gmail → App Password al → WP Mail SMTP → Other SMTP → 587 TLS → Test Mail