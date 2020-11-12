# botwaa

Bot WhatsApp lama punya alveeria, dibuat pakai Node.js dan Baileys. Dulu dijalankan lewat Termux.

Ini arsip dari 2020, udah nggak diurus. Banyak API dan dependency-nya juga udah lama, jadi jangan berharap semua fitur masih jalan.

## Fitur

- Bikin sticker dari gambar
- Pantun dan gambar random
- Ayat Quran dan Wikipedia
- Balasan teks
- Link download YouTube, Instagram, Facebook, dan Twitter

Sebagian fitur bergantung ke API pihak ketiga. Fitur quotes dan beberapa percobaan lain masih ada di kode, tapi dikomentari.

## Kalau mau ngoprek

```bash
git clone https://github.com/alveeria/botwaa.git
cd botwaa
cp .env.example .env
```

Nama bot, kontak, Instagram, dan link grup bisa diubah di bagian atas `index.js`. Kontak dan link bawaan udah dikosongin.

Isi `.env` kalau butuh API key:

```env
FARZAIN_API_KEY=
MHANKBARBAR_API_KEY=
SOUNDCLOUD_CLIENT_ID=
```

SoundCloud cuma dipakai di kode yang dikomentari. `.env` nggak otomatis dibaca; kalau pakai Node.js 20.6 ke atas, jalankan dengan:

```bash
node --env-file=.env index.js
```

Kalau environment variable udah diatur lewat shell, cukup `npm start`.

Dependency ada di `package.json`. Skrip `install.sh` masih bawaan Termux dulu, cek dulu sebelum dijalankan. Instalasi dan login bot ini belum dites ulang di versi Node.js sekarang.

## Catatan

- Dependency lama punya temuan keamanan. Jangan langsung dipakai buat bot publik.
- Jangan pakai nomor WhatsApp utama; bot tidak resmi bisa berisiko kena pembatasan akun.
- Jangan bagikan QR login atau `session.json`. File itu berisi akses sesi WhatsApp.
- Kode lama masih mencetak nomor pengirim dan isi pesan ke terminal.
- `.env` dan session udah masuk `.gitignore`.
- `npm test` cuma cek sintaks, bukan ngetes koneksi atau fitur bot.

## Kredit

Berawal dari [botst4rz](https://github.com/Bintang73/botst4rz) oleh Bintang Nur Pradana dan [termux-whatsapp-bot](https://github.com/fdciabdul/termux-whatsapp-bot) oleh Abdul Muttaqin / fdciabdul.

## Lisensi

[Unlicense](LICENSE).
