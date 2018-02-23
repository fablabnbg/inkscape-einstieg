                                jw, Fr 23. Feb 16:02:59 CET 2018

Abstract
========

Inkscape für Maker (Grundlagen und Erweiterungen)
-------------------------------------------------

Mit dem kostenlosen und quelloffenen Zeichenprogramm Inkscape konstruieren wir
Gegenstände, die mit Lasercutter, Schneidplotter und auch 3D-Drucker realisiert
werden können.
Am Beispiel von Tisch und Stuhl wird der Umgang mit den wichtigsten
Konstruktionswerkzeugen Kreis und Rechteck in der Zeichenebene gezeigt. 
Freiform-Konturen werden mit Hilfe von sog. Splines dargestellt.
Wir demonstieren abschliessend die am FabLab Nürnberg entwickelten
Erweiterungen für die Ansteuerungen der in einem typischen FabLab frei
zugänglichen Maschinen. Der Aufbau eines räumlichen Modells mit unserer
"zwei-einhalb D" Technik hat eine niedrige Einstiegshürde und erlaubt eine
steile Lernkurve mit schnellen Erfolgen.


Präsentation und Software
=========================

* https://fablabnbg.github.io/inkscape-einstieg/Inkscape-fuer-Maker.pdf
* https://inkscape.org/download
* 3D-Druck via openSCAD https://github.com/fablabnbg/inkscape-paths2openscad
* Andere Inkscape Erweiterungen https://github.com/fablabnbg?q=inkscape-
* Ansteuerung unseres Lasers im FabLab Nürnberg https://wiki.fablab-nuernberg.de/w/ZING_4030


Übungen
=======

Folie 7
-------

`cp backup/hallo_tomate.svg . ; inkscape hallo_tomate.svg`

Hier ist ein Smiley. Tomate mit Gesicht und Stil.
Den lösche ich und wir zeichnen das neu:
 - Die Augen sind schräg stehende Ellipsen, gespiegelt, symmetrisch
 - Der Mund ist ein Rechteck, in einen Pfad umgewandelt,
   die unteren beiden Eckpunkte mit `Entf` gelöscht.
 - Diskussion Stil-Ansatz:
   - Der Laser würde die Kreislinie durchschneiden. Das fällt auseinander!
   - `Pfad -> Vereinigung` oder passend öffnen.

Folie 8
-------
`cp backup/table_w_drawer.svg . ; inkscape table_w_drawer.svg`

 - Schublade löschen.

Hier ist ein Rechteck mit vier kleinen Rechtecken. 

 - Wir sehen die Platte ist 90 x 90 mm gross.
 - `Rechts-Klick -> Objekteigenschaften`
   - Hier sehen wir die Höhe der Platte in der dritten Dimension
     `Height: 5 mm`
   - Bei den Beinen steht da 
     `Height: 62 mm`

**Achtung Denksportaufgabe:**
Stellen wir uns vor, das wäre ein Tisch von unten. Okay?

 - `Erweiterungen -> aus Pfad erzeugen -> Pfade nach openSCAD...`
   Inkscape und openscad nebeneinander (ohne Editor und ohne Konsole)

 - Nun wollen wir eine Schublade unter den Tisch hängen.
 - Rechteck von Rechteck subtrahieren, um einen 3-seitigen Rahmen 
   zu erzeugen. Wir nutzen ein Schnappgitter für gleiche Abstände.
 - Dieser Rahmen bekommt `Height: 12 mm` und auch `Raise: 5 mm`
 - Eine dünne Bodenplatte `Height: 1 mm` innen hinein bei `Raise: 15 mm`
 - ins Leere klicken, `Alt-Q`
 - Frontplatte etwas breiter und etwas höher: `Height: 13 mm`
 - Griff (nur eine offene gebogene Linie) mit 2mm Linienbreite, `Height: 2 mm`
 - ins Leere klicken, `Alt-Q`

