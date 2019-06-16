---
layout: post
title: "OpenSUSE Tumbleweed ausprobiert"
date: 2013-11-21 00:00:00
categories: linux
---

Die Linux-Distribution [openSUSE](http://de.opensuse.org/Hauptseite) war für mich wie für viele andere wahrscheinlich
auch das erste GNU/Linux. Auf eine LTS-Version (long term support – 5 Jahre Support) wie bei Ubuntu müssen wir “Geekos”
verzichten. Jedoch wäre das sehr zu wünschen, da man nicht alle 18 Monate sein System neu aufsetzen möchte, gerade wenn
die Installation stark verändert wurde im Laufe der Zeit.

Doch es gibt eine Alternativen: z.B. das [Tumbeleweed](http://de.opensuse.org/Portal:Tumbleweed)-Projekt, welches aus
den normalen openSUSE-Releases ein sog. Rolling Release macht. Das bedeutet, Packete werden konstant aktualisiert und es
gibt keinen Schnitt zwischen den Releases. Da man sich openSUSE Tumbleweed aber nicht als ISO downloaden und
installieren kann, sondern man seine aktuelle Version dazu umkonfigurieren muss, ist es für Einsteiger recht
abschreckend und kann durch seine Eigenheiten auch Profis zur Verzweiflung bringen.

Da die Informationen auf dem Portal jedoch begrenzt sind, glaube ich dass es sinnvoll ist, meine aktuelle Erfahrung und
vorgehensweise mit Tumbleweed, welches ich selber testete, zu erörtern.

Die Informationen auf dem Portal sind etwas wenige, aber jetzt habe ich verstanden wie es läuft, nachdem am Anfang der
Woche der offizielle Release von openSUSE 13.1 war. Das ganze läuft so: zu den Repositories der aktuellen openSUSE
Version muss das Tumbleweed-Repository hinzugefügt werden, was einen mit den Softwareupdates aus der Entwicklerversion
(Factory) versorgt, die die Maintainer für stabil genug halten. Immer wenn ein neues openSUSE rauskommt werden dann
automatisch ihre Repositories übernommen und das Tumbleweed Repository wird leer.

Das ganze hat ein paar [Haken](https://www.youtube.com/watch?v=oIY4X8yi5Oo):

* Wenn es einen neuen Kernel gibt, kann man davon ausgehen, dass einem eigene Funktionen fehlen. So haben die Maintainer
  zum Beispiel diesmal keine Zeit gehabt, die Vitrtualbox für einen neuen zu Verfügung stehenden Kernel zu bauen.
  Funktionalität für Aktualität zu opfern ist allerdings nicht gut.
* Bei den Tumbleweed-Packeten wird anscheinend nicht darauf geachtet, dass die Versionen nicht die des kommenden
  Releases überschreiten. So muss man tatsächlich, wenn mit dem neuen Release das Tumbleweed geleert wird und man auf
  die regulären Repos zurückfällt, so einiges gedowngraded werden. Das macht den übergang zu neuen Releases aufwändiger
  als ein einfaches Dist-Upgrade von Release zu Release, was sich überhaupt nicht nach “rolling distribution” anhört.
* Wenn es z.B. um proprietäre Grafikkartentreiber geht, die ja auch gegen den aktuellen Kernel gebaut werden: man muss
  den Treiber bei jedem Kernel-Upgrade neu bauen lassen, was den zusätzlichen Aufwand nicht Wert ist.

Insgesamt konnte ich keinen Vorteil finden, denn von leicht vorgerückten Versionsnummern der Packete merkt man als
Endanwender grundsätzlich wenig. Seinen Sinn als rollende Distribution erfüllt es wegen dem erhöhten Aufwand auch
wenig.

Also kann ich eher empfehlen, Tumbleweed nicht auszuprobieren, besonders nicht wenn man auf dem PC produktiv arbeiten
will. Wer gerne rumexperimentiert, der sei natürlich nicht davon abgehalten. Jedoch sehe ich die Zielgruppen von
Tumbleweed nicht. Endbenutzer? Haben bei neuen Release nicht weniger Arbeit als sonst. Bastler? Haben Factory als
Spielplatz.

Einen Vorteil hatte das ganze aber: über Umwege, bei denen Xorg nicht mehr starten wollte, bin ich jetzt tatsächlich zum
Stand openSUSE 13.1 gerutscht. Ich werde also wieder 18 Monate mit Updates versorgt. Der Weg der regulären Releases
scheint mir am Ende doch am unkompliziertesten. Das Tumbleweed-Repository lasse ich trotzdem mit niedriger Priorität
aktiviert, so kann ich mir einzelne Software, die ich doch in neuerer Version verwenden möchte, unkompliziert besorgen.
Aber bestimmt nicht neue Kernel.

{% include image.html
            img="../images/posts/2013-11-21-opensuse-tumbleweed/schoenes_KDE4-1024x576.png"
            url="../images/posts/2013-11-21-opensuse-tumbleweed/schoenes_KDE4.png"
            title="Mein aktueller Desktop - mit was will Apple und Microsoft mich locken? Mit Optik wohl eher nich :-)"
            caption="Mein aktueller Desktop - mit was will Apple und Microsoft mich locken? Mit Optik wohl eher nich :-)" %}
