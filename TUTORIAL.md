# Tutorial Pemakaian — Jurnal Trade

## Daftar isi
1. [Hal penting yang wajib dibaca dulu](#hal-penting-yang-wajib-dibaca-dulu)
2. [Cara catat posisi baru](#cara-catat-posisi-baru)
3. [Cara tutup posisi (full & partial)](#cara-tutup-posisi-full--partial)
4. [Cara baca tab Analitik](#cara-baca-tab-analitik)
5. [Cara Save & Backup data](#cara-save--backup-data)
6. [Cara Load / pindah data ke device lain](#cara-load--pindah-data-ke-device-lain)
7. [Atur batas trade mingguan](#atur-batas-trade-mingguan)
8. [Pertanyaan umum](#pertanyaan-umum)

---

## Hal penting yang wajib dibaca dulu

**App ini gak punya server atau database.** Semua data trade yang lo input tersimpan di **browser** yang lo pakai saat itu — teknisnya disebut `localStorage`. Ini artinya:

| Situasi | Apakah data aman? |
|---|---|
| Tutup tab / tutup browser, buka lagi besok | ✅ Aman, data tetap ada |
| Restart laptop/HP | ✅ Aman, data tetap ada |
| Buka pakai browser yang sama, device yang sama | ✅ Aman |
| Buka pakai browser **berbeda** (misal biasa pakai Chrome, terus buka pakai Firefox) | ❌ Data gak akan muncul (browser beda = penyimpanan beda) |
| Buka di **HP**, padahal data lo ada di **laptop** | ❌ Data gak akan muncul (device beda = penyimpanan beda) |
| Pakai mode **Incognito/Private** | ❌ Data otomatis terhapus begitu jendela ditutup |
| Clear browser data / cache / "Clear browsing data" | ❌ **Data hilang permanen** kalau belum di-backup |
| Install ulang browser atau OS | ❌ **Data hilang permanen** kalau belum di-backup |

**Kesimpulan: lo HARUS rutin export/backup data.** Anggap ini seperti nabung di bawah kasur — aman selama kasurnya gak dibongkar, tapi kalau dibongkar tanpa backup, hilang semua.

Rekomendasi: **export data setiap habis nambah atau nutup trade penting**, minimal seminggu sekali.

---

## Cara catat posisi baru

1. Di tab **Jurnal**, scroll ke bagian **"Buka posisi baru"**
2. Centang semua **5 kriteria checklist**:
   - Ada news/catalyst yang jelas
   - Setup teknikal confirmed (order block/VWAP)
   - R:R minimal 2:1
   - Position size sesuai rule
   - Bukan revenge trade/FOMO
3. Isi semua kolom bertanda **●** (ticker, harga masuk, jumlah unit, USD/IDR saat masuk, target, stop, setup type, alasan masuk)
4. Perhatikan **preview R:R** yang muncul otomatis di bawah form — kalau di bawah 1:2, pertimbangkan ulang sebelum lanjut
5. Tombol **"Catat posisi"** baru bisa diklik kalau checklist dan semua kolom lengkap
6. Klik → posisi masuk ke daftar **"Posisi terbuka"**

> Kalau tombol gak nyala-nyala padahal kerasa udah isi semua, cek lagi: kemungkinan ada checklist yang belum dicentang, atau kolom yang ke-skip.

---

## Cara tutup posisi (full & partial)

1. Di kartu posisi terbuka, klik **"Tutup posisi (full/partial)"**
2. Form kecil muncul, isi:
   - **Unit ditutup** — kosongkan kalau mau tutup semua sisa posisi
   - **Harga keluar (USD)**
   - **USD/IDR saat keluar**
   - **Catatan emosi** — tulis jujur 1 kalimat (ini data yang dipakai di tab Analitik buat ngedeteksi pola emosi lo)
3. Pilih salah satu:
   - **"Tutup sebagian unit"** — kalau cuma mau exit sebagian, sisanya tetap jadi posisi terbuka
   - **"Tutup semua sisa"** — kalau mau exit total

Setelah ditutup (sebagian atau penuh), P&L otomatis dihitung dan dipisah jadi **dari saham** vs **dari kurs**, lalu muncul di **Riwayat tertutup**.

---

## Cara baca tab Analitik

Klik tab **Analitik** di pojok kanan atas. Isinya:

- **Ringkasan atas** — total trade, win rate, net P&L, rata-rata conviction
- **Checklist Compliance vs Hasil** — insight paling penting: apakah trade yang checklist-nya lengkap (5/5) memang menghasilkan lebih baik dibanding yang bolong. Ini baru muncul akurat kalau udah ada cukup data (minimal beberapa trade tertutup dengan variasi compliance)
- **Performa per Setup Type** — bar chart, setup mana (breakout, pullback, dll) yang paling profitable buat lo secara historis
- **Pola Emosi Saat Rugi** — kata-kata yang sering muncul di catatan emosi pas posisi rugi. Kalau sering muncul "fomo" atau "panik", itu sinyal buat benerin disiplin entry, bukan cuma analisa teknikal

---

## Cara Save & Backup data

1. Scroll ke bagian bawah tab **Jurnal**
2. Klik tombol **"Export semua (JSON)"**
3. Browser otomatis download file bernama `jurnal-trade-YYYY-MM-DD.json`
4. **Simpan file ini baik-baik** — bisa di Google Drive, email ke diri sendiri, atau folder backup khusus

Lakukan ini secara rutin. File JSON ini adalah satu-satunya cara lo bisa memulihkan data kalau sesuatu terjadi ke browser/device lo.

---

## Cara Load / pindah data ke device lain

Skenario: lo ganti laptop, install ulang browser, atau mau buka data yang sama di HP.

1. Pastikan lo punya file backup `jurnal-trade-YYYY-MM-DD.json` dari export sebelumnya
2. Buka Jurnal Trade di device/browser baru
3. Scroll ke bawah, klik **"Import JSON"**
4. Pilih file backup tadi
5. Konfirmasi import

**Catatan penting:** import itu **menambahkan** data baru ke yang sudah ada, bukan menimpa/replace. Jadi kalau device baru itu masih kosong, hasilnya sama persis dengan data lama lo. Tapi kalau device itu sudah punya data lain, hasilnya akan jadi gabungan keduanya (bisa double kalau file yang sama di-import dua kali — jadi cek dulu sebelum import berulang).

---

## Atur batas trade mingguan

Default-nya 5 trade per minggu. Untuk mengubah:

1. Klik **"Atur batas trade/minggu"**
2. Masukkan angka baru
3. Bar di bagian atas (di bawah kartu statistik) akan otomatis update — kalau jumlah trade minggu ini melebihi batas, bar berubah warna merah sebagai peringatan

---

## Pertanyaan umum

**Q: Saya pakai di HP dan laptop, apakah datanya sinkron otomatis?**
Tidak. Tidak ada sinkronisasi otomatis karena tidak ada server. Kalau mau pakai di dua device, harus manual export dari satu device lalu import ke device lain setiap kali ada update.

**Q: Saya tutup browser/laptop, apakah perlu export ulang?**
Tidak perlu setiap saat — data tetap tersimpan otomatis di browser. Export hanya diperlukan sebagai **backup** untuk berjaga-jaga (misalnya kalau browser di-uninstall, cache dibersihkan, atau pindah device).

**Q: Apakah data saya bisa dilihat orang lain yang juga akses link yang sama?**
Tidak. localStorage itu unik per browser per device. Orang lain yang membuka link yang sama di device mereka akan punya penyimpanan kosong sendiri, terpisah total dari punya lo.

**Q: File JSON yang saya export bisa dibuka di Excel?**
Bisa dibuka tapi formatnya bukan tabel biasa (ini format JSON, terstruktur bukan flat). Untuk lihat-lihat datanya secara teknis, bisa dibuka pakai text editor atau browser. Untuk analisis di Excel, lebih baik gunakan tab Analitik di dalam app langsung.

**Q: Saya tidak sengaja hapus trade yang penting, bisa dikembalikan?**
Tidak ada fitur undo. Kalau punya backup JSON sebelumnya, bisa di-import lagi untuk mengembalikan data tersebut, tapi trade lain yang dicatat setelah backup terakhir tidak akan ikut kembali. Ini alasan lain kenapa backup rutin penting.
