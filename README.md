# Computerlinguistische Annotation & Statistische Auswertung

**Bachelorarbeit:** Untersuchung digitaler Kochrezepte im Spannungsfeld von kulinarischer Tradition und künstlicher Intelligenz
**Autorin:** Milena Schwindt
**Institution:** Technische Universität Darmstadt – FB 02 Institut für Sprach- und Literaturwissenschaft

---

## 1. Übersicht

Dieses Repository enthält den Python-Code zur automatisierten syntaktischen und lexikalischen Annotation sowie zur statistischen Auswertung der Datenbasis für die vorliegende Bachelorarbeit. 

Das Skript analysiert ein Korpus von **N = 200 isolierten Zubereitungstexten** (100 human verfasste Rezepte von *eatsmarter.de* vs. 100 KI-generierte Rezepte via *GPT-4*). 

### Extrahierte Indikatoren & Hypothesenprüfungen
- **H1 (Infinitivdominanz):** Erfassung unpersönlicher Instruktionsmuster (VerbForm = Infinitiv/Partizip als Ellipse).
- **H2 (Syntaktische Komplexität):** Erfassung der Nebensatzdichte via Dependency-Parsing (`rc`, `advcl`, `ccomp`) und unterordnenden Konjunktionen (`SCONJ`).
- **H3 (Satzlänge):** Erfassung der Mean Sentence Length in Token (ohne Interpunktion).
- **H4 (Sequenzierung):** Erfassung temporaler und prozeduraler Konnektoren über eine definierte Whitelist.
- **H5 (Imperativ- und Passivgebrauch):** Erfassung von Finito-Imperativen (`Mood=Imp`) sowie des Vorgangspassivs via Satzklammer-Dependency (`aux:pass`)[cite: 4, 5].
- **Lexik & Stil:** Berechnungen zur Type-Token-Ratio (TTR) und zum Nominalstil (Substantiv-Quote)[cite: 4].

---

## 2. Voraussetzungen & Systemanforderungen

- **Python-Version:** 3.10 oder höher
- **Betriebssystem:** Windows, macOS, Linux, oder Google Colab

### Benötigte Bibliotheken (Dependencies)
- `spacy` (>= 3.7.0)
- `pandas` (>= 2.0.0)
- `numpy` (>= 1.24.0)
- `scipy` (>= 1.10.0)
- `statsmodels` (>= 0.14.0)

---

## 3. Installation & Einrichtung

### Schritt 1: Korpusdaten bereitstellen
Laden Sie die Dateien zu beiden Untersuchungskorpora "Korpus_Rezepte_ChatGPT.txt" und "Korpus_Rezepte_EAT SMARTER.txt" in Ihrem Google Colab Notebook hoch.

### Schritt 2: SpaCY einlesen
Führen Sie über die Konsole den Code aus Datei "Code_spaCY einlesen.txt" aus.

### Schritt 3: Rezepte einlesen
Führen Sie über die Konsole den Code aus Datei "Code_Rezepte_einlesen.txt" aus.

### Schritt 4: Annotation durchführen
Führen Sie über die Konsole den Code aus Datei "Code_Annotationen.txt" aus.
