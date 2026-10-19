# Like Bot

Telegram Auto Like Bot berbasis Python dan `pyTelegramBotAPI`.

## 🚀 Quick Start

### 1. Siapkan Python dan dependensi

Pastikan Python 3.10 atau lebih baru sudah terpasang, lalu jalankan dari folder repositori:

```bash
python -m pip install -r requirements.txt
```

### 2. Atur token bot Telegram

Buat atau kelola token melalui [@BotFather](https://t.me/BotFather). Atur token sebagai environment variable; **jangan menaruh token asli di `main.py`, README, atau commit GitHub**.

**Termux (untuk sesi terminal saat ini):**

```bash
export TELEGRAM_BOT_TOKEN='TEMPELKAN_TOKEN_BARU_DI_SINI'
```

Ganti teks contoh dengan token baru milikmu. Jika terminal/sesi baru dibuka, atur variabel ini lagi.

**Hosting:** buka menu *Environment Variables* atau *Secrets*, lalu tambahkan:

- Name: `TELEGRAM_BOT_TOKEN`
- Value: token bot baru

### 3. Periksa konfigurasi bot

Sebelum dijalankan, buka `main.py` dan pastikan nilai berikut sesuai:

- `OWNER_ID`: ID numerik owner yang benar.
- `LIKE_API_URL` dan `LIKE_API_URL_2`: endpoint API like yang benar-benar aktif.
- `BOT_NAME`, `SUPPORT_USERNAME`, dan `OFFICIAL_GROUP`: nama bot, akun dukungan, dan channel/grup.
- Konfigurasi pembayaran dan zona waktu, jika digunakan.

Owner dan channel sudah disamakan dengan konfigurasi info-bot saat terakhir diperbarui. Endpoint API like tetap perlu diperiksa sendiri sebelum dipakai.

### 4. Jalankan bot

```bash
python main.py
```

Biarkan proses tetap berjalan. Untuk menghentikannya, tekan `Ctrl+C` di terminal yang menjalankan bot.

### 5. Jika bot tidak merespons

1. Pastikan `TELEGRAM_BOT_TOKEN` terisi dan masih berlaku.
2. Periksa pesan error di terminal atau log hosting.
3. Pastikan hanya ada **satu proses polling** untuk token bot yang sama; hentikan instance lama sebelum menjalankan ulang.
4. Pastikan endpoint API dan konfigurasi lainnya valid.

## ⚠️ Catatan keamanan

Token yang pernah dibagikan di chat harus dianggap sudah terekspos. Cabut/ganti token melalui [@BotFather](https://t.me/BotFather), lalu simpan token pengganti hanya di environment variable atau Secrets hosting. Jangan kirim token ke chat atau commit token ke repositori.

## Catatan data

- Bot menyimpan database JSON di folder `database/`; data runtime tidak seharusnya di-commit ke Git.
- README ini menjelaskan cara instalasi, tetapi bot **belum dinyatakan berhasil diuji saat berjalan**.
