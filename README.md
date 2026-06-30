# Jurnal Trade — Otoman

Trade journal dengan **entry gate**: sebelum bisa catat posisi baru, lo wajib lolos checklist kriteria entry dulu (news/catalyst, setup teknikal, R:R minimal 2:1, sizing, dan kondisi mental). Dibuat buat trader saham US lewat Pluang yang pegang USD, jadi P&L-nya otomatis dipisah: **berapa untung/rugi dari pergerakan saham, berapa dari pergerakan kurs USD/IDR**.

🔗 **Live demo:** _(isi link Vercel setelah deploy)_

## Fitur

- **Entry gate** — 5 kriteria checklist wajib dicentang sebelum bisa input posisi baru
- **R:R preview real-time** — dihitung otomatis dari target & stop yang lo isi
- **Partial close** — bisa tutup sebagian posisi, sisanya tetap kebuka
- **P&L split** — pisah hasil dari saham vs dari kurs
- **Pembatas trade mingguan** — biar gak overtrade
- **Tab Analitik** — checklist compliance vs hasil, performa per setup type, pola emosi saat rugi
- **Export/Import JSON** — buat backup data atau pindah device
- **100% jalan di browser, tanpa server/database** — semua data tersimpan lokal di browser lo sendiri (lihat bagian Privasi & Data di bawah)

## Tech stack

Vanilla HTML/CSS/JS — gak ada framework, gak ada build step, gak ada dependency. File-nya cuma satu: `index.html`.

## Cara jalanin secara lokal

Gak perlu install apa-apa. Tinggal buka `index.html` di browser mana pun (Chrome, Safari, Firefox, Edge — desktop atau HP).

## Deploy ke Vercel

Lihat `DEPLOY.md` untuk panduan lengkap upload ke GitHub + deploy ke Vercel.

## Cara pakai

Lihat `TUTORIAL.md` untuk panduan lengkap, termasuk cara save dan load data (penting dibaca karena ini nentuin apakah data trading lo aman atau bisa hilang).

## Privasi & Data

Semua data trade tersimpan di **localStorage browser lo sendiri** — tidak ada server, tidak ada database, tidak ada yang dikirim ke mana pun. Artinya:

- Data lo gak bisa dilihat siapa pun selain lo
- Data lo **terikat ke browser & device tertentu** — kalau lo ganti device, clear browser data, atau pakai mode incognito, data bisa hilang
- **Wajib export/backup data secara rutin** (lihat TUTORIAL.md) — ini bukan saran, ini keharusan

## Lisensi

Bebas dipakai dan dimodifikasi untuk keperluan pribadi maupun komunitas Trader Otodidak.
