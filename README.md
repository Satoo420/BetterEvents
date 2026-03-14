# BetterEvents

Deutsches Event- und Minigames-Plugin fuer BetterAttack.net. Entwickelt fuer Paper `1.21.x`, Java `21+` und Velocity-Netzwerke mit Ingame-GUI, Event-Editor, Spectator-System und serveruebergreifender Reward-Zustellung.

## 📌 Allgemein

| Bereich | Wert |
|---|---|
| 👨‍💻 Autoren | BetterAttack Team |
| 🎮 Netzwerk | BetterAttack.net |
| 💬 Discord | `discord.gg/betterattack.net` |
| 🌐 Website | `betterattack.shop` |
| ⚙️ Plattform | Paper `1.21.x` · Java `21+` |
| 🌍 Proxy | Velocity |
| 📦 Softdepend | WorldGuard |
| 🔌 Integrationen | TAB, PlaceholderAPI, LuckPerms, ExcellentCrates, ItemsAdder |

## 🧩 Was ist BetterEvents?

BetterEvents ist das zentrale Event-Plugin fuer euren Event-Server. Teamler koennen Events komplett ingame verwalten, konfigurieren, starten, beobachten und dokumentieren, ohne direkt in Dateien arbeiten zu muessen.

Der Fokus liegt auf:

- vollstaendiger GUI-Verwaltung
- deutschen Menues und Texten
- modularen Event-Konfigurationen pro Spiel
- sauberem Spectator- und Rollen-Flow
- Reward-System mit serveruebergreifender Zustellung
- Event-Logs, Gewinnerhistorie und Preisverwaltung

## ✨ Kernfeatures

### 🎛️ Ingame Event-Verwaltung

- `/betterevents` als zentrales Hauptmenue
- Event erstellen, bearbeiten, starten und stoppen
- Eventliste mit Direktaktionen
- Config-Unterseiten je Modus
- Werte direkt ueber GUI-Klicks anpassbar
- deutsche GUI-Texte mit einheitlichem Stil

### 🧱 Modulare Event-Konfiguration

- jedes Event liegt als eigene Datei in `plugins/BetterEvents/games/`
- globale Einstellungen bleiben in `config.yml`
- getrennte Unterseiten wie:
  - `locations`
  - `messages`
  - `prize`
  - `commands`
  - `options`
  - `values`
  - `scoreboard`
  - `kit`
  - `worldguard`

### 👥 Teamler-Workflow

- Spieler direkt einem Event zuweisen
- Sucher / Verstecker setzen
- Rollen-Liveansicht mit `/betterevents roles`
- Spectator-System mit Teleport
- ForceJoin, Kick, ForceStart und Rollenpruefung
- klickbare Hide&Seek-Overview fuer Staff

### 🏆 Reward-System

- Gewinner-Ansicht
- Preise-Log mit Reward-Historie
- Letzte Events mit Dokumentation
- Pending-Reward-Queue in MySQL
- Zustellung ueber Hauptserver `Betterattack-3`
- kein unsauberes lokales Reward-Geben auf dem Event-Server

### 🗺️ Event-Map- und Region-Flow

- Spawn-, Spectator-, Lobby- und Event-Locations
- `Ecke 1` und `Ecke 2` fuer Event-Maps
- WorldGuard-Region-Erstellung ueber Event-Daten
- WorldGuard-Flags pro Event in der GUI

## 🎮 Aktive Event-Modi

| Modus | Status | Beschreibung |
|---|---|---|
| Hide & Seek | erweitert | Verstecker / Sucher, Shop, Coins, Spectator, Rollenverwaltung |
| Capture | aktiv | Team-Event mit Flaggen-Flow, Spawns und Teamlogik |
| Spleef | aktiv | Konfigurierbare Arena, Blockabbau, Runden- und Knockout-Flow |
| Sumo | aktiv | Duell-/Rundenmodus mit sauberem Respawn- und Spectator-Flow |
| Parkour | aktiv | Start, Ziel, Checkpoints, Zuschauer-Lobby und Zielerkennung |

## 🧪 Vorbereitete oder geplante Modi

- Bedwars
- BlockParty
- Boatrace
- Bomberman
- Fight
- Frog
- GlassRunner
- HorseRace
- HotPotato
- Paintball
- Quake
- Runner
- SkyWars
- SheepWars
- SpeedBuilders
- Spleeg
- TopKiller
- Tribal

## 🧰 Verwendete Systeme und Bibliotheken

| Bibliothek / System | Zweck |
|---|---|
| HikariCP | performanter MySQL-Connection-Pool |
| MySQL | Reward-Queue, Status, serverweite Nachvollziehbarkeit |
| Velocity | Netzwerk-Routing und Server-Struktur |
| WorldGuard | Event-Regionen und Flag-Verwaltung |
| TAB | Scoreboard-/Anzeige-Integration |
| PlaceholderAPI | Platzhalter fuer Texte und Anzeigen |
| LuckPerms | Permissions und Teamler-Zugriffe |
| ExcellentCrates | Crate-Key-Rewards |
| ItemsAdder | Custom Item-Rewards |

## 🖥️ GUI-Struktur

### Hauptmenue

- Event erstellen
- Eventliste
- Config
- Spieler-Stats

### Eventliste

- Event direkt starten
- Event rechtsklick-basiert bearbeiten
- Eventdetails oeffnen

### Event-Editor

- Locations
- Messages
- Prize
- Commands
- Bossbar
- Options
- Values
- Music
- Scoreboard
- Kit
- WorldGuard

### Reward-Verwaltung

- Gewinner
- Preise
- Letzte Events
- Reward Selection
- Reward Confirmation

## ⌨️ Befehle

### 🎮 Allgemein

| Befehl | Beschreibung |
|---|---|
| `/betterevents` | Hauptmenue oeffnen |
| `/betterevents list` | Eventliste oeffnen |
| `/betterevents create` | neues Event erstellen |
| `/betterevents stats` | Stats-Ansicht oeffnen |

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
| `/betterevents start` | Event regulär starten |
| `/betterevents forcestart` | Event zwangsstarten |
| `/betterevents stop` | laufendes Event stoppen |
| `/betterevents forcejoin <spieler>` | Spieler ins Event holen |
| `/betterevents kick <spieler>` | Spieler aus Event entfernen |
| `/betterevents sucher <spieler>` | Spieler als Sucher setzen |
| `/betterevents hider <spieler>` | Spieler als Verstecker setzen |
| `/betterevents roles` | Live-Rollenuebersicht anzeigen |
| `/betterevents reload` | Konfiguration neu laden |

### 🗺️ WorldGuard-Helfer

| Befehl | Beschreibung |
|---|---|
| `/betterevents wg region create <name>` | Event-Region fuer die aktuelle Map anlegen |

### 🏆 Reward-Admin

| Befehl | Beschreibung |
|---|---|
| `/betterevents reward status <id>` | Status eines Rewards anzeigen |
| `/betterevents reward retry <id>` | fehlgeschlagenen Reward erneut anstossen |
| `/betterevents reward cancel <id>` | Reward abbrechen |

## 🔐 Permissions

### 👤 Spieler

| Permission | Default | Beschreibung |
|---|---|---|
| `betterevents.use` | ✅ Alle | Grundzugriff auf das Plugin |
| `betterevents.player.menu` | ✅ Alle | Spieler-Menues oeffnen |
| `betterevents.player.join` | ✅ Alle | Events beitreten |
| `betterevents.player.leave` | ✅ A
