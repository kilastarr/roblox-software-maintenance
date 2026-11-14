# Changelog

Catatan riwayat perubahan versi pada proyek **Sistem Manajemen Game Roblox**.

## [1.1.0] - `fix.html`
### Fixed (Corrective Maintenance)
- **Issue #001:** Menambahkan `.trim()` untuk menolak input kosong atau berisi spasi saja.
- **Issue #002:** Menambahkan validasi `pemain < 0` untuk menolak input pemain aktif negatif.
- **Issue #003:** Memperbaiki bug perhitungan statistik dashboard dengan mengubah inisialisasi `totalPemain = 0` dan konversi `Number()`.
- **Issue #005:** Memperbaiki fungsi hapus agar menghapus item sesuai nama game yang dipilih serta menambahkan dialog konfirmasi `confirm()`.

### Added (Perfective & Preventive Maintenance)
- **Issue #004:** Menambahkan pengecekan anti-duplikasi nama game (`dataGame.some(...)`).
- Menambahkan validasi format huruf awal pada nama game dan developer, serta khusus huruf pada genre.
- Menambahkan fitur pencarian langsung (*live search*) berdasarkan nama, genre, maupun developer.

## [1.0.0] - `bug.html`
### Added
- Rilis awal aplikasi Manajemen Game Roblox (mengandung 5 bug fungsional dan logika untuk bahan evaluasi maintenance).