# BetterEvents

<div align="center">

### Premium Event Framework fuer BetterAttack.net

Modulares Minecraft-Eventplugin fuer Paper `1.21.x`, Java `21+` und Velocity-Netzwerke  
mit Ingame-GUIs, Event-Editor, Live-Uebersichten, Event-Modulen und serveruebergreifendem Reward-System.

<p>
  <img alt="Platform" src="https://img.shields.io/badge/Paper-1.21.x-ff77c8?style=for-the-badge&labelColor=1a1325">
  <img alt="Java" src="https://img.shields.io/badge/Java-21+-ffb3de?style=for-the-badge&labelColor=1a1325">
  <img alt="Proxy" src="https://img.shields.io/badge/Velocity-Network-f58bd8?style=for-the-badge&labelColor=1a1325">
  <img alt="Status" src="https://img.shields.io/badge/Status-Active-ffa7df?style=for-the-badge&labelColor=1a1325">
</p>

</div>

---

## 📌 Allgemein

| Bereich | Wert |
|---|---|
| 👨‍💻 Team | BetterAttack Team |
| 🎮 Netzwerk | BetterAttack.net |
| 💬 Discord | `discord.gg/betterattack.net` |
| 🌐 Website | `betterattack.shop` |
| ⚙️ Plattform | Paper `1.21.x` · Java `21+` |
| 🌍 Proxy | Velocity |
| 🧩 Softdepends | WorldGuard, ItemsAdder |
| 💾 Datenhaltung | YAML + MySQL + HikariCP |

---

## 🧩 Was ist BetterEvents?

**BetterEvents** ist das zentrale Event-Framework fuer euren Event-Server.  
Teamler koennen Events komplett **ingame** erstellen, bearbeiten, starten, verwalten, spectaten und inklusive Rewards dokumentieren, ohne direkt im Dateisystem arbeiten zu muessen.

Der Fokus liegt auf:

- hochwertigen Inventar-GUIs im BetterAttack-Stil
- klaren Event-spezifischen Editor-Unterseiten
- stabilen Runtime-Flows fuer Join, Leave, Spectator und Staff
- modularer Event-Erweiterbarkeit
- sauberer Velocity-/MySQL-Reward-Architektur
- performanter und erweiterbarer Serverstruktur

---

## ✨ Hauptfeatures

### 🎛️ Ingame Event Management

- `/betterevents` als zentrales Hauptmenue
- Event erstellen, bearbeiten, starten und stoppen
- Eventliste mit Direktaktionen
- zentrale Live-Uebersicht aller aktiven Events
- komplette Config-Unterseiten pro Modus
- Werte direkt per Klick anpassbar
- Reward-Verwaltung direkt ueber GUI

### 🗂️ Premium Editor-Struktur

Jedes Event ist in saubere Bereiche unterteilt:

- `locations`
- `messages`
- `prize`
- `commands`
- `options`
- `values`
- `scoreboard`
- `bossbar`
- `music`
- `worldguard`
- `kit` (wenn der Modus Kits benoetigt)

### 👥 Teamler-Workflow

- Staff-Menues fuer Start, Stop, ForceJoin, Kick und Live-Steuerung
- Event-Live-Seiten pro Modus
- Spectator-Menue mit Teleport
- Rollensystem fuer Hide & Seek
- Teamwahl fuer Capture in der Lobby
- klare Live-Statusanzeigen fuer Teamler

### 🧩 Event Module / Extras System

Optional aktivierbare Module pro Eventmodus:

- `No Player Collisions`
- `Hide All Players`
- weitere Module spaeter leicht erweiterbar

### 🏆 Netzwerkweites Reward-System

- Rewards werden **nicht lokal** auf dem Event-Server vergeben
- BetterEvents erzeugt nur Pending-Rewards
- Zustellung erfolgt serveruebergreifend auf `Betterattack-3`
- MySQL-Queue mit Statuswerten wie:
  - `PENDING`
  - `PROCESSING`
  - `DELIVERED`
  - `FAILED`
  - `CANCELLED`

### 🧱 Map-, Region- und Runtime-Handling

- Lobby-, Spawn-, Spectator- und Modus-Spawns
- `Ecke 1` / `Ecke 2` fuer Eventregionen
- WorldGuard-Setup ueber GUI
- WorldGuard-Flags pro Event
- strukturierte Capture-Flaggenlogik
- mehrstufige Dropper-Stages

---

## 🎮 Aktive Event-Modi

| Modus | Status | Kurzbeschreibung |
|---|---|---|
| Capture | stark erweitert | Team-CTF mit Flaggenstatus, Teamspawns, Respawn, Shop, Carrier-Debuffs, Return-Timer und Capture-Live-Flow |
| Spleef | aktiv | Blockabbau, Arena-Regeln und Last-Man-Standing |
| Sumo | aktiv | Duell-/Rundenmodus mit sauberem Respawn-Flow |
| Hide & Seek | stark erweitert | Sucher, Verstecker, Coins, Shop, Border, Rollen, Spezialevents und Live-Menues |
| Parkour | aktiv | Start, Ziel, Checkpoints und Zuschauer-Flow |
| Ampel Run | integriert | Gruen / Orange / Rot, Reaction-Phasen, Hotbar-Ampel und Reset-Logik |
| Teamler sagt | integriert | Simon-Says-Stil mit Aufgaben, Zeitfenstern und Elims |
| HungerGames | integriert | Loot, Grace Period, Border und Survival-Flow |
| Dropper | stark erweitert | Multi-Stage Dropper mit 1 bis 5 Maps, Stage-Fortschritt, Retries und Platzierungen |

---

## 🖼️ GUI-Konzept

### Hauptmenue

- Neues Event erstellen
- Eventliste
- Konfiguration
- Spielerstatistiken
- Event Module
- Live-Uebersicht

### Eventliste

- `Linksklick` startet ein Event
- `Rechtsklick` oeffnet den Editor
- Teamler koennen Events direkt aus der Liste verwalten

### Event-Editor

- unterteilt in klare Unterseiten
- feldgenaue Werte pro Modus
- Eventbezogene Lores, Materialien und Bedienhinweise
- Delete-Sicherheitsabfrage beim Entfernen eines Events

### Live-GUIs

- zentrale Live-Uebersicht in `/betterevents`
- Detailseiten fuer:
  - Hide & Seek
  - Capture
  - Ampel Run
  - HungerGames
  - Teamler sagt
  - Dropper

### Reward-Verwaltung

- Gewinner
- Preise
- Letzte Events
- Reward-Auswahl
- Reward-Bestaetigung
- Status- und Retry-Aktionen

---

## 🏁 Modus-Highlights

### 🟥 Capture

- klare Rot-/Blau-Teamstruktur
- getrennte Team-Spawns, Flaggenbasen und Capture-Zonen
- Flaggenstatus:
  - `AT_BASE`
  - `TAKEN`
  - `DROPPED`
  - `RETURNING`
- Lobby-Teamauswahl mit fairer Random-Verteilung beim Start
- Capture-Shop mit persoehnlicher Kill-/Assist-Waehrung
- Respawn-System mit Spawn-Protection
- Grace-Barrier und Capture-Kit-Flow
- Capture-Live-GUI, Capture-Bossbar und eigenes Scoreboard

### 👀 Hide & Seek

- Sucher-/Verstecker-Rollen
- PlayerOverview und Live-Menues
- Sucher-Freigabe mit Countdown / Titles / Sound
- Border- und Shrink-System
- Hider-/Seeker-Special-Events
- Reward- und Coin-Logik
- Staff-Live-Menues im BetterAttack-Stil

### 💧 Dropper

- 1 bis 5 Stages pro Event
- eigene Stage-Verwaltung im Editor
- pro Stage:
  - Spawn
  - Finish-Zone
  - Death-Height
  - Spectator-Spawn
  - Difficulty
  - Display-Name
- Ranking nach Stage-Fortschritt, Zeit und Fails

### 🚦 Ampel Run

- Gruen / Orange / Rot Phasen
- komplette Ampel-Hotbar
- Movement-Checks bei Rot
- Reset statt Elim bei Verstoessen
- Bossbar, Actionbar, Title und Sound

---

## 🌐 Reward-Architektur

BetterEvents fuehrt Rewards **nicht lokal** auf dem Event-Server aus.

### Ablauf

1. Teamler bestaetigt einen Reward im GUI
2. BetterEvents speichert einen Pending-Reward in MySQL
3. `BARewardBridge` auf `Betterattack-3` erkennt offene Rewards
4. Die Zustellung passiert lokal auf dem Zielserver
5. Spieler erhaelt Chat-Nachricht und Title

### Vorteile

- keine unsauberen Direktvergaben auf dem Event-Server
- offline-sichere Zustellung
- klare Fehlergruende und Statuswerte
- zentrale Dokumentation aller Reward-Aktionen

Weitere Infos:

- [BA3 Reward Bridge README]
---

## 📦 Reward-Typen

Unterstuetzt werden aktuell unter anderem:

- ExcellentCrates Keys
  - `BetterKey`
  - `BoosterKey`
  - `Legendary Key`
  - `Möbel Key`
- Vanilla-Items
  - Elytra
  - Dragon Head
  - Diamanten, Erze, Ingots, Bloecke
- ItemsAdder-Rewards
  - strukturierte IA-ID statt rohem Vanilla-Stack
  - Katalog-/Pack-Auswahl im GUI
  - Pack-/Item-Vorschau
- Custom Commands
- erweiterbar fuer Coins, Ränge und Permissions

---

## 🔌 Integrationen

| System | Aufgabe |
|---|---|
| Velocity | Proxy- und Netzwerkstruktur |
| MySQL | Reward-Queue, Status, Logs |
| HikariCP | performanter Connection Pool |
| WorldGuard | Regionen und Flags |
| PlaceholderAPI | Platzhalter in Anzeigen und Texten |
| LuckPerms | Rechte und Teamler-Zugriffe |
| ExcellentCrates | Key-Rewards |
| ItemsAdder | Custom-Item-Rewards |
| SunLight / externe Scoreboards | Serverweites Scoreboard, das BetterEvents pro Eventmodus bewusst uebersteuert |

---

## ⌨️ Befehle

### 🎮 Allgemein

| Befehl | Beschreibung |
|---|---|
| `/betterevents` | Hauptmenue oeffnen |
| `/betterevents list` | Eventliste oeffnen |
| `/betterevents create` | neues Event erstellen |
| `/betterevents stats` | Statistikansicht oeffnen |
| `/betterevents live` | Live-Uebersicht aktiver Events |

### 👤 Spieler

| Befehl | Beschreibung |
|---|---|
| `/betterevents join` | laufendem Event beitreten |
| `/betterevents leave` | Event verlassen |
| `/betterevents spec <event>` | Event spectaten |
| `/betterevents unspec` | Spectator-Modus verlassen |
| `/betterevents team` | Team-/Rollenansicht oeffnen |

### 🛠️ Teamler

| Befehl | Beschreibung |
|---|---|
| `/betterevents start` | Event normal starten |
| `/betterevents forcestart` | Event zwangsstarten |
| `/betterevents stop` | laufendes Event stoppen |
| `/betterevents forcejoin <spieler>` | Spieler ins Event holen |
| `/betterevents kick <spieler>` | Spieler aus Event entfernen |
| `/betterevents sucher <spieler>` | Spieler als Sucher setzen |
| `/betterevents hider <spieler>` | Spieler als Verstecker setzen |
| `/betterevents roles` | Live-Rollenuebersicht |
| `/betterevents reload` | Konfiguration neu laden |

### 🏆 Reward-Admin

| Befehl | Beschreibung |
|---|---|
| `/betterevents reward status <id>` | Reward-Status anzeigen |
| `/betterevents reward retry <id>` | fehlgeschlagenen Reward neu anstossen |
| `/betterevents reward cancel <id>` | Reward abbrechen |

---

## 🔐 Permissions

### Spieler

| Permission | Default | Beschreibung |
|---|---|---|
| `betterevents.use` | ✅ Alle | Grundzugriff |
| `betterevents.player.menu` | ✅ Alle | Menues oeffnen |
| `betterevents.player.join` | ✅ Alle | Events beitreten |
| `betterevents.player.leave` | ✅ Alle | Events verlassen |
| `betterevents.player.spectate` | ✅ Alle | Spectator nutzen |
| `betterevents.player.team` | ✅ Alle | Team-/Rollenansicht |
| `betterevents.player.stats` | ✅ Alle | Stats ansehen |

### Teamler

| Permission | Default | Beschreibung |
|---|---|---|
| `betterevents.staff.gui` | OP | GUI-Zugriff |
| `betterevents.staff.create` | OP | Events erstellen |
| `betterevents.staff.edit` | OP | Events bearbeiten |
| `betterevents.staff.start` | OP | Events starten |
| `betterevents.staff.forcestart` | OP | ForceStart |
| `betterevents.staff.stop` | OP | Event stoppen |
| `betterevents.staff.forcejoin` | OP | ForceJoin |
| `betterevents.staff.kick` | OP | Spieler entfernen |
| `betterevents.staff.reload` | OP | Reload |
| `betterevents.staff.*` | OP | Sammelrecht |

---

## 📁 Ordnerstruktur

```text
plugins/BetterEvents/
├─ config.yml
├─ games/
├─ data/
└─ logs/
```

| Pfad | Bedeutung |
|---|---|
| `config.yml` | globale Nachrichten, Branding, Performance- und Reward-Einstellungen |
| `games/` | einzelne Eventdateien pro Modus / Arena |
| `data/` | interne Daten, Statistiken, Laufzeitinformationen |
| `logs/` | Event- und Reward-Dokumentation |

---

## ⚙️ Konfiguration

Die Struktur ist bewusst in **globale Defaults** und **eventbezogene Einzeldateien** getrennt.

### Globale Config

- Branding
- Prefixe und Nachrichten
- Scoreboard-Defaults
- Reward-/Database-Struktur
- HikariCP-Werte
- Logging und Performance

Datei:

- [config.yml]

### Eventdateien

Jedes Event liegt separat im `games/`-Ordner und hat eigene:

- Orte
- Nachrichten
- Optionen
- Werte
- Rewards
- WorldGuard-Daten

### Modul-Config

Die Extras / Module werden zusaetzlich ueber eine eigene Datei verwaltet:

- `modules.yml`

---

## 🚀 Installation

1. `BetterEvents.jar` in `plugins/` legen
2. Server starten
3. BetterEvents erstellt automatisch:
   - `config.yml`
   - `games/`
   - `data/`
   - `logs/`
4. Optional installieren:
   - WorldGuard
   - PlaceholderAPI
   - LuckPerms
   - ItemsAdder
5. Rewards auf Netzwerkinstallation mit `BARewardBridge` abstimmen

---

## 🏗️ Build

```bash
mvn -DskipTests package
```

Artefakt:

- `target/BetterEvents-1.0.0.jar`

---

## 📄 Wichtige Dateien

- [BetterEventsPlugin.java]
- [EventManager.java]
- [GuiController.java]
- [ConfigManager.java]
- [config.yml]
- [plugin.yml]
---

## 📈 Projektfokus

Der aktuelle Schwerpunkt liegt auf:

- GUI-Qualitaet und Teamler-Bedienung
- hochwertige Event-Modi
- Capture-Stabilitaet und CTF-Flow
- Multi-Stage Dropper
- Reward-Queue mit BA3-Bridge
- Performance, HikariCP und MySQL-Stabilitaet
- modularer Erweiterbarkeit pro Modus

---

<div align="center">

### Made for BetterAttack.net

Premium Events fuer ein modernes Velocity-Netzwerk.

</div>
