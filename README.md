# Akuisisi Data Tempat Wisata Bali

## 1. Deskripsi Project
Project ini merupakan tugas praktik individu mata kuliah Akuisisi dan Manajemen Data INSTIKI.
Project yang saya buat bertujuan untuk mengambil data pariwisata di Bali menggunakan metode API yang legal.

## 2. Sumber Data
- **Nama:** OpenStreetMap
- **Penerbit:** OpenStreetMap Contributors
- **Website:** https://www.openstreetmap.org/
- **API:** https://overpass-api.de/api/interpreter
- **Lisensi:** Open Database License (ODbL)
- **Atribusi:** © OpenStreetMap contributors.

## 3. Waktu Akuisisi
- **Tanggal dan Waktu:** 2026-11-16 (sesuai catatan pada `docs/provenance.json`)

## 4. Metode Akuisisi
Metode yang digunakan adalah API menggunakan Python `requests`.
- **Endpoint:** https://overpass-api.de/api/interpreter
- **Wilayah pengambilan data:** Bali, Indonesia.
- **Parameter:** Objek dengan kategori `tourism`.

## 5. Etika dan Batasan
- Menggunakan sumber data publik.
- Mengikuti lisensi ODbL.
- Mencantumkan atribusi OpenStreetMap.
- Menggunakan `User-Agent` yang mencantumkan identitas pengambil.
- Menggunakan `timeout` dan jeda antar-request (`time.sleep`).
- Menghindari request berulang yang tidak diperlukan.
- Tidak mengambil data pribadi.
- Tidak menyimpan API key di notebook.

## 6. Penjelasan Kolom Dataset
| Kolom | Keterangan |
| :--- | :--- |
| `osm_id` | ID objek OpenStreetMap |
| `osm_type` | Jenis objek OSM |
| `nama_tempat` | Nama tempat |
| `kategori_wisata` | Kategori wisata |
| `kategori_historis` | Kategori historis |
| `latitude` | Garis lintang |
| `longitude` | Garis bujur |
| `website` | Website tempat jika tersedia |

## 7. Cara Menjalankan
1. Buka Google Colab.
2. Buka notebook di folder `notebooks`.
3. Jalankan seluruh sel dari awal.
4. Pastikan koneksi internet tersedia.
5. Periksa hasil dataset pada `data/raw/`.

## 8. Struktur Project
- `notebooks/`: notebook akuisisi data.
- `data/raw/`: dataset mentah.
- `docs/`: dokumentasi provenance dan etika.
