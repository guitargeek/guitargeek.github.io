---
layout: post
title: "Linux-Installationsevent Herbst 2013"
date: 2013-10-31 00:00:00
categories: linux
---

Diese Woche fanden an der ETHZ wieder einmal die [Linuxtage](http://www.project21.ch/projekte/thealternative/linuxtage)
statt, zu denen auch ein Event gehört, wo wir Interessieren bei der Installation von Fedora behilflich sind. Zwei Dinge
fielen mir diesmal auf. Erstmal: der Raum war voll! Endlich ueberstieg die Zahl der Neulinge die Zahl der Helfer bei
weitem. Zuerst dachte ich, dass dies eine Folge des NSA-Skandals sei. Dass die Leute also endlich verstanden haben, dass
Windows und OS X u.a. "Spyware" sind und sie ihren Laptop davon befreien moechten. Nach genauerer Nachfrage stellte sich
allerdings das gefloppte Windows 8 als der Grund heraus, weshalb die meisten gekommen sind.

Zweitens war der Tapetenwechsel von [Ubuntu](http://www.ubuntu.com/) auf [Fedora](http://fedoraproject.org/de/) mit
[Gnome 3](http://www.gnome.org/gnome-3/) interessant. Wie wuerden man auf den Wechsel reagieren? Zweifelte man an
unserer Intergrität? Man tat es nicht, denn auch unsere Besucher empfanden Ubuntus aktuelle
[Politik](http://www.heise.de/open/meldung/Big-Brother-Award-Austria-fuer-Mark-Shuttleworth-2034943.html) als
abschreckend und verstanden das Argument, dass Fedora auch auf den ETH-Computern sei und man sich so wenig umgewöhnen
muesste.

Allerdings war ich als [openSUSE](http://de.opensuse.org/Hauptseite)-Jünger etwas skeptisch, was sich jedoch als
unbegründet herausstellte. Die Installation lief mach der Verkleinerung der Windowspartition unter Windows reibungslos,
wenn man es einmal geschafft hat, SecureBoot zu deaktivieren. Nach der Installation musste man allerdings noch einige
Anpassungen vornehmen, um den von Ubuntu gewohnten Comfort zu erreichen. Dank dem Programm “[Fedora
Utils](http://satya164.github.io/fedorautils/)” ist dies jedoch kinderleicht. Meine Empfehlung war, nach dem starten
der Fedora Utils unter "Essential tweaks & tasks" die folgenden Haekchen zu setzten:

{% include image.html
            img="../images/posts/2013-10-31-linux-installation-event/utils-235x300.png"
            url="../images/posts/2013-10-31-linux-installation-event/utils.png"
            title="utils"
            caption="Empfohlene tweaks & tasks unter fedorautils" %}

Danach konnte noch jeder unter "Install additional Software" die proprietäre Software installieren die er brauchte, wie
z.B. Skype oder Dropbox.

Insgesamt waren alle am Ende glücklich und ich freue mich schon auf das nächste mal!
