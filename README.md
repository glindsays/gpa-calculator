# Kalkulator Target IPK Mahasiswa

Aplikasi web single page untuk menghitung IPK minimal yang harus diperoleh pada
semester berjalan agar IPK kumulatif mencapai target kelulusan.

## Masalah yang Diselesaikan

Banyak mahasiswa menunda urusan nilai. Mereka tahu target IPK kelulusan atau
target IPK semester depan, tapi tidak tahu angka berapa yang harus dikumpulkan
semester ini untuk mencapainya. Akibatnya, semester berjalan terlewati tanpa arah
dan target kelulusan baru terasa saat mendekati batas waktu.

Kalkulator ini menerjemahkan target IPK menjadi angka konkret: berapa rata-rata
per mata kuliah yang harus dicapai semester ini, dengan memperhitungkan bobot SKS
yang sudah diambil dan SKS yang sedang diambil.

## Fitur

- Empat input: IPK saat ini, total SKS yang sudah diambil, SKS semester ini, dan
  target IPK kelulusan/semester depan.
- Rumus perhitungan:

  ```
  IPK semester ini = ((Target IPK × (Total SKS + SKS Semester Ini))
                      - (IPK Saat Ini × Total SKS))
                     ÷ SKS Semester Ini
  ```

- Peringatan eksplisit bila hasil di atas **4.00**, karena target tidak realistis.
- Status hasil: hijau (target tercapai), kuning (sangat menantang, ≥ 3.50), dan
  merah (tidak realistis, > 4.00).
- Menampilkan IPK kumulatif akhir beserta rincian perhitungan.
- Validasi input dengan pesan error per field.
- Antarmuka responsif, mobile-friendly, tanpa dependensi eksternal.

## Cara Menjalankan

Aplikasi ini murni HTML, CSS, dan JavaScript tanpa build step, server, atau
dependency. Cukup buka `index.html` di browser:

1. Buka File Explorer, navigasi ke folder proyek ini.
2. Klik dua kali `index.html`, atau klik kanan lalu **Open with** browser Anda.

Alternatif, jalankan perintah ini dari dalam folder proyek:

```bash
start index.html
```

Alternatif kedua, bila Anda ingin aplikasi disajikan lewat server lokal:

```bash
python -m http.server 8000
```

lalu buka `http://localhost:8000` di browser.

## Teknologi

HTML5, CSS3, JavaScript vanilla. Tanpa framework, tanpa proses build, tanpa
langkah instalasi.

## Struktur Proyek

```
GPA-Calculator/
└── index.html
```

Seluruh aplikasi berada dalam satu file `index.html`.