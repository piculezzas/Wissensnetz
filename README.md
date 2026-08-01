# Wissensnetz „Growth Mindset & Beurteilung" — Projektübersicht

**Kontext:** Bachelorarbeit von Leonie Halser.
**Leitfrage:** *Welche Strategien nutzen Lehrpersonen der 1.–3. Klasse, um im Kontext von Beurteilung ein Growth Mindset zu fördern?*
**Stand dieser Beschreibung:** 01.08.2026 · aktueller Netz-Stand: **`wissensnetz-Version_2_05.json`** (129 Knoten, 194 Kanten, 25 Literatur- + 3 Abbildungseinträge) — identisch in `index.html` eingebacken.

> **Hinweis zum GitHub-Repo:** Seit dem Push vom 31.07.2026 enthält das Repo nur noch einen reduzierten Kernbestand (Tool, aktuellster Netz-Stand, README, Rückmeldungsdokument, zwei PDFs). Die vorherige lokale Ordnerstruktur mit nummerierten Zwischenständen (`_1…_12`), HTML-Backups sowie den Ordnern `neue_Quellen/` und `Quellen_GR/` ist **nicht** Teil dieses Repos. Abschnitt 6 (Historie) bleibt als inhaltliches Gedächtnis stehen, auch wenn die dort genannten Einzeldateien hier nicht mehr vorliegen.

Dieses Dokument macht das Projekt auf jedem Gerät nahtlos weiterbearbeitbar: Es beschreibt alle Dateien, das Tool, das Datenmodell, die Konventionen, die Historie und die offenen Aufgaben.

---

## 1. Schnellstart auf einem neuen Gerät

1. Repo klonen/pullen (`git clone https://github.com/piculezzas/Wissensnetz.git`) oder den Ordner übertragen — alles Nötige liegt darin, es gibt keine externen Abhängigkeiten.
2. `index.html` im Browser öffnen (Doppelklick genügt, läuft komplett offline). Der jeweils aktuellste Netz-Stand ist direkt eingebacken, ein Import ist für den reinen Einstieg nicht nötig.
3. Falls ein anderer/älterer Stand geladen werden soll: oben **«Boards» → «Import»** und die passende JSON-Datei wählen (aktuell: **`wissensnetz-Version_2_05.json`**).
4. Arbeiten. Vor Schluss: **«Export»** klicken und als nächste Nummer speichern (`wissensnetz-Version_2_06.json` usw.), die Datei in den Ordner legen **und committen/pushen** — das Repo ist die geräteübergreifende Wahrheit.

> ⚠️ **Wichtig:** Das Tool sichert den Arbeitsstand automatisch im Browser-Speicher (localStorage) — dieser ist aber **gerätespezifisch**. Die JSON-Stände im Git-Repo sind die einzige geräteübergreifende Wahrheit. Deshalb: nach jeder Session exportieren, fortlaufend nummerieren, committen und pushen.

---

## 2. Dateien im Repo

| Datei | Inhalt |
|---|---|
| `index.html` | **Das Tool** (interaktives Board, alles inline: JS/CSS/Bilder/Literaturliste), mit dem jeweils aktuellsten Netz-Stand fest eingebacken |
| `wissensnetz-Version_2_03.json` | Älterer Netz-Stand (128 Knoten, 185 Kanten) |
| `wissensnetz-Version_2_04.json` | Vorheriger Netz-Stand (129 Knoten, 194 Kanten, 27 Literatureinträge) |
| `wissensnetz-Version_2_05.json` | **Aktueller Netz-Stand** (129 Knoten, 194 Kanten, 25 Literatur- + 3 Abbildungseinträge) — identisch mit dem in `index.html` eingebackenen Stand |
| `Wissensnetz_Version_2_00_Gross.pdf` | Vektor-PDF des Netzes (Stand `_2_00`) in Originalgröße (4714×5055 px) — beliebig zoombar, Text durchsuchbar. ⚠️ nicht mehr inhaltsgleich mit dem aktuellen Stand, siehe Abschnitt 8 zum Neu-Erzeugen |
| `Überarbeitete_Version_2.pdf` | Überarbeitete Version des Posters/Netzes |
| `Welche Strategien nutzen Lehrpersonen….pdf` | Ursprüngliches Poster (1:1-Vorlage des Netzes, Stand 11.07.) |
| `Rueckmeldung_Wissensnetz_2026-07-17.md` | Kritische Analyse + Abarbeitungs-Checkliste + Bibliotheksliste |
| `README.md` | dieses Dokument |

**Nicht (mehr) im Repo, aber in Abschnitt 6/7 referenziert:** HTML-Backups vor einzelnen Feature-Ausbauten, die nummerierten Zwischenstände `_1…_12`, sowie die Ordner `neue_Quellen/` (Literatur-PDFs von David) und `Quellen_GR/` (Schulgesetz, AVS-Weisungen, Handreichung DFB, LP21 GR). Falls diese für die Weiterarbeit gebraucht werden, liegen sie ggf. noch auf einem anderen Gerät oder müssen aus der Cloud/dem Original-Ordner nachgezogen werden.

---

## 3. Das Tool: Bedienung

**Ansichtsmodus (Standard):**
- **Klick auf Themen-Hex** → ganzer Teilbaum wird hervorgehoben.
- **Klick auf Detail-Box** → Herleitungskette zurück zur Wurzel (mit Nummern-Badges).
- **Shift-Klick (oder Alt-Klick) auf beliebige Box** → **Verbindungs-Fokus**: Box + alle direkt verbundenen Boxen über *alle* Pfeilarten (auch pinke Querverbindungen), Rest abgedunkelt, Auto-Zoom. Nochmal klicken/Esc hebt auf. *Das ist das Werkzeug, um z. B. die Belege einer Strategie quer übers Board zu sehen.*
- **Klick auf Quellenangabe oder Literatureintrag** → alle Boxen dieser Quelle leuchten auf. **Cmd-/Shift-/Ctrl-Klick in der Literaturliste** → Mehrfachauswahl: mehrere Quellen sammeln und gemeinsam im Netz anzeigen (funktioniert in der Board-Litbox und im Seitenpanel; das Panel bleibt bei additiver Auswahl offen). Erneuter Modifier-Klick wählt eine Quelle wieder ab; Klick auf leere Fläche/Esc setzt zurück. Die Liste ist **auch im Bearbeiten-Modus** klickbar; Klicks auf Listeneinträge starten nie einen Drag der Litbox (verschieben weiterhin über Titel/Rand möglich).
- **Hover** → direkte Nachbarn leuchten kurz auf.
- **Pfeil-Filter** in der Sidebar (Klick auf Legendenzeile) blendet Pfeilarten ein/aus — wirkt auch auf den Verbindungs-Fokus.
- **Esc** = alles zurücksetzen + Übersicht. **Cmd/Ctrl+Scrollen** = Zoom.
- **Deep-Links:** `#topic=<id>`, `#chain=<id>`, `#link=<id>` (Verbindungs-Fokus), `#src=<Literatur-Index>` in der Adresszeile.

**Bearbeitungsmodus** («Bearbeiten»-Button): Klick auf Box öffnet Editor (Text, Farbe/Ebene, Breite, Löschen); «+ Box» erstellt neue; Pfeile per Zug von den Randgriffen einer Box; Klick auf Pfeil → Art ändern/biegen/löschen. **Button «✎ Text bearbeiten» oben in der lavendelfarbigen Literaturbox** öffnet einen eigenen Editor für Literatur- und Abbildungsverzeichnis als Freitext (eine Quelle/Bildunterschrift pro Zeile) — Tippfehler, Klammern und Jahreszahlen lassen sich so direkt im Tool korrigieren, ohne den HTML-Code anzufassen. Siehe Abschnitt 4 für die Klammer-Kurztitel-Konvention, falls ein neuer Eintrag dadurch nicht automatisch mit seinen Kurzbelegen im Netz verknüpft wird.

**Persistenz:** Auto-Save in localStorage; benannte Boards + JSON-Import/-Export unter «Boards».

---

## 4. Datenmodell (JSON)

```
{ "version": 1, "savedAt": "…", "nodes": [...], "edges": [...], "references": [...], "figures": [...] }
```

`references`/`figures` sind seit dem Literatur-Editor (siehe Abschnitt 3) Teil des Exports: einfache String-Arrays mit je einem Literatur- bzw. Abbildungseintrag pro Zeile. Ältere JSON-Stände ohne diese Felder werden beim Import automatisch mit der im Tool eingebackenen Standard-Literaturliste aufgefüllt.

**Node:** `id`, `tier`, `shape`, `x`, `y`, `w`, `h`, dazu je nach Form: `label` (hex/banner/note/hand), `heading`+`text`+`list`+`cite` (rect), `img`+`caption`+`alt` (figure).

**Tiers (Farben):** `uebertitel` (pink) · `kernthema` (grün) · `zentral` (blau, „zentral, aber nicht Kernthema") · `irrelevant` (rot) · Sonderformen `banner`, `figure`, `note`, `hand`, `lit`, `legend`.

**Edge:** `{ "f": <von-id>, "t": <nach-id>, "k": <art> }`, optional `bn`/`bt` (Biegung).
**Pfeilarten:** `grey` = Gliederung/Hierarchie · `pink-dash`/`pink2` = inhaltliche Querverbindung · `red-dash` = Hintergrundtheorie-Bezug.

**ID-Präfixe (Cluster):**
`gm-` Growth-Mindset-Theorie · `uf-` Umgang mit Fehlern · `bw-` Bewertung/Noten · `fb-` Feedback · `syn-` Synthese-Strategien (S1–S6) · `gr-` Kanton GR/LP21 · `sec-` Übertitel · `b-top`/`b-bottom` Banner (Achtung: im aktuellen Layout vertauscht — `b-bottom` = Leitfrage oben, `b-top` = Art. 41 unten) · `note*`/`umrjl*` Notizzettel.

**Wichtig fürs Zitat-Klicken:** Die Quellen-Verlinkung matcht `cite`-Kurzbelege gegen die Literaturliste über *(erstes Wort, Jahreszahl)*. Kurzbelege ohne Jahr (z. B. „Schulgesetz GR, BR 421.000") sind nicht klickbar. Beginnt ein Literatureintrag nicht mit dem Wort, unter dem er im Netz zitiert wird (typischerweise bei Behörden-/Institutionsquellen, deren voller Name als Erstes steht), hilft ein **Klammer-Kurztitel** irgendwo im Eintrag, z. B. `… Graubünden. (2016). Lehrplan 21 Graubünden (Lehrplan). Verfügbar unter: …` macht den Eintrag zusätzlich unter `Lehrplan, 2016` auffindbar — genau nach diesem Muster löst sich der Kurzbeleg „Lehrplan 21 GR, 2016" der drei LP21-Kästchen auf.

---

## 5. Inhaltlicher Aufbau des Netzes

- **Theorie-Cluster (`gm-`):** Dweck-Grundlagen, Forschungsphasen, Übertragung (Haltung ≠ Verhalten!), SOMA/Ego-Threat, falsches GM, Studien (Park 2016 = Zielstufe!, Muthukrishnan 2025, Seaton 2018).
- **Fehler-Cluster (`uf-`):** negatives Wissen, Unterrichtsmuster, Lern-/Leistungssituations-Vermischung, funktionales Fehlerklima.
- **Bewertungs-Cluster (`bw-`):** Gütekriterien, Situationstypen, Bezugsnormen, Notenkritik (seit `_9` den drei Brügelmann-Ebenen zugeordnet: Verfahren / Bezugsnorm / Darstellungsform), Referenzgruppenfehler vs. BFLPE (seit `_8` korrekt getrennt), Meritokratie-Kritik.
- **Feedback-Cluster (`fb-`):** wirksames Feedback, Feedback/Feedup/Feed-Forward, formativ vs. summativ, Feedback-Regler.
- **Synthese-Cluster (`syn-`, oben links bei der Leitfrage):** Wirkmechanismus (Ego-Threat entschärfen) + **fünf Strategien** (seit `_10`; Fusion auf Wunsch von David): **S1** Prozess- statt performanzorientiert — loben, rückmelden, strukturieren (fusioniert aus alt-S1 Prozesslob + alt-S5 Performanzpraktiken vermeiden; ID des gelöschten alt-S5 war `syn-s5`) · **S2** Fehler zu Lernanlässen machen · **S3** Individuelle Bezugsnorm · **S4** Lern-/Leistungssituationen trennen, formativ beurteilen · **S5** Selbst-/Peerbeurteilung stärken (vormals S6; ID bleibt `syn-s6`!). → Das ist die theoretische Antwort auf die Leitfrage und das künftige Kategoriensystem für die Empirie.
- **SDT-Cluster (`sdt-`, rechts beim Theorie-Teil, seit `_10`):** Selbstbestimmungstheorie als Hintergrundtheorie — drei Grundbedürfnisse, informational vs. kontrollierend (Mechanismus hinter S1), Ego-Involvement (Brücke zum Ego-Threat). Dazu die Senko-&-Dawson-Differenzierung der Ziel-Ära (`gm-ziele-diff`). Die beiden „Deci & Ryan"-Notizzettel sind damit aufgelöst.
- **GR-Cluster (`gr-`, unten beim Art.-41-Banner):** Art.-41-Wortlaut, drei Zeugnisformen der 1./2. Klasse (Schulratsentscheid! Noten ab 1. Klasse möglich, ab 3. verbindlich), kantonale Förderorientierung, Handreichung DFB (Beurteilung = „wichtigste Form des Feedbacks", Note = Ermessensentscheid), Lernbericht, LP21-Knoten (Fehlerkultur als Qualitätsmerkmal S. 9, Bezugsnorm-Vorgabe S. 11 — soziale Norm kommt nicht vor!, Selbstreflexion als Kompetenz S. 13).

---

## 6. Historie der Stände

| Stand | Inhalt |
|---|---|
| `_1`, `_2` | Ausgangsstand Leonie (identischer Inhalt, nur Layout) |
| `_3` | +42 fehlende Strukturkanten (Hex→Box, Feedback-Übertitel, Banner, Abbildungen) |
| `_4` | +Synthese-Cluster (Hub, Wirkmechanismus, S1–S5, S6-Platzhalter, 15 Beleg-Links) |
| `_5` | Sicherung durch David (Layout-Anpassungen) |
| `_6` | +GR-Cluster (Art. 41, Zeugnisformen, Förderorientierung, Handreichung, Ermessensentscheid, Lernbericht) |
| `_7` | +LP21-Knoten (Fehlerkultur, Bezugsnorm, Selbstreflexion); S6 kurrikular fundiert |
| `_8` | BFLPE/Referenzgruppenfehler-Korrektur (Sachfehler behoben, Brücke BFLPE→Fixed Mindset) |
| `_9` | Notenkritik den drei Brügelmann-Ebenen zugeordnet (3 Ebenen-Boxen + Zuordnungskanten + Klima-Querbefund) |
| `_10` | S1+alt-S5 fusioniert (alt-S6 → S5 nachgerückt), SDT-Cluster (Ryan & Deci 2019), Senko-&-Dawson-Box zur Ziel-Ära, Deci-&-Ryan-Notizzettel aufgelöst |
| `_11` | Kurzzitate der GR-Knoten mit Jahreszahlen (Schulgesetz 2012, Weisungen 2025) — nötig für die klickbare Quellen-Hervorhebung |
| `_12` | BFLPE-Box-Zitat durch David ergänzt (Trautwein & Baeriswyl, 2007) — damit sind alle 29 Literatureinträge klickbar wirksam |
| `Version_2_00` | Meilenstein — inhaltsgleich `_12`, von David als Abschluss der inhaltlichen Runde benannt |
| `Version_2_03` | Zwischenstand, 31.07.2026 — 128 Knoten, 185 Kanten (Details zu den Schritten zwischen `_2_00` und `_2_03` liegen nicht in diesem Repo vor) |
| `Version_2_04` | 01.08.2026 — 129 Knoten, 194 Kanten. Neuer Knoten `umsafabfk` (Cluster `bw`): „Kontrollierte Subjektivität" + „Kommunikative Validierung" (Beleg: Lötscher et al., 2023, S. 98). 8 neue pinke Querverbindungen, u. a. LP21-Knoten → Synthese-Strategien S2–S4 sowie GR-Bewertungsrahmen ↔ Bezugsnorm-Box. Reine Erweiterung, nichts entfernt. |
| **`Version_2_05`** | **aktuell**, 01.08.2026 — Knoten/Kanten unverändert; erste Bearbeitung der Literaturliste direkt im Tool (neuer „Text bearbeiten"-Editor der Literaturbox). Zwei veraltete/doppelte LP21-Einträge sowie die Weisungen-zu-Zeugnissen-Quelle entfernt (letztere war ungenutzt), dafür ein neuer, korrekter LP21-Eintrag ergänzt und per Klammer-Kurztitel `(Lehrplan)` mit den drei LP21-Kästchen verknüpft, die bisher auf keine Quelle zeigten. |

**HTML-Änderungen** (unabhängig von den JSON-Ständen): Shift-Klick-Verbindungs-Fokus inkl. `#link=`-Deep-Link und Sidebar-Hilfetext; Literaturliste erweitert um 4 amtliche Quellen (AVS-Handreichung 2020, EKUD-Weisungen 2025, Schulgesetz 2012, LP21 GR 2016) sowie Ryan & Deci (2019) und Senko & Dawson (2017) — jetzt 29 Einträge; Mehrfachauswahl in der Literaturliste (Cmd-/Shift-Klick); Klick-Fixes (Litliste vom Box-Drag ausgenommen, Litliste auch im Bearbeiten-Modus aktiv); robusteres Zitat-Matching (Ziffern in Quellennamen wie „Lehrplan 21", Klammer-Kurztitel wie „(Schulgesetz)").

**Neue Quellen** (`neue_Quellen/`, 17.07. abends): Ryan & Deci 2019 „Brick by Brick" (SDT-Primärquelle, Preprint — für BA publizierte Paginierung prüfen) und Senko & Dawson 2017 (Meta-Analyse Performance-Approach-Ziele) sind ins Netz eingearbeitet. Die Buchrezension (csr) und die PHGR-Folie (PNG) dienen nur der Orientierung, nicht als Belege.

---

## 7. Offene Aufgaben

**A. Literaturbeschaffung (Bibliothek, vor dem Einbau recherchieren):** Details und Tabelle in `Rueckmeldung_Wissensnetz_2026-07-17.md`. Kurzfassung: Black & Wiliam (formatives Assessment), Hattie & Timperley 2007, Nicholls 1978 (Fähigkeitskonzept 6–9 J.), Selbst-/Peerbeurteilung junger Lernender (→ S6), Marsh (→ BFLPE-Box), Sisk et al. 2018 (kritische Mindset-Debatte), Deci & Ryan Primärquelle.

**B. Kleinere Netz-Pflege:**
- Doppelkante „Befund 3" ↔ „Übertragungs-Box" auf eine Richtung reduzieren (I6).
- Burnette-Seitenzahlen auf publizierte Paginierung (S. 655–701) korrigieren (I3).
- Oser-Zitierweise vereinheitlichen (I4); Sekundärzitate nach Literaturbeschaffung ersetzen (I5).
- Schulgesetz-PDF ist Stand 2013 → aktuelle konsolidierte Fassung auf gr-lex.gr.ch gegenprüfen (nur im Browser zugänglich).
- Zwei Notizzettel „Deci & Ryan" auflösen, sobald SDT-Primärquelle eingebaut ist.

**C. Perspektive BA:** Die sechs Synthese-Strategien in einen Interviewleitfaden / ein Codiersystem für den Empirieteil übersetzen; Muthukrishnan-Befunde als externe Validierung von S1/S2 nutzen; GR-Besonderheit (Schulrats-Wahl der Zeugnisform) als Interviewfrage einbauen.

---

## 8. Technische Hinweise

- Die HTML-Datei ist selbstständig (keine Internetverbindung nötig); Gesetzes-/Lehrplan-Server blocken automatisierte Zugriffe, im Browser funktionieren sie normal.
- **Kurzzitat-Format für klickbare Quellen:** „Nachname (Grossbuchstabe!), Jahr" muss im `cite`-Feld stehen (z. B. „Trautwein & Baeriswyl, 2007, S. 119ff."). Ohne Jahr oder kleingeschrieben greift die Verknüpfung zur Literaturliste nicht.
- **Gross-PDF neu erzeugen** (nach inhaltlichen Änderungen): Headless-Chrome rendert eine UI-bereinigte Kopie der HTML mit dem gewünschten JSON-Stand und druckt sie als Vektor-PDF in Weltgrösse (`puppeteer-core`, `page.pdf` mit width/height in px). Das Skript-Muster liegt in der Claude-Code-Session vom 17./18.07.2026.
- `node --check` bzw. ein Blick in die Browser-Konsole hilft nach manuellen HTML-Eingriffen.
- Beim Bearbeiten der JSON-Stände per Skript: Kanten-Anker eindeutig wählen (Zitat-Texte im DATA-Block enthalten dieselben Namen wie die Literaturliste!) und Kollisionen der Knoten-Rechtecke prüfen — die bisherigen Skript-Muster stecken in der Chat-Historie der Claude-Code-Session vom 17.07.2026.
