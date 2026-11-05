# MAQNA VERSE · Inventory Hub

Pintu masuk web untuk sistem inventory MAQNA (Broadcast · Studio · Warehouse).

**Link:** https://maqnaverse.github.io/inventory/

Halaman ini membalut web app Google Apps Script dalam iframe dan menyediakan:
- Domain sendiri + favicon + ikon logo MAQNA VERSE
- Splash screen semasa app dimuatkan
- "Add to Home Screen" (PWA) untuk iPhone & Android
- Jambatan storan: login diingat 30 hari walaupun iPhone sekat storan iframe
- Halaman offline

## Fail
| Fail | Fungsi |
|---|---|
| `index.html` | Pembalut iframe + jambatan storan sesi |
| `manifest.webmanifest` | Tetapan app (nama, ikon, warna) |
| `sw.js` | Service worker (cache logo & halaman offline) |
| `offline.html` | Dipaparkan bila tiada internet |
| `icons/` | Favicon, ikon app, logo |

## Tukar URL Apps Script
Edit `index.html` → cari `PASTE_URL_WEB_APP_DI_SINI` → ganti dengan URL `/exec` dari Apps Script.
URL tak berubah bila buat **Manage deployments → Edit → New version**, jadi fail ini jarang perlu disentuh.
