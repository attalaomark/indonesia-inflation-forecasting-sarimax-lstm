# Final Results

Folder ini berisi keluaran akhir yang dipilih dari `revisi.zip`. Berkas duplikat, nama lama, grafik prediksi individual yang berulang, dan tabel yang identik tidak disertakan.

## Ringkasan hasil

| Kriteria | Model | Nilai |
|---|---|---:|
| MAE terendah | Hybrid_DOM | 0.3225 |
| RMSE terendah | Hybrid_GLOBAL | 0.4705 |
| MASE terendah | Hybrid_DOM | 0.3523 |

`Hybrid_DOM` dipilih sebagai model terbaik karena memperoleh nilai MASE terendah sebesar 0,3523. MASE digunakan sebagai metrik utama dalam pemilihan model pada penelitian ini. Model tersebut juga memperoleh MAE terendah sebesar 0,3225, sedangkan RMSE terendah diperoleh `Hybrid_GLOBAL` sebesar 0,4705. Dibandingkan `SARIMAX_DOM`, perbaikannya adalah:

- MAE: 0.3256 menjadi 0.3225 (0.95% lebih rendah).
- RMSE: 0.5004 menjadi 0.4779 (4.50% lebih rendah).
- MASE: 0.3558 menjadi 0.3523 (0.98% lebih rendah).

Perlu dicatat bahwa model dengan RMSE terendah adalah `Hybrid_GLOBAL`, sehingga klaim “model terbaik” harus selalu menyebutkan dasar metriknya.

## Struktur

```text
results/
├── tables/
│   ├── core/
│   │   ├── model_evaluation.csv
│   │   ├── test_predictions.csv
│   │   ├── sarimax_orders.csv
│   │   ├── sarimax_residual_ljungbox.csv
│   │   ├── best_hyperparameters_lstm_hybrid.csv
│   │   └── tabel inti lainnya
│   └── tuning/
│       ├── empat tabel kandidat AIC SARIMA/SARIMAX
│       └── delapan tabel grid search 54 kombinasi
└── figures/
    ├── eda/
    ├── diagnostics/
    └── forecast/
```

## Pemilihan berkas

Disertakan:

- tabel evaluasi akhir dan prediksi data uji;
- order SARIMA/SARIMAX;
- diagnostik Ljung–Box;
- hyperparameter terbaik;
- seluruh grid tuning 54 kombinasi;
- pengaruh skenario BASE, DOM, GLOBAL, dan ALL;
- visualisasi EDA utama, diagnostik, dan hasil peramalan.

Tidak disertakan:

- file CSV yang isinya identik dengan file lain;
- file lama `SARIMAX_BASE` yang telah digantikan `SARIMA_BASE`;
- grafik `beras` lama karena variabel final menggunakan nama Harga Pangan Global;
- 12 grafik prediksi individual karena sudah diwakili grafik model terbaik dan grafik seluruh model;
- tabel top-10 tuning karena seluruh 54 kombinasi sudah tersedia.
