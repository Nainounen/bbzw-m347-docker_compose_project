# Mini Compose Motivation

## Ziel

In diesem Auftrag untersuchen Sie ein kleines Mehrcontainer-System mit Docker Compose.

Sie lernen dabei:
- mehrere Services in einer `compose.yaml` zu erkennen
- den Unterschied zwischen `image` und `build` zu verstehen
- ein System mit Docker Compose zu starten
- einfache Fehler in einer Compose-Konfiguration zu finden und zu beheben

## Ausgangslage

Das Repository enthält eine kleine Demo-Anwendung mit mehreren Services:

- `web` = statische Webseite
- `api` = kleine Python-API
- `admin` = zusätzlicher Container

Nicht alles ist bereits korrekt konfiguriert.

## Hinweise

* Arbeiten Sie strukturiert
* Lesen Sie die Fehlermeldungen im Terminal genau
* Nicht alles muss auf Anhieb funktionieren
* Ziel ist das Verstehen, nicht nur das Ausführen

## Abgabe / Nachweis

Am Ende sollte:

* das System startbar sein
* `questions.md` beantwortet sein

## Arbeitsauftrag

Bearbeiten Sie den Auftrag in Ihrem eigenen Repository:

```bash
cp -rf mini-compose-motivation ~/bbzw/bbzw-m347-<klasse>_<nachname>_<vorname>/pw01/02_task/
````

### 1. System starten

Starten Sie das System mit Docker Compose:

```bash
docker compose up --build
````

### 2. Beobachten

Prüfen Sie:

* Welche Services starten?
* Welche Services starten nicht?
* Was ist im Browser erreichbar?
* Was sehen Sie im Terminal?

### 3. Konfiguration analysieren

Öffnen Sie die Datei `compose.yaml` und analysieren Sie:

* welche Services definiert sind
* welche Services `image` verwenden
* welche Services `build` verwenden
* welche Ports definiert sind

### 4. Fehler beheben

Beheben Sie den Fehler in der Konfiguration, damit das System vollständig startet.

### 5. Kleine Anpassung

Ändern Sie den Web-Port von `8080` auf `8000`.

### 6. Docker Compose CLI kennenlernen

Sobald das System korrekt läuft, machen Sie sich mit weiteren Docker Compose Befehlen vertraut.

Führen Sie die folgenden Befehle aus und beobachten Sie jeweils, was passiert:

#### Container temporär stoppen
```bash
docker compose stop
````

* Was passiert mit den Containern?
* Läuft die Anwendung noch im Browser?

---

#### Container wieder starten

```bash
docker compose start
```

* Startet das System wieder korrekt?

---

#### Container pausieren / fortsetzen

```bash
docker compose pause
docker compose unpause
```

* Was ist der Unterschied zu `stop` / `start`?

---

#### Logs anzeigen (Fehlersuche)

```bash
docker compose logs
```

* Welche Informationen sehen Sie?
* Von welchem Service stammen die Logs?

---

#### Status der Container anzeigen

```bash
docker compose ps
```

* Welche Container laufen aktuell?
* Welche Ports sind aktiv?

---

### Ziel

Sie verstehen, wie Sie ein laufendes System:

* stoppen und starten
* analysieren
* überwachen

### 7. Fragen beantworten

Beantworten Sie anschliessend die Fragen in `questions.md`.
