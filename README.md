# 🛏️ Smart Pillow — Sistem Rekod Komunikasi AAC + NFC

Aplikasi web progresif untuk membantu kanak-kanak bukan verbal (Autisme, Down Syndrome, dll.) berkomunikasi menggunakan tag NFC fizikal atau papan pemuka responsif.

---

## ✨ Ciri-ciri

- **WebNFC API** — Imbas tag NFC secara langsung dari Chrome Android
- **8 Butang Komunikasi AAC** — Termasuk `Tolong saya` & `Saya sakit` (keutamaan merah)
- **Text-to-Speech** — Sebutan automatik dalam Bahasa Melayu
- **Log Rekod** — Simpan setiap komunikasi dengan cap masa
- **Eksport CSV** — Muat turun rekod untuk laporan
- **Analisis Data** — Graf frekuensi dan aktiviti harian
- **Pengurusan Murid** — Tambah, edit, padam profil murid
- **Tetapan NFC** — Jana payload Teks Mudah atau JSON untuk ditulis ke tag
- **Storan Tempatan** — Data kekal antara sesi

---

## 🚀 Cara Guna

### Pilihan 1: GitHub Pages

1. Fork repositori ini
2. Pergi ke **Settings → Pages**
3. Set source ke `main` branch, folder `/` (root)
4. Laman anda akan tersedia di `https://<username>.github.io/<repo-name>/`

> ⚠️ WebNFC **hanya berfungsi pada HTTPS**. GitHub Pages / Vercel menyediakan HTTPS secara automatik.

### Pilihan 2: GitHub Actions (Auto-Deploy)

Salin fail `deploy.yml` ke dalam `.github/workflows/deploy.yml` dalam repositori anda. Deploy akan berlaku secara automatik setiap kali anda push ke `main`.

### Pilihan 3: Vercel

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy dari folder projek
vercel --prod
```

Atau sambungkan repositori GitHub anda terus di [vercel.com](https://vercel.com).

---

## 📱 Keperluan WebNFC

| Platform | Sokongan |
|----------|----------|
| Chrome Android (v89+) | ✅ Penuh |
| Chrome Desktop | ❌ Tidak disokong |
| Safari / Firefox | ❌ Tidak disokong |
| Perlu HTTPS | ✅ Wajib |

Tanpa NFC, gunakan **butang simulasi** pada papan pemuka — semua fungsi log & TTS tetap berfungsi.

---

## 🏷️ Cara Tulis Tag NFC

1. Muat turun **NFC Tools** (Android/iOS)
2. Buka Smart Pillow → Tab **Tetapan NFC**
3. Pilih format (Teks Mudah atau JSON)
4. Salin payload untuk butang yang dikehendaki
5. Dalam NFC Tools: Write → Add Record → Text → Tampal → Tulis

**Format Teks Mudah:**
```
makan_minum
```

**Format JSON:**
```json
{"id":"makan_minum","label":"Saya nak makan / minum","icon":"🍽️"}
```

---

## 🛠️ Teknologi

- **Vanilla HTML/CSS/JS** — Tiada framework, fail tunggal
- **Tailwind CSS** (CDN) — Styling responsif
- **WebNFC API** — Imbas tag NFC
- **Web Speech API** — Text-to-speech Bahasa Melayu
- **localStorage** — Storan data tempatan

---

## 📁 Struktur Fail

```
/
├── index.html          # Aplikasi penuh (SPA satu fail)
├── .github/
│   └── workflows/
│       └── deploy.yml  # GitHub Actions untuk Pages
└── README.md
```

---

## 📄 Lesen

MIT License — Bebas digunakan untuk tujuan pendidikan khas.
