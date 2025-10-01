---
title: "README – Suche nach Datasets: Spotify Churn"
team: jAIm
members: Jan Ritt, Imre Obermüller
date: 01.10.2025
---

<div align="center">

  <img src="img/logo_jaim.png" alt="logo" style="display: block; margin: 0 auto; width: 400px; height: auto;" />

</div>

- ### Thema: *Suche nach Datasets – Spotify Churn* <!-- <title:topic> -->

- ### Team: ${ \color{skyblue}\texttt{ j\color{royalblue}{AI}\color{skyblue}{m} } }$ <!-- <title:team> -->
  
  - #### **Mitglieder**
  
    - Jan Ritt
    - Imre Obermüller

- ### **Datum des Arbeitsauftrags**: 01.10.2025 <!-- <title:date> -->

- ### **Ausgearbeitete Dokumente**

  - [Präsentation](spotify_presentation.pdf)

  - [Bericht](spotify_report.pdf)

---

***Inhaltsverzeichnis*** <!-- <section:toc> -->

- [Workflow ](#workflow-)
- [Ergebnisse ](#ergebnisse-)
  - [Analyse der Aufgabenstellung ](#analyse-der-aufgabenstellung-)
  - [Lösungen ](#lösungen-)
    - [Statements ](#statements-)
    - [Ergebnis der Statements ](#ergebnis-der-statements-)
    - [Interpretation ](#interpretation-)
  - [Zusammenfassung der Ergebnisse ](#zusammenfassung-der-ergebnisse-)

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
  ![Zielverteilung is_churned](img/counts_churned.png) <!-- <figure:counts_churned_ref> -->

#### Interpretation <!-- <solutions:interpretation> -->

Die Verteilung von `is_churned` ist für binäre Klassifikation geeignet. Die Kombination aus Nutzungsintensität (`listening_time`), Interaktionen (`skip_rate`) und Kontextmerkmalen (`subscription_type`, `device_type`) liefert eine sinnvolle Grundlage für Baseline‑Modelle (z. B. logistische Regression, Bäume). <!-- <interpretation:readiness> -->

### Zusammenfassung der Ergebnisse <!-- <zusammenfassung-ergebnisse> -->

Das Dataset erfüllt alle Muss‑Kriterien, die EDA zeigt eine konsistente Zielvariable und aussagekräftige Prädiktoren. Es eignet sich für Lehrzwecke (Datenaufbereitung, Visualisierung, Klassifikation) und kann ohne rechtliche Hürden verwendet werden. <!-- <summary:fit> -->
