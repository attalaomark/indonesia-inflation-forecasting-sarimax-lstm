# Indonesia Inflation Forecasting: Hybrid SARIMAX–LSTM

Repositori ini memuat kode dan data penelitian skripsi **“Peramalan Inflasi Indonesia Berdasarkan IHK Menggunakan Hybrid SARIMAX–LSTM dengan Indikator Makroekonomi Domestik dan Global.”**

## Ruang lingkup

- Target: Inflasi Indonesia Berdasarkan IHK *Year-on-Year* (YoY).
- Periode: Januari 1990–Desember 2025.
- Indikator domestik: suku bunga acuan, kurs USD/IDR, dan cadangan devisa.
- Indikator global: harga minyak WTI, harga pangan global, harga emas dunia, dan indeks volatilitas global (VIX).
- Model: SARIMAX, LSTM, dan Hybrid SARIMAX–LSTM berbasis koreksi residual.
- Skenario: BASE, DOM (Domestik), GLOBAL, dan ALL (Domestik dan Global).

## Struktur repositori

```text
.
├── notebooks/
│   └── inflation_forecasting_sarimax_lstm.ipynb
├── data/
│   ├── README.md
│   ├── DATA_LICENSE.md
│   ├── raw/
│   │   └── delapan berkas Excel sumber penelitian
│   └── processed/
│       ├── delapan berkas CSV terstandar
│       ├── dataset_model_final.csv
│       ├── source_manifest.csv
│       ├── data_dictionary.csv
│       ├── validation_report.csv
│       └── SHA256SUMS.txt
├── results/
├── requirements.txt
├── .gitignore
└── CODE_AUDIT.md
```

## Menjalankan notebook

Gunakan Python 3.12.

```bash
python -m venv .venv
pip install -r requirements.txt
```

Buka `notebooks/inflation_forecasting_sarimax_lstm.ipynb`, kemudian jalankan seluruh sel secara berurutan. Notebook membaca XLSX dari `data/processed/` dan menyimpan hasil ke `results/`.

## Validasi

Seluruh variabel memiliki 432 observasi bulanan dari Januari 1990 sampai Desember 2025, tanpa bulan hilang, tanggal duplikat, atau nilai kosong. Rincian tersedia pada `data/processed/validation_report.csv`.

## Hasil Akhir Revisi

| Model/kriteria | MAE | RMSE | MASE |
|---|---:|---:|---:|
| Hybrid_DOM | 0.3225 | 0.4779 | 0.3523 |
| SARIMAX_DOM | 0.3256 | 0.5004 | 0.3558 |
| RMSE terendah: Hybrid_GLOBAL | 0.3586 | 0.4705 | 0.3918 |

Hybrid_DOM dipilih sebagai model utama karena memperoleh MAE dan MASE terendah. Seluruh tabel dan gambar terpilih tersedia pada folder `results/`.
