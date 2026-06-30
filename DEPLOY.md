# Cara Deploy ke GitHub + Vercel

Panduan ini buat lo yang mau orang lain bisa akses Jurnal Trade ini lewat link, tanpa perlu download file.

Total waktu: ~10-15 menit, gratis sepenuhnya.

---

## Bagian 1 — Upload ke GitHub

### 1. Bikin akun GitHub (kalau belum punya)
Daftar di **github.com** — gratis.

### 2. Bikin repository baru
- Klik tombol **+** di kanan atas → **New repository**
- Nama repo: `jurnal-trade` (atau nama lain sesuai selera)
- Pilih **Public** (biar Vercel bisa akses gratis)
- **Jangan** centang "Add a README file" (kita udah punya sendiri)
- Klik **Create repository**

### 3. Upload file
Ada 2 cara, pilih yang paling gampang buat lo:

**Cara A — Lewat browser (paling gampang, gak perlu command line):**
- Di halaman repo yang baru dibuat, klik **uploading an existing file**
- Drag & drop semua file: `index.html`, `README.md`, `TUTORIAL.md`, `DEPLOY.md`
- Scroll ke bawah, klik **Commit changes**

**Cara B — Lewat Git command line (kalau udah biasa):**
```bash
git init
git add .
git commit -m "Initial commit - Jurnal Trade v2"
git branch -M main
git remote add origin https://github.com/USERNAME/jurnal-trade.git
git push -u origin main
```
Ganti `USERNAME` dengan username GitHub lo.

---

## Bagian 2 — Deploy ke Vercel

### 1. Bikin akun Vercel
Ke **vercel.com** → **Sign Up** → pilih **Continue with GitHub** (biar otomatis terhubung, gak perlu input ulang)

### 2. Import project
- Di dashboard Vercel, klik **Add New** → **Project**
- Vercel bakal nunjukin list repository GitHub lo — cari `jurnal-trade`
- Klik **Import**

### 3. Konfigurasi (biasanya otomatis kedetect)
Karena ini cuma file HTML statis (gak ada framework), Vercel otomatis akan:
- **Framework Preset**: pilih "Other" kalau gak otomatis kedetect
- **Build Command**: kosongkan (gak perlu build apa-apa)
- **Output Directory**: kosongkan / biarkan default

### 4. Deploy
Klik **Deploy**. Tunggu sekitar 30-60 detik.

### 5. Selesai
Vercel kasih lo link publik, formatnya kira-kira:
```
https://jurnal-trade-xxxxx.vercel.app
```
Link ini yang bisa lo share ke komunitas Trader Otodidak. Siapa pun yang buka link ini bisa langsung pakai app-nya — datanya tersimpan masing-masing di browser mereka sendiri (gak campur sama punya lo atau orang lain).

---

## Update di kemudian hari

Setiap kali lo mau update kode (misal nambah fitur atau benerin bug):

1. Edit file di komputer lo
2. Upload ulang via GitHub (drag & drop file yang sama, akan menimpa otomatis) — atau `git add . && git commit -m "update" && git push` kalau pakai command line
3. **Vercel otomatis re-deploy** setiap ada perubahan baru di GitHub — gak perlu trigger manual

---

## Opsional — pakai domain sendiri

Kalau nanti mau pakai domain custom (misal `jurnal.otoman-trader.com`), bisa diatur di **Vercel → Project Settings → Domains**. Butuh domain yang udah lo beli sebelumnya dari registrar (Niagahoster, Namecheap, dll).
