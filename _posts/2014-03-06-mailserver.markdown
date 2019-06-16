---
layout: post
title: "Sich von Google losreissen mit eigenem Mailserver"
date: 2014-03-06 00:00:00
categories: linux
---

Google weiss zu viel über mich. Seit 2007, dem Jahr in dem ich mein Gmail-Konto eröffnet habe, hat sich schleichend eine
Infrastruktur aufgebaut, die sich durch alle Lebenslagen erstreckt. Die Bequemlichkeit erstickt aber die Vorsätze, sich
davon unabhängig zu machen, meistens schon sehr früh. Und so habe ich bin zum Überwachungsskandal letzten Jahres wenig
Gedanken darüber gemacht, dass Google meine Kontakte, meine elektronische Post, mein Telefon, meine Termine und zum Teil
meine elektronische Unterhaltung fest im Griff hat.

Von Gmail, dem wohl wichtigsten Teil der Infrastruktur, wollte ich also weg. Bei der Suche nach Alternativen mit mehr
Privatsphäre stiess ich auf [Lavabit](http://lavabit.com/), dem Email-Provider den auch Snowden verwendete. Doch schon
ein paar Tage später musste ich auch Lavabit aufgeben. Die NSA zwang Ladar Levison, den Admin von Lavabit, die Schlüssel
zum uneingeschränkten Zugriff auf die Lavabit-Server rauszurücken. Doch Levison schaltete seinen Dienst lieber ganz ab,
anstatt seine User zu verraten. Die Schlussfolgerung: alle amerikanischen Internet-Dienstleister, die noch online sind,
sind potentielle Verräter.

Warum dann nicht einen deutschen Email-Provider? Leider hat mir die Erfahrung dann doch gezeigt, dass man im Netz
möglichst niemandem vertrauen sollte. So hat uns die europäische Firma “United Internet”, zu der u.a. GMX und Web.de
gehören, letzte Woche ja auch [eiskalt absichtlich
fehlinformiert](http://www.heise.de/newsticker/meldung/Seitenmanipulierende-Add-ons-United-Internet-startet-Kampagne-gegen-Adblocker-2125592.html),
indem sie uns erklären wollten, das Adblocker der Sicherheit schaden. Das bringt auch nicht gerade Sympathie ein. Das
sind wahrscheinlich alles Folgen dieses verrückten Geschäftsmodells im Internet: der User ist nicht der Kunde, sondern
das Produkt für die Werbeindustrie, und so wird man auch behandelt. Bevor ich jetzt weiter ausschweife, hier ist meine
Lösung:

{% include image.html
            img="../images/posts/2014-03-06-mailserver/server-1024x768.jpg"
            url="../images/posts/2014-03-06-mailserver/server.png"
            title="Mein Raspberry Pi mit selbstgebautem LEGO-Gehäuse"
            caption="Mein Raspberry Pi mit selbstgebautem LEGO-Gehäuse als Mailserver" %}

Seit zwei Wochen betreibe ich also meinen eigenen Mailserver bei mir auf dem Schreibtisch. Auf die technische Seite
möchte ich aber nicht weiter eingehen, da alles in diesem [Tutorial](https://workaround.org/ispmail) wunderbar erklärt
wird. Es war auch fast meine einzige Informationsquelle für mein Projekt, neben einem Artikel in der c’t, der Hinweise
zum Betrieb eines Mailservers auf dem Raspberry Pi lieferte.

Man bekommt bei der Umsetzung eines solchen Projektes natürlich einen gutes Grundverständnis zur Funktionsweise von
Email. Doch man merkt immer wieder, dass die Technologie noch aus der Zeit stammt wo es keine “bösen Leute” im Internet
waren. So wurden mit der Zeit viele Mechanismen eingebaut, um Spammern und Hackern das Leben schwerer zu machen, die das
System aber auch insgesamt recht kompliziert machen. Das muss man natürlich sauber beachten, damit die verschickten
Mails auch angenommen werden und man selber nicht ohne Schutz den Spam-Fluten ausgelegt ist. Daher würde ich das Projekt
schwieriger als einen eigenen Webserver einstufen.

Deswegen kann es nur solchen Leuten weiterempfehlen, die schon etwas Erfahrung in dem Bereich haben und die Zeit haben,
sich damit auseinander zu setzen. Und vielleicht ist das coolste am Ende vor allem, dass man sagen kann: “Ich haben
meinen eigenen Mailserver!”. Die eigene Domain in der Addresse hat schon einen netten Protzfaktor.
