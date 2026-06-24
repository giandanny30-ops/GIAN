# 🤖 GIANNI Bot — v3.0

Discord bot za Bosnian/Serbian servere. Prefiks: `.` (mobile) i `/` (slash komande).

---

## 🚀 Pokretanje

### 1. Kloniraj repo
```bash
git clone https://github.com/tvoj-username/mrak-bot.git
cd mrak-bot
```

### 2. Instaliraj zavisnosti
```bash
pip install -r requirements.txt
```

### 3. Postavi token
Napravi fajl `.env` (ili postavi environment varijablu):
```bash
cp .env.example .env
# Otvori .env i upiši svoj Discord bot token
```

Ili direktno u terminalu:
```bash
export DISCORD_TOKEN="tvoj_token_ovdje"
```

### 4. Pokreni bota
```bash
python bot.py
```

---

## ☁️ Hosting (Railway / Render / VPS)

| Platform | Upute |
|----------|-------|
| **Railway** | Postavi `DISCORD_TOKEN` u Environment Variables, deploy grane `main` |
| **Render** | Build Command: `pip install -r requirements.txt` / Start: `python bot.py` |
| **VPS (Linux)** | `screen -S bot python bot.py` ili systemd service |

### Persistent data (Railway/Render)
Bot automatski čuva podatke u `/app/data/oleun_data.json`.  
Na Railway postavi **Volume** na `/app/data` da se podaci sačuvaju između restarta.

---

## ⚙️ Konfiguracija u kodu

Na početku `bot.py` podesi:

```python
OWNER_IDS = {tvoj_discord_id}          # Linija ~2471
OFFICIAL_GUILD_ID = tvoj_server_id     # Linija ~25

# Emoji IDs (zamijeni sa emoji-ima sa tvog servera):
E_FIRE1 = "<a:vatrice1:EMOJI_ID>"
E_FIRE2 = "<a:vatrice2:EMOJI_ID>"
```

---

## 📋 Komande

### 🎮 Igre
| Komanda | Opis |
|---------|------|
| `/kaladont` | Pokretanje igre kaladont |
| `/kviz` | Kviz pitanja |
| `/slots` | Slot machine |
| `/bingo` | Bingo igra |
| `/rusija` | Ruska rulet |

### 💰 Ekonomija
| Komanda | Opis |
|---------|------|
| `/balans` | Provjeri stanje |
| `/daily` | Dnevna nagrada |
| `/transfer` | Pošalji novac |
| `/kockanje` | Kladionica |

### ⭐ XP & Leveli
| Komanda | Opis |
|---------|------|
| `/rank` | Tvoj rank i XP |
| `/top` | Leaderboard |
| `/set-level` | [Admin] Postavi level korisniku |

### 🛠️ Admin
| Komanda | Opis |
|---------|------|
| `/ban`, `/kick`, `/warn` | Moderacija |
| `/setchannel` | Postavi kanal za kategoriju |
| `/setup-uloge` | Postavi role panele |
| `/backup` | Manuelni backup podataka |

---

## 🗂️ Struktura fajlova

```
mrak-bot/
├── bot.py              # Glavni bot fajl
├── requirements.txt    # Python zavisnosti
├── .env.example        # Template za environment varijable
├── .gitignore          # Git ignore pravila
└── README.md           # Ovaj fajl
```

---

## 📝 Napomene

- **Token nikad ne pushaj** na GitHub — koristaj `.env` ili Environment Variables na hostingu
- Bot automatski pravi backup podataka u privatni Discord kanal
- Data fajl: `oleun_data.json` — ne brišaj ga bez backupa

---

*GIANNI Bot v3.0 — Za MRAK Discord server*
