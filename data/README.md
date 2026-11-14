# Data

Dataset lengkap **tidak** disimpan di repo ini. Repo hanya berisi `sample/` (≤ 20 gambar yang sudah disensor) untuk contoh dan demo.

## Ringkasan

- Tautan folder Google Drive (akses terbatas): https://drive.google.com/drive/folders/1cwfMBu8_TSttkfKk5gQlDdswu6RdRzmx?usp=drive_link
- Jumlah citra: **200** gambar (200 baris anotasi; 200 berkas foto terdaftar).
- Foto sendiri per anggota: `nuryansyahsw27` **15**, `riyadhsmit1` **15**, `kautsarapp` **15**, `Oscarmulya` **15**; total **60**.
- Foto publik: **140** gambar; sumber Indonesian-License-Plate-Lighting-Dataset, lisensi **CC BY 4.0**: https://github.com/salsabilaputri95/Indonesian-License-Plate-Lighting-Dataset
- Jumlah baris anotasi: **200**; kolom `berkas,x,y,w,h,teks_pelat`.
- Cara pengambilan foto sendiri: dikumpulkan langsung oleh keempat anggota. Informasi perangkat, tanggal, dan lokasi umum sebaiknya didokumentasikan sesuai fakta masing-masing anggota; tidak diasumsikan di sini.
- Pelat pada publik dilokalisasi dari label YOLO dan teks pelat ditranskripsi serta diperiksa secara visual; hasil disimpan di Google Drive, bukan repo publik.

## Anotasi

Kotak lokasi pelat (x, y, lebar, tinggi dalam piksel) dan teks pelat tanpa spasi.

Simpan sebagai `anotasi.csv` di folder Drive, satu baris per citra (atau per pasangan), dengan kolom persis seperti [format_anotasi.csv](format_anotasi.csv). Baris contoh di berkas itu fiktif.

## Etika dan privasi

Wajah orang wajib diburamkan. Di data/sample, sebagian karakter pelat diburamkan. Teks pelat lengkap hanya disimpan di Drive. Jangan menulis NIM, nama orang lain, atau data pribadi lain di repo ini.
