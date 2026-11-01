# Niiu Store - Panduan Hosting di Netlify

Isi folder:
- index.html   -> seluruh website (harga, logo, keranjang, checkout WhatsApp)
- images/apps/ -> tempat logo lokal (opsional, boleh dibiarkan kosong)
- netlify.toml -> pengaturan Netlify (tidak perlu diubah)

## Cara 1: Netlify Drop (paling cepat, tanpa akun Git)
1. Buka https://app.netlify.com/drop lalu login/daftar (gratis).
2. Seret FOLDER ini (atau file ZIP-nya) ke kotak "Drag and drop your site output folder here".
   - Di HP: ketuk area unggah lalu pilih file ZIP. Kalau ditolak, pakai Cara 2 atau laptop.
3. Tunggu beberapa detik sampai muncul alamat seperti https://nama-acak.netlify.app. Selesai.
4. Ganti nama: Site configuration > Change site name > pilih nama, misalnya niiu-store.netlify.app.

## Cara 2: Lewat GitHub (bisa dari HP, update mudah)
1. Buat akun di https://github.com lalu buat repository baru bernama niiu-store (Public).
2. Klik "Add file" > "Upload files", unggah isi folder ini (index.html, netlify.toml, folder images), lalu "Commit changes".
3. Buka https://app.netlify.com > "Add new site" > "Import an existing project" > GitHub > pilih niiu-store.
4. Build command dikosongkan, Publish directory isi titik ( . ). Klik "Deploy".
5. Setiap kali kamu mengganti index.html di GitHub, Netlify otomatis memperbarui website.

## Mengubah isi website
- Nomor WhatsApp: buka index.html, cari WA_NUMBER, formatnya 628xxxxxxxxxx.
- Harga: cari bagian RAW di index.html. Format: Nama|Kategori|Jenis akun=Durasi:Harga dalam ribuan,Durasi:Harga;Jenis akun lain=...
- Logo lokal: simpan PNG di images/apps/<streaming|education|editing|games>/ dengan nama file yang sama seperti di website lama (contoh netflix.png).
- Domain sendiri: Domain management > Add a domain.

## Catatan
- Logo diambil dari internet (domain resmi aplikasi dan aset websitemu). Di Netlify gambar dari luar tidak diblokir seperti di claude.ai.
- Kalau logo tertentu tidak muncul, otomatis tampil lingkaran berinisial.
