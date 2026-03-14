# <span style="color:#ff7fd1;">BetterEvents</span>

<p align="center">
  <b>Premium Event-System für Paper/Spigot 1.21.x</b><br>
  <span>Ingame-Editor • Deutsche GUI • Team-Events • Hide & Seek • Reward-Management</span>
</p>

<p align="center">
  <img alt="Minecraft" src="https://img.shields.io/badge/Minecraft-1.21.x-6aa84f">
  <img alt="Platform" src="https://img.shields.io/badge/Platform-Paper%20%7C%20Spigot-4a86e8">
  <img alt="Language" src="https://img.shields.io/badge/Language-Deutsch-d946ef">
  <img alt="Style" src="https://img.shields.io/badge/Style-BetterEvents%20Pink-ff7fd1">
</p>

---

## <span style="color:#ff7fd1;">Was ist BetterEvents?</span>

**BetterEvents** ist ein Event-Plugin für Minecraft-Server, mit dem Teamler Events komplett **ingame per GUI** erstellen, konfigurieren und starten können, ohne Dateien manuell zu bearbeiten.

Der Fokus liegt auf:

- einfacher Bedienung für Teamler
- schöner, einheitlicher GUI-Optik
- klaren Admin-Workflows
- modularen Event-Konfigurationen pro Modus

---

## <span style="color:#ff7fd1;">Event-Modi</span>

Aktuell im Plugin enthalten:

- `Capture`
- `Spleef`
- `Sumo`
- `Hide & Seek`
- `Parkour`

Jeder Modus hat eigene:

- Locations
- Optionen
- Werte
- Nachrichten
- Commands
- Prize/Reward-Einstellungen
- Scoreboard-Setup

---

## <span style="color:#ff7fd1;">Haupt-Features</span>

### Event-Verwaltung

- Events ingame erstellen und verwalten
- Eventliste mit Start (Linksklick) / Edit (Rechtsklick)
- Startprüfungen (z. B. Mindestspieler, Ecken/Map-Vollständigkeit)
- Forcestart / Forcejoin / Kick

### GUI-Editor (pro Event)

- Unterseiten wie:
  - Locations
  - Messages
  - Prize
  - Commands
  - Options
  - Values
  - Scoreboard
  - WorldGuard
- Zahlwerte mit:
  - Linksklick `+1`
  - Shift+Linksklick `+10`
  - Rechtsklick `-1`
  - Shift+Rechtsklick `-10`

### Hide & Seek Features

- Rollen: **Verstecker** / **Sucher**
- Sucher-Freigabe (konfigurierbar)
- Shopsystem (Verstecker/Sucher)
- Radar (konfigurierbar & kaufbar)
- Sound-Ability mit Cooldown
- Supply Drops (an/aus + Inhalte konfigurierbar)
- Phasen-Status im Scoreboard

### Reward-Management (im Prize-Bereich)

- Gewinnerübersicht
- Spieler-Statistiken
- Reward-Auswahl per GUI
- Kategorien:
  - Crate Keys
  - Reichtum-Items
  - ItemsAdder
- Bestätigungsmenü
- Offline-Pending-Rewards (werden beim Join zugestellt)

### Zusätzliche Systeme

- Spectator-System inkl. GUI
- WorldGuard-Flags pro Event per GUI
- Bossbar/Scoreboard-Integration
- Optional: internes Scoreboard deaktivieren bei TAB-Nutzung
- Plugin-Ordnerstruktur:
  - `plugins/BetterEvents/config.yml`
  - `plugins/BetterEvents/games/*.yml`
  - `plugins/BetterEvents/data/*`
  - `plugins/BetterEvents/logs/*`

---

## <span style="color:#ff7fd1;">Befehle</span>

Hauptbefehl:

```text
/betterevents <subcommand>
```

Verfügbare Subcommands:

- `menu` / `open` → Hauptmenü öffnen
- `list` → Eventliste öffnen
- `create <capture|spleef|sumo|hideseek|parkour> [name]` → Event erstellen
- `start <event-id>` → Event öffnen/starten
- `join` → laufendem Event beitreten
- `leave` → Event verlassen
- `team` → Teamauswahl öffnen (wenn Modus unterstützt)
- `spec [event]` → als Spectator zuschauen
- `unspec` → Spectator verlassen
- `roles` → Live-Übersicht Sucher/Verstecker
- `seeker <spieler>` / `sucher <spieler>` → Sucher setzen
- `hider <spieler>` / `verstecker <spieler>` → Verstecker setzen
- `forcestart` → Event trotz Countdown sofort starten (mit Prüfungen)
- `forcejoin <spieler>` → Spieler zwangsweise hinzufügen
- `kick <spieler>` → Spieler aus Event entfernen
- `wg region create <name>` → WorldGuard-Region anlegen
- `stop` / `cancel` → laufendes Event stoppen
- `reload` → Configs neu laden
- `stats` → Spielerstatistiken öffnen

---

## <span style="color:#ff7fd1;">Permissions</span>

### Basis

- `betterevents.use`

### Player

- `betterevents.player.menu`
- `betterevents.player.join`
- `betterevents.player.leave`
- `betterevents.player.spectate`
- `betterevents.player.team`
- `betterevents.player.stats`

### Staff

- `betterevents.staff.gui`
- `betterevents.staff.create`
- `betterevents.staff.edit`
- `betterevents.staff.start`
- `betterevents.staff.forcestart`
- `betterevents.staff.stop`
- `betterevents.staff.forcejoin`
- `betterevents.staff.kick`
- `betterevents.staff.reload`
- `betterevents.staff.*` (alle Staff-Rechte)

---

## <span style="color:#ff7fd1;">Installation</span>

1. BetterEvents-JAR in den Ordner `plugins/` legen
2. Server neu starten
3. Rechte per LuckPerms vergeben
4. `/betterevents menu` öffnen und erstes Event erstellen

---

## <span style="color:#ff7fd1;">Empfohlene Plugin-Kombination</span>

- **WorldGuard** (Regionen/Flags)
- **TAB** (wenn externes Scoreboard gewünscht)
- **ExcellentCrates** (Crate-Key-Commands)
- **ItemsAdder** (Custom-Item-Rewards)

---

## <span style="color:#ff7fd1;">Philosophie</span>

BetterEvents ist darauf ausgelegt, Teamlern eine starke Ingame-Kontrolle zu geben:

- keine umständliche Dateipflege für jeden Schritt
- klare, lesbare Menüs
- saubere Trennung pro Event-Modus
- fairer, konfigurierbarer Event-Flow

---

## <span style="color:#ff7fd1;">Support / Mitarbeit</span>

Wenn du Feedback, Ideen oder Bugs hast:

- Feature-Issue erstellen
- Bug mit Eventmodus + Reproduktionsschritten melden
- bei GUI-Themen am besten mit Screenshot + Klickfolge

---

<p align="center">
  <b style="color:#ff7fd1;">BetterEvents</b><br>
  <span>ᴘʀᴇᴍɪᴜᴍ ᴍɪɴᴇᴄʀᴀꜰᴛ ᴇᴠᴇɴᴛ ᴇxᴘᴇʀɪᴇɴᴄᴇ</span>
</p>

