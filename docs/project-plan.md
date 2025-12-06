# Project Plan  
Self Photoshoot / Photobox Web App  
Teknologi: Laravel 12 + Blade + JavaScript (Frontend), HTML Canvas (Image Processing)

---

## 1. Tujuan Proyek
Membuat aplikasi web photobox mandiri yang mampu:
- Menggunakan berbagai jenis kamera (webcam/DSLR/capture card).
- Mengambil beberapa foto (layout 2×2).
- Menghasilkan file A4 landscape siap cetak.
- Menambahkan watermark event.
- Menyediakan tampilan UI yang mudah digunakan.
- Memiliki workflow kerja yang jelas antara tim desainer dan tim developer.

---

## 2. Ruang Lingkup Fitur
### Fitur Utama
- Pemilihan kamera.
- Pengaturan resolusi kamera.
- Tampilan live preview.
- Timer countdown.
- Multi-shot (4 foto).
- Galeri sementara (session based).
- Pembuatan layout A4 landscape.
- Watermark pada hasil akhir.
- Download hasil.
- Upload gambar alternatif.

### Fitur Opsional
- Sistem penyimpanan sesi.
- Mode layout selain 2×2.
- Pengaturan watermark.
- Riwayat sesi di Laravel backend.
- PDF output menggunakan Browsershot atau DOMPDF.

---

## 3. Struktur Tim dan Tanggung Jawab

### Tim Desainer (DKV)
Tanggung jawab:
- Mendesain UI/UX lengkap di Figma atau Balsamiq.
- Menyediakan seluruh aset visual (ikon, watermark, logo, background).
- Menentukan style guide (warna, font, ukuran komponen).
- Menyusun user flow sederhana.
- Melakukan revisi sesuai feedback PM dan developer.

Output tim desainer:
- File desain final (Figma/Balsamiq).
- Export aset: PNG/SVG, icon pack, watermark, logo.
- Style guide singkat.

---

### Tim Developer (RPL/PPLG)
Developer 1:
- Implementasi UI Blade berdasarkan desain Figma.
- Implementasi JavaScript untuk kamera (getUserMedia).
- Timer countdown.
- Capture foto dan galeri 4 foto.
- Event handling UI.

Developer 2:
- Implementasi generator A4 landscape berbasis canvas.
- Watermark otomatis.
- Mekanisme download.
- Error handling kamera.
- Integrasi ringan dengan Laravel jika diperlukan.

Output tim developer:
- Halaman photobox yang berfungsi penuh.
- Hasil gambar layout A4 siap cetak.
- Kode rapi dan mudah dibaca.

---

### Project Manager / Senior Developer
Tanggung jawab:
- Menentukan arsitektur dan batasan fitur.
- Membuat repo, branch workflow, dan dokumentasi awal.
- Memberikan pengarahan dan mentoring kepada tim.
- Melakukan review desain dan implementasi.
- Melakukan testing menyeluruh.
- Menyusun dokumentasi final.

Output:
- Project siap digunakan pada event atau produksi.
- Revisi dan perbaikan berdasarkan hasil uji coba.

---

## 4. Jadwal Pengerjaan (2 Minggu / 10 Hari Kerja)

### Minggu 1
Hari 1–2  
- Desainer membuat desain awal UI/UX.  
- PM membuat struktur Laravel dan folder frontend.

Hari 2–3  
- Developer mulai implementasi Blade berdasarkan desain awal.

Hari 4–5  
- Implementasi kamera, countdown, capture, dan galeri.

Review Minggu 1  
- PM melakukan review awal desain dan fitur.

### Minggu 2
Hari 1–2  
- Implementasi generator A4 landscape dan watermark.

Hari 3  
- Integrasi desain final dengan Blade.

Hari 4  
- Testing internal (developer + PM).

Hari 5  
- Testing user (panitia atau pengguna internal).

---

## 5. Pembagian Tugas Detail

### Tugas Tim Desainer
1. Membuat wireframe kasar di Figma atau Balsamiq.
2. Menyusun layout final untuk:
   - Halaman utama.
   - Halaman photobox.
   - Area preview A4.
3. Menentukan warna dan typografi.
4. Menyediakan aset visual:
   - Logo event.
   - Watermark Swakarya 2025.
   - Tombol, ikon, ilustrasi.
5. Menjelaskan interaksi UI dalam Figma (prototype mode).

### Tugas Tim Developer
1. Menerjemahkan desain ke Blade template.
2. Membuat komponen berdasarkan file desain:
   - Kamera preview.
   - Tombol aksi.
   - Galeri foto.
   - Preview A4.
3. Mengembangkan fitur JavaScript:
   - Ambil kamera dan resolusi.
   - Timer countdown.
   - Capture foto.
   - Penyimpanan sementara.
   - Render A4 layout 2×2 landscape.
4. Menyediakan fungsi download.
5. Menyelesaikan bug dan testing internal.

---

## 6. Workflow Kolaborasi Desainer → Developer

### Jika Desainer Menggunakan Figma
1. Desainer membuat halaman desain lengkap.
2. Desainer memberikan:
   - Link Figma dengan permission “Can View”.
   - Export aset (SVG/PNG).
   - Style guide.
3. Developer membuka Inspect Panel di Figma:
   - Mengambil ukuran komponen.
   - Mengambil warna, border, shadow.
   - Mengambil jarak antar elemen.
4. Developer mengimplementasikan UI Blade sesuai layout Figma.
5. Revisi jika:
   - Desain tidak realistis secara teknis.
   - Ada ketidaksesuaian ukuran atau proporsi.
6. Final approval oleh PM.

### Jika Desainer Menggunakan Balsamiq (Wireframe)
1. Desainer membuat wireframe low-fidelity.
2. PM dan developer mendiskusikan kemungkinan teknis.
3. Desainer menyiapkan aset visual terpisah (karena Balsamiq tidak menyediakan styling).
4. Developer menerjemahkan wireframe ke UI final dengan gaya visual yang ditentukan oleh style guide.
5. Revisi dilakukan sampai layout cocok kebutuhan.

---

## 7. Checklist Teknis Implementasi

### Frontend (Blade + JS)
- [ ] Struktur Blade layout siap.
- [ ] Import CSS global.
- [ ] UI sesuai desain final.
- [ ] Kamera dapat dipilih.
- [ ] Resolusi dapat dipilih.
- [ ] Video preview berfungsi.
- [ ] Timer countdown berjalan.
- [ ] Capture foto ke canvas berfungsi.
- [ ] Galeri 4 foto tampil rapi.
- [ ] Generator A4 landscape berfungsi.
- [ ] Watermark muncul di hasil.
- [ ] Download file berjalan.
- [ ] Error handling kamera.

### Backend (Laravel)
- [ ] Routing dasar.
- [ ] Controller halaman utama.
- [ ] Storage untuk hasil (opsional).
- [ ] Konfigurasi permissions storage.
- [ ] Dokumentasi untuk deploy.

### Testing
- [ ] Test beberapa jenis kamera.
- [ ] Test laptop dan PC lab.
- [ ] Test hasil cetak.
- [ ] Test layout landscape di printer.
- [ ] Test performa untuk resolusi tinggi (4K).

---

## 8. Dokumentasi Akhir
- Penjelasan fitur.
- Petunjuk penggunaan aplikasi.
- Cara menjalankan lokal dan produksi.
- Troubleshooting kamera.
- Penjelasan struktur folder.
- Catatan pengembangan lanjutan.

---

## 9. Deliverables Final
- Aplikasi photobox berjalan penuh.
- Desain final dan aset lengkap.
- Dokumentasi lengkap.
- Hasil layout A4 landscape siap cetak.
