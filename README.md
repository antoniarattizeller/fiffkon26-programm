# FIfFKon42 – Programm

Eine schlanke, inoffizielle Programmansicht für die **FIfFKon42 „Keine Panik! Resilienz in der Polykrise“** (30. Oktober – 1. November 2026, Delphi Saal).

Eine einzige `index.html`, keine Build-Tools, kein Backend – einfach im Browser öffnen oder über GitHub Pages ausliefern.

## Features

- **Tagesauswahl** für die drei Konferenztage
- **Live-Markierung** des gerade laufenden Programmpunkts (Zeitzone Europe/Berlin) und ein „Jetzt“-Sprung
- **Tagesverlauf-Leiste** mit Fortschrittspunkt und Sprungmarken zu jedem Programmpunkt
- **Filter** nach Volltext und Track (Programm / Kultur)
- **„Merken“** – persönliche Auswahl, lokal im Browser gespeichert (`localStorage`)
- **Detailansicht** mit Abstract, Referent:innen-Bios und Link in den offiziellen Fahrplan
- **Hell / Dunkel / Automatisch** umschaltbar

## Daten

Die Programmdaten sind aus dem offiziellen FIfFKon-Fahrplan (pretalx) exportiert und direkt in `index.html` eingebettet
(`<script type="application/json" id="data">`). Quelle: <https://fahrplan.2026.fiffkon.de/fiffkon26/schedule/>

Stand: 30. Oktober 2026. Spätere Änderungen am offiziellen Programm sind ggf. nicht enthalten.

## Daten aktualisieren

```bash
curl -s https://fahrplan.2026.fiffkon.de/fiffkon26/schedule/export/schedule.json -o schedule.json
# danach das eingebettete JSON in index.html (Block #data) neu erzeugen
```

---

Aufbau und Gestaltung angelehnt an [devcon-map](https://github.com/cicerohellmann/devcon-map). Inoffiziell, nicht vom FIfF betrieben.
