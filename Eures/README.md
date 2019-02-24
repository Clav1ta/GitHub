# Was für Fachkräfte suchen Schweizer Firmen im Ausland? 

Vorliegendes Datenprojekt ist im Rahmen des CAS Datenjournalismus 18-19 an der Schweizer Journalistenschule MAZ in Luzern entstanden (http://www.maz.ch/studiengaenge/journalismus-weiterbildung/cas-datenjournalismus/) und wurde am 28.Februar 2019 eingereicht.


### These
Heute sind viele spezialisierte Fachkräfte oft nur noch im Ausland zu finden. Das europäische Portal zur beruflichen Mobilität EURES (https://ec.europa.eu/eures/public/de/homepage) ist ein Netzwerk für Anstellungen innerhalb der EU. Die Plattform zeigt offene Stellen in 31 europäischen Ländern an, darunter der Schweiz. Wer ein Jobinserat publizieren will muss sich registrieren ( https://ec.europa.eu/eures/public/de/employers). Es ist deshalb naheliegend, dass vorallem Firmen auf EURES Stellen ausschreiben, welche Mühe haben die Stelle mit Inländern zu besetzen. Deshalb könnte Eures eine spannende Plattform sein, um herauszufinden, für welche Berufe Schweizer und EU Firmen im EU-Raum auf Mitarbeitersuche gehen. In einem zweiten Schritt lässt sich überprüfen, ob in den gesuchten Berufen tatsächlich im jeweiligen Land ein Fachkräftemangel herrscht (zb gemessen an der Arbeitslosigkeit) und ob der Jobmarkt in der EU funktioniert, respektive suchen alle Länder nach den gleichen Fachkräften oder nach unterschiedlichen Fachkräften.


### Ziel
Ziel ist ein Tool zu bauen, mit welchem man in Echtzeit abfragen kann, welche Fachkräfte Schweizer Firmen und Firmen in der EU im Ausland suchen.


### Methodik und Vorgehen
Im Kurs  haben wir verschiedene Methoden der Datenbeschaffung kennengelernt: Scrapen mit API, Beautiful Soup und Silenium. Ich will mit vorliegender Arbeit eine weitere Methode lernen und vertiefen: die Anfragemethode mittels POST-Request. Diese Methode eigent sich insbesondere für dynamische Webseiten und vereinfacht das scrapen. Da der Request im Datenformat Json erfolgt, können alle Inserate direkt als Json-Datei ausgelesen werden.

In einem ersten Schritt soll ein Scraper für die Jobinserate von Schweizer Firmen entwickelt werden. Gelingt das lässt sich darauf aufbauend ein Scraper für die ganze Plattform entwickeln.


### Geschätzter Arbeitsaufwand
**TAG 1:** Auslesen der Jobinserate von Schweizer Firmen
**Tag 2:** Auslesen der Jobinserate von Schweizer Firmen 
**Tag 3:** Datensatz reinigen
**Tag 4:** Visualisierung der Daten und Skizze eines Scrapers für die ganze Plattform.
**Tag 5:** Dokumentation und Storyskizze

Der tatsächliche Zeitaufwand ist unter `Zeitprotokoll.csv` portokolliert.


### Entwicklung Scraper
Die Jobsuchplattform EURES beitet für Private keine APIs. Die Datenbank muss somit automatisiert ausgelesen (gescrapt) werden um einen Datensatz zu erstellen.

Im Ordner `EURES_CH` sind vier Jupyter Notebooks mit dem entwickelten Programmiercode sowie die der gescrapte Datensatz abgelegt:

`1_EURES_CH_Entwicklung_Scraper`: In diesem Notebook wird die Webseite analysiert und ein Scraper entwickelt.
`2_EURES_CH_Scraper`: In diesem Notebook ist der entwickelte Scraper ohne Kommentar abgelegt.
`3_EURES_CH_Pandas_Daten_reinigen`: In diesem Notebook werden die Daten gereinigt.
`4_EURES_CH_Pandas_Plotten`: In diesem Notebook werden die Daten visualisiert.


### Skalierung
Der entwickelte Srcaper kann leicht abgeändert auch dazu genutzt werden die ganze Jobsuchplattform auszulesen. Eine Möglichkeit wird im Ordner `EURES_Total` aufgezeigt. Viele Jobsuchplattformen schicken bei einer Anfrage einen Post-Request. Die hier erarbeite Methode kann auch zum Scrapen auf andere Suchplattformen angewendet werden wie zum Beispiel https://www.job-room.ch.


### Ergebnis
Das Ergebnis mit einer Skizze einer möglichen journalistischen Story findet sich im Dokument `ARTIKEL_Diese_Fachkräfte_suchen_Firmen_im_Ausland.pdf`. 


### Weitere Informationen
Im Dokument `INTERVIEW_Christian_Hanisch.pdf` ist das Gespräch mit der Briefing-Person zusammengefasst.


# Knackpunkts des Projektes
Aufwand/Ertrag. Es würde an Aussagekraft gewinnen


### Technische Voraussetzungen
Der Scraper, Datenanalyse und Visualisierung sind in Python 3 programmiert. Die benötigten Libraries sind in `Requirements.txt` aufgelistet.


### Über mich
Ich bin Wirtschaftsjournalistin beim Schweizer Radio und Fernsehen SRF. Bei Fragen Mail an claudia.stahel@srf.ch


### Danksagung
An dieser Stelle möchte ich all jenen danken, die durch ihre fachliche Unterstützung zum Gelingen dieser Abschlussarbeit beigetragen haben.

Zuerst gebührt mein Dank Ale Rimoldi von der OpenTechSchool Zürich (http://www.opentechschool.org/zurich/). Ale organisiert zwei Mal wöchentlich (jeweils Di und So Abend) ein zweistündiges Meetup für Python-Anfänger und fortgeschrittene Programmierer. Für all seine wertvollen Tipps bei der Entwicklung des Scrapers möchte ich mich herzlich bei ihm bedanken!

Ein besonderer Dank gilt auch allen (wechselnden) Teilnehmer der Meetup-Gruppe, welche immer hilfsbereit Auskunft gaben. Hervorheben möchte ich  insbesondere Lars Beutler. Ebenfalls möchte ich mich bei meinem Kollegen Timo Grossenbacher von SRF Data für die wertvollen Inputs bedanken.
