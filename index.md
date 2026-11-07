# Gebärden-App auf Handy und Tablet – Anleitung

Stand: 07.11.2026 · gilt für `Gebaerden-App.html` ab Fassung o (mit Knopf „🎬 Videos zeigen“)
**Auf echten Handys und Tablets noch nicht getestet.**

## 1. Kurz gesagt

- Übertragen wird **nur eine Datei: `Gebaerden-App.html`** (ca. 3 MB) aus dem Ordner
  `05_Piktogramm-Tool/Gebaerden-Piktogramme/`.
  Python, `video_cache/`, `.venv` und alle anderen Dateien bleiben auf dem PC.
- **Installiert wird nichts.** Die Datei ist eine Webseite und läuft im Browser des Geräts
  (Safari, Chrome, Firefox).
- **iPhone/iPad:** Die Datei muss im Internet unter einer Adresse liegen (Weg A).
  Eine auf das iPhone kopierte Datei zeigt iOS nur als Vorschau an. Dort laufen keine
  Programme, die Knöpfe funktionieren also nicht.
- **Android:** Weg A geht auch, alternativ die Datei direkt aufs Gerät kopieren (Weg B).
- Für die **Videos** braucht das Gerät immer Internet; die Gebärdenschrift-Bilder nicht.

## 2. Vorher am PC (einmalig und nach jeder Änderung)

1. Video-Verzeichnis bauen (braucht Internet, einige Minuten):
   `.venv/bin/python videos.py --index`
2. Browser-Seite neu bauen:
   `.venv/bin/python app_bauen.py`
3. Am PC prüfen: `Gebaerden-App.html` doppelklicken, Text einfügen, „Gebärden zeigen“,
   „🎬 Videos zeigen“. Läuft das, ist die Datei fertig zum Übertragen.

Wichtig: Nach jeder Änderung (Wörterbuch, Video-Verzeichnis) die Datei **neu übertragen**,
sonst arbeitet das Gerät mit der alten Fassung.

## 3. Weg A – online stellen (empfohlen, für alle Geräte)

Die Datei kommt auf einen Webspace und hat dann eine feste Adresse
(z. B. `https://name.github.io/gebaerden/`). Jedes Gerät öffnet diese Adresse im Browser.

**Datenschutz:** Der eingegebene Text bleibt auch dann auf dem Gerät, denn die Seite schickt ihn
nirgendwohin. Nur beim Abspielen von Videos sieht SignDict, welche Gebärden abgerufen werden.

### A1. Datei online stellen (kostenlos, z. B. mit GitHub Pages)

1. Auf github.com ein kostenloses Konto anlegen.
2. Neues **öffentliches** Repository anlegen, z. B. `gebaerden`.
3. Die Datei **umbenennen in `index.html`** und hochladen („Add file → Upload files“).
4. Im Repository: Settings → Pages → als Quelle den Zweig `main` wählen → speichern.
5. Nach ein bis zwei Minuten steht dort die Adresse, z. B. `https://NAME.github.io/gebaerden/`.

Wer schon einen eigenen Webspace hat (z. B. für eine Homepage), lädt die Datei einfach dorthin
hoch. Wichtig ist nur: Die Seite muss im Browser **angezeigt** werden und darf nicht bloß als
Download angeboten werden. Cloud-Speicher wie Dropbox, Google Drive oder iCloud bieten die Datei
meist nur als Download an und reichen deshalb nicht.

**Lizenz beim Online-Stellen:** Die Fußzeile mit den Quellenangaben nicht entfernen
(CC BY-SA 3.0, siehe `LIZENZEN.md`). Am besten `LIZENZEN.md` mit hochladen.
Die Seite enthält selbst keine Videos, nur Verweise auf SignDict.

### A2. iPhone / iPad

1. **Safari** öffnen, die Adresse eingeben, Seite lädt.
2. Als App-Symbol ablegen: Teilen-Knopf (Viereck mit Pfeil) → **„Zum Home-Bildschirm“** → „Hinzufügen“.
3. Ab jetzt öffnet das Symbol auf dem Home-Bildschirm die Gebärden-App.

### A3. Android

1. **Chrome** öffnen, die Adresse eingeben, Seite lädt.
2. Als App-Symbol ablegen: Menü (⋮) → **„Zum Startbildschirm hinzufügen“** → „Hinzufügen“.

## 4. Weg B – nur Android: Datei direkt aufs Gerät

1. Datei aufs Handy bringen: per USB-Kabel in den Ordner „Download“ kopieren, per E-Mail an sich
   selbst schicken oder über einen Cloud-Speicher herunterladen.
2. Die App **„Dateien“** öffnen → `Gebaerden-App.html` antippen.
3. Erscheint nur eine Vorschau oder funktionieren die Knöpfe nicht:
   lange antippen bzw. Menü → **„Öffnen mit“ → Chrome** (oder Firefox).
4. Je nach Gerät und Android-Fassung klappt das unterschiedlich gut. Wenn nicht: Weg A.

Vorteil: Die Gebärdenschrift funktioniert dann auch ganz ohne Internet.
Nachteil: Ein Symbol auf dem Startbildschirm lässt sich so meist nicht ablegen, und jede neue
Fassung muss wieder von Hand kopiert werden.

## 5. Benutzung auf dem Gerät

Wie am PC: Text einfügen oder „Textdatei wählen …“ → **„Gebärden zeigen“** → darüber
**„🎬 Videos zeigen“**. Ins Video tippen = Abspielen/Pause; ↺ = nochmal, 🐢 = langsamer.
Die Lesehilfe steht auf dem Handy unter den Bildern. Querformat oder Tablet ist zum Lesen
angenehmer.

## 6. Wenn etwas nicht klappt

| Problem | Lösung |
|---|---|
| iPhone: Seite erscheint, aber Knöpfe tun nichts | Es ist nur die Vorschau einer kopierten Datei. Weg A nehmen |
| „Video nicht ladbar“ | Internet prüfen (WLAN/Mobilfunk) |
| „noch kein Video-Verzeichnis eingebaut“ | am PC Schritt 2 (`--index`, `app_bauen.py`) und neu übertragen |
| Neue Wörter fehlen auf dem Gerät | alte Fassung: neu hochladen bzw. kopieren; im Browser die Seite neu laden |
| Video ruckelt oder lädt lange | langsame Verbindung; WLAN nehmen. Beim zweiten Abspielen geht es meist flüssiger |

## 7. Noch offen (für die To-do-Liste)

- Echter Test auf iPhone, iPad und einem Android-Gerät (Safari ist bisher ungetestet).
- Ob die Seite ohne Internet vom Home-Bildschirm startet (Weg A), ist nicht sichergestellt.
  Das ließe sich später als „Web-App mit Offline-Speicher“ (PWA) nachrüsten.
- Ob SignDict das Abspielen seiner Videos aus fremden Seiten auf Dauer zulässt, ist ungeprüft.
