---
title: Theming
summary: ""
linktitle: 
toc: true
type: docs
date: "2019-05-05T00:00:00+01:00"
draft: true
menu:
  grav:
    parent: GRAV CMS
    weight: 2

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 2
highlight: true
highlight_languages: 
    - "powershell" 
---


Für die lokale Bearbeitung der OpenGeoEdu Inhalte können Sie [VS CODE](https://code.visualstudio.com/),
[atom.io](https://atom.io/) oder die Online-Editierfunktion von GitHub nutzen.

## Überschriften

Überschriften der Ebenen `h1` bis  `h6` werden durch die entsprechende Anzahl von `#` generiert.

[columns count=2]
markdown:
```markdown
# h1 Heading
## h2 Heading
### h3 Heading
#### h4 Heading
```
HTML:
```html
<h1>h1 Heading</h1>
<h2>h2 Heading</h2>
<h3>h3 Heading</h3>
<h4>h4 Heading</h4>
```

[/columns]

wird zu:
![Überschriften](ueberschriften.png)


<br>

## Notices (farbige Hinweisekästchen)

In OGE GRAV werden ``!`` für die Farbboxen (Notices) genutzt

[columns count=2]
markdown:
```markdown
! verweis/link(Links und Verweise auf Literatur oder Webseiten)
!! Gedankenanstöße in anderer Farbe
!!! Definition
!!!! Fragen / Lernziele
!!!!! Hintergründe
```
HTML:
```html
<div class="notices yellow">
  <p>Links und Verweise auf Literatur oder Webseiten</p>
</div>
```
[/columns]

! Links und Verweise auf Literatur oder Webseiten

!! Gedankenanstöße in anderer Farbe

!!! Definition

!!!! Fragen / Lernziele

!!!!! Hintergründe



## Kommentare

Kommentare sind HTML kompatibel und können Bearbeitungshinweise für andere Autoren enthalten.
[columns count=2]
markdown:
```html
<!--
This is a comment
-->
```
folgendes HTML  Kommentar ist **nicht** sichtbar:
<br>
<br>

<!--
This is a comment
-->
[/columns]


<br>

## Zitat mit Autor

Zur Angabe des Autors wird `<cite></cite>` am ende des Blockquote angefügt:

markdown
```markdown

> **Fusion Drive** combines a hard drive with a flash storage (solid-state drive) and presents it as a single logical volume with the space of both drives combined.
<cite>[Michael Kuster](https://example.com)</cite>
```
HTML:
```html
<blockquote>
<p><strong>Fusion Drive</strong> combines a hard drive with a flash storage (solid-state drive) and presents it as a single logical volume with the space of both drives combined. <cite><a href="https://example.com" target="_blank" rel="nofollow noopener noreferrer" class="external-link no-image">Michael Kuster</a></cite></p>
</blockquote>
```

> **Fusion Drive** combines a hard drive with a flash storage (solid-state drive) and presents it as a single logical volume with the space of both drives combined. <cite>[Michael Kuster](https://example.com)</cite>


## Inline HTML

HTML und Markdown funktionieren problemlos miteinander. So können Sie beispielsweise Klassen definiert werden:
```html
Paragraph in Markdown.

<div class="class">
</div>

Paragraph in Markdown.
```

### Markdown in HTML

Für die Verwendung von markdown in html-inline-Abschnitten muss folgender Wert gesetzt werden: `markdown="1"`

```
<div class="container" markdown="1">
  ![Bildalttext](URL)
</div>
```

## Fußnoten (bigfoot.js)

Fußnoten werden im Fließtext folgendermaßen ausgezeichnet:

markdown
```markdown

Hier ist ein wenig Text mit einer Fußnote.[^1]  
  
[^1]: Und hier ist die Fußnote.  
```

HTML
```html
<p>Hier ist ein wenig Text mit einer Fußnote.  <div class="bigfoot-footnote__container"><button class="bigfoot-footnote__button" id="fnref1:1" data-footnote-number="1" data-footnote-identifier="1" alt="See Footnote 1" rel="footnote" data-bigfoot-footnote="<p>Und hier ist die Fußnote.</p>"> <svg class="bigfoot-footnote__button__circle" viewBox="0 0 6 6" preserveAspectRatio="xMinYMin"><circle r="3" cx="3" cy="3" fill="white"></circle></svg> <svg class="bigfoot-footnote__button__circle" viewBox="0 0 6 6" preserveAspectRatio="xMinYMin"><circle r="3" cx="3" cy="3" fill="white"></circle></svg> <svg class="bigfoot-footnote__button__circle" viewBox="0 0 6 6" preserveAspectRatio="xMinYMin"><circle r="3" cx="3" cy="3" fill="white"></circle></svg> </button></div><sup id="fnref1:1" data-footnote-backlink-ref="fnref1:1" data-footnote-ref="#fn:1" class="footnote-print-only"><a href="#fn:1" class="footnote-ref">1</a></sup>
</p>
```

Hier ist ein wenig Text mit einer Fußnote.[^1]
[^1]: Und hier ist die Fußnote. 
* Hier ist markdown erlaubt
* text **formatierung**
* Listen
* und sogar Bilder ![logo](http://www.opengeoedu.de/images/logo/oge.svg)

## Listen

### Ungeordnet

Auflistung von dingen in unbestimmter Reihenfolge. Zur Auszeichnung einer ungeordneten Liste wird entweder ein `*` `-` oder ein `+` verwendet


```markdown
* valid bullet
- valid bullet
+ valid bullet
```

Im folgenden Beispiel mit Einrückungen für Unterpunkte

```markdown
+ Lorem ipsum dolor sit amet
+ Consectetur adipiscing elit
+ Nulla volutpat aliquam velit
  - Phasellus iaculis neque
  - Purus sodales ultricies
  - Ac tristique libero volutpat at
+ Faucibus porta lacus fringilla vel
+ Eget porttitor lorem
```
<br>

+ Lorem ipsum dolor sit amet
+ Consectetur adipiscing elit
+ Nulla volutpat aliquam velit
  - Phasellus iaculis neque
  - Purus sodales ultricies
  - Ac tristique libero volutpat at
+ Faucibus porta lacus fringilla vel
+ Eget porttitor lorem

### Geordnete Liste

Eine Auflistung von Dingen in einer vorgegebenen Reihenfolge:
markdown
```markdown
1. Lorem ipsum dolor sit amet
2. Consectetur adipiscing elit
3. Integer molestie lorem at massa
4. Facilisis in pretium nisl aliquet
5. Nulla volutpat aliquam velit
6. Faucibus porta lacus fringilla vel



```
<br>

wird zu:

1. Lorem ipsum dolor sit amet
2. Consectetur adipiscing elit
3. Integer molestie lorem at massa
4. Facilisis in pretium nisl aliquet
5. Nulla volutpat aliquam velit
6. Faucibus porta lacus fringilla vel


!!! **TIP**: Beachten Sie die `1.` für jede Zeile, Markdown numeriert die Zeilen dann automatisch:

<br>

## Tabellen

Tabellen werden durch Hinzufügen von Pipes `|` als Trennlinien zwischen den einzelnen Zellen und durch Hinzufügen einer Linie von Strichen (ebenfalls durch Balken getrennt) unter der Kopfzeile erstellt. Beachten Sie, dass die Pipes nicht vertikal ausgerichtet sein müssen.

```markdown
| Option | Description |
| ------ | ----------- |
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |
```

| Option | Description |
| ------ | ----------- |
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |

Für die Erstellung komplexer Markdowntabellen hat sich folgendes Onlinewerkzeug als nützlich erwiesen: http://www.tablesgenerator.com/markdown_tables


## Texthervorhebungen

### Fett

For emphasizing a snippet of text with a heavier font-weight.

The following snippet of text is **rendered as bold text**.

```markdown
**rendered as bold text**
```
renders to:

**rendered as bold text**

and this HTML

```html
<strong>rendered as bold text</strong>
```

### Italics

For emphasizing a snippet of text with italics.

The following snippet of text is _rendered as italicized text_.

```markdown
_rendered as italicized text_
```

renders to:

_rendered as italicized text_

and this HTML:

```html
<em>rendered as italicized text</em>
```


### strikethrough

In GFM (GitHub flavored Markdown) you can do strikethroughs.

```markdown
~~Strike through this text.~~
```
Which renders to:

~~Strike through this text.~~

HTML:

```html
<del>Strike through this text.</del>
```

<br>

## Code

### Inline code

Wrap inline snippets of code with `` ` ``.

```markdown
In this example, `<section></section>` should be wrapped as **code**.
```

Renders to:

In this example, `<section></section>` should be wrapped with **code**.

HTML:

```html
<p>In this example, <code>&lt;section&gt;&lt;/section&gt;</code> should be wrapped with <strong>code</strong>.</p>
```

### Indented code

Or indent several lines of code by at least four spaces, as in:

<pre>
  // Some comments
  line 1 of code
  line 2 of code
  line 3 of code
</pre>

Renders to:

    // Some comments
    line 1 of code
    line 2 of code
    line 3 of code

HTML:

```html
<pre>
  <code>
    // Some comments
    line 1 of code
    line 2 of code
    line 3 of code
  </code>
</pre>
```


### Block code "fences"

Use "fences"  ```` ``` ```` to block in multiple lines of code.

<pre>
``` markup
Sample text here...
```
</pre>


```
Sample text here...
```

HTML:

```html
<pre>
  <code>Sample text here...</code>
</pre>
```

### Syntax highlighting

GFM, or "GitHub Flavored Markdown" also supports syntax highlighting. To activate it, simply add the file extension of the language you want to use directly after the first code "fence", ` ```js `, and syntax highlighting will automatically be applied in the rendered HTML. For example, to apply syntax highlighting to JavaScript code:

<pre>
```js
grunt.initConfig({
  assemble: {
    options: {
      assets: 'docs/assets',
      data: 'src/data/*.{json,yml}',
      helpers: 'src/custom-helpers.js',
      partials: ['src/partials/**/*.{hbs,md}']
    },
    pages: {
      options: {
        layout: 'default.hbs'
      },
      files: {
        './': ['src/templates/pages/index.hbs']
      }
    }
  }
};
```
</pre>

Renders to:

```js
grunt.initConfig({
  assemble: {
    options: {
      assets: 'docs/assets',
      data: 'src/data/*.{json,yml}',
      helpers: 'src/custom-helpers.js',
      partials: ['src/partials/**/*.{hbs,md}']
    },
    pages: {
      options: {
        layout: 'default.hbs'
      },
      files: {
        './': ['src/templates/pages/index.hbs']
      }
    }
  }
};
```
<!--
!!! For syntax highlighting to work, the [Highlight plugin](https://github.com/getgrav/grav-plugin-highlight) needs to be installed and enabled. It in turn utilizes a jquery plugin, so jquery needs to be loaded in your theme too.
-->
<br>
<br>
<br>





## Links

### Basic link

```markdown
[Assemble](http://assemble.io)
```

Renders to (hover over the link, there is no tooltip):

[Assemble](http://assemble.io)

HTML:

```html
<a href="http://assemble.io">Assemble</a>
```


### Add a title

```markdown
[Upstage](https://github.com/upstage/ "Visit Upstage!")
```

Renders to (hover over the link, there should be a tooltip):

[Upstage](https://github.com/upstage/ "Visit Upstage!")

HTML:

```html
<a href="https://github.com/upstage/" title="Visit Upstage!">Upstage</a>
```

## Bilder 
Die folgende Syntax fügt dem Bild `oge.svg` mit dem Zusatz 
* `?lightbox=800` ein anklickbare Vergrößerung (mit Breite 800px) hinzu
* `&resize=300` eine Größenänderung auf 300px
* `&classes=caption "Text der Bildunterschrift"` die eigentliche Bildunterschrift

```markdown
![OGE-Logo](http://www.opengeoedu.de/images/logo/oge.svg?lightbox=800&resize=300&classes=caption "Diese Abbildung zeigt das OpenGeoEdu-Logo")
```

Vorschau:

![](http://www.opengeoedu.de/images/logo/oge.svg?lightbox=800&resize=300&classes=caption "Diese Abbildung zeigt das OpenGeoEdu-Logo")

!!!!! Zu beachten ist der **erste** Zusatz erfordert **immer** ein `?` weitere Parameter ein `&`


## Bild mit Link im Bild **und** der Bildunterschrift
```markdown
[![OGE-Logo](http://www.opengeoedu.de/images/logo/oge.svg?resize=300&classes=caption "Diese Abbildung zeigt das OpenGeoEdu-Logo")](https://www.opengeoedu.de)
```
Vorschau:

[![OGE-Logo](http://www.opengeoedu.de/images/logo/oge.svg?resize=300&classes=caption "Diese Abbildung zeigt das OpenGeoEdu-Logo")](https://www.opengeoedu.de)


---

## Code Markierung
Einfaches Einrücken mit **4 Leerzeichen am Zeilenanfang** oder mit ` ``` ` am Anfang und am Ende des Code-Blocks.

```markdown
    codezeile1
    codezeile2
```
wird zu html
```html
<pre>
  <code>
    codezeile1
    codezeile2
  </code>
</pre>
```

## Shortcodes

Das [Shortcode-core-Plugin](https://github.com/getgrav/grav-plugin-shortcode-core/) enthält ein paar einfache Shortcodes, die folgend mit Beispielen illustriert werden können:

### Anwendung der Shortcodes für die Reichweitenlegende und Level der Übung (s. [Datenblätter](/uebersicht/datenblatt))

##### A B C lokal 
[color=orange][fa=fa-street-view extras=fa-2x][/color] [color=green] [fa=fa-street-view extras=fa-2x][/color][color=blue] [fa=fa-street-view extras=fa-2x][/color]

[raw]
```markdown
[color=orange][fa=fa-street-view extras=fa-2x][/color] [color=green][fa=fa-street-view extras=fa-2x][/color] [color=blue][fa=fa-street-view extras=fa-2x][/color]
```
[/raw]

##### A B C regional 
[color=orange] [fa=map-marked extras=fa-2x][/color] [color=green] [fa=map-marked extras=fa-2x][/color] [color=blue] [fa=map-marked extras=fa-2x][/color]
[raw]
```markdown
[color=orange][fa=map-marked extras=fa-2x][/color] [color=green][fa=map-marked extras=fa-2x][/color] [color=blue][fa=map-marked extras=fa-2x][/color]
```
[/raw]

##### A B C national/global 
[color=orange][fa=fa-globe-africa extras=fa-2x][/color] [color=green][fa=fa-globe-africa extras=fa-2x][/color] [color=blue][fa=fa-globe-africa extras=fa-2x][/color]
[raw]
```markdown
[color=orange][fa=fa-globe-africa extras=fa-2x][/color] [color=green][fa=fa-globe-africa extras=fa-2x][/color] [color=blue][fa=fa-globe-africa extras=fa-2x][/color]
```
[/raw]

#### Underline
Underline a section of text

```
This is some [u]bb style underline[/u] and not much else
```

#### Font Size
Set the size of some text to a specific pixel size

```
This is [size=30]bigger text[/size]
```

#### Alignment
Left align the text between this shortcode

```
[left]This text is left aligned[/left]
```
[left]This text is left aligned[/left]


Center a selection of text between this shortcode

```
[center]This text is centered[/center]
```
[center]This text is centered[/center]


Right align the text between this shortcode

```
[right]This text is right aligned[/right]
```
[right]This text is right aligned[/right]



#### Div

Allows you to wrap markdown in an HTML `div` tag that supports both `id` and `classes` attributes

```
[div class="text-center"]

 This text is **centered** aligned

[/div]
```

or

```
[div class="table table-striped"]
| header 1 | header 2 |
|----------|----------|
| A 1      | B 1      |
| A 2      | B 2      |
| A 3      | B 3      |
[/div]
```


#### Span

Allows you to wrap markdown in an HTML `span` tag that supports both `id` and `classes` attributes

```
[span class="text-center"]
This text is **centered** aligned
[/span]
```


#### Columns

Take advantage of powerful CSS columns support by using this shortcode

```
[columns]
### Headline

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
consequat.

Duis aute irure dolor in reprehenderit in voluptate velit esse
cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
consequat.
[/columns]

```
[columns]
### Headline

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
consequat.

Duis aute irure dolor in reprehenderit in voluptate velit esse
cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
consequat.
[/columns]


Defaults to 2 columns.  You can also explicitly set the number of `columns`, `width`, `gap`, and `rule` styling for the column divider:

```
[columns count=3 width=200px gap=30px rule="1px dotted #930"]
### Headline

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
consequat.

Duis aute irure dolor in reprehenderit in voluptate velit esse
cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
consequat.
[/columns]
```
[columns count=3 width=200px gap=30px rule="1px dotted #930"]
### Headline

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
consequat.

Duis aute irure dolor in reprehenderit in voluptate velit esse
cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
consequat.
[/columns]


#### Raw

Do not process the shortcodes between these raw shortcode tags

```
[raw]This is some [u]bb style underline[/u] and not much else[/raw]
```
[raw]This is some [u]bb style underline[/u] and not much else[/raw]


#### Safe-Email

Encode an email address so that it's not so easily 'scrapable' by nefarious scripts.  This one has a couple of options: `autolink` toggle to turn the email into a link, and an `icon` option that lets you pick a font-awesome icon to prefix the email.  Both settings are optional.

```
Safe-Email Address: [safe-email autolink="true" icon="envelope-o"]user@domain.com[/safe-email]
```
Safe-Email Address: [safe-email autolink="true" icon="envelope-o"]user@domain.com[/safe-email]


#### Section

The **section** shortcode is a powerful way to encompass some text in your markdown page with a `[section][/section]` tag and then this is cached by Grav so it can be accessed later.  For example you could have a page with a variety of sections described in it that let you create many **chunks** of data. These are then added to Twig as an array of shortcode objects.  An example of this would be the following markdown:

```
[section name="author"]
![](author.jpg?cropResize=100,100&classes=left)

### Johnny Appleseed
Johnny Appleseed was an American pioneer nurseryman who introduced apple trees to large parts of Pennsylvania, Ontario, Ohio, Indiana, and Illinois, as well as the northern counties of present-day West Virginia. He became an American legend while still alive, due to his kind, generous ways, his leadership in conservation, and the symbolic importance he attributed to apples.
[/section]

[section name="quote"]
> Some are born great, some achieve greatness, and some have greatness thrust upon them.
  Read more at http://www.brainyquote.com/quotes/topics/topic_great.html#tdqt3strtEYBCH43.99
> <cite>William Shakespeare</cite>

Regular **Markdown** content that will be output as `page.content`
[/section]
```

This we be removed from the page content and made available in Twig variables so you could insert these into custom HTML structures, for example:

```
<div id="author">{{ shortcode.section.author }}</div>

<div id="article">
    <div class="left">
        {{ page.content }}
    </div>
    <div class="right">
        {{ shortcode.section.quote }}
    </div>
</div>
```

#### Sections from other pages

You can even retrieve a section from another page utilizing the shortcodes as they are stored in the page's `contentMeta` with this syntax:

```
<div id="author">{{ page.find('/my/custom/page').contentMeta.shortcodeMeta.shortcode.section.author }}</div>
```

#### FontAwesome

[FontAwesome](https://fortawesome.github.io/Font-Awesome/) is a powerful library of font-based icons.  This shortcode makes it simple to add fontawesome icons to your page content without using HTML.

[fa=cog /] Simplest Format

[fa=fa-cog /] Format using `fa-` prefix

[fa icon=fa-camera-retro /] Explicit format

[fa icon=fa-camera-retro extras=fa-4x /] Explicit format with extras - [See FontAwesome Examples](https://fortawesome.github.io/Font-Awesome/examples/)

[fa icon=fa-circle-o-notch extras=fa-spin,fa-3x,fa-fw,margin-bottom /] The full monty! - [See FontAwesome Examples](https://fortawesome.github.io/Font-Awesome/examples/)



! Bitte beachten Sie die ausführliche Markdown Dokumentation auf https://learn.getgrav.org/content/markdown<br>
! Eine Markdown Übersicht hat heise hier auf einer Seite Zusammengefasst: https://www.heise.de/mac-and-i/downloads/65/1/1/6/7/1/0/3/Markdown-CheatSheet-Deutsch.pdf