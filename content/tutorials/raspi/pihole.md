---
title: Pihole auf dem Raspberry Pi als Werbeblocker
summary: "Ein schwarzes Loch für Internetwerbung. Mit diesem Projekt wird Ihr Pi Zero W zu einem DNS (Domain Name Server). Das macht das Surfen im Internet nicht nur schneller, sondern auch sicherer."
linktitle: Pihole
toc: true
type: docs
date: "2019-05-05T00:00:00+01:00"
draft: false
menu:
  raspi:
    parent: 
    weight: 2

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 2
---

Pi hole lässt sich auch auf anderen Modellen nutzen. Ich habe gute Erfahrungen mit einem dedizierten Pi Zero W, der ausschließlich Pi hole beherbergt, gemacht.

## Erklärvideo

{{< youtube vKWjx1AQYgs >}}
Als kleinen Einstieg in das Thema guckt euch das obige Video an. Das gibt einen guten Überblick zu diesem Vorhaben.

## Projektinfos
{{% alert note %}}
* Zeit: Circa 45 Minuten
* Richtet sich an: Einsteiger und Fortgeschrittene
* Kein Werkzeug benötigt
  
{{% /alert %}}

## Einkaufszettel
{{% alert note %}}
* Raspberry Pi (ich nutze aktuell den [Zero W](https://shop.pimoroni.de/products/raspberry-pi-zero-w))
* Micro USB Netzteil (mind. 2,5A)
* Gehäuse (optional)
* microSD 16GB Class 10
{{% /alert %}}

## Vorraussetzungen

* Wifi
* SSH
* git




## Downloads
pihole
iso to SD

## Setup

```
git clone --depth 1 https://github.com/pi-hole/pi-hole.git Pi-hole
cd "Pi-hole/automated install/"
sudo bash basic-install.sh
```

## Weitere Hilfen
https://discourse.pi-hole.net/c/bugs-problems-issues/deutschsprachige-hilfe

## Quellen
https://docs.pi-hole.net/main/prerequesites/
