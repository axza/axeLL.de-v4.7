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
draft: true

---
Auf meiner letzten Jobsuche konnte ich einige Erfahrungen sammeln, die ich hier festhalten möchte. Eventuell helfen meine Erfahrungen anderen, die sich in vergleichbarer Situation befinden.

## Zur Ausgangslage:

Meine aktuelle Projektstelle läuft planmäßig aus, daher habe ich mich im Dezember ($ t_{ 0 } $) mal über offene Stellen informiert. Mit einem Rundumschlag auf gängigen Jobaggregatoren- und Seiten, die die Geo*- und IT-Zielgruppe bedienen wie beispielsweise [digital-geography.com](https://de.digital-geography.com/jobs/ "digital-geography.com") oder [greenjobs.de](https://www.greenjobs.de/ "greenjobs.de") habe ich angefangen.

![](/img/digitalgeography.jpg)

Dieser war schon sehr ergiebig. Ergänzend habe ich die handverlesenen Angebote von [gesinesjobtipps.de](https://gesinesjobtipps.de/ "gesinesjobtipps.de") gescannt sowie die Suchfunktion für Stellenangebote von Google durchforstet.

![Screenshot der Google Jobsuche](/img/googlejobs.jpg "Google Jobsuche")

## Automatisierung der Erstellung von Bewerbungsunterlagen.

($ t_{ 1 } $) Für die Zusammenführung meiner Bewerbungsunterlagen habe ich die Serienbrief Funktionen von Google Documents, Google Forms und Google Sheets verwendet.

![](/img/dokumente.png)

### Vorbereitung der Dokumente

Zuallererst habe ich ein leeres Dokument erstellt und die feststehenden Eintragung vorgenommen. Diese entsprechen denen eines Standardbriefes (eigene Anschrift, Begrüßung, Verabschiedung, Unterschrift).

![newdoc](/img/newdoc.png)

Die weiteren Unterlagen wie Lebenslauf, Zeugnisse und Beurteilungen werden ebenfalls in das Dokument eingefügt. So ist das Grundgerüst fertig.

Nun fügen wir in das Anschreiben Platzhalter ein. Diese sind in dem Format `{{$Platzhaltername}}` einzusetzen. Ich habe folgende Variablen verwendet:

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
erstellen wir nun ein neues Formular.
![Neues Formular](/img/newform.jpg)

Die Antworten auf die Fragen stellen wir auf das gewünschten Format um. Hier beispielsweise richten wir ein Datumsfeld ein.
![Antwortenformat](/img/newform-editformat.jpg)

Weiter erstellen wir für jede Platzhaltervariable eine Frage.



### Tabelle mit Antworten prüfen


### Skript zur Zusammenführung
Damit wir ein  öffnen dort unter `Menü -> Skripteditor`

```
function myFunction(e) {
  //e.values is an array of form values
  var zeitstempel = e.values[0];
  var heutigesdatum = e.values[1];
  var adresse = e.values[2];
  var quelle = e.values[3];
  var stellentitel = e.values[4];
  var kennziffer = e.values[5];
  var anrede = e.values[6];
  var anschreiben = e.values[7];
  var arbeitsbeginn = e.values[8];                     
  var jahresbrutto = e.values[9];
  var firma = e.values[10];
                        
  //file is the template file, and you get it by ID
  var file = DriveApp.getFileById('1wT1bGXV_lkhzvqmSeekbisAf4nR_3mL1pHXghTS9VAw'); 
  
  //We can make a copy of the template, name it, and optionally tell it what folder to live in
  //file.makeCopy will return a Google Drive file object
  var folder = DriveApp.getFolderById('15OseirfALhMRyOT8eOVhOEm2HzeN5Bfp')
  var copy = file.makeCopy('Bewerbung_Lorenzen-Zabel' + '_' + stellentitel + '_' + heutigesdatum, folder); 
  
  //Once we've got the new file created, we need to open it as a document by using its ID
  var doc = DocumentApp.openById(copy.getId()); 
  
  //Since everything we need to change is in the body, we need to get that
  var body = doc.getBody(); 
  
  //Then we call all of our replaceText methods
  body.replaceText('{{Adresse}}', adresse); 
  body.replaceText('{{heutiges datum}}', heutigesdatum); 
  body.replaceText('{{Stellentitel}}', stellentitel);  
  body.replaceText('{{kennziffer}}', kennziffer); 
  body.replaceText('{{Anrede}}', anrede); 
  body.replaceText('{{Quelle des Stellenangebotes}}', quelle); 
  body.replaceText('{{Anschreiben}}', anschreiben); 
  body.replaceText('{{Arbeitsbeginn}}', arbeitsbeginn); 
  body.replaceText('{{Jahresbrutto}}', jahresbrutto); 
  body.replaceText('{{trackingurl}}', firma);
  
  //Lastly we save and close the document to persist our changes
  doc.saveAndClose(); 
}
```

### Prüfung und Export als pdf

## To-Do

* \[ \] Zusammenstellung der Vorlage
* \[ \] Formularbasierte Dokumentenerstellung
* \[ \] Automatische PDF Generierung
* \[ \] Manuelle Prüfung und Versand