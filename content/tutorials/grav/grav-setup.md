---
title: Setup
summary: ""
linktitle: 
toc: true
type: docs
date: "2019-05-05T00:00:00+01:00"
draft: true
menu:
  grav:
    parent: GRAV CMS
    weight: 1

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 1
highlight: true
highlight_languages: 
    - "powershell" 
---

Grav wurde im Hinblick auf wenige Anforderungen entwickelt. Dies zeigt sich vor Allem an den geringen Systemanforderungen. 

## Vorraussetzungen:
1. Webserver (Apache, Nginx, LiteSpeed, Lightly, IIS usw.)
1. PHP 7.2 und [erforderliche Module](#php-module)
1. das war es auch schon... denn Grav baut aus einfachen Textdateien die Inhalte der Seiten. Es wird _keine Datenbank_ benötigt.

## Webserver
Zu Details der lokalen Entwicklung auf [Mac und Windows](https://learn.getgrav.org/basics/requirements#mac) sowie den Apache- und IIS-Anforderungen (`mod_rewrite/URL Rewrite`) konsultieren Sie bitte die [Dokumentation von GRAV](https://learn.getgrav.org/16/basics/requirements#apache-requirements)

## PHP-Module

```bash
sudo apt install php7.2 php7.2-curl php7.2-ctype php7.2-dom php7.2-gd php7.2-json php7.2-mbstring php7.2-openssl php7.2-session php7.2-simplexml php7.2-xml php7.2-zip
```


## Installation mit GitHub

`git clone` wird verwendet um vorhandene Git-Repository zu kopieren. 

1. Klonen des Grav Repositories [GitHub](https://github.com/getgrav/grav) in ein Verzeichnis auf dem Webserver, bspw. `~/webroot/grav`.

```bash
cd ~/webroot
git clone https://github.com/getgrav/grav.git
```
2. Installieren der Anbieter-Abhängigkeiten (`vendor dependencies`) mit [composer](https://getcomposer.org/doc/00-intro.md#installation-linux-unix-osx):

```bash
cd ~/webroot/grav
composer install --no-dev -o
```

1. Installieren Sie die im Pfad `/grav` **Plugin**- und **Themenabhängigkeiten** mit Hilfe der [Grav-CLI-Anwendung](https://learn.getgrav.org/16/cli-console/grav-cli) `bin/grav`:

```bash
bin/grav install
```

4. Als nächstes wollen wir das OpenGeoEdu-Theme in den entsprechenden Pfad kopieren:

```bash
cd user/themes
git clone https://github.com/opengeoedu/grav-theme-oge-learn.git oge-learn
```

5. Nun wollen wir abschließend die Inhaltsseiten von OpenGeoEdu in den Pfad `user/pages` kopieren.

```bash
cd grav/user
git clone --no-checkout https://github.com/opengeoedu/learn.opengeoedu.de.git tmp && mv tmp/.git . && rmdir tmp && git checkout master
```
6. Zum Aktivieren des OpenGeoEdu Themes muss die Zeile `theme:quark` in der Datei `user\config\system.yaml` in `theme:oge-lean` geändert werden und schon sollte es so aussehen:


{{% alert warning %}}
Beachten Sie auch die ausführliche [Installationsbeschreibung von GRAV](https://learn.getgrav.org/16/basics/installation) mit Unterstützung zur Fehlerbeseitigung.
{{% /alert %}}