# Studi Ablasi RNN, LSTM, GRU vs ANN untuk Prediksi Trafik Seluler Milan

Tugas Workshop Deep Learning — Teknik Telekomunikasi ITERA.

## Kelompok

Dikerjakan secara individu.

| Peran | Nama | NIM |
|---|---|---|
| Ketua (individu) | Zahra Shakilla | 124400021 |

- **Kelas:** RA
- **Lokasi kelompok:** 1 — Navigli (Darsena) (digit terakhir NIM terkecil)
- **Laporan:** `laporan-latex/main.pdf`

## Cara Menjalankan

```bash
uv sync
uv run jupyter lab
```

Buka `tugas_ablasi.ipynb`, isi `LOKASI_KELOMPOK`, lalu jalankan semua sel. Semua run tercatat di `hasil/ablasi.csv`.

Perangkat yang saya pakai: laptop ASUS Vivobook Flip 14 AMD Ryzen 7 4700U with Radeon Graphics, total waktu training: 89,6 menit.

## Ringkasan Hasil

Pada konfigurasi acuan di Duomo, RNN dan GRU (test MAE 229,6 dan 237,2) lebih baik daripada ANN (309,9) dan baseline naif terbaik (467,6). Test MAE konfigurasi terbaik (dipilih dengan val MAE): ANN 269,4 (W=6), RNN 224,5 (W=48), LSTM 245,6 (hidden 128), GRU 220,3 (hidden 128). Menggabungkan semua nilai terbaik justru lebih buruk daripada satu faktor terbaik. Di Navigli urutan model berubah (GRU 190,8 dan RNN 193,0 terbaik pada acuan) dan konfigurasi terbaik Duomo tidak konsisten lebih baik pada minggu uji.

## Struktur

## Data

Telecom Italia Big Data Challenge (Barlacchi dkk., 2015, *Scientific Data*, lisensi ODbL), versi per jam dari Zhang dkk. (INFOCOM 2021). Disiapkan oleh pengajar di repo [mctosima/dl-workshop](https://github.com/mctosima/dl-workshop).
