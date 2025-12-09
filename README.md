# ADayS – KI-gestützte To-Do-Liste für Menschen mit ADS/ADHS



##  Zusammenfassung
ADayS ist eine KI-gestützte To-Do-Liste für Menschen mit ADS/ADHS. Die App hilft, große Aufgaben in kleine, machbare Schritte zu zerlegen, eine überschaubare Tagesplanung zu erstellen und Überforderung zu reduzieren. Projekt im Kurs „KI entwickeln“.

## Ihre Idee in Kürze

Projektname: ADayS – Eine intelligente To-Do-Liste für Menschen mit ADS/ADHS

**Kurzbeschreibung:**  
ADayS ist eine KI-unterstützte To-Do- und Alltagsplanungs-App, die speziell auf die Bedürfnisse von Menschen mit ADS/ADHS zugeschnitten ist.  
Statt nur Aufgaben zu sammeln, hilft ADayS dabei,

- große Aufgaben in kleine, machbare Schritte zu zerlegen,
- eine kurze, überschaubare Liste an „nächsten sinnvollen Schritten“ vorzuschlagen,
- Energielevel, Zeitfenster und Überforderung zu berücksichtigen.

Das Ziel ist nicht Perfektion, sondern ein alltagstaugliches, freundliches Werkzeug, das Struktur gibt, ohne zusätzlichen Druck zu erzeugen.

---

## Hintergrund

### Welches Problem soll die Idee lösen?

Viele Menschen mit ADS/ADHS haben Schwierigkeiten mit:

- Aufgaben überhaupt anzufangen,
- Aufgaben zu Ende zu bringen,
- Prioritäten zu setzen („Was ist wirklich wichtig?“),
- Zeit realistisch einzuschätzen,
- sich von klassischen To-Do-Apps nicht erschlagen zu fühlen.

Normale Produktivitäts-Apps richten sich meist an neurotypische Nutzer:innen: viele Listen, viele Optionen, viel Text. Für Menschen mit ADS/ADHS kann das schnell überfordern. Es fehlt eine Lösung, die speziell auf ihre Art zu denken eingeht: kleinschrittig, visuell, freundlich, nicht wertend.

### Wie verbreitet ist das Problem?

ADS/ADHS betrifft einen relevanten Anteil der Bevölkerung.  
Betroffen sind Kinder, Jugendliche und Erwachsene – in Schule, Ausbildung, Studium, Job und Privatleben.  
Organisations- und Planungsprobleme im Alltag sind eines der häufigsten Themen im Umgang mit ADS/ADHS.

### Persönliche Motivation

Ich habe selbst ADS und kenne den Frust:  
To-Do-Listen werden schnell zu langen Schuldlisten, statt zu hilfreichen Werkzeugen. Dinge bleiben liegen, obwohl man sie eigentlich erledigen möchte. Meine Motivation ist, ein System zu entwickeln, das sich an meine Realität anpasst – nicht umgekehrt.

### Warum ist das Thema wichtig oder interessant?

- Es verbindet **KI-Techniken** mit einem **konkreten, realen Alltagsproblem**.
- Es kann direkt die Lebensqualität von Betroffenen verbessern.
- Es zeigt, dass KI nicht nur „smart“, sondern auch **empathetisch und unterstützend** gestaltet werden kann.

---

## Daten und KI-Techniken

### Datenquellen

Für einen ersten Prototyp kann ADayS mit relativ einfachen Daten arbeiten:

- Aufgaben, die Nutzer:innen eingeben (Text), z.B.
  - „Steuererklärung machen“
  - „Küche aufräumen“
  - „Mail an Lehrer schreiben“
- Zusatzangaben pro Aufgabe (optional):
  - geschätzte Dauer (z.B. 5 / 15 / 30 / 60 Minuten),
  - Kontext (z.B. „zu Hause“, „unterwegs“, „PC nötig“, „Telefon nötig“),
  - aktuelles Energielevel („müde“, „okay“, „fit“),
  - Deadline oder Wunschdatum,
  - subjektive Einschätzung: „fühlt sich schwer an“ / „ist okay“.

Für das Kursprojekt können diese Daten

- teilweise **synthetisch** erzeugt werden (Beispielaufgaben),
- teilweise aus **eigener Erfahrung** (anonymisiert) stammen.

Später, in einer echten App, würden die Daten lokal auf dem Gerät oder datenschutzfreundlich gespeichert.

### Geplante KI-Techniken

1. **NLP zur Aufgabenanalyse**
   - Einfache Textklassifikation: Zuordnung von Aufgaben zu Kategorien wie „Haushalt“, „Arbeit/Schule“, „Finanzen“, „Soziales“.
   - Einschätzung, ob eine Aufgabe „groß/komplex“ wirkt (z.B. viele abstrakte Begriffe → eher in Teilaufgaben aufteilen).
   - Technische Umsetzung (mögliche Optionen):
     - TF-IDF + klassische Klassifikatoren (z.B. Logistic Regression, SVM),
     - oder leichte vortrainierte Sprachmodelle (z.B. über Hugging Face).

2. **Regelbasierte + KI-unterstützte Priorisierung**
   - Kombination aus:
     - einfachen Regeln (Deadlines, Dauer, Energielevel, Kontext)
     - und einem einfachen Modell, das mit Nutzungsdaten lernt, welche Vorschläge gut angenommen werden.
   - Ziel ist eine **kurze Prioritätenliste** (z.B. 3–5 Aufgaben), um Überforderung zu vermeiden.

3. **Personalisierung anhand von Feedback**
   - Nutzer:innen markieren, ob Vorschläge „hilfreich“ waren.
   - Das System passt sich schrittweise an individuelle Muster an (z.B. bevorzugte Tageszeiten oder Aufgabentypen).

### Mögliche Demo

Für das Kursprojekt reicht ein einfacher Prototyp, z.B.:

- Ein Jupyter-Notebook oder eine kleine Web-App,
- Eingabe: Liste von Aufgaben + optional Energielevel und verfügbare Zeit,
- Ausgabe:
  - eine sortierte Liste an „empfohlenen nächsten Aufgaben“,
  - eventuell automatisch vorgeschlagene Teilaufgaben.

---

## Wie wird es eingesetzt?

### Nutzungskontext

ADayS soll Menschen mit ADS/ADHS im Alltag unterstützen, z.B.

- beim Planen des Tages,
- beim Strukturieren von Hausaufgaben / Studium,
- beim Managen von Haushalt, Terminen und Bürokratie.

Typischer Ablauf:

1. Nutzer:in sammelt alle Aufgaben als einfache Liste (Brain Dump).
2. ADayS analysiert die Liste und:
   - ordnet Aufgaben grob in Kategorien ein,
   - identifiziert große / schwierige Aufgaben und schlägt Teilaufgaben vor,
   - wählt basierend auf Energielevel, Zeit und Dringlichkeit eine kleine Auswahl an Aufgaben für „jetzt“.
3. Nutzer:in arbeitet mit dieser kleinen Liste und kann Feedback geben („hat geholfen“ / „war zu viel“).

### Beteiligte Personen

- **Primäre Zielgruppe:** Menschen mit ADS/ADHS.
- **Sekundäre Gruppen:** Angehörige, Therapeut:innen, Coaches, die gemeinsam an Struktur und Alltagorganisation arbeiten (nur, wenn Nutzer:innen das möchten und es datenschutzkonform ist).

Wichtig ist, die Sicht der Betroffenen ernst zu nehmen:

- Sprache in der App soll **unterstützend, nicht wertend** sein.
- Fehler und Vergessen sind normal, nicht ein „Versagen“.

---

## Herausforderungen

### Was löst das Projekt nicht?

- ADayS ist **keine medizinische Behandlung** und ersetzt keine professionelle Diagnose oder Therapie.
- Es kann nicht alle Ursachen von Prokrastination, Erschöpfung oder Stress lösen.
- Ohne große Datenmengen bleiben die KI-Modelle relativ einfach und ungenau.
- Die App kann unpassende Vorschläge machen (falscher Zeitpunkt, falsche Einschätzung der Schwierigkeit).

### Technische Grenzen

- Anfangs stehen nur wenige Trainingsdaten zur Verfügung.
- Datenschutz und lokale Verarbeitung können die Wahl der Modelle einschränken.
- KI „versteht“ Aufgaben nicht wirklich, sondern erkennt nur Muster in Texten und Nutzungsdaten.

---

## Wie geht es weiter?

Mögliche Entwicklungsschritte:

1. **Prototyp (Version 0.1)**
   - Einfache Web-Oberfläche oder Notebook,
   - Manuelle Eingabe von Aufgaben,
   - Regelbasierte Priorisierung + erste Textklassifikation.

2. **Nutzerfeedback sammeln**
   - Erste Tests mit Betroffenen (Freunde, Community),
   - Feedback zu Bedienung, Sprache, Menge der Aufgaben.

3. **Ausbau der KI-Komponenten**
   - Bessere Textmodelle zur Aufgabenanalyse,
   - Lernende Priorisierung (Recommender-Ansatz),
   - evtl. Integration von Kalenderdaten.

4. **Produktreife Version**
   - Mobile App oder Web-App,
   - starke Fokussierung auf Datenschutz (z.B. On-Device-Verarbeitung),
   - klare Kommunikation der Grenzen (Hilfsmittel, keine Therapie).

---

## Danksagung

Dieses Projekt verwendet oder könnte verwenden:

- Open-Source-Bibliotheken wie:
  - **Python**, **pandas**, **scikit-learn**, evtl. **PyTorch** oder **TensorFlow**,
  - **NLP-Tools** wie Hugging Face Transformers.
- Ideen und Konzepte aus:
  - Online-Kursen wie „Elements of AI“,
  - öffentlich zugänglichen Informationen zu ADS/ADHS,
  - Blogs, Erfahrungsberichten und Community-Beiträgen von Betroffenen.

Die konkreten Quellen (Repos, Blogposts, Paper, Bilder etc.) werden in dieser README ergänzt, sobald sie im Projekt tatsächlich verwendet werden.  
Bitte beachten Sie: Alle externen Ressourcen werden nur unter Einhaltung der jeweiligen Lizenzen genutzt, und Urheber:innen werden namentlich genannt.
<img width="1024" height="1536" alt="adays-frau-todolist png" src="https://github.com/user-attachments/assets/6965c12b-423e-44b9-843f-e279f6604f88" 
