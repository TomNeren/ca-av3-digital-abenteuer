# CA AV3 – Das große Digital-Abenteuer

Ein Lern- und Wiederholungsspiel für **Computeranwendungen** in der Ausbildungsvorbereitung
(AV/AVdual, Baden-Württemberg). Eine einzige HTML-Datei, **läuft komplett offline** – kein Server,
keine Bibliotheken, kein Internet nötig.

7 Welten (BPE 1–6 + Finale) mit vielen Aufgabentypen (Quiz, Zuordnen, Sortieren, Lückentext,
Memory, Entscheidungs-Simulationen, Fake-Webseiten-Detektiv, Passwort-Baukasten, echte Excel-Zelle,
Postfach-Triage, Online-Formular). Mit Punkten, Rängen, Abzeichen, Vorlese-Funktion, „Nochmal
versuchen", Streak-Kombo, Bericht-Export und einer **Offline-Bestenliste**.

---

## Für Schüler:innen – so spielt man

1. **`index.html` öffnen** (Doppelklick oder im Browser).
2. Namen eingeben und losspielen. Der Fortschritt wird **auf diesem PC** im Browser gespeichert.
   ⚠️ Wichtig bei Nutzung als lokale Datei: immer **dieselbe Datei am selben PC** öffnen, sonst ist
   der Fortschritt weg. (Bei Nutzung über einen Link/GitHub Pages entfällt dieses Problem.)

## Für die Lehrkraft – Bestenliste (ohne Server, ohne Internet)

Es gibt **keinen** zentralen Speicher – jeder PC speichert nur für sich. Die Bestenliste funktioniert
über **Ergebnis-Codes**:

1. Jede/r SuS öffnet **📊 Bericht → „📋 Code kopieren"** und teilt den Code mit dir
   (vorlesen, Schul-Chat, gemeinsame Textdatei auf dem Netzlaufwerk, USB …).
2. Auf deinem PC/Beamer: **📊 Bericht → „🏅 Bestenliste (für die Lehrkraft)"**.
3. Alle Codes in das Feld einfügen (einer pro Zeile) oder per **„📂 Datei laden"** eine gesammelte
   `.txt`/`.csv` einlesen → **„🏆 Rangliste erstellen"**.

Der Parser ist tolerant: auch Zeilen wie `Max M. 120` werden erkannt; pro Name zählt das beste Ergebnis.
Alle Daten bleiben nur auf dem Lehrer-PC.

> Zusätzlich: **„📄 Bericht als Datei speichern"** exportiert eine CSV pro Schüler:in (Name, Punkte,
> pro Aufgabe richtig/falsch) – gut als Bewertungs-/Fördergrundlage.

---

## Online stellen mit GitHub Pages (kostenlos)

`index.html` ist die zu veröffentlichende Datei. So kommt das Spiel unter einen Link:

1. Auf **github.com** ein **neues, öffentliches Repository** anlegen (z. B. `digital-abenteuer`).
2. Dieses lokale Repo verbinden und hochladen (im Projektordner):
   ```bash
   git remote add origin https://github.com/<DEIN-NAME>/digital-abenteuer.git
   git push -u origin main
   ```
   (Beim ersten Push nach GitHub-Login/Token fragen – das kann nur dein Account.)
3. Im Repo: **Settings → Pages → Branch: `main` / `root` → Save**.
4. Nach ein paar Minuten ist das Spiel erreichbar unter
   `https://<DEIN-NAME>.github.io/digital-abenteuer/` – **ein Link für alle**.

**Hinweis Datenschutz/Öffentlichkeit:** Kostenlose GitHub Pages sind **öffentlich** sichtbar. Die
Datei enthält **keine Schülerdaten** (Namen liegen nur lokal im Browser), das Veröffentlichen des
Spiels ist also unbedenklich. Es wird lediglich dein Unterrichtsmaterial öffentlich sichtbar.
Die Bestenliste bleibt auch dann rein lokal (kein Cloud-Speicher).

### Wenn du das Spiel änderst
Die Arbeitskopie heißt `CA-AV3_Digital-Abenteuer.html` (liegt lokal, nicht im Repo). Nach Änderungen
die veröffentlichte Version aktualisieren:
```bash
cp "CA-AV3_Digital-Abenteuer.html" index.html
git add index.html && git commit -m "Update Spiel" && git push
```
(Oder direkt in `index.html` arbeiten.)

---

## Technik
Reines HTML/CSS/Vanilla-JavaScript, ein einziges File, Speicherung über `localStorage`.
Keine externen Abhängigkeiten, keine Tracker, keine Server-Kommunikation.
