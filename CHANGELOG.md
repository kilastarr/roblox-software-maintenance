# Changelog

## [1.1.0] — FIX Version
### Fixed (Corrective Maintenance)
- Validasi kolom wajib menggunakan `.trim()` dan penandaan merah pada kolom yang kosong (BUG-001).
- Validasi jumlah pemain aktif agar tidak bernilai negatif `< 0` (BUG-002).
- Perbaikan label status publikasi menjadi "Terverifikasi & Aktif" (BUG-003).

### Added (Preventive & Adaptive Maintenance)
- Pencegahan duplikasi nama game terhadap katalog referensi dan data tersimpan.
- Tata letak responsif mobile (`@media (max-width: 700px)` dan `tabel-scroll`) agar nyaman digunakan di layar HP tanpa melebar.

## [1.0.0] — BUG Version
### Added
- Dashboard statistik, katalog game Roblox, formulir input, simulasi perbandingan kode, dan penyimpanan riwayat di `localStorage`.