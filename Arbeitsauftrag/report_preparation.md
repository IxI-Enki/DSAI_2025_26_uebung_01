---
title: "Bericht – Suche nach Datasets: Spotify Churn"
puppeteer:
  format: "A4"
  printBackground: true
  displayHeaderFooter: true
  margin:
    top: "1.5cm"
    bottom: "1.8cm"
    left: "1.8cm"
    right: "1.8cm"
  headerTemplate: "<div style='font-size:8px; width:100%; text-align:center;'></div>"
  footerTemplate: "<div style='font-size:9px; width:100%; padding:0 1cm;'><span style='float:left;'>Team: Jan Ritt; Imre Obermüller</span><span style='display:block; text-align:center;'>Thema: Suche nach Datasets – Spotify Churn</span><span style='float:right;'><span class='pageNumber'></span>/<span class='totalPages'></span></span></div>"
---

  <img src="../img/logo_jaim.png" alt="logo" style="display: block; margin: 0 auto; width: 400px; height: auto;" />

- ### Thema: *Suche nach Datasets – Spotify Churn* <!-- <title:topic> -->

- ### Team: ${ \color{navy}\texttt{ j\color{royalblue}{AI}\color{navy}{m} } }$ <!-- <title:team> -->
  
  - #### **Mitglieder**
  
    - Jan Ritt
    - Imre Obermüller

- ### **Datum des Arbeitsauftrags**: 01.10.2025 <!-- <title:date> -->

---

<div style="page-break-after: always;"></div>

***Inhaltsverzeichnis*** <!-- <section:toc> -->

- [Workflow ](#workflow-)
- [Ergebnisse ](#ergebnisse-)
  - [Analyse der Aufgabenstellung ](#analyse-der-aufgabenstellung-)
  - [Lösungen ](#lösungen-)
    - [Statements ](#statements-)
    - [Ergebnis der Statements ](#ergebnis-der-statements-)
    - [Interpretation ](#interpretation-)
  - [Zusammenfassung der Ergebnisse ](#zusammenfassung-der-ergebnisse-)
- [Detaillierter Bericht](#detaillierter-bericht)
  - [Zusammenfassung ](#zusammenfassung-)
  - [1. Datensatz-Suche und Auswahl ](#1-datensatz-suche-und-auswahl-)
  - [2. Metadaten-Analyse ](#2-metadaten-analyse-)
  - [3. Datenstruktur-Analyse ](#3-datenstruktur-analyse-)
  - [4. Explorative Datenanalyse (EDA) ](#4-explorative-datenanalyse-eda-)
  - [5. Eignung für Klassifikation ](#5-eignung-für-klassifikation-)
  - [6. Referenzen ](#6-referenzen-)
  - [Anhang A – Kurzüberblick Felder ](#anhang-a--kurzüberblick-felder-)

---

## Workflow <!-- <section:workflow> -->

- **Ablauf des Projektes**: <!-- <workflow:overview> -->

  : Suche passender Datasets →
    : Kriterien prüfen →
      : Metadaten analysieren →
        : Datenstruktur prüfen →
          : EDA durchführen →
            : Bericht/Präsentation erstellen

- **Detailabschnitte**:  

  - Datensatz-Suche und Auswahl (Kriterien, Quellen) <!-- <workflow:search> -->  
  - Metadaten-Analyse (Quelle, Lizenz, Semantik) <!-- <workflow:metadata> -->  
  - Datenstruktur-Analyse (Spalten, Typen) <!-- <workflow:structure> -->  
  - EDA (Zielverteilung, erste Beobachtungen) <!-- <workflow:eda> -->

<div style="page-break-after: always;"></div>

## Ergebnisse <!-- <section:results> -->

### Analyse der Aufgabenstellung <!-- <results:analysis> -->

Die Aufgabe verlangt ein CSV-Dataset mit klarer Klassifizierungsspalte. Das ausgewählte Kaggle‑Dataset „Spotify Dataset for Churn Analysis“ ist synthetisch, enthält die Zielvariable `is_churned` (0/1) und erfüllt Lizenz‑, Format‑ und Dokumentationsanforderungen. <!-- <results:requirements_match> -->

### Lösungen <!-- <results:solutions> -->

#### Statements <!-- <solutions:statements> -->

- Der Datensatz liegt als CSV vor und besitzt die Klassifizierungsspalte `is_churned`. <!-- <stmt:csv_target> -->
- Die Feature‑Menge ist gemischt (kategorial + numerisch) und EDA‑tauglich. <!-- <stmt:mixed_features> -->
- Metadaten und Lizenz (Apache 2.0) erlauben freie Nutzung für Lehre/Analyse. <!-- <stmt:license> -->

#### Ergebnis der Statements <!-- <solutions:results> -->

- Zielverteilung (siehe Abbildung):  
  ![Zielverteilung is_churned](../img/counts_churned.png) <!-- <figure:counts_churned_ref> -->

#### Interpretation <!-- <solutions:interpretation> -->

Die Verteilung von `is_churned` ist für binäre Klassifikation geeignet. Die Kombination aus Nutzungsintensität (`listening_time`), Interaktionen (`skip_rate`) und Kontextmerkmalen (`subscription_type`, `device_type`) liefert eine sinnvolle Grundlage für Baseline‑Modelle (z. B. logistische Regression, Bäume). <!-- <interpretation:readiness> -->

### Zusammenfassung der Ergebnisse <!-- <zusammenfassung-ergebnisse> -->

Das Dataset erfüllt alle Muss‑Kriterien, die EDA zeigt eine konsistente Zielvariable und aussagekräftige Prädiktoren. Es eignet sich für Lehrzwecke (Datenaufbereitung, Visualisierung, Klassifikation) und kann ohne rechtliche Hürden verwendet werden. <!-- <summary:fit> -->

---

## Detaillierter Bericht

### Zusammenfassung <!-- <section:abstract> -->

Wir haben ein geeignetes, frei verfügbares Tabellendataset zur Klassifikationsaufgabe „Churn-Vorhersage“ ausgewählt: das „Spotify Dataset for Churn Analysis“ (synthetisch generiert). Der Datensatz erfüllt die in der Aufgabenstellung geforderten Kriterien (CSV-Format, Klassifizierungsspalte), ist gut dokumentiert (Metadaten vorhanden) und für EDA sowie den Aufbau einfacher Baseline-Modelle geeignet. Die Zielvariable `is_churned` klassifiziert Nutzer in „aktiv“ (0) und „gekündigt“ (1). Erste EDA-Ergebnisse (Notebook) zeigen eine sinnvolle Merkmalsstruktur aus numerischen und kategorialen Feldern. Der Datensatz ist damit für Lehrexperimente zu Datenaufbereitung, Visualisierung und Klassifikation angemessen. <!-- <meets_requirements> -->

---

### 1. Datensatz-Suche und Auswahl <!-- <section:search_and_selection> -->

- Quelle(n): data.gv.at, kaggle.com <!-- <sources:list> -->  
- Auswahl: `Kaggle – Spotify Dataset for Churn Analysis` (Apache-2.0-Lizenz) <!-- <selection> -->  
- Begründung:  
  - CSV-Format und klarer Klassifikations-Target (`is_churned`) <!-- <criterion:csv_target> -->  
  - Ausreichende Feature-Vielfalt (Nutzer-, Nutzungs- und Geräteattribute) für EDA und Baselines <!-- <criterion:features> -->  
  - Frei zugänglich, mit Metadaten und klarer Lizenz <!-- <criterion:metadata_license> -->

---

<div style="page-break-after: always;"></div>

### 2. Metadaten-Analyse <!-- <section:metadata> -->

- **Titel**: Spotify Analysis Dataset 2025 <!-- <meta:title> -->  
- **Katalog/Quelle**: Kaggle – `spotify-dataset-for-churn-analysis` <!-- <meta:catalog_source> -->  
- **Ersteller (Creator)**: nabiha zahid <!-- <meta:creator> -->  
- **Lizenz**: Apache 2.0 (`https://www.apache.org/licenses/LICENSE-2.0`) <!-- <meta:license> -->  
- **Publikation/Update**: veröffentlicht 2025-08-29; zuletzt geändert 2025-08-28 <!-- <meta:dates> -->  
- **Zugriff**: kostenfrei zugänglich; Live-Dataset <!-- <meta:access> -->  
- **Datencharakter**: synthetisch generiert für EDA/ML (kein realer Zeitraum) <!-- <meta:nature> -->  
- **Distribution**: ZIP-Archiv mit `spotify_churn_dataset.csv` <!-- <meta:distribution> -->  
- **Zeilen-Semantik**: eine Zeile = ein Spotify-Nutzer <!-- <meta:row_semantics> -->  
- **Zielvariable**: `is_churned` (0 = aktiv, 1 = gekündigt) <!-- <meta:target> -->

---

### 3. Datenstruktur-Analyse <!-- <section:data_structure> -->

Der Datensatz ist tabellarisch (CSV) mit numerischen und kategorialen Merkmalen. Vorgesehene Felder (intended types): <!-- <from:preparation.md> -->

- `user_id` (Text) <!-- <col:user_id> -->  
- `gender` (Text) <!-- <col:gender> -->  
- `age` (Integer) <!-- <col:age> -->  
- `country` (Text) <!-- <col:country> -->  
- `subscription_type` (Text) <!-- <col:subscription_type> -->  
- `listening_time` (Integer, Minuten/Tag) <!-- <col:listening_time> -->  
- `songs_played_per_day` (Integer) <!-- <col:songs_played_per_day> -->  
- `skip_rate` (Float) <!-- <col:skip_rate> -->  
- `device_type` (Text) <!-- <col:device_type> -->  
- `ads_listened_per_week` (Integer) <!-- <col:ads_listened_per_week> -->  
- `offline_listening` (Integer-Flag) <!-- <col:offline_listening> -->  
- `is_churned` (Integer-Flag, Target) <!-- <col:is_churned target> -->

Hinweise zur Nutzung: <!-- <notes:data_usage> -->

- Kategoriale Merkmale können via One-Hot-Encoding oder Target-Encoding verarbeitet werden.  
- Numerische Merkmale sollten auf Ausreißer geprüft und ggf. skaliert werden.  
- Die Zielvariable ist binär; geeignete Metriken sind z. B. Accuracy, F1, ROC-AUC.

---

### 4. Explorative Datenanalyse (EDA) <!-- <section:eda> -->

Die EDA wurde in `notebooks/spotify_churn_eda_executed.ipynb` durchgeführt und dokumentiert. <!-- <ref:notebook_executed> -->  
Zentrale Visualisierung der Zielverteilung: <!-- <viz:target_distribution> -->

![Zielverteilung is_churned](../img/counts_churned.png) <!-- <figure:counts_churned> -->

Beobachtungen (aus der EDA, qualitativ zusammengefasst): <!-- <observations> -->

- Die Zielvariable `is_churned` ist klar definiert (0/1) und für Klassifikation geeignet.  
- Die Feature-Menge deckt Nutzungsintensität (z. B. `listening_time`), Interaktion (`skip_rate`), Produktvariante (`subscription_type`) und Kontext (`device_type`, `ads_listened_per_week`) ab.  
- Für Baselines sind einfache Vorverarbeitungsschritte ausreichend; weiterführend könnte Feature-Engineering (z. B. Interaktionen, Binning) nützlich sein.

---

### 5. Eignung für Klassifikation <!-- <section:classification> -->

Begründung der Eignung: <!-- <justification> -->

- Binäres Ziel (`is_churned`) und mehrere erklärende Variablen mit plausibler Beziehung zur Churn-Neigung.  
- Synthetische Daten vermeiden Datenschutzprobleme und sind für didaktische Zwecke geeignet.  
- CSV-Format erleichtert den Einstieg in Datenaufbereitung und Modellierung.

---

<div style="page-break-after: always;"></div>

### 6. Referenzen <!-- <section:references> -->

- Kaggle Katalogeintrag: `https://www.kaggle.com/datasets/nabihazahid/spotify-dataset-for-churn-analysis` <!-- <ref:kaggle> -->  
- Lokale Metadaten: `spotify-dataset-for-churn-analysis-metadata.json` <!-- <ref:local_metadata> -->  
- Datendatei: `spotify_churn_dataset.csv` <!-- <ref:local_csv> -->  
- EDA-Notebook: `notebooks/spotify_churn_eda_executed.ipynb` <!-- <ref:local_notebook> -->  
- Präsentation: `spotify_presentation.pdf` <!-- <ref:local_presentation> -->

---

### Anhang A – Kurzüberblick Felder <!-- <appendix:fields> -->

Kurzzusammenfassung der Felder (siehe auch Abschnitt 3): <!-- <crossref:section3> -->

| Feld | Typ (intended) | Bedeutung |
|---|---|---|
| user_id | Text | Nutzer-ID |
| gender | Text | Geschlecht |
| age | Integer | Alter |
| country | Text | Land |
| subscription_type | Text | Abo-Typ (Free/Premium/Family/Student) |
| listening_time | Integer | Minuten pro Tag |
| songs_played_per_day | Integer | Songs pro Tag |
| skip_rate | Float | Anteil übersprungener Songs |
| device_type | Text | Gerätetyp (Mobile/Desktop/Web) |
| ads_listened_per_week | Integer | Werbeeinblendungen pro Woche |
| offline_listening | Integer (Flag) | Offline-Modus genutzt |
| is_churned | Integer (Flag) | Zielvariable: 0 aktiv, 1 gekündigt |

<!-- End of file -->
