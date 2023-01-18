# BADUT

## Bahan

[Termux](https://f-droid.org/repo/com.termux_118.apk)

[Code Editor](https://play.google.com/store/apps/details?id=com.rhmsoft.code&hl=id&gl=US)

[Referensi](https://github.com/vsec7/DiscordSelfbot)

## Tutorial

### Download semua bahannya untuk hp (kalau vps skip saja)

### Cek repo termux dengan cara

masukan command 

```
termux-change-repo
```
Klik OK > OK Saja
Setelah itu masukan command

```
apt-get upgrade
apt-get update
```

### Install Python

```
pkg install python
```

### Install github

```
pkg install github
```

### Membuat Folder Baru Di Internal Memory HP

caranya ya tinggal ke file manajer bikin folder baru aja
contoh disini saya bikin folder namanya "badut"

### Masuk ke folder yang sudah dibikin tadi di internal hp (kalau vps lebih simple)

```
cd /storage/emulated/0/badut
```

### Copy github

```
git clone https://github.com/vsec7/DiscordSelfbot
```

setelah itu dicek terlebih dahulu apa sudah ada foldernya dengan ketik command

```
dir
```

jika sudah muncul lanjut ke next step

### Open folder yg sudah didownload melalui termux

```
cd DiscordSelfbot
```

catatan untuk hp : jika termux sudah dikeluarkan dan ingin masuk folder langsung maka perintahnya

```
cd /storage/emulated/0/badut/DiscordSelfbot
```

### Install Requirements

```
pip install -r requirements.txt
```

### Edit cofig.yaml

Edit config.yaml dengan app code editor agar mudah
Buka code editor yang sudah diinstall dan open cari file config.yaml

• Edit  *config.yaml* file

```env
BOT_TOKEN:                      # Di bagian discord token 1-2 diisi discord token *Required
    - Discord Token 1           # Kalian bisa menambahkan beberapa akun discord
    - Discord Token 2                     
CHANNEL_ID:                     # Diisikan channel id yang akan dituju *Required
    - Channel Id 1
    - Channel Id 2              # Bisa mengisi beberapa channel id
MODE:                           # mode: (quote, repost, simsimi) pilih salah satu mode
REPLY: Y                        # Untuk simsimi mode saja *Kosongin jika tidak menggunakannya
SIMSIMI_LANG: 				    # Simsimi Language (id/en) *Leave blank Default: id
DELAY: 60	                    # Delay per chat waktunya *second
DEL_AFTER: Y                    # Auto hapus setelah kirim chat *Kosongkan jika tidak ingin menggunakannya 
REPOST_LAST_CHAT: 100           # Repost from last ?n chat in channel          
```

• Bagaimana cara dapat discord token?

```
javascript:var i = document.createElement('iframe');i.onload = function(){var localStorage = i.contentWindow.localStorage;prompt('DC Token By @github.com/vsec7', localStorage.getItem('token').replace(/["]+/g, ''));};document.body.appendChild(i);
```

Paste in your url bar when open discord desktop browser

word **javascript** may removed by browser , you can type it manual.

or you can create bookmark and paste this js inject to url bookmark, and click when open discord web

• Bagaimana cara dapat discord id channel?

- Buka discord via browser mode desktop
- Pilih server dc yg mau badut
- Pilih room chatnya (misalkan general/lainnya yg bisa dichat untuk badut)
- Copy link address webnya
- Paste angka(id) terakhir di config.yaml
(contohnya : saya copy link address "https://discord.com/channels/1064162983175008296/1064487230707609650" maka saya ambil nomor id terakhir jadinya = 1064487230707609650 )
- Dono

### Eksekusi Badut DC

```
python bot.py
```

### Dono Menjadi Badut

