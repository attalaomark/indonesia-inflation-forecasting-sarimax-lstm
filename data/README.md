# Data Penelitian

Folder data dibagi menjadi dua lapisan:

- `raw/`: delapan berkas Excel yang benar-benar digunakan sebagai sumber penelitian.
- `processed/`: data CSV terstandar yang dibaca oleh notebook.

## Periode dan kualitas data

- Periode penelitian: Januari 1990–Desember 2025.
- Frekuensi: bulanan.
- Jumlah observasi setiap variabel: 432.
- Format tanggal CSV: `YYYY-MM-01`.
- Nilai kosong: tidak ada.
- Tanggal duplikat: tidak ada.
- Bulan yang hilang: tidak ada.

Berkas inflasi sumber mencakup Januari 1989–Desember 2025. Untuk konsistensi dengan variabel lain dan batasan penelitian, data yang digunakan dimulai Januari 1990.

## Berkas terproses

| Berkas | Kolom nilai |
|---|---|
| `inflasi_ihk_yoy.csv` | `inflasi_yoy_pct` |
| `suku_bunga_acuan.csv` | `suku_bunga_acuan_pct` |
| `kurs_usd_idr.csv` | `kurs_usd_idr` |
| `cadangan_devisa.csv` | `cadangan_devisa_juta_usd` |
| `harga_minyak_wti.csv` | `harga_minyak_wti_usd_per_barel` |
| `harga_pangan_global.csv` | `harga_pangan_global_usd_per_ton` |
| `harga_emas_dunia.csv` | `harga_emas_dunia_usd_per_troy_ounce` |
| `indeks_vix.csv` | `indeks_vix` |
| `dataset_model_final.csv` | seluruh variabel dalam satu tabel |

## Dokumentasi tambahan

- `source_manifest.csv`: hubungan antara berkas unggahan, berkas mentah repositori, sheet, periode, dan checksum.
- `data_dictionary.csv`: definisi variabel dan satuan.
- `validation_report.csv`: hasil pemeriksaan kelengkapan.
- `SHA256SUMS.txt`: checksum berkas CSV untuk pemeriksaan integritas.

## Catatan lisensi

Penyertaan berkas tidak mengubah hak cipta atau ketentuan penggunaan sumber asli. Pastikan setiap penyedia data mengizinkan redistribusi publik sebelum repositori dipertahankan dalam status publik.
