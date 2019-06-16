---
layout: post
title: "Snake auf einem FPGA"
date: 2014-05-25 00:00:00
categories: electronics
---

Dieses Semester belegte ich die Vorlesung “[Elektronik für Physiker
II](https://www.ini.uzh.ch/~tobi/wiki/doku.php?id=dig:start)“, in der es im Gegensatz zum ersten Teil um digitale
Elektronik ging. In der zweiten Hälfte der Vorlesung beschäftigten wir uns mit
[FPGAs](http://de.wikipedia.org/wiki/Field_Programmable_Gate_Array), also einem integrierten Schaltkreis, in den man
logische Schaltungen hineinprogrammieren kann. Dadurch dass also nicht die Software, die auf der Hardware läuft,
programmiert wird, sondern direkt die Hardware, kann ein FPGA in bestimmten Anwendungsgebieten sehr schnell sein. So
werden sie zum Beispiel zum [Triggern](http://archiv.ub.uni-heidelberg.de/volltextserver/1403/) der riesigen Datenmengen
aus dem ATLAS-Detektor verwendet.

Wir sollten am Ende des Semesters in Gruppenarbeit das aus den Nokia-Handys bekannte Spiel
[Snake](http://de.wikipedia.org/wiki/Snake) implementieren. Zumindest kennt meine Generation das Spiel als Handyspiel.
Dabei wird jetzt nicht gerade das volle Potential unseres FPGAs, einem Spartan3E-250 von Xilinx, genutzt, aber es war
trotzdem ein spannendes Projekt, von dem ich hier berichten möchte.

{% include image.html
            img="../images/posts/2014-05-25-fpga-snake/Snakeshot.png"
            url="../images/posts/2014-05-25-fpga-snake/Snakeshot.png"
            title="Snakeshot"
            caption="Ein “Screenshot” von unserem Snake" %}

Die Idee war, dass man einen alten Computerbildschirm an unser Entwicklerboard anschliesst, auf dem das Spiel läuft, und
man steuert es mit den Knöpfen auf dem Board. Zusätzlich gab es
[hier](http://www.ini.uzh.ch/~tobi/~hdlworld/HDLWorld/Mod13/HTML/wsdindex.html) einen groben Vorschlag, wie man das
Spiel programmieren soll. Der Vorschlag lieferte aber keinen Code, sondern nur ein paar Diagramme.

Aber was ist denn genau das besondere daran, einen FPGA zu programmieren? Achtung, der nächste Abschnitt wird etwas
technisch. Wie unterscheidet es sich vom “normalen” Programmieren? Beginne ich mal mit den Gemeinsamkeiten. So wie man
in modernen Programmiersprachen versucht, durch Objektorientierung alles modular und übersichtlich zu gestalten, seinen
Code also in “Klassen” aufbaut, so versucht man hier seine programmierte Schaltung in kleinere “Module” aufzuteilen, die
sich Bits hin- und herschieben. Wer sich das genauer angucken will, findet den Quellcode auf
[Github](https://github.com/guitargeek/PolJonasSnake), Und bei Bits bleibt es auch. Es gibt keine Integer oder Floats,
sondern nur “Wires” (Bits, deren Zustand unmittelbar von anderen Bits abhängt) und “Register” (Bits, die ihren Zustand
alleine halten können, also quasi ein Flip-Flop). Diese Register kann man nun manipulieren, und zwar “synchron” (immer
wenn eine Uhr tickt passiert etwas) oder “asynchron” (immer wenn sich andere Bits verändern passiert etwas). Im Code
sieht man das schön in den “always@”-Blöcken.

Genug der Theorie, hier geht es ja auch um Unterhaltung. [Hier](../images/posts/2014-05-25-fpga-snake/Snake-240p.avi)
also ein Video (11 MB) mit dem Spiel was man sich downloaden kann. Obwohl sich der Zähler offensichtlich verzählt sei
das Spiel “schön genug”? Ich muss wohl schon sehr müde gewesen sein, als ich das Video gemacht habe. Mittlerweile habe
ich den Bug aber gefixt und alles läuft prima. Ein neues Video kann ich aber nicht mehr machen, da wir das Board wieder
abgeben müssen. Der rote Bildschirm bedeutet übrigens, dass man verloren hat, weil die Schlange sich selbst gefressen
hat. Bei grünem Bildschirm hat man gewonnen.

Das Spiel geht also nicht unendlich lange. Das liegt daran, dass es schwierig ist, in Hardware eine Schlange mit
variabler Länge zu programmieren. Pro Längeneinheit müssen ein paar Register mehr genutzt werden, und es muss schon
vorher feststehen, welches Register sich wie verhalten sollen. Also kann man höchstens, so wie wir es gemacht haben, a
priori eine maximale Anzahl an Schlangenteilen festlegen, wobei am Anfang nicht alle Schlangenteile aktiv sind. Deswegen
ist das Spiel irgendwann vorbei.

{% include image.html
            img="../images/posts/2014-05-25-fpga-snake/Basys2-1024x768.jpg"
            url="../images/posts/2014-05-25-fpga-snake/Basys2.jpg"
            title="Basys2"
            caption="Das Entwicklerboard, auf dem das Spiel läuft – Rechts unten der Punktestand." %}

Die Entwicklung des Spiels hat uns viel Freude bereitet und es war toll, Programmieren so aus einem anderen Blickwinkel
kennenzulernen. Vorallem hilft es auch dabei, die grundsätzliche Funktionsweise von Computern sehr nahe an der Hardware
zu verstehen. Zum privaten Basteln sind FPGAs und besonders die Entwicklerboards hier in Europa allerdings fast noch zu
teuer. Das Board, das wir benutzt haben, kostet bei Farnel z.B. 130 CHF. Dazu kommt die 30 GB grosse Software. Eine
Open-Source-Lösung wäre mir lieber gewesen, aber vermutlich kann man das bei einer so neuen Technologie nicht erwarten.
Aber vorallem bin ich als Videospiel-Fan natürlich sehr stolz darauf, einmal Snake selber programmiert zu haben!
