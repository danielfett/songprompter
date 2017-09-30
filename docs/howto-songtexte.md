# Songtexte bereitstellen

Songtexte für den Songprompter werden einfach auf einem USB-Stick gespeichert.

## USB-Stick vorbereiten

USB-Sticks müssen mit FAT32 formatiert sein. Das ist bei neu gekauften USB-Sticks in der Regel der Fall. Erkennt der Songprompter den USB-Stick nicht, hilft eventuell eine [Neuformatierung](http://praxistipps.chip.de/usb-stick-formatieren_2850) - hierbei gehen allerdings alle Daten auf dem USB-Stick verloren. 

## Songtexte speichern

Songtexte werden einfach direkt auf dem USB-Stick als TXT-Dateien gespeichert. Die Dateinamen müssen auf .txt enden und die Dateien müssen im Wurzelverzeichnis des USB-Sticks liegen und dürfen nicht in Unterordnern sein. Andere Dateien dürfen aber auf dem USB-Stick enthalten sein, sie stören den Songprompter nicht.

Alle .txt-Dateien im Wurzelverzeichnis des beim Start angeschlossenen Sticks werden im Songprompter zur Auswahl angezeigt.

![](/assets/images/usb-stick-contents.jpg)

Die .txt-Dateien sollten nicht mit einer Textverarbeitung wie Word oder Wordpad bearbeitet werden sondern mit einem einfachen Texteditor wie dem bei Windows enthaltenen Notepad.

![](/assets/images/songtext-notepad.jpg)

## Songtexte formatieren

Songtexte werden einfach im TXT-Format gespeichert, wobei einige einfache Formatierungsanweisungen verwenden können (siehe auch Beispieldatei unten):

### Absätze
Absätze in der Textdatei werden 1:1 auch am Songprompter angezeigt. (Lediglich Leerzeilen über und unter dem Text werden zur besseren Ausnutzung des Platzes entfernt.)

```
Erste Strophe.

Zweite Strophe.
```

### Neue Seite beginnen
Eine Zeile mit drei oder mehr Strichen ("-----") beginnt eine neue "Seite" im Songtext. Die Seiten werden einzeln angezeigt und zwischen ihnen kann man mit dem Fußschalter umgeschaltet werden. So kann ein Lied in übersichtliche Stücke aufgeteilt werden.

```
Erste Strophe.

Zweite Strophe.
-----
Dritte Strophe.

Vierte Strophe.
```

### Textgröße
Die Textgröße zur Anzeige der einzelnen Seiten wird automatisch so gewählt, dass der Platz möglichst gut ausgenutzt wird.

### Dicktengleiche Schrift (Monospace)
Text, der auf die Anweisung "<pre>" folgt, wird in einer dicktengleichen Schrift angezeigt. Das erleichtert es, beispielsweise Akkorde an exakte Stellen über einem Text zu platzieren, denn die Anzeige auf dem Songprompter sieht i.d.R. genauso aus wie bei der Eingabe im Texteditor. Die Anweisung gilt nur bis zum Ende einer Seite oder bis sie mit "<pre>" beendet wird.

```
<pre>
E  A  D   G
Erste Strophe.

----
<pre>
E  A  D   G
Zweite Strophe.
```

### Fettdruck, Kursiv, ...
Einige [übliche HTML-Formatierungen](http://doc.qt.io/qt-5/richtext-html-subset.html) können ebenso genutzt werden.

```
Dies ist <b>besonders</b> wichtig.

Dies ist <i>kursiv</i>.

Dies ist <u>unterstrichen</u>.
```

## Beispieldatei

In [dieser Beispieldatei](https://github.com/webhamster/songprompter/blob/master/examples/02%20Far%20Away.txt) werden einige der Formatierungsanweisungen benutzt.

[zurück](/)
