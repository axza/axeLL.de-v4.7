---
authors: ''
date: 2020-03-06T14:03:00Z
featured: false
projects: ''
subtitle: "Erfahrungen meiner kürzlichen Jobsuche"
summary: "Auf meiner letzten Jobsuche konnte ich einige Erfahrungen mit der automatisierten Erstellung von Bewerbungsunterlagen sammeln."
tags: ["Lebenslanges Lernen", "Digitalisierung", "Automatisierung"]
title: "Projekt: Arbeitssuche"
image:
  caption: ""
  focal_point: ""
  preview_only: true

---
Auf meiner letzten Jobsuche konnte ich einige Erfahrungen sammeln, die ich hier festhalten möchte. Eventuell helfen meine Erfahrungen anderen, die sich in vergleichbarer Situation befinden.

## Zur Ausgangslage:

Meine aktuelle Projektstelle läuft planmäßig aus, daher habe ich mich im Dezember ($ t_{ 0 } $) mal über offene Stellen informiert. Mit einem Rundumschlag auf gängigen Jobaggregatoren- und Seiten, die die Geo*- und IT-Zielgruppe bedienen wie beispielsweise [digital-geography.com](https://de.digital-geography.com/jobs/ "digital-geography.com") oder [greenjobs.de](https://www.greenjobs.de/ "greenjobs.de") habe ich angefangen. Dieser war schon sehr ergiebig. Ergänzend habe ich die handverlesenen Angebote von [gesinesjobtipps.de](https://gesinesjobtipps.de/ "gesinesjobtipps.de") gescannt sowie die Suchfunktion für Stellenangebote von Google durchforstet.

![Screenshot der Google Jobsuche](/img/googlejobs.jpg "Google Jobsuche")

## Automatisierung der Erstellung von Bewerbungsunterlagen.

($ t_{ 1 } $) Für die Zusammenführung meiner Bewerbungsunterlagen habe ich die Serienbrief Funktionen von Google Documents, Google Forms und Google Sheets verwendet.

![](/img/dokumente.png)

### Vorbereitung der Dokumente

Zuallererst habe ich ein leeres Dokument erstellt und die feststehenden Eintragung vorgenommen. Diese entsprechen denen eines Standardbriefes (eigene Anschrift, Begrüßung, Verabschiedung, Unterschrift)

Die weiteren Unterlagen wie Lebenslauf, Zeugnisse und Beurteilungen werden ebenfalls in das Dokument eingefügt. So ist das Grundgerüst fertig.

Nun fügen wir in das Anschreiben Platzhalter ein. Diese sind in dem Format `{{Platzhaltername}}` einzusetzen. Bei mir sind es

`{{Adresse}}
{{heutiges datum}}    
{{Stellentitel}} {{kennziffer}}
{{Anrede}}, sehr geehrte Damen und Herren,
bezugnehmend auf Ihr Stellenangebot auf {{Quelle des Stellenangebotes}} bewerbe ich mich auf die vakante oben genannte Stelle als {{Stellentitel}}.

{{Anschreiben}}

Ich bin ab {{Arbeitsbeginn}} {{Jahr}}, evtl auch früher, einsetzbar und stehe Ihnen gerne zur Verfügung.`

## To-Do

* \[ \] Zusammenstellung der Vorlage
* \[ \] Formularbasierte Dokumentenerstellung
* \[ \] Automatische PDF Generierung
* \[ \] Manuelle Prüfung und Versand