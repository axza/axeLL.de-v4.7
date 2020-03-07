---
authors: ''
date: 2020-03-06T14:03:00.000+00:00
featured: false
projects: ''
subtitle: Erfahrungen meiner kürzlichen Jobsuche
summary: Auf meiner letzten Jobsuche konnte ich einige Erfahrungen mit der automatisierten
  Erstellung von Bewerbungsunterlagen sammeln.
tags:
- Lebenslanges Lernen
- Digitalisierung
- Automatisierung
title: 'Projekt: Arbeitssuche'
image:
  caption: ''
  focal_point: ''
  preview_only: true

---
Auf meiner letzten Jobsuche konnte ich einige Erfahrungen sammeln, die ich hier festhalten möchte. Eventuell helfen meine Erfahrungen anderen, die sich in vergleichbarer Situation befinden.

## Zur Ausgangslage:

Meine aktuelle Projektstelle läuft planmäßig aus, daher habe ich mich im Dezember ($ t_{ 0 } $) mal über offene Stellen informiert. Mit einem Rundumschlag auf gängigen Jobaggregatoren- und Seiten, die die Geo*- und IT-Zielgruppe bedienen wie beispielsweise [digital-geography.com](https://de.digital-geography.com/jobs/ "digital-geography.com") oder [greenjobs.de](https://www.greenjobs.de/ "greenjobs.de") habe ich angefangen.

![](/img/digitalgeography.jpg) Dieser war schon sehr ergiebig. Ergänzend habe ich die handverlesenen Angebote von [gesinesjobtipps.de](https://gesinesjobtipps.de/ "gesinesjobtipps.de") gescannt sowie die Suchfunktion für Stellenangebote von Google durchforstet.

![Screenshot der Google Jobsuche](/img/googlejobs.jpg "Google Jobsuche")

## Automatisierung der Erstellung von Bewerbungsunterlagen.

($ t_{ 1 } $) Für die Zusammenführung meiner Bewerbungsunterlagen habe ich die Serienbrief Funktionen von Google Documents, Google Forms und Google Sheets verwendet.

![](/img/dokumente.png)

### Vorbereitung der Dokumente

Zuallererst habe ich ein leeres Dokument erstellt und die feststehenden Eintragung vorgenommen. Diese entsprechen denen eines Standardbriefes (eigene Anschrift, Begrüßung, Verabschiedung, Unterschrift)

Die weiteren Unterlagen wie Lebenslauf, Zeugnisse und Beurteilungen werden ebenfalls in das Dokument eingefügt. So ist das Grundgerüst fertig.

Nun fügen wir in das Anschreiben Platzhalter ein. Diese sind in dem Format `{{Platzhaltername}}` einzusetzen. Ich habe folgende Variablen eingesetzt:

```
{{Adresse}}
{{heutiges datum}}  

{{Stellentitel}} {{kennziffer}}

{{Anrede}}
{{Quelle des Stellenangebotes}}{{Stellentitel}}.

{{Anschreiben}}

{{Arbeitsbeginn}} {{Jahr}}
```

Im folgenden Bild sind die Platzhaltervariablen im Dokumententext zu sehen:
![](/img/jobformular.png)

### Formular erstellen


### Skript zur Zusammenführung

### Prüfung und Export als pdf

## To-Do

* \[ \] Zusammenstellung der Vorlage
* \[ \] Formularbasierte Dokumentenerstellung
* \[ \] Automatische PDF Generierung
* \[ \] Manuelle Prüfung und Versand