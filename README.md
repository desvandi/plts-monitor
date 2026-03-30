# PLTS Monitor v5.0 - LiFePO4 16S 300Ah

## Spesifikasi Sistem
- **Baterai**: LiFePO4 16S 300Ah
- **Tegangan Nominal**: 51.2V
- **Tegangan Max**: 58.4V
- **Tegangan Min**: 40.0V
- **Kapasitas Energi**: 15.36 kWh

## Fitur
- Dashboard monitoring realtime
- Aliran energi PV → Baterai + Beban (simultan)
- Ekonomi energi harian dengan logika Coulomb
- Grafik historis SOC, daya, dan kapasitas
- Notifikasi peringatan
- Dark/Light mode
- PWA (Progressive Web App) - dapat diinstall

## Deploy ke GitHub Pages

### Langkah 1: Buat Repository GitHub
1. Login ke GitHub
2. Klik "New repository"
3. Nama repository: `plts-monitor` (atau nama lain)
4. Pilih "Public"
5. Klik "Create repository"

### Langkah 2: Upload File
Upload file-file berikut ke repository:
- `index.html` (file utama)
- `manifest.json` (untuk PWA)
- `service-worker.js` (untuk offline caching)
- `README.md` (opsional)

### Langkah 3: Aktifkan GitHub Pages
1. Buka repository di GitHub
2. Klik "Settings" tab
3. Scroll ke "Pages" di sidebar kiri
4. Di "Source", pilih "Deploy from a branch"
5. Pilih branch "main" dan folder "/ (root)"
6. Klik "Save"

### Langkah 4: Akses Aplikasi
Setelah beberapa menit, aplikasi akan tersedia di:
```
https://[username].github.io/[repository-name]/
```

## Install sebagai Aplikasi (PWA)

### Di Android:
1. Buka URL aplikasi di Chrome
2. Tunggu hingga loading selesai
3. Ketuk menu (⋮) atau akan muncul popup "Install"
4. Pilih "Add to Home screen" atau "Install"
5. Aplikasi akan muncul di home screen seperti aplikasi native

### Di iOS:
1. Buka URL aplikasi di Safari
2. Ketuk tombol Share (kotak dengan panah ke atas)
3. Pilih "Add to Home Screen"
4. Beri nama dan ketuk "Add"

## Kalibrasi Sensor

Aplikasi mendukung kalibrasi:
- **Tegangan (INA219)**: Factor kalibrasi untuk pembacaan tegangan
- **Daya Baterai**: Kalibrasi sensor arus baterai
- **Daya Beban**: Kalibrasi sensor arus beban

Kalibrasi disimpan di localStorage browser.

## Konfigurasi API

Edit `SCRIPT_URL` di bagian JavaScript untuk mengubah endpoint Google Apps Script:
```javascript
const SCRIPT_URL = 'https://script.google.com/macros/s/YOUR_SCRIPT_ID/exec';
```

## Troubleshooting

### Data tidak muncul:
- Periksa koneksi internet
- Periksa URL Google Apps Script
- Cek console browser untuk error (F12 → Console)

### Tidak bisa install PWA:
- Pastikan akses via HTTPS (GitHub Pages sudah HTTPS)
- Clear cache browser dan coba lagi
- Pastikan semua file PWA ter-upload

### Notifikasi tidak muncul:
- Pastikan browser mengizinkan notifikasi
- Di Chrome: Settings → Site Settings → Notifications

---
Dibuat untuk monitoring sistem PLTS dengan baterai LiFePO4 16S 300Ah
