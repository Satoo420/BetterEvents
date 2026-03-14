# BetterEvents

Deutsches Event- und Minigames-Plugin fuer Paper `1.21.x` mit Ingame-GUI, Event-Editor, Teamler-Workflow und serveruebergreifendem Reward-System.

## Auf einen Blick

BetterEvents ist fuer Event-Server gebaut, auf denen Teamler Events direkt im Spiel verwalten sollen:

- Events erstellen, starten und stoppen
- Eventwerte direkt im GUI aendern
- Spieler verwalten, spectaten und Rollen setzen
- Rewards dokumentieren und serveruebergreifend zustellen
- mehrere Event-Modi ueber eine gemeinsame Verwaltungsoberflaeche pflegen

## Highlights

### Ingame-Verwaltung
- komplettes Hauptmenue ueber `/betterevents`
- Eventliste mit Start- und Edit-Flow
- editorbasierte Konfiguration ohne Dateibrowser
- deutsche GUI mit einheitlichem Stil

### Teamler-Workflow
- Rollen direkt im Event setzen
- Live-Rollenuebersicht bei Hide and Seek
- Spectator-System mit Teleport-Funktion
- Kick-, ForceJoin- und ForceStart-Tools

### Event-System
- event-spezifische Config-Dateien im `games`-Ordner
- getrennte Unterseiten wie `locations`, `messages`, `prize`, `commands`, `options`, `values`, `scoreboard`, `kit`, `worldguard`
- WorldGuard-Helfer und Event-Region-Flow

### Reward-System
- Gewinner-Ansicht
- Preise / Auszahlungs-Log
- Letzte Events
- MySQL-basierte Reward-Queue
- serveruebergreifende Zustellung ueber BA3-Bridge

## Aktive Modi

| Modus | Status | Fokus |
|---|---|---|
| Hide and Seek | erweitert | Rollen, Shop, Coins, Spectator, Teamler-Tools |
| Capture | aktiv | Teams, Spawns, Scoreboard, Flag-Flow |
| Spleef | aktiv | Runden, Knockout, konfigurierbare Bloecke |
| Sumo | aktiv | Runden, Knockout, Spawn- und Spectator-Flow |
| Parkour | aktiv | Start, Ziel, Checkpoints, Zuschauer |

## Vorbereitete bzw. geplante Modi

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

## GUI-Struktur

### Hauptmenue
- Event erstellen
- Eventliste
- Config
- Stats

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

## Commands

### Spieler-Commands

| Command | Funktion |
|---|---|
| `/betterevents join` | dem laufenden Event beitreten |
| `/betterevents leave` | Event verlassen |
| `/betterevents spec <event>` | Event spectaten |
| `/betterevents unspec` | Spectator-Modus verlassen |

### Teamler-Commands

| Command | Funktion |
|---|---|
| `/betterevents` | Hauptmenue oeffnen |
| `/betterevents forcestart` | Event manuell starten |
| `/betterevents stop` | laufendes Event stoppen |
| `/betterevents forcejoin <spieler>` | Spieler in Event holen |
| `/betterevents kick <spieler>` | Spieler aus Event entfernen |
| `/betterevents sucher <spieler>` | Spieler als Sucher setzen |
| `/betterevents roles` | Live-Rollenuebersicht |

### Reward-Admin

| Command | Funktion |
|---|---|
| `/betterevents reward status <id>` | Reward-Status anzeigen |
| `/betterevents reward retry <id>` | Reward erneut auf `PENDING` setzen |
| `/betterevents reward cancel <id>` | Reward abbrechen |

### WorldGuard-Helfer

| Command | Funktion |
|---|---|
| `/betterevents wg region create <name>` | WG-Region fuer Event anlegen |

## Permissions

### Spieler

| Permission | Bedeutung |
|---|---|
| `betterevents.player.join` | Event beitreten |
| `betterevents.player.leave` | Event verlassen |
| `betterevents.player.spectate` | Event spectaten |

### Teamler

| Permission | Bedeutung |
|---|---|
| `betterevents.staff.gui` | GUI-Zugriff |
| `betterevents.staff.create` | Events erstellen |
| `betterevents.staff.edit` | Events bearbeiten |
| `betterevents.staff.start` | Events starten |
| `betterevents.staff.forcestart` | ForceStart |
| `betterevents.staff.stop` | Event stoppen |
| `betterevents.staff.forcejoin` | ForceJoin |
| `betterevents.staff.kick` | Spieler kicken |
| `betterevents.staff.reload` | Config / Plugin neu laden |

## Ordnerstruktur

```text
plugins/BetterEvents/
├─ config.yml
├─ games/
├─ data/
└─ logs/
```

### Bedeutung

| Pfad | Inhalt |
|---|---|
| `config.yml` | globale Nachrichten, Prefixe, Features, Scoreboards |
| `games/` | einzelne Event-Configs pro Arena |
| `data/` | Daten, Laufzeit-Infos, Statistiken |
| `logs/` | interne Dokumentation und Runtime-Logs |

## Reward-Architektur

BetterEvents ist auf deinem Event-Server der **Reward-Producer**.

Das bedeutet:

1. Ein Teamler bestaetigt einen Reward im BetterEvents-GUI.
2. BetterEvents speichert nur einen Pending-Reward in MySQL.
3. Die lokale Ausfuehrung findet **nicht** auf dem Event-Server statt.
4. Die Zustellung auf `Betterattack-3` uebernimmt die separate BA3-Bridge.

### Zustellung auf dem Hauptserver

Die Dokumentation dafuer findest du hier:

- [BA3 Reward Bridge README](C:\Users\nick\Documents\New project\ba3-reward-bridge\README.md)

## Netzwerk-Rollen

| Komponente | Aufgabe |
|---|---|
| BetterEvents auf Event-Server | Rewards erstellen, Events verwalten |
| MySQL | zentrale Queue und Statusspeicher |
| BA3RewardBridge auf Betterattack-3 | Rewards lokal zustellen |

## Integrationen

- Paper / Spigot `1.21.x`
- Velocity-Netzwerk
- WorldGuard
- TAB
- PlaceholderAPI
- LuckPerms
- ExcellentCrates
- ItemsAdder

## Build

```bash
mvn -DskipTests package
```

Artefakt:

- `target/BetterEvents-1.0.0.jar`

## Wichtige Dateien
- [config.yml]
- [BetterEventsPlugin.java]
- [EventManager.java]
- [GuiController.java]
## Status

Der aktuelle Schwerpunkt liegt auf:

- GUI-Qualitaet und Teamler-Bedienung
- Hide and Seek
- Reward-Queue + BA3-Bridge
- sauberer Event-/Spectator-Flow
- individuelle Event-Konfigurationen
