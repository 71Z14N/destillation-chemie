# Auf GitHub Pages veröffentlichen

## Kurz: ja, das geht — aber vorher drei Dinge prüfen

### 1. Die Teilchenmodell-Grafik (`assets/teilchenmodell.png`)

Das ist die einzige Datei auf der Seite, die nicht von euch stammt. Wenn sie aus dem
Unterrichtsskript, einem Lehrmittel oder einer Bilddatenbank kommt, ist sie
urheberrechtlich geschützt und darf **nicht** ohne Erlaubnis öffentlich ins Netz.

Drei Wege:

- **a)** Lehrperson fragen, ob die Grafik verwendet werden darf, und die Quelle in der
  Bildunterschrift nennen.
- **b)** Bild löschen. Die animierte Simulation darüber ist eigenständig gebaut und
  erklärt dasselbe — die Seite funktioniert ohne das Bild vollständig. Dazu in
  `index.html` den Block `<figure class="figurebox"> … </figure>` entfernen.
- **c)** Repository privat lassen (siehe Variante B weiter unten).

### 2. Namen und Personendaten

Auf der Seite stehen drei volle Namen. Die beiden anderen sollten einverstanden sein,
dass ihr Name öffentlich und für Suchmaschinen auffindbar im Netz steht. Falls nicht:
Vornamen oder Initialen verwenden. Den Namen der Lehrperson und den Schulnamen habe ich
bewusst weggelassen.

### 3. Messdaten

Eure eigenen Messwerte — unproblematisch.

---

## Variante A — öffentlich, kostenlos (Standardweg)

1. Auf [github.com](https://github.com) einloggen, oben rechts **+ → New repository**.
2. Name z. B. `destillation`, Sichtbarkeit **Public**, kein README ankreuzen
   (wir haben schon eins). **Create repository**.
3. Dateien hochladen. Entweder per Drag & Drop über **Add file → Upload files**
   (`index.html`, `README.md`, `VEROEFFENTLICHEN.md` und den Ordner `assets`), oder im
   Terminal:

   ```sh
   cd ~/Documents/destillation-website
   git init
   git add .
   git commit -m "Präsentationsseite Destillationsversuch"
   git branch -M main
   git remote add origin https://github.com/DEIN-USERNAME/destillation.git
   git push -u origin main
   ```

4. Im Repository auf **Settings → Pages**.
5. Unter *Build and deployment*: **Source: Deploy from a branch**,
   **Branch: `main`**, Ordner **`/ (root)`** → **Save**.
6. Ein bis zwei Minuten warten, dann Seite neu laden. Oben steht die Adresse:

   ```
   https://DEIN-USERNAME.github.io/destillation/
   ```

Fertig. Jede spätere Änderung an `index.html` einfach committen und pushen — Pages
baut automatisch neu (ein paar Sekunden bis Minuten Verzögerung).

## Variante B — nicht öffentlich auffindbar

GitHub Pages aus einem **privaten** Repository braucht GitHub Pro (für Studierende über
[GitHub Education](https://education.github.com) gratis) — und die veröffentlichte Seite
ist dann trotzdem über die URL erreichbar, nur nicht der Quellcode.

Wer die Seite gar nicht ins Netz stellen will, hat es einfacher: Der Ordner funktioniert
lokal genauso. `index.html` doppelklicken, fertig — oder den ganzen Ordner auf einen
USB-Stick kopieren und im Schulzimmer am Beamer-Rechner öffnen.

## Häufige Stolpersteine

| Problem | Ursache |
|---|---|
| Seite bleibt 404 | Nach dem ersten Aktivieren dauert es 1–2 Minuten. Danach Cache leeren (Cmd+Shift+R). |
| Bild fehlt, Rest lädt | Ordner `assets` wurde nicht mit hochgeladen, oder Datei heisst anders. Gross-/Kleinschreibung zählt auf GitHub Pages! |
| Animation läuft nicht | JavaScript im Browser deaktiviert, oder die Seite wurde als reine Datei aus einer E-Mail geöffnet. |
| Ganz weisse Seite | `index.html` liegt nicht im Wurzelverzeichnis des Repos, sondern in einem Unterordner. |
