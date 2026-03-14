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
| `betterevents.player.leave` | ✅ Alle | Events verlassen |
| `betterevents.player.spectate` | ✅ Alle | Events spectaten |
| `betterevents.player.team` | ✅ Alle | Team-/Rollenansicht nutzen |
| `betterevents.player.stats` | ✅ Alle | Stats ansehen |

### 🛠️ Teamler

| Permission | Default | Beschreibung |
|---|---|---|
| `betterevents.staff.gui` | OP | GUI-Zugriff fuer Teamler |
| `betterevents.staff.create` | OP | Events erstellen |
| `betterevents.staff.edit` | OP | Events bearbeiten |
| `betterevents.staff.start` | OP | Events starten |
| `betterevents.staff.forcestart` | OP | ForceStart nutzen |
| `betterevents.staff.stop` | OP | Events stoppen |
| `betterevents.staff.forcejoin` | OP | ForceJoin nutzen |
| `betterevents.staff.kick` | OP | Spieler aus Events entfernen |
| `betterevents.staff.reload` | OP | Config / Plugin neu laden |
| `betterevents.staff.*` | OP | alle Teamler-Rechte gesammelt |

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
| `config.yml` | globale Nachrichten, Prefixe, Features, Delivery- und Anzeigeeinstellungen |
| `games/` | einzelne Event-Configs pro Arena / Event |
| `data/` | Daten, Runtime-Infos, interne Stat-Dateien |
| `logs/` | Event- und Reward-Dokumentation |

## ⚙️ Konfiguration

Die Konfiguration ist bewusst in globale und eventbezogene Bereiche getrennt.

### Globale Konfiguration

Datei:

- `plugins/BetterEvents/config.yml`

Typische Inhalte:

- Branding
- allgemeine Nachrichten
- Scoreboard-Defaults
- Reward-System / MySQL
- HikariCP-Settings
- Logging

### Event-Konfigurationen

Ordner:

- `plugins/BetterEvents/games/`

Jedes Event besitzt seine eigene Datei, zum Beispiel:

- `hideseek-1.yml`
- `spleef-1.yml`
- `sumo-1.yml`
- `capture-1.yml`
- `parkour-1.yml`

## 🌐 Reward-Architektur im Netzwerk

BetterEvents fuehrt Rewards **nicht lokal** auf dem Event-Server aus.

Der Ablauf:

1. Ein Teamler bestaetigt einen Reward in der GUI.
2. BetterEvents erstellt einen `Pending Reward` in MySQL.
3. Das Ziel ist der Hauptserver `Betterattack-3`.
4. Die lokale Zustellung uebernimmt die `BARewardBridge`.
5. Der Reward bleibt pending, bis der Spieler sauber zugestellt werden kann.

### Rollen im Netzwerk

| Komponente | Aufgabe |
|---|---|
| BetterEvents auf Event-Server | Eventverwaltung, Reward-Erstellung |
| MySQL | zentrale Reward-Queue und Statusspeicher |
| BARewardBridge auf Betterattack-3 | lokale Reward-Ausfuehrung |

Weitere Infos:

- [BA3 Reward Bridge README](C:\Users\nick\Documents\New%20project\ba3-reward-bridge\README.md)

## 🧠 Features im Detail

### Hide & Seek

- Sucher- und Verstecker-System
- Staff-Rollenverwaltung
- Spectator-Spawn
- Teamler-Overview mit Teleport und Rollenpruefung
- Shop-System
- Coins
- Sucher-Freigabe
- Eventphasen und passende Scoreboards

### Capture

- 2 Teams
- Teamspawns
- Eventstart ueber Lobby-/Join-Flow
- Flag- und Teamstatus-Mechaniken

### Spleef

- konfigurierbare Arena
- Blockabbau-Regeln
- Eventbezogene Spawn- und Spectator-Logik
- rundenbasierter Last-Man-Standing-Flow

### Sumo

- Arena mit Duell-/Rundencharakter
- saubere Respawn- und Spectator-Behandlung
- Eventbezogene Anzeige und Winner-Flow

### Parkour

- Start- und Endpunkt
- Checkpoints
- Zuschauer-Lobby
- Zielerkennung auf der Map

## 🚀 Installation

1. `BetterEvents.jar` in den `plugins/`-Ordner legen
2. Server starten
3. `config.yml`, `games/`, `data/` und `logs/` werden automatisch vorbereitet
4. Optional:
   - WorldGuard
   - PlaceholderAPI
   - LuckPerms
   - TAB
   - ExcellentCrates
   - ItemsAdder
5. Event-Dateien erstellen oder ueber die GUI anlegen

## 🏗️ Build

```bash
mvn -DskipTests package
```

Artefakt:

- `target/BetterEvents-1.0.0.jar`

## 📄 Wichtige Dateien

- [plugin.yml](C:\Users\nick\Documents\New%20project\src\main\resources\plugin.yml)
- [config.yml](C:\Users\nick\Documents\New%20project\src\main\resources\config.yml)
- [BetterEventsPlugin.java](C:\Users\nick\Documents\New%20project\src\main\java\de\betterevents\BetterEventsPlugin.java)
- [EventManager.java](C:\Users\nick\Documents\New%20project\src\main\java\de\betterevents\event\EventManager.java)
- [GuiController.java](C:\Users\nick\Documents\New%20project\src\main\java\de\betterevents\gui\GuiController.java)

## 📈 Status

Der aktuelle Schwerpunkt liegt auf:

- GUI-Qualitaet und Teamler-Bedienung
- Hide & Seek
- Reward-Queue mit BA3-Bridge
- sauberen Event- und Spectator-Flows
- individueller Event-Konfiguration
- performanter MySQL- und HikariCP-Struktur

Made for BetterAttack.net
