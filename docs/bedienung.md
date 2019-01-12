* TOC
{:toc}

Der Songprompter verfügt nur über die absolut nötige Anzahl an Bedienelementen, damit das Gerät auch wenn es schnell gehen muss sofort einsatzbereit ist.

# Inbetriebnahme

Nach Vorbereitung der Songtexte auf dem USB-Stick (siehe unten) muss der Songprompter nur noch gestartet werden: 

1. Fußschalter und USB-Stick jeweils in einen der beiden USB-Anschlüsse einstecken
2. Stromversorgung einschalten
3. fertig! 

Der Songprompter zeigt jetzt die Songtexte auf dem USB-Stick in einer übersichtlichen Liste an. Mit den beiden äußeren Fußschaltern wird in dieser Liste ein Eintrag ausgewählt und mit dem mittleren Fußschalter bestätigt.

Der Songtext wird jetzt in selbst definierbaren Abschnitten (siehe unten) angezeigt. Mit den äußeren beiden Fußschaltern kann zwischen diesen Abschnitten hin- und hergeschaltet werden. Nach dem Ende eines Songs wird der erste Abschnitt des nächsten Songs angezeigt. Mit dem mittleren Fußschalter kann wieder zum Hauptmenü zurückgekehrt werden.

# Songtexte bereitstellen

Songtexte für den Songprompter werden einfach an einem Computer auf einen USB-Stick gespeichert.


## Dateien anlegen und speichern

Songtexte werden einfach direkt auf dem USB-Stick als TXT-Dateien gespeichert. Die Dateinamen müssen auf .txt enden und die Dateien müssen im Wurzelverzeichnis des USB-Sticks liegen und dürfen nicht in Unterordnern sein. Andere Dateien dürfen aber auf dem USB-Stick enthalten sein, sie stören den Songprompter nicht.

Alle .txt-Dateien im Wurzelverzeichnis des beim Start angeschlossenen Sticks werden im Songprompter zur Auswahl angezeigt.

![](/assets/images/usb-stick-contents.jpg)

Die .txt-Dateien sollten nicht mit einer Textverarbeitung wie Word oder Wordpad bearbeitet werden sondern mit einem einfachen Texteditor wie dem bei Windows enthaltenen Notepad.

![](/assets/images/songtext-notepad.jpg)

## Sortieren

Die Sortierung der Songtexte erfolgt in alphabetischer Reihenfolge der Dateinamen. Eine individuelle Reihenfolge der Dateien kann also einfach über Ziffern vor dem Dateinamen festgelegt werden. Für eine korrekte Sortierung sollten einstelligen Zahlen Nullen vorangestellt werden. Ein Beispiel ist im Bild oben zu sehen. 

## Formatieren

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

# Es geht nicht, was tun?

Startet der Songprompter nicht oder zeigt nicht die erwarteten Songtexte an, helfen vielleicht die folgenden Tipps. Sollte keine Lösung dabei sein, bitte eine E-Mail mit einer genauen Problembeschreibung (am besten mit Bildschirmfotos) an [songprompter@danielfett.de](mailto:songprompter@danielfett.de) schreiben.

## USB-Stick formatieren

USB-Sticks müssen mit FAT32 formatiert sein. Das ist bei neu gekauften USB-Sticks in der Regel der Fall. Erkennt der Songprompter den USB-Stick nicht, hilft eventuell eine [Neuformatierung](http://praxistipps.chip.de/usb-stick-formatieren_2850) - hierbei gehen allerdings alle Daten auf dem USB-Stick verloren. 

## Tipps und Tricks

### Bildschirm rotieren oder spiegeln
Je nach Aufstellung des Songprompters - oder bei Benutzung der Software mit externen Monitoren - kann es sinnvoll sein, den Bildschirm zu drehen. Dies kann leicht wie folgt erreicht werden:

  * Nehmen Sie die Micro-SD-Karte im Songprompter aus dem Gerät und legen Sie diese in Ihren Computer ein (ein entsprechender Kartenleser wird benötigt)
  * Öffnen Sie die Datei config.txt auf der SD-Karte mit einem Texteditor - beispielsweise mit [Notepad++](https://notepad-plus-plus.org/)
  * Anschließend suchen Sie die Zeile "# display_rotate=0".
  * Fügen Sie darunter folgende Zeile ein: "display_rotate=x" wobei Sie x durch einen der folgenden Werte ersetzen:

|Wert |	Rotation |
|-----|----------|
| 0 |	normal |
| 1 |	90° |
| 2 |	180° |
| 3 |	270° |
| 0x10000 |	horizontal spiegeln |
| 0x20000 |	vertikal spiegeln |

[zurück](/)

