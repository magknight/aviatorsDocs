Pfad: tree/master/docs/faq
Quelle: faq.md

# Häufig gestellte Fragen
## Was ist der blaue Kasten?
Der blaue Kasten ist ein Diagnose-Werkzeug für den fctl2-Zweig, der zur Zeit auf dem Cygnus-Kanal läuft. Er ist wichtig, und nein, du kannst ihn nicht abstellen.

## Warum zeigt der Updater "locked for maintenance" an?
Allgemein gibt es dafür 2 Gründe:
* Wir spielen gerade eine Aktualisierung auf, was Zeit braucht - warte einfach ein bisschen
* Es ist für diesen Zweig keine Aktualisierung verfügbar

Es ist **nicht** möglich, von 1.4.x auf 1.5.0 mit dem Updater zu aktualisieren. Du musst die 787 aus dem Store neu installieren.

## Wann wird ... Update veröffentlich?
Wenn es fertig ist...

## Was ist Cygnus?
Cygnus ist der Name für unser Updater-basiertes öffentliches Beta-Programm. Es ist nicht als stabil bezeichnet, sollte also nur benutzt werden, wenn du Bugs erkennen und weitermelden möchtest. Es kann über den Skunkcraft's Updater mit dem "Enable beta channel"-Kästchen aktiviert oder deaktiviert werden.

## Was ist Discord?
Wir benutzen Discord als unsere primäre Kommunikations- und Support-Plattform für Kunden. Du kannst unserem Server auf https://magknight.org/discord beitreten.

## Meine Seriennummer kann nicht weiter aktiviert werden
Wenn deine Seriennummer nicht mehr aktiviert werden kann, kannst du uns im Forum, über soziale Netzwerke oder per E-Mail kontaktieren, um weitere Aktivierungen zu ermöglichen.

## Wie kann ich Regeneffekte aktivieren?
Regeneffekte, die von librain bereitgestellt werden, können auf der Einstellungsseite im EFB aktiviert werden. Diese Einstellung befindet sich auf Seite 2.

## Wie kann ich Kabinendurchsagen durchführen?
Kabinendurchsagen werden über die COMM-Seiten im MFD gesteuert. Um diese Seite zu aktivieren, drücke auf COMM auf einer der MFD-Kontrollfeldern, dann drücke auf CABIN.

## Warum sind meine MCP/Radio-Bildschirme schwarz?
Wenn du kalt und dunkel startest, ist die Hintergrundbeleuchtung des MCP und Pedestal auf der kleinsten Einstellung. Dieser Drehknopf kontrolliert außerem die Bildschirmhelligkeit vom MCP und den Radios.
Um die Radios einzuschalten, drehe den AISLE STAND PNL Drehknopf auf die äußerste rechte Position, dieser ist auf der hinteren rechten Seite vom Pedestal.
Um das MCP einzuschalten, drehe den GLARE PNL Drehknopf auf die äußerste rechte Position, dieser ist auf der unteren linken Seite vom Überkopf-Bedienfeld.

## Unterstützt die 787 MacOS?
Ja, tut sie! Du musst auf 1.2.10 oder später aktualisieren, um Unterstützung dafür zu erhalten.

## Der Treibstoffverbrauch der 787 ist viel zu niedrig
Stelle sicher, dass das "Experimentelle Flugmodell" in den X-Plane-Einstellungen  **deaktiviert** ist. Wir bieten im Moment keine Unterstützung für das experimentelle Flugmodell an.

## Wie aktualisiere ich meine 787?
Mit der **787**: Aviator's Edition kommt die Fähigkeit, das Flugzeug mit dem SkunkCrafts-Updater automatisch zu aktualisieren. Kleinere Aktualisierungen (1.0.x) werden ausschließlich über diesen übertragen.

Der SkunkCrafts-Updater kann [hier](https://forums.x-plane.org/index.php?/forums/topic/144828-updater-download-page-v22-available/) gefunden werden.

Du wirst ein Änderungsprotokoll im Flugzeug-Ordner finden.

Fehlt die Konfigurationsdatei? Lade sie [hier](https://docs.magknight.org/img/skunkcrafts_updater.zip) herunter. Du musst diese im Hauptverzeichnis deines Flugzeugs platzieren.

## Was macht der VATSIM-Modus?

!!! Achtung "Veraltet"
    Der VATSIM-Modus wurde mit Version 1.5.0 entfernt - seine Funktionalität wurde fast vollständig von ACARS ersetzt.

Der VATSIM-Modus aktiviert die Integration mit dem [VATSIM Netzwerk](https://vatsim.net). Er aktiviert die SELCAL-Identifikation, Funk-Übertragungen die die contact-me-Nachrichten nutzen und ein paar andere Funkübertragungsbezogene Fähigkeiten. *Der VATSIM-Modus funktioniert nur mit X-Squawkbox; wegen dem Fehlen der Verfügbarkeit von datarefs sind der Swift-Client und IVAO-Clients nicht unterstützt.*

## Funktionieren alte Bemalungen mit 1.5.0?
Bemalungen, die seit 1.4.0 veröffentlich wurden, **werden** mit 1.5.0 funktionieren, allerdings haben wir mit 1.5.0 einen aktualisierten Bemalungsbaukasten veröffentlicht, der neue Heck- und Flügel-Texturen beinhaltet, ein paar Rumpfänderungen und die SATCOM-Kuppel. Bemalungen müssen mit diesem neuen Bemalungsbaukasten aktualisiert werden, um diese Verbesserungen nutzen zu können, sie werden aber trotzdem funktionieren. Außerdem benötigen die Bemalungen eine Aktualisierung um die neuen GE und RR Triebwerkmodelle der Version 1.5.0 nutzen zu können.

## Wie wechsele ich die Triebwerkmodelle?
Geh auf die EFB-Einstellungsseite und suche nach der **ENGINE TYPE**-Einstellung. Bemalungen sollten mit einer aktualisierten liverySettings-Datei daherkommen, die die Triebwerkmodelle definiert, die unterstützt werden.

## Wie wechsele ich zwischen 1.4.0 und 1.5.0 GE Triebwerken?
Geh auf die EFB-Einstellungsseite und suche nach der **LIVERY VERSION**-Einstellung. Bemalungen sollten mit einer aktualisierten liverySettings-Datei daherkommen, die die Triebwerkmodelle definiert, die unterstützt werden.

## Kann ich den Klappen-Hebel einer Achse zuweisen?
Nein. Der Klappen-Hebel ist nicht für die Nutzung mit einer Achse geeignet, da es weder möglich ist, gerastete Stellungen festzulegen, in denen der Klappen-Hebel aktuell ist, noch es möglich ist, sicherzustellen, dass eine versehentliche Betätigung des Hebels nicht zu einem ungewollten, möglicherweise Flug-endenen Verhalten kommt. Wenn du der Meinung bist, dass deine Lösung eine Zuweisung der Klappen auf eine Achse erfordert, kannst du das gerne mit uns diskutieren und wir werden dir verschiedene Lösungen zeigen.

## Funktioniert die 787 in VR?
Wir unterstützen nicht direkt VR und haben keine speziellen Funktionen eingebaut, die es erlauben würden zu funktionieren. Viele Nutzer haben jedoch berichtet, dass das Flugzeug in VR funktioniert.

Wir empfehlen folgende Modifikationen, wenn du das Flugzeug in VR nutzen willst:

- [VR hotspots for cockpit seats](https://forums.x-plane.org/index.php?/forums/topic/172655-vr-hotspots-for-cockpit-seats/) von [Xplaner-73](https://forums.x-plane.org/index.php?/profile/428045-xplaner73/&wr=eyJhcHAiOiJmb3J1bXMiLCJtb2R1bGUiOiJmb3J1bXMtY29tbWVudCIsImlkXzEiOjE3MjY1NSwiaWRfMiI6MTYwMjY4OX0=) (X-Plane.org)
- [MoveVR](https://forums.x-plane.org/index.php?/files/file/44809-movevr-move-external-windows-into-x-plane-even-into-vr/) von [Folko](https://forums.x-plane.org/index.php?/profile/215470-folko/&wr=eyJhcHAiOiJkb3dubG9hZHMiLCJtb2R1bGUiOiJkb3dubG9hZHMiLCJpZF8xIjo0NDgwOX0=) (X-Plane.org)
