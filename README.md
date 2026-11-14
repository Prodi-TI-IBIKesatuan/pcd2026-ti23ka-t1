# Deteksi dan Pengenalan Pelat Nomor Kendaraan

Proyek kelompok **Pengolahan Citra Digital 2026** · kelas `ti23ka` · topik **T1**

[![Cek proyek](https://github.com/Prodi-TI-IBIKesatuan/pcd2026-ti23ka-t1/actions/workflows/cek-proyek.yml/badge.svg)](https://github.com/Prodi-TI-IBIKesatuan/pcd2026-ti23ka-t1/actions/workflows/cek-proyek.yml)

**Lingkup kelompok kami:** Deteksi dan pengenalan karakter pelat nomor kendaraan bermotor pada foto kendaraan di lingkungan nyata.

Menemukan letak pelat nomor pada foto kendaraan di lingkungan nyata, lalu membaca karakternya. Anggota dan perannya ada di [ANGGOTA.yml](ANGGOTA.yml); cara kerja kelompok ada di [PANDUAN.md](PANDUAN.md).

## Notebook

| Notebook | Tahap | Isi | Buka |
| --- | --- | --- | --- |
| `01_dataset_preprocessing.ipynb` | 1 | Statistik dataset, cek anotasi, preprocessing, gambar sebelum–sesudah | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Prodi-TI-IBIKesatuan/pcd2026-ti23ka-t1/blob/main/notebooks/01_dataset_preprocessing.ipynb) |
| `02_metode_klasik.ipynb` | 2 | 2 metode klasik dan metriknya | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Prodi-TI-IBIKesatuan/pcd2026-ti23ka-t1/blob/main/notebooks/02_metode_klasik.ipynb) |
| `03_metode_modern.ipynb` | 2 | Inferensi model pralatih dan metriknya | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Prodi-TI-IBIKesatuan/pcd2026-ti23ka-t1/blob/main/notebooks/03_metode_modern.ipynb) |
| `04_evaluasi.ipynb` | 2 | Tabel perbandingan, uji ablasi, kasus gagal | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Prodi-TI-IBIKesatuan/pcd2026-ti23ka-t1/blob/main/notebooks/04_evaluasi.ipynb) |

## Dataset (Tahap 1)

- Jumlah citra: **200** (200 gambar terbaca dan beranotasi).
- Foto sendiri: **60**, masing-masing 15 foto dari nuryansyahsw27, riyadhsmit1, kautsarapp, dan Oscarmulya.
- Data publik: **140** gambar dari Indonesian-License-Plate-Lighting-Dataset, lisensi **CC BY 4.0**; sumber: https://github.com/salsabilaputri95/Indonesian-License-Plate-Lighting-Dataset. Anotasi YOLO digunakan sebagai kandidat kotak pelat dan teks pelat diperiksa manual.
- Format anotasi: `berkas,x,y,w,h,teks_pelat`; koordinat dalam piksel foto asli, teks tanpa spasi.
- Langkah preprocessing: resize maksimal 1024 piksel (rasio dipertahankan) → grayscale → CLAHE (`clipLimit=2.0`, `tileGridSize=(8,8)`) → sharpening/unsharp masking dengan Gaussian blur 5×5 → BGR untuk kompatibilitas visualisasi.

Rincian dataset, format anotasi, dan tautan Drive: [data/README.md](data/README.md). Contoh sebelum–sesudah di [outputs/figures/](outputs/figures/).

## Hasil (Tahap 2)

| Metode | Jenis | IoU | CER |
| --- | --- | --- | --- |
| [isi: nama metode klasik 1] | klasik | [isi] | [isi] |
| [isi: nama metode klasik 2] | klasik | [isi] | [isi] |
| [isi: nama model] | modern | [isi] | [isi] |

- **Uji ablasi:** [isi: parameter atau langkah yang diubah, dan pengaruhnya pada metrik]
- **Kasus gagal:** [isi: minimal 3 contoh dan penyebabnya, gambar di outputs/figures/]
- **Kesimpulan:** [isi: metode mana yang terbaik untuk lingkup kami dan mengapa]

## Demo

Aplikasi: [isi: tautan https://huggingface.co/spaces/...]

Unggah foto kendaraan, tampilkan kotak pelat dan teks yang terbaca. Kode aplikasi ada di [app/](app/).

## Sumber dan atribusi

Tuliskan setiap kode, model, dataset, atau bantuan AI yang dipakai beserta sumbernya. Pemakaian tanpa sumber dihitung plagiarisme.

| Yang dipakai | Sumber | Dipakai untuk |
| --- | --- | --- |
| [isi] | [isi] | [isi] |
