# daftar-backup

نسخة احتياطية **متشفّرة** من كود «الدفتر» (manasikai.net) بتاريخ تعديلاته كله.
الملف `daftar.bundle.enc` ما بيتقراش من غير المفتاح.

- **المفتاح:** متغير `DAFTAR_BACKUP_KEY` في مشروع الدفتر على Vercel (فريق المالية، بيئة Development).
- **الاسترجاع:**
  ```
  openssl enc -d -aes-256-cbc -pbkdf2 -iter 600000 -in daftar.bundle.enc -out daftar.bundle -pass env:DAFTAR_BACKUP_KEY
  git clone daftar.bundle daftar
  ```
- بيتحدث مع كل نشرة للدفتر.
