# Evalusai Tengah Semester PBKK C

### Lampiran & Source Code Proyek: <br>
Project Blog : [Link](https://aminudinwijaya25.blogspot.com/2026/10/tugas-week-7-pbkk-c-tugas-kelompok.html)
PRD (Product Requirement Documents) : [Link](https://docs.google.com/document/d/1KNcMuJ8tfM7rHSonIshSZgrMpbPjbxR_3NZptWiBrBg/edit?usp=sharing) <br>
Source Code : [Link](https://github.com/KangZERO650/Tugas-Week-7-PBKK-C) <br>
Demo : [Link](https://youtu.be/KbPny8O5P1E)

## 1. Jelaskan perbedaan aplikasi desktop dengan aplikasi lain? Mengapa masih dibutuhkan
 
Aplikasi desktop dipasang dan dijalankan langsung di sistem operasi komputer (pada SIHIFA: Windows lewat WPF/.NET). Aplikasi web berjalan di browser dan bergantung pada server, sedangkan aplikasi mobile berjalan di Android/iOS dengan layar kecil dan input sentuhan.
 
| Aspek | Desktop (native) | Web / Cloud | Mobile |
| :---- | :---- | :---- | :---- |
| Tempat berjalan | Langsung di OS, memakai sumber daya perangkat keras | Browser, bergantung pada server dan internet | Smartphone/tablet |
| Koneksi internet | Bisa sepenuhnya offline | Umumnya wajib online | Bervariasi |
| Penyimpanan data | Lokal | Server milik penyedia layanan | Lokal dan cloud |
| Performa | Tinggi, akses penuh ke CPU, RAM, dan file system | Dibatasi browser dan jaringan | Dibatasi baterai dan layar |
| Kendali data | Penuh di tangan pengguna | Dipegang penyedia layanan | Campuran |
| Cocok untuk | Pekerjaan data besar, multitasking, tampilan lebar | Akses lintas perangkat dan kolaborasi | Mobilitas dan penggunaan cepat |
 
### Mengapa aplikasi desktop masih dibutuhkan
 
- **Offline-first.** Aplikasi tetap bisa dipakai tanpa internet. Ini berbeda dengan aplikasi berbasis web yang membutuhkan koneksi.
- **Performa dan efisiensi.** Aplikasi native WPF jauh lebih ringan daripada web atau wrapper Electron yang sering memakan RAM berlebih.
- **Keamanan Privasi** Seluruh data tersimpan di mesin pengguna tanpa terhubung dengan pihak ketiga, sehingga tidak terpengaruh perubahan kebijakan atau penutupan layanan SaaS.
- **Akses ke sistem file.** Backup/restore database `.db`, ekspor JSON/CSV, dan cache gambar lokal dapat dilakukan langsung lewat dialog Windows.
 
## 2. Tuliskan problem yang akan diselesaikan oleh aplikasi yang kamu buat? Definisikan fitur aplikasi yang merupakan solusi dari problem tersebut.
 
| Problem | Fitur solusi (SIHIFA) |
| :---- | :---- |
| **Data tersebar di banyak platform.** Anime di MyAnimeList, film di Letterboxd, musik di Spotify, buku di Goodreads, dan catatan di Notion, sehingga sulit melihat seluruh koleksi dalam satu tempat. | **CRUD multi-entitas (P0)**: satu aplikasi untuk Anime, Film, Musik, Buku, dan Materi, dengan form tervalidasi (`INotifyDataErrorInfo`). **Dashboard statistik dan grafik (P1)**: kartu Total Koleksi, Selesai, Wishlist, serta grafik distribusi genre/rating (LiveCharts2). |
| **Ketergantungan SaaS dan risiko privasi.** Layanan online bisa berubah menjadi berbayar, menutup API, atau memonetisasi data. | **Local SQLite engine (P0)**: data tersimpan lokal dengan transaksi ACID. |
| **Aplikasi web terlalu berat dan butuh internet.** | **Aplikasi native WPF/.NET dengan arsitektur MVVM**: ringan, startup cepat, dan berjalan offline. |
| **Sulit mencari di koleksi besar.** | **Instant filter dan DataGrid ter-virtualisasi (P0)**: pencarian real-time lewat `CollectionViewSource` untuk judul, kreator, dan kategori, serta tampilan Card View. |
| **Ketidaknyamanan visual**, terutama saat dipakai malam hari. | **Navigasi sidebar dan theme toggle (P0)**: dark/light mode yang berganti instan tanpa restart (`DynamicResource`). |
| **Input metadata manual yang cukup banyak**| **Asynchronous API fetcher (P1)**: mengambil sinopsis dan poster dari AniList, TMDB, atau OpenLibrary secara opsional. Gambar di-cache di folder lokal dan jika gagal aplikasi beralih ke mode manual tanpa crash. |
| **Ingin merangking dan membagikan favorit secara visual.** | **Tier List Generator (P2)**: kanvas drag-and-drop untuk tingkatan S/A/B/C/D yang dapat disimpan sebagai gambar PNG. |

## 3. Buat Poster Infografis aplikasi yang telah dibuat dalam 1 halaman

<img width="2400" height="7600" alt="Infografis SIHIFA (3)" src="https://github.com/user-attachments/assets/53e88637-f2d1-48f9-940d-60733b8ff420" />


## Dokumentasi

<img width="1600" height="950" alt="SIHIFA-1" src="https://github.com/user-attachments/assets/189409d8-558d-45eb-9ad7-b0ac7e303487" />
<img width="1600" height="950" alt="SIHIFA-2" src="https://github.com/user-attachments/assets/6950d77c-3eb2-4c1e-8814-fbd2b69e2592" />
<img width="1600" height="950" alt="SIHIFA-3" src="https://github.com/user-attachments/assets/153f6a64-a9d3-4881-bf24-cc7aeb40902a" />
<img width="1600" height="950" alt="SIHIFA-4" src="https://github.com/user-attachments/assets/7c954e90-e3c3-4f9b-991c-faf944295f30" />
<img width="1600" height="950" alt="SIHIFA-5" src="https://github.com/user-attachments/assets/efc90154-428b-4322-b2a4-e93edf5cca7f" />
