# Bug Report — Sistem Manajemen Game Roblox

**Environment:** Google Chrome, Windows 11, Aplikasi `bug.html` (v1.0.0)  
**Reporter:** Nabhita Akhilla (F5212520057)

---

## ISSUE #001 — Input Spasi Kosong Tersimpan ke Daftar
- **Kategori:** Corrective Maintenance | **Severity:** Medium | **Priority:** High | **Status:** Closed
- **Steps to Reproduce:** Kosongkan kolom Nama Game atau isi dengan spasi (`"   "`), lalu klik **+ Simpan Game**.
- **Expected Result:** Sistem menolak input dan menampilkan pesan peringatan.
- **Actual Result:** Baris kosong tetap tersimpan ke tabel.

## ISSUE #002 — Jumlah Pemain Aktif Negatif (-) Diterima Sistem
- **Kategori:** Corrective Maintenance | **Severity:** High | **Priority:** High | **Status:** Closed
- **Steps to Reproduce:** Isi kolom Pemain Aktif dengan `-500`, lalu klik **+ Simpan Game**.
- **Expected Result:** Sistem menolak angka negatif (`< 0`).
- **Actual Result:** Nilai `-500` tersimpan ke tabel.

## ISSUE #003 — Kesalahan Perhitungan Total Pemain Aktif (String Concatenation)
- **Kategori:** Corrective Maintenance | **Severity:** Critical | **Priority:** High | **Status:** Closed
- **Steps to Reproduce:** Buka halaman `bug.html` dan perhatikan kartu statistik **Total Pemain Aktif**.
- **Expected Result:** Menampilkan hasil penjumlahan angka `635,000`.
- **Actual Result:** Menampilkan penggabungan string `45000015000035000` karena variabel `totalPemain` diinisialisasi sebagai string `""`.

## ISSUE #004 — Duplikasi Nama Game Diperbolehkan
- **Kategori:** Preventive Maintenance | **Severity:** Medium | **Priority:** Medium | **Status:** Closed
- **Steps to Reproduce:** Input nama game `Brookhaven RP` yang sudah ada di tabel.
- **Expected Result:** Sistem menolak data ganda dan memberi notifikasi.
- **Actual Result:** Data game ganda tersimpan di tabel.

## ISSUE #005 — Tombol Hapus Selalu Menghapus Baris Pertama & Tanpa Konfirmasi
- **Kategori:** Corrective Maintenance | **Severity:** High | **Priority:** High | **Status:** Closed
- **Steps to Reproduce:** Klik tombol **Hapus** pada baris ke-3 (*Adopt Me!*).
- **Expected Result:** Muncul dialog konfirmasi dan menghapus *Adopt Me!*.
- **Actual Result:** Langsung menghapus baris ke-1 (*Brookhaven RP*) tanpa konfirmasi karena parameter `hapusGame(0)` di-*hardcode*.