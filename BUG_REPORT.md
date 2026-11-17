# Bug Report — Sistem Manajemen Game Roblox

## BUG-001 — Formulir menerima input kosong dan spasi
- **Severity:** Medium | **Priority:** High | **Status:** Fixed
- **Deskripsi:** Pada versi BUG (`simpanGameBug`), data game tetap disimpan meskipun seluruh kolom kosong atau hanya diisi spasi.
- **Langkah Reproduksi:** Pilih Skenario 1 atau 2, lalu klik **Jalankan BUG**.
- **Perbaikan:** `simpanGameFix()` menggunakan `.trim()` dan menolak pengajuan jika ada kolom wajib yang kosong.

## BUG-002 — Jumlah pemain aktif negatif (-) diterima sistem
- **Severity:** High | **Priority:** High | **Status:** Fixed
- **Deskripsi:** Nilai minus (misalnya `-5000`) tetap disimpan ke data game sehingga merusak statistik pemain aktif.
- **Langkah Reproduksi:** Pilih Skenario 3, lalu klik **Jalankan BUG**.
- **Perbaikan:** Ditambahkan validasi numerik `Number(data.pemain_aktif) < 0` pada `simpanGameFix()`.

## BUG-003 — Duplikasi nama game diizinkan & label status salah
- **Severity:** Medium | **Priority:** Medium | **Status:** Fixed
- **Deskripsi:** Nama game yang sudah ada di katalog (seperti *Brookhaven RP*) dapat diinput kembali, serta status game valid tertulis "Draft Belum Rilis".
- **Perbaikan:** Ditambahkan validasi anti-duplikasi nama game dan perbaikan status menjadi "Terverifikasi & Aktif".