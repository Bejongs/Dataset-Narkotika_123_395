# Dataset Putusan Narkotika PN Palembang

> Dataset putusan pengadilan untuk memenuhi tugas **Sub-CPMK 2 - Metadata, Format Dokumen, dan Markup Language** pada mata kuliah Temu Kembali Informasi.

![Dataset](https://img.shields.io/badge/Dataset-50%20Putusan-0B6E4F)
![Format](https://img.shields.io/badge/Format-PDF%20%7C%20XLSX-2563EB)
![Tahun](https://img.shields.io/badge/Tahun-2025-F59E0B)
![Pengadilan](https://img.shields.io/badge/PN-Palembang-7C3AED)

## Identitas Kelompok

| Anggota | Nama | NIM |
|---|---|---|
| 1 | `Maulana Bima Hedy Pratama` | `202310370311123` |
| 2 | `Novita Dian Nazarina` | `202310370311395` |

Nama repository yang digunakan:

```text
Dataset-Narkotika_123_395
```

## Tentang Dataset

Dataset ini terdiri atas **50 dokumen putusan Pengadilan Negeri Palembang** pada perkara **Pidana Khusus - Narkotika dan Psikotropika** tahun 2025. Dokumen diperoleh secara manual dari Direktori Putusan Mahkamah Agung Republik Indonesia dan disimpan dalam format PDF.

Dataset disusun untuk mempelajari:

- pengelolaan koleksi dokumen hukum;
- identifikasi metadata putusan;
- struktur dan format dokumen PDF;
- penyusunan ringkasan data dalam spreadsheet; dan
- persiapan dataset untuk proses Temu Kembali Informasi.

## Ringkasan Koleksi

| Informasi | Nilai |
|---|---:|
| Jumlah dokumen PDF | 50 |
| Nomor putusan unik | 50 |
| Hash SHA-256 unik | 50 |
| Lembaga peradilan | PN Palembang |
| Kategori perkara | Pidana Khusus |
| Klasifikasi | Narkotika dan Psikotropika |
| Tahun putusan | 2025 |
| Barang bukti teridentifikasi | 50 dokumen |
| Amar putusan teridentifikasi | 50 dokumen |
| Bahasa dokumen | Bahasa Indonesia |

## Struktur Repository

```text
Dataset-Narkotika_XXX_YYY/
├── Dataset/
│   └── Narkotika.zip
├── Overview/
│   └── Overview.xlsx
└── README.md
```

### `Dataset/Narkotika.zip`

Arsip ZIP berisi 50 dokumen putusan asli dalam format PDF. Nama file dipertahankan agar setiap dokumen dapat ditelusuri kembali dan dicocokkan dengan metadata pada workbook.

### `Overview/Overview.xlsx`

Workbook berisi ringkasan seluruh putusan. Sheet utama menggunakan kolom yang diwajibkan dalam panduan tugas:

| Kolom | Deskripsi |
|---|---|
| `No` | Nomor urut dokumen |
| `No Putusan` | Nomor perkara pada putusan |
| `Lembaga Peradilan` | Pengadilan yang menerbitkan putusan |
| `Barang Bukti` | Barang bukti yang disebutkan dalam putusan |
| `Amar Putusan` | Bagian amar atau keputusan majelis hakim |

Workbook juga menyediakan sheet **Audit** dan **ReadMe** untuk membantu pemeriksaan metadata, sumber ekstraksi, nama file, jumlah halaman, hash dokumen, serta catatan validasi.

## Metode Penyusunan

1. Memilih satu Pengadilan Negeri, yaitu PN Palembang.
2. Memilih kategori Pidana Khusus dan klasifikasi Narkotika dan Psikotropika.
3. Mengunduh dokumen putusan dari Direktori Putusan Mahkamah Agung RI.
4. Memeriksa keterbacaan dan keutuhan setiap PDF.
5. Mengidentifikasi nomor putusan, lembaga peradilan, barang bukti, dan amar putusan.
6. Menyusun metadata ke dalam `Overview.xlsx`.
7. Memeriksa nomor perkara dan hash SHA-256 untuk mencegah dokumen duplikat.
8. Mengemas seluruh PDF ke dalam `Narkotika.zip`.

## Kualitas dan Validasi Data

Validasi yang telah dilakukan:

- seluruh file dapat dibuka sebagai dokumen PDF;
- 50 nomor putusan berbeda;
- 50 hash SHA-256 berbeda;
- seluruh dokumen berasal dari PN Palembang;
- seluruh nomor perkara menggunakan kode `Pid.Sus`;
- konteks perkara narkotika ditemukan pada seluruh dokumen;
- kolom barang bukti dan amar putusan terisi untuk seluruh data; dan
- file PDF asli tidak dimodifikasi.

Barang bukti diutamakan dari bagian amar putusan. Pada 10 dokumen yang tidak mencantumkan daftar barang bukti secara lengkap pada amar akhir, informasi diambil dari bagian tuntutan Penuntut Umum dan diberi penanda `tuntutan_penuntut_umum` pada sheet **Audit**.

## Status Berkekuatan Hukum Tetap

Status berkekuatan hukum tetap tidak selalu tercantum di dalam file PDF. Oleh karena itu, status setiap putusan harus diperiksa kembali melalui halaman detail Direktori Putusan Mahkamah Agung sebelum tugas dikumpulkan.

Dataset ini tidak menganggap ketiadaan tulisan status di dalam PDF sebagai bukti bahwa putusan belum berkekuatan hukum tetap.

## Sumber Data

Seluruh dokumen bersumber dari:

**Direktori Putusan Mahkamah Agung Republik Indonesia**  
<https://putusan3.mahkamahagung.go.id/>

Dokumen digunakan untuk kepentingan akademik dan pembelajaran. Isi putusan tetap menjadi bagian dari sumber resmi yang menerbitkannya.

## Batasan Dataset

- Dataset hanya mencakup PN Palembang.
- Seluruh dokumen dalam koleksi ini memiliki nomor perkara tahun 2025.
- Metadata diperoleh melalui ekstraksi dan pemeriksaan dokumen sehingga masih memerlukan verifikasi manusia.
- Tata letak antarputusan tidak selalu seragam.
- Informasi status BHT harus diverifikasi pada halaman detail sumber.
- Kesalahan penulisan yang berasal dari putusan asli tidak diubah di dalam PDF.

## Cara Menggunakan Dataset

1. Unduh atau clone repository ini.
2. Ekstrak `Dataset/Narkotika.zip`.
3. Buka `Overview/Overview.xlsx` untuk melihat ringkasan metadata.
4. Gunakan kolom `No Putusan` atau nama file untuk mencocokkan metadata dengan PDF asli.

```bash
git clone https://github.com/USERNAME/Dataset-Narkotika_XXX_YYY.git
cd Dataset-Narkotika_XXX_YYY
```

<div align="center">
  <strong>Sub-CPMK 2 - Temu Kembali Informasi</strong><br>
  Dataset Putusan Narkotika PN Palembang
</div>
