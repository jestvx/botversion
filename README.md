# 🎙️ Voice Channel Moderation Bot – Konfiguration

Dieses Repository enthält die Konfiguration für einen Discord-Bot, der Voice-Channel-Spam erkennt und Nutzer automatisch in den Timeout versetzt. Zusätzlich benachrichtigt er Support-Rollen, wenn jemand im Support-Warteraum wartet.

## 📁 Konfigurationsdatei

Die zentrale Datei ist `config.json`, in der alle Einstellungen für das Verhalten des Bots vorgenommen werden.

### 🔐 Authentifizierung
```json
"token": ""
"licensekey": "RECON-"
```
- `token`: Bot-Token (muss aus Sicherheitsgründen **leer bleiben** in öffentlichen Repos)
- `licensekey`: Lizenzschlüssel für den Bot

### 🔊 Voice-Channel-Überwachung
```json
"voiceChannelIds": [ "1364242161792712775", "1364087210764275812" ]
```
- Liste von Voice-Channel-IDs, die überwacht werden sollen

### ⚠️ Spam-Erkennung
```json
"spamThreshold": 5
"spamWindowMs": 30000
"timeoutDurationMs": 900000
```
- `spamThreshold`: Max. erlaubte Kanalwechsel in der Zeitspanne
- `spamWindowMs`: Zeitfenster zur Erkennung von Spam (in Millisekunden)
- `timeoutDurationMs`: Dauer des Timeouts (in Millisekunden)

### 📩 Nachrichtenkonfiguration

#### Timeout-Benachrichtigung
```json
"timeoutNotification"
```
Sendet eine eingebettete Nachricht an einen Channel, wenn ein User wegen Spam in Timeout geschickt wird.

#### Support-Warteraum
```json
"supportWaitingRoom"
```
Wenn ein User einem bestimmten Warteraum beitritt, werden Support-Rollen automatisch benachrichtigt.

## 🛠️ Anpassung

1. Kopiere `config.json` und passe die Werte an deine Serverstruktur an.
2. Setze deinen Discord-Bot-Token ein (nicht öffentlich hochladen!).
3. Starte den Bot mit deiner bevorzugten Bot-Logik/Implementierung.

## 🧾 Beispielausgabe

**Timeout:**
```
🚫 Voice-Channel Spam
🔇 @User wurde getimeoutet.
🛑 Aktion: Timeout für Spam
⏱️ Dauer: 15 Minuten
```

**Support-Warteraum:**
```
📞 Support-Warteraum
@Support-Rolle
🧑‍💼 @User wartet im Warteraum „Support“ auf Support.
```

## 📸 Medien

- Icon & Thumbnail: `https://files.brokev-rp.de/uploads/reconservice.gif`
