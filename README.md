# botwaa

Arsip bot WhatsApp **alveeria** dari tahun **2020**, berbasis Node.js dan Baileys generasi lama.

> **Tidak dipelihara.** Disimpan untuk dokumentasi dan pembelajaran, bukan bot siap produksi. Dependency memiliki temuan keamanan; protokol WhatsApp dan endpoint pihak ketiga mungkin sudah tidak kompatibel. Jangan gunakan akun WhatsApp utama. Bot tidak resmi ini tidak berafiliasi dengan WhatsApp dan penggunaannya dapat berisiko terhadap akun.

## Isi arsip

Kode mencakup perintah sticker, pantun, pencarian gambar, Quran, Wikipedia, balasan teks, serta tautan downloader. Sebagian fitur lama dikomentari atau bergantung pada layanan eksternal. Keberhasilan fitur saat ini tidak dijamin.

## Konfigurasi

Konfigurasi nama bot ada di awal `index.js`. Instagram, nomor kontak/donasi, dan tautan grup sengaja dikosongkan. Jangan commit informasi pribadi atau kredensial ke repository.

API key bawaan sudah dihapus dari versi kode terbaru. Jika layanan terkait masih tersedia, sediakan sendiri lewat environment variable:

- `FARZAIN_API_KEY`
- `MHANKBARBAR_API_KEY`
- `SOUNDCLOUD_CLIENT_ID` (hanya referensi kode lama yang dikomentari)

File `.env` tidak otomatis dimuat oleh kode ini. Gunakan environment shell atau pengelola proses.

## Referensi instalasi lama

```bash
git clone https://github.com/alveeria/botwaa.git
cd botwaa
```

`install.sh` adalah skrip historis untuk Termux. Tinjau sebelum menjalankan: skrip memasang paket global dan dependency lama, serta bukan prosedur instalasi yang telah diuji untuk sistem sekarang.

Entrypoint bot adalah `index.js` (`npm start`), yang akan mencoba menghubungkan akun WhatsApp. Kredensial tersimpan di `session.json`; jangan bagikan file ini maupun QR login. Pesan dan nomor pengirim dicetak ke terminal oleh kode lama.

## Pemeriksaan

```bash
npm test
```

Perintah ini hanya memeriksa sintaks JavaScript, tidak menjalankan bot atau membuktikan fiturnya masih bekerja. Tidak ada modernisasi dependency pada pembaruan arsip ini.

## Kredit

Dikelola sebagai arsip oleh [alveeria](https://github.com/alveeria).

Kode historis berasal dari proyek [botst4rz](https://github.com/Bintang73/botst4rz) oleh Bintang Nur Pradana dan [termux-whatsapp-bot](https://github.com/fdciabdul/termux-whatsapp-bot) oleh Abdul Muttaqin / fdciabdul. Kredit sumber asli tetap dipertahankan.

## Lisensi

File [LICENSE](LICENSE) bawaan arsip berisi **Unlicense**; metadata paket diselaraskan dengan file tersebut. Lisensi dependency dan materi pihak ketiga tetap mengikuti ketentuan masing-masing.
