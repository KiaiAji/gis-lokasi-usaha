# GIS Lokasi Usaha

**Sistem Rekomendasi Lokasi Usaha Berbasis Analisis Spasial Menggunakan Python**

## Deskripsi Proyek

Proyek ini merupakan studi kasus penerapan *Geographic Information System* (GIS) untuk membantu menentukan lokasi usaha yang potensial berdasarkan data geografis dan beberapa kriteria, seperti jumlah penduduk dan jarak terhadap lokasi pesaing.

Program dibuat menggunakan Python untuk menghitung jarak antar lokasi, menghitung jumlah pesaing dalam radius tertentu, serta memberikan skor rekomendasi untuk setiap kandidat lokasi usaha.

Proyek ini dibuat sebagai implementasi materi tentang karier dan penerapan GIS di era industri.

## Tujuan

- Memahami penerapan GIS dalam analisis lokasi usaha.
- Menggunakan Python untuk mengolah data geografis sederhana.
- Menghitung jarak antara lokasi usaha dan lokasi pesaing.
- Membandingkan kandidat lokasi berdasarkan kriteria tertentu.
- Menghasilkan rekomendasi lokasi usaha berdasarkan skor analisis.

## Teknologi yang Digunakan

- **Python** — bahasa pemrograman utama.
- **Pandas** — mengolah dan menganalisis data.
- **Matplotlib** — dapat digunakan untuk visualisasi data.
- **Jupyter Notebook / Google Colab** — menjalankan eksperimen dan analisis.

## Struktur Proyek

```text
gis-lokasi-usaha/
├── main.py
├── gis_lokasi_usaha_colab.ipynb
├── hasil_rekomendasi.csv
├── requirements.txt
├── README.md
└── .gitignore
```

## Cara Kerja Program

1. Menyiapkan data kandidat lokasi usaha beserta koordinat dan jumlah penduduk.
2. Menyiapkan data koordinat lokasi pesaing.
3. Menghitung jarak antara kandidat lokasi dan pesaing menggunakan rumus Haversine.
4. Menghitung jumlah pesaing dalam radius 1 kilometer.
5. Menghitung skor setiap kandidat berdasarkan jumlah penduduk dan tingkat persaingan.
6. Menampilkan hasil analisis dan kandidat lokasi dengan skor tertinggi.
7. Menyimpan hasil rekomendasi ke file CSV.

## Cara Menjalankan

### 1. Clone repository

```bash
git clone https://github.com/USERNAME/gis-lokasi-usaha.git
cd gis-lokasi-usaha
```

Ganti `USERNAME` dengan nama pengguna GitHub kamu.

### 2. Instal dependensi

```bash
pip install -r requirements.txt
```

### 3. Jalankan program

```bash
python main.py
```

Hasil analisis akan ditampilkan di terminal dan disimpan dalam file `hasil_rekomendasi.csv`.

### Alternatif: Google Colab

Buka file `gis_lokasi_usaha_colab.ipynb` melalui Google Colab, lalu jalankan setiap sel kode secara berurutan.

## Metode Analisis

Program menggunakan rumus Haversine untuk memperkirakan jarak antara dua titik berdasarkan koordinat lintang (*latitude*) dan bujur (*longitude*).

Skor rekomendasi menggunakan pembobotan sederhana:

- 70% berdasarkan jumlah penduduk.
- 30% berdasarkan jumlah pesaing, dengan asumsi semakin sedikit pesaing maka lokasi semakin menarik.

Bobot tersebut merupakan asumsi untuk studi kasus dan dapat diubah sesuai kebutuhan penelitian.

## Contoh Hasil

Program menghasilkan tabel kandidat lokasi yang berisi informasi seperti:

- Nama kandidat lokasi.
- Jumlah penduduk.
- Jumlah pesaing dalam radius 1 kilometer.
- Skor rekomendasi.

Lokasi dengan skor tertinggi menjadi kandidat yang direkomendasikan oleh model sederhana ini.

## Catatan dan Keterbatasan

- Data lokasi, koordinat, jumlah penduduk, dan pesaing yang digunakan merupakan **data simulasi**.
- Hasil program belum dapat dijadikan dasar keputusan bisnis nyata.
- Skor yang dihasilkan hanya merupakan model awal, bukan jaminan bahwa suatu lokasi akan sukses.
- Proyek ini merupakan prototipe analisis menggunakan Python, bukan aplikasi Web GIS interaktif.
- Untuk pengembangan lebih lanjut, proyek dapat menggunakan data geografis nyata, peta interaktif, database spasial seperti PostGIS, serta framework web.

## Pengembangan Selanjutnya

- Menampilkan kandidat lokasi pada peta interaktif.
- Mengintegrasikan data geografis nyata.
- Menambahkan kriteria aksesibilitas dan jaringan jalan.
- Mengembangkan aplikasi Web GIS.
- Menggunakan database spasial untuk menyimpan dan menganalisis data.

## Kesimpulan

Studi kasus ini menunjukkan bahwa GIS dan pemrograman Python dapat digunakan untuk membantu analisis lokasi usaha melalui pengolahan data geografis, penghitungan jarak, dan pemeringkatan kandidat lokasi. Proyek ini juga menjadi dasar untuk mempelajari pengembangan sistem rekomendasi berbasis GIS.

## Lisensi

Proyek ini dibuat untuk tujuan pembelajaran dan pengembangan akademik.
