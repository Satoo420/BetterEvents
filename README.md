# BetterEvents

<div align="center">

### Premium Event Framework fuer BetterAttack.net

Modulares Minecraft-Eventplugin fuer Paper `1.21.x`, Java `21+` und Velocity-Netzwerke  
mit Ingame-GUIs, Event-Editor, Spectator-System, Reward-Queue und BetterAttack-Stil.

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
| 🧩 Softdepends | WorldGuard, PlaceholderAPI, LuckPerms, TAB, ExcellentCrates, ItemsAdder |
| 💾 Datenhaltung | YAML + MySQL + HikariCP |

---

## 🧩 Was ist BetterEvents?

**BetterEvents** ist das zentrale Event-Framework fuer euren Event-Server.  
Das Plugin erlaubt Teamlern, Events komplett **ingame** zu erstellen, zu bearbeiten, zu starten, zu beobachten und inklusive Rewards zu dokumentieren, ohne direkt im Dateisystem arbeiten zu muessen.

Der Fokus liegt auf:

- hochwertigen Inventar-GUIs
- deutscher, einheitlicher BetterAttack-Optik
- modularen Eventkonfigurationen pro Spielmodus
- nativen Spectator-, Join-, Leave- und Staff-Flows
- sauberer Velocity-/MySQL-Reward-Architektur
- skalierbarer und performanter Serverstruktur

---

## ✨ Hauptfeatures

### 🎛️ Ingame Event Management

- `/betterevents` als zentrales Hauptmenue
- Event erstellen, bearbeiten, starten, stoppen
- Eventliste mit Direktaktionen
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

- Staff-Menues fuer Eventsteuerung
- Rollenvergabe bei Hide & Seek
- `/betterevents roles` als Live-Uebersicht
- Spectator-Menue mit Teleport
- ForceJoin, Kick, ForceStart und Rollenpruefung
- Teamler-Untermenues direkt in Uebersichten

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

### 🧱 Map- und Region-Handling

- Lobby-, Spawn-, Spectator- und Event-Spawns
- `Ecke 1` / `Ecke 2` fuer Eventregionen
- WorldGuard-Setup ueber GUI
- WorldGuard-Flags pro Eventmodus

### 🧩 Event Module / Extras System

Optional aktivierbare Module pro Modus:

- `No Player Collisions`
- `Hide All Players`
- weitere Module spaeter leicht erweiterbar

---

## 🎮 Aktive Event-Modi

| Modus | Status | Kurzbeschreibung |
|---|---|---|
| Capture | aktiv | Zwei Teams, Flaggen-Flow, Teamspawns und Rundenlogik |
| Spleef | aktiv | Blockabbau, Arena-Regeln und Last-Man-Standing |
| Sumo | aktiv | Duell-/Rundenmodus mit sauberem Respawn-Flow |
| Hide & Seek | erweitert | Verstecker, Sucher, Shop, Coins, Spectator, Rollen |
| Parkour | aktiv | Start, Ziel, Checkpoints und Zuschauer-Flow |
| Ampel Run | neu | Gruen / Orange / Rot, Reaction-Phasen und Reset-Logik |
| Teamler sagt | neu | Simon-Says-Stil mit Aufgaben, Zeitfenstern und Elims |
| HungerGames | neu | Loot, Grace Period, Border und Survival-Flow |
| Dropper | neu | Fall-Level, Reset-Logik, Zielerkennung und Platzierungen |

---

## 🖼️ GUI-Konzept

### Hauptmenue

- Neues Event erstellen
- Eventliste
- Konfiguration
- Spielerstatistiken
- Event Module

### Eventliste

- `Linksklick` startet ein Event
- `Rechtsklick` oeffnet den Editor
- Teamler koennen Events direkt aus der Liste verwalten

### Event-Editor

- unterteilt in klare Unterseiten
- feldgenaue Werte pro Modus
- Eventbezogene Lores, Materialien und Bedienhinweise
- Delete-Sicherheitsabfrage beim Entfernen eines Events

### Reward-Verwaltung

- Gewinner
- Preise
- Letzte Events
- Reward-Auswahl
- Reward-Bestaetigung
- Status- und Retry-Aktionen

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
  - `/betterkey`
  - `/legendarykey`
  - `/boosterkey`
  - `/möbelkey`
- Vanilla-Items
  - Elytra
  - Dragon Head
  - Diamanten, Erze, Ingots, Bloecke
- ItemsAdder-Rewards
  - strukturierte IA-ID statt rohem Vanilla-Stack
  - Katalog-/Pack-Auswahl im GUI
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
| TAB | optionale Anzeige-/Scoreboard-Integration |
| PlaceholderAPI | Platzhalter in Anzeigen und Texten |
| LuckPerms | Rechte und Teamler-Zugriffe |
| ExcellentCrates | Key-Rewards |
| ItemsAdder | Custom-Item-Rewards |

---

## ⌨️ Befehle

### 🎮 Allgemein

| Befehl | Beschreibung |
|---|---|
| `/betterevents` | Hauptmenue oeffnen |
| `/betterevents list` | Eventliste oeffnen |
| `/betterevents create` | neues Event erstellen |
| `/betterevents stats` | Statistikansicht oeffnen |

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
| `/betterevents reward retry <id>` | fehlgeschlagenen Reward neu anstoßen |
| `/betterevents reward cancel <id>` | Reward abbrechen |

### 🗺️ WorldGuard

| Befehl | Beschreibung |
|---|---|
| `/betterevents wg region create <name>` | Region fuer das aktuelle Event vorbereiten |

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
   - TAB
   - ExcellentCrates
   - ItemsAdder
5. Events ueber GUI oder Dateien anlegen

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
- [config.yml]
- [plugin.yml]

---

## 📈 Projektfokus

Der aktuelle Schwerpunkt liegt auf:

- GUI-Qualitaet und Teamler-Bedienung
- hochwertige Event-Modi
- sauberen Spectator- und Rollen-Flows
- Reward-Queue mit BA3-Bridge
- Performance, HikariCP und MySQL-Stabilitaet
- modularer Erweiterbarkeit pro Modus

---

<div align="center">

### Made for BetterAttack.net

Premium Events fuer ein modernes Velocity-Netzwerk.

</div>
