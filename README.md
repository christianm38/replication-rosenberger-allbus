# Erweiterte Replikation: Kriminalitätsfurcht und Medienkonsum — ALLBUS 2021

Seminararbeit im Rahmen des Studiums (Empirische Forschungspraktikum 2).
Autorinnen und Autoren: Adrianna Stelmach, Christian Mann, Feyza Dogan, Jennifer Scherer

---

## Einordnung

Diese Studie knüpft an Rosenberger et al. (2023) an und erweitert deren Rahmen in drei Hinsichten.

**Erstens — Kontextübertragung:** Die Originalstudie wird auf den deutschen Kontext übertragen. Da sich die Mediensysteme beider Länder strukturell unterscheiden, ist die Übertragbarkeit der Befunde eine eigenständige empirische Frage, die nicht vorausgesetzt werden kann.

**Zweitens — Theoretische Erweiterung:** Zusätzlich zur medialen Rezeption wird die Viktimisierungserfahrung als moderierende Variable integriert. Damit wird das komplexe Zusammenspiel von medialer Kriminalitätsdarstellung und persönlicher Betroffenheit empirisch erschlossen.

**Drittens — Methodische Kontinuität:** Der intersektionale Analyseansatz aus Rosenberger et al. (2023) — die Berücksichtigung von Geschlecht und Migrationshintergrund als sich wechselseitig bedingende Kategorien — bleibt in dieser Analyse erhalten.

**Originalstudie:**
Rosenberger, J. S., Dierenfeldt, R., & Ingle, H. (2023). Media Consumption and Fear of Crime: Evidence of the Need for an Intersectional Approach. *Victims & Offenders, 18*(4), 691–714. https://doi.org/10.1080/15564886.2021.1991069

---

## Forschungsfragen

- Beeinflusst die Häufigkeit des Fernseh- und Internetkonsums die Kriminalitätsfurcht in der deutschen Bevölkerung?
- Moderieren Geschlecht und Migrationshintergrund diesen Zusammenhang im Sinne eines intersektionalen Ansatzes?
- Moderiert die Viktimisierungserfahrung den Zusammenhang zwischen Medienkonsum und Kriminalitätsfurcht?

---

## Datenbasis

**ALLBUS 2021** — Allgemeine Bevölkerungsumfrage der Sozialwissenschaften
- Erhebungsjahr: 2021
- Stichprobengröße nach Bereinigung: N ≈ 2.600
- Bezug: [GESIS — gesis.org/allbus](https://www.gesis.org/allbus) (ZA5280)

> Der Datensatz ist aus lizenzrechtlichen Gründen nicht im Repository enthalten.

---

## Methodik

**Datenaufbereitung**
- Selektion und Rekodierung relevanter Variablen
- Konstruktion der Migrationshintergrundvariable aus drei Einzelindikatoren (Geburtsland der Person sowie beider Elternteile)

**Indexbildung Kriminalitätsfurcht**
- 8 Items (cf04–cf11), Faktoranalyse zur Dimensionsprüfung
- Item cf04 lädt unter 0.4 → ausgeschlossen
- Cronbach's α = 0.896 → gute interne Konsistenz
- Mittelwertindex aus 7 verbleibenden Items

**Regressionsmodelle**
- H1: Haupteffekte Medienkonsum mit Kontrollvariablen (Alter, Bildung, Einkommen, Wohnort, Haushalt, Region)
- H2: Moderationsanalyse — Geschlecht und Migrationshintergrund (intersektionaler Ansatz)
- H3: Moderationsanalyse — Viktimisierungserfahrung

**Annahmetests**
- Autokorrelation: Durbin-Watson (D-W = 1.97, unauffällig)
- Homoskedastizität: Breusch-Pagan signifikant → robuste Standardfehler (HC1)
- Multikollinearität: VIF-Werte alle unter 5

---


## Verwendete Pakete

```r
dplyr, ggplot2, haven, psych, ltm, car, lmtest, sandwich,
stargazer, marginaleffects, corrplot, table1, flextable,
webshot2, ggeffects, tidycomm, pscl, olsrr, MASS
```

---

## Reproduzierbarkeit

```r
# Datensatz nach Bezug von GESIS ablegen unter:
# Daten/Datensatz2021/ZA5280_v2-0-1.dta

rmarkdown::render("G1_Code_EmpFoPa2.Rmd")
```
