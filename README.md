# Lasercutter
- Typ: `K40`
- Leistung: 40 Watt
- Art: CO2 Laser
## Disclaimer
Benutzung auf eigene Gefahr! Bitte beachtet die Sicherheitshinweise des Herstellers und fragt im MakerSpace nach, wenn Ihr Euch unsicher seid. Ein Laser ist ein gefährliches Gerät und sollte nur mit größter Vorsicht benutzt werden.
## Programme
Unser Lasercutter arbeitet mit RD-Dateien. Diese müssen über ein spezielles [Konstruktionsprogramm](##Programme) erstellt werden.
Diese RD-Datei kann dann über die entsprechenden Programme auf den Laser hochgeladen oder direkt aus dem Konstruktionsprogramm gestartet werden.
Hierzu muss unser Lasercutter in den Programmen eingerichtet werden. 
Der Laser wird mit einem DSP der Firma `Ruida` angesteuert. Der Laser hat die interne IP-Adresse `192.168.41.25`.
Die Programme werden wie typische Zeichenprogramme bedient, nur das eben zum Schluss ein anderes Dateiformat rauskommt.
### LightBurn
LightBurn ist ein Konstruktionsprogramm zur Bedienung von Lasercuttern. [LightBurn](https://lightburnsoftware.com/collections/frontpage/products/lightburn-dsp) ist kostenpflichtig. Die passende Lizenz für DSP-Bedienung kostet zirka 120€. Der MakerSpace hat die Lizenz erworben und auf dem Packard Bell im MakerSpace kann es benutzt werden.
In diesem Repository im Ordner `LightBurn` befindet sich eine passende Einstellungsdatei, welche in LightBurn importiert werden kann.
### RDWorks
RDWorks ist die Originalsoftware des Herstellers und kostenfrei, hat jedoch viele Funktionen nicht und ist sehr umständlich in der Bedienung. Es eignet sich für einfache Formen.

## Manuelle Bedienung am Laser
- Lasercutter am Seitenpanel einschalten. Es wird laut und das Hauptmenü erscheint auf dem Display.
- Unbedingt den Abluftschlauch aus dem Fenster hängen
</br>
<img src="./img/Lasercutter_Seitenpanel.jpg" width="200" height="200" />
<img src="./img/Lasercutter_Startmenu.jpg" width="200" height="200" />
- Man wählt über den Knopf "File" und die Hoch/Runter und Enter-Taste die zuvor hochgeladene Datei aus
</br>
<img src="./img/Lasercutter_Menu_File.jpg" width="200" height="200" />
<img src="./img/Lasercutter_Menu_File_Selection.jpg" width="200" height="200" />
<img src="./img/Lasercutter_Menu_File_Selection_Up_Down_Enter.jpg" width="200" height="200" />
- Mit dem Knopf "Origin" gelangt man zum Startpunkt (0,0) des zu lasernden Objektes
- Der Knopf "Frame" sorgt dafür, dass der gesamte Frame-Umfang des Objektes abgefahren wird
</br>
<img src="./img/Lasercutter_Menu_File.jpg" width="200" height="200" />
- Kontrolliere anhand des "Frame", dass das Werkstück korrekt im Laser liegt. (siehe dazu Video in `./img/Lasercutter_Frame_Movement.mp4`)
- Bezahlvorgang mit MakerSpace Karte
Der Laser verbraucht viel Strom und die Wartungs- und Ersatzteilkosten sind sehr hoch, weshalb wir einen Beitrag von 15ct pro Minute erheben. Dieser wird von deiner MakerSpace Karte direkt eingezogen. Bitte lege deine Karte auf das auf dem Laser befindliche Bezahlterminal und starte dann den Laservorgang.
</br>
<img src="./img/Lasercutter_Payment.jpg" width="200" height="200" />
- Bitte belasse deine Karte so lange der Laser arbeitet auf dem Bezahlterminal. Es wird nur solange Guthaben abgebucht wie der Laser aktiv läuft.

## Tipps & Tricks
### Gerade Kanten
Leider besitzt der Laser keinen Anschlag, sodass wir Werkstoffe exakt ausrichten können. Deshalb bietet es sich an, dass man bereits im Konstruktionsprogramm einen Rahmen um das gewünschte Objekt zieht und auslasert, sodass man anhand dessen komplexere Figuren ausrichten kann und stets ein gerades Ergebnis herauskommt.

### Tabellen Einstellung des Lasers zu Material - Erfahrungswerte
Die nachfolgenden Tabellen sind eine Sammlung von Erfahrungswerten von unseren Makern welche Einstellungen für die jeweiligen Werkstoffe vorgenommen werden müssen um gewünschte Ergebnisse zu erzielen. Wir unterscheiden zwischen "Schneiden" und "Gravieren", wobei die jeweiligen Ergebnisse abhängig vom Werkstoff sind. Im Zweifel fragt bitte einen erfahrenen Maker nach seiner Meinung, ob euer Werkstück den Angaben in der Tabelle entspricht oder weitere Feinjustierungen notwendig sind.
#### Schneiden
Material | Materialstärke (mm)| Leistung (%) | Speed (mm/sec) | Fokus | Kommentar
-------- | ------------------ | ------------ | -------------- | ----- | ---------
Sperrholz | 3 | 70 | 10 | 90 |
Sperrholz | 5 | 70 | 10 | 90 | 2 Durchgänge
MDF | 3 | 70 | 10 | 11 | 4 Durchgänge
Plexiglas, klar | 7 | 70 | 5 | 80 |
Plexiglas, transparent, rot | 7 | 70 | 5 | 70 |
Plexiglas, schwarz | 7 | 70 | 5 | 100 |
Plexiglas, rot | 3 | 70 | 5 | |
Presspappe | | 70 | 9 | |
Plexiglas, klar | 5 | 70 | 4 | |

#### Gravieren
Die Tabelle für das Gravieren beinhaltet keine Materialstärke, da wir nur die Oberfläche bearbeiten möchten und es irrelevant ist wie stark das Werkstück ist.
Material | Leistung (%) | Speed (mm/sec) | Fokus | Kommentar
--------  | ------------ | -------------- | ----- | ---------
Sperrholz | 60 | 250 |  |
Holz | 30 | 150 | 100 | besonders für Bilder gut geeignet
Zollstock, Holz, weiß | 30 | 400 | 100 |
Holzschale | 30 | 200 | 100 |
Presspappe | 20 | 100 | |
Plexiglas | 70 | 250 | 100 |
Glas | 20 | 200 | | funktioniert nur bedingt, bitte erfahrenen Maker fragen!
Schiefer | 70 | 200 | 100 |
Spiegel | 40 | 100 | 90 |
Platinenlack | 10 | 90 | | leider nicht für sehr Filigranes geeignet!

### Gefährliche Materialien
Nicht alle Werkstoffe sind sicher zu lasern und können gefährliche Gase / Dämpfe bilden. Hierzu beachtet bitte die neben dem Laser aushängende Liste von gefährlichen Materialien.
Lieber einmal mehr nachfragen ist hier äußerst erwünscht!

## TL;DR Anleitung
- Konstruktionsdateien mit Software erstellen
- RD-File auf Laser hochladen
- Manuelle Bedienung am Gerät und Bezahlung


