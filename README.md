# CI4 K‑Means + Elbow (Project Template)

Deskripsi singkat
- Aplikasi web sederhana untuk melakukan clustering K‑Means dari file CSV, dengan pra‑proses (imputasi, encoding, scaling), KMeans++ init, perhitungan SSE untuk rentang K, dan deteksi elbow otomatis.
- Dibangun untuk CodeIgniter 4 (file ini berisi Controller, Service, Views, Routes).

Instalasi cepat
1. Buat proyek CodeIgniter 4 (jika belum):
   - composer create-project codeigniter4/appstarter myci
   - cd myci
2. Salin file‑file dari folder `app/` dan `app/Views/` yang saya sediakan ke dalam proyekmu:
   - app/Controllers/KmeansController.php
   - app/Services/KMeansService.php
   - app/Views/upload.php
   - app/Views/result.php
   - app/Config/Routes.php (opsional: gabungkan route bagian bawah jika ingin mempertahankan routes default)
3. Jalankan server dev:
   - php spark serve
   - buka http://localhost:8080
4. Upload CSV lewat halaman utama, atur separator/header/max K, tekan Run.

Catatan & rekomendasi
- Data kategorikal di‑one‑hot encode; hati‑hati untuk cardinality tinggi.
- Implementasi dimaksudkan untuk dataset kecil‑sedang. Untuk dataset besar, gunakan backend Python/DB/queue.
- Untuk produksi tambahkan validasi file, pembatasan ukuran, dan authentication.

Fitur pengembangan yang bisa saya tambahkan:
- API REST untuk integrasi mobile
- Export clustering ke CSV
- Silhouette score / metrik validasi tambahan
- Queue / background processing untuk dataset besar
- Dockerfile + nginx + php-fpm
