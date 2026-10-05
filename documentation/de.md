<!-- ELUCENIA technical documentation · indice-de-baux-revisado · de · no clinical/professional/rights approval -->

# Revidierter Baux-Score

[Bedingungen, Quellen und Berechtigungen](https://elucenia.org/de/werkzeuge/indice-de-baux-revisado)

## Verwendung

Verwenden Sie das Werkzeug im Portal oder öffnen Sie index.html über einen lokalen HTTP-Server. Wählen Sie die Sprache, füllen Sie die Felder aus und berechnen Sie das Ergebnis.

## Eingaben und Einheiten

### Alter

`idade`

Jahre · Bereich: 0–110

### Verbrannte Körperoberfläche

`scq`

% · Bereich: 0–100

### Inhalationstrauma?

`inalacao`

- `0` — Nein
- `1` — Ja

## Fassung der Methode

Revidierter Baux/Osler 2010: Alter+Fläche+17 Inhalationstrauma; ursprüngliches logistisches Modell

## Dokumentierte Formel

Revidierter Baux = Alter (Jahre) + verbrannte KOF (%) + 17 × Inhalationstrauma (1=ja, 0=nein).

Im Osler-Modell (39888 Brandverletzte im US-Register) waren Alter und Fläche fast gleich gewichtet; Inhalationstrauma entsprach 17 Jahren oder 17% Fläche. Die Sterbewahrscheinlichkeit ergibt sich aus der logistischen Scoretransformation.

## Grenzen und Population

Der revidierte Baux addiert Alter, Prozentsatz verbrannter Körperoberfläche und 17 bei Inhalationsverletzung. Die rohe Summe ist kein Mortalitätsprozentsatz: Die Wahrscheinlichkeit erfordert die logistische Transformation der Version. Das vereinfachte Modell schnitt im Artikel schlechter als das komplexere Modell ab und erfordert Interpretation in der geeigneten klinischen Population.

## Referenzen

- [Osler T, Glance LG, Hosmer DW. Simplified estimates of the probability of death after burn injuries: extending and updating the Baux score. J Trauma, 2010.](https://doi.org/10.1097/TA.0b013e3181c453b3)

- [Dokter J et al. External validation of the revised Baux score for the prediction of mortality in patients with acute burn injury. J Trauma Acute Care Surg, 2014.](https://doi.org/10.1097/TA.0000000000000124)

## Technische Tests reproduzieren

Führen Sie node test.cjs im Stammverzeichnis dieses Repositorys aus, um die dokumentierten synthetischen Fälle zu wiederholen. Ursprüngliche Eingaben, erwartete Ergebnisse und Toleranzen bleiben erhalten. Technische Tests stellen keine klinische Validierung dar.

```sh
node test.cjs
```

tool.json enthält Quellen, Ausgabe und Umfang der Überprüfung. examples.json bewahrt die synthetischen Eingaben und erwarteten Ergebnisse; results.json dokumentiert die tatsächlich erhaltenen Ergebnisse.

[Eintrag und Referenzen](../tool.json) · [JavaScript-Code](../calculator.js) · [Referenzfälle](../examples.json) · [results.json](../results.json)

## Überprüfung und Nutzungsbedingungen

Eine unabhängige klinische Prüfung wurde nicht durchgeführt.

Diese Benutzeroberfläche ist eine selbst erstellte Übersetzung und keine offizielle oder zertifizierte Ausgabe. Eine unabhängige klinische Überprüfung, eine professionelle sprachliche Prüfung und eine Klärung der Rechte an den Instrumenten wurden nicht durchgeführt.

Ergebnis der Formel oder Klassifikation. Interpretation, Vorgehen und Anwendbarkeit hängen von der fachlichen Beurteilung und der ausgewählten Quelle ab.

## Lizenz und Urheberangaben

Apache-2.0 gilt nur für den ELUCENIA-Code. Die Rechte an Instrumenten, Veröffentlichungen, Übersetzungen und Daten verbleiben bei den jeweiligen Rechteinhabern. Bewahren Sie LICENSE und NOTICE auf.

ELUCENIA · Felipe Guedes · Copyright © 2026
