# Destillation — Chemie-Praktikum Versuch 01

Präsentationsseite zum Praktikumsversuch «Destillation eines Alkohol/Wasser-Gemischs».
Gruppe: Laurin Antz, Janis von Allmen, Laurin Zoss.

Enthält:

- kurze Erklärung des Experiments (Ziel, Prinzip, physikalische Grundlage)
- geschichtlicher Teil als Zeitstrahl (3500 v. Chr. bis heute)
- interaktive, animierte Teilchenmodell-Simulation der Destillationsapparatur
- die drei geforderten x/y-Diagramme aus unseren Messdaten
  (Temperatur, Dichte und Alkoholgehalt über dem kumulierten Volumen)
- das vollständige Messprotokoll als Tabelle
- Interpretation und Fehlerdiskussion

## Aufbau

```
index.html                  komplette Seite (HTML, CSS, JS in einer Datei)
assets/teilchenmodell.png   Übersichtsgrafik zum Teilchenmodell
```

Keine externen Abhängigkeiten, kein Build-Schritt, kein CDN. Die Datei lokal im Browser
öffnen genügt.

## Lokal ansehen

```sh
python3 -m http.server 8000
# dann http://localhost:8000 öffnen
```

## Auf GitHub Pages veröffentlichen

Siehe `VEROEFFENTLICHEN.md`.

## Daten

Alle Messwerte stammen aus unserem eigenen Protokoll (Tab. 1, 25 Fraktionen à 2 mL).
Die Diagramme werden im Browser direkt aus diesen Zahlen gerechnet — sie stehen als
Arrays am Anfang des `<script>`-Blocks in `index.html` und lassen sich dort korrigieren.
