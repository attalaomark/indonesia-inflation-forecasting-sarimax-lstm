# Code Audit

## Basis yang dipilih

`RAPI_PRESENTASI` dipilih sebagai basis karena struktur, narasi, dan pemisahan fungsi lebih mudah dibaca. `REVISI` sebaiknya dipertahankan hanya sebagai arsip keluaran lama.

## Perbaikan

1. Jalur lokal diganti jalur relatif repositori.
2. Nama berkas, kolom, periode, duplikasi tanggal, dan nilai kosong divalidasi.
3. Folder hasil dibersihkan sebelum eksekusi.
4. Kesalahan `SARIMAX_BASE` diperbaiki menjadi `SARIMA_BASE`.
5. Seed dan operasi deterministik diperkuat.
6. `val_s1` tidak lagi dipakai ulang sebagai validasi setelah sudah masuk `train_s2`.
7. Training final memakai `best_epoch` dari Stage 1.
8. Riwayat prediksi test tidak menggandakan periode validasi.
9. Output lama notebook dihapus.

## Wajib sebelum publikasi

- Jalankan ulang seluruh notebook dengan data final sampai Desember 2025.
- Cocokkan MAE, RMSE, MASE, order SARIMAX, dan hyperparameter dengan naskah akhir.
- Periksa ketentuan redistribusi data.

## Keluaran Akhir Revisi

Folder `results/` telah diperbarui menggunakan keluaran pada `revisi.zip`. Hasil utama versi ini adalah:

- Hybrid_DOM: MAE 0.3225, RMSE 0.4779, MASE 0.3523.
- SARIMAX_DOM: MAE 0.3256, RMSE 0.5004, MASE 0.3558.
- Hybrid_GLOBAL memperoleh RMSE terendah, yaitu 0.4705.
- Pemilihan Hybrid_DOM sebagai model utama didasarkan pada MAE dan MASE, bukan seluruh metrik sekaligus.

Notebook publik mempertahankan alur final run agar konsisten dengan keluaran revisi, dengan perubahan hanya pada jalur data, nama berkas, dokumentasi, dan koreksi label SARIMA_BASE.
