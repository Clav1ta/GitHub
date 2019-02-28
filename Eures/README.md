# Was für Fachkräfte suchen (Schweizer) Firmen im Ausland? 

Vorliegendes Datenprojekt ist im Rahmen des CAS Datenjournalismus 18-19 an der Schweizer Journalistenschule MAZ in Luzern entstanden (http://www.maz.ch/studiengaenge/journalismus-weiterbildung/cas-datenjournalismus/) und wurde am 28.Februar 2019 eingereicht.


### These
Heute sind viele spezialisierte Fachkräfte oft nur noch im Ausland zu finden. Das europäische Portal zur beruflichen Mobilität EURES (https://ec.europa.eu/eures/public/de/homepage) ist ein Netzwerk für Anstellungen innerhalb der EU. Die Plattform zeigt offene Stellen in 31 europäischen Ländern an, darunter der Schweiz. Wer ein Jobinserat publizieren will muss sich registrieren ( https://ec.europa.eu/eures/public/de/employers). Es ist deshalb naheliegend, dass vor allem Firmen auf EURES Stellen ausschreiben, welche Mühe haben die Stelle mit Inländern zu besetzen. Deshalb könnte Eures eine spannende Plattform sein, um herauszufinden, für welche Berufe Schweizer und EU Firmen im EU-Raum auf Mitarbeitersuche gehen. In einem zweiten Schritt lässt sich überprüfen, ob in den gesuchten Berufen tatsächlich im jeweiligen Land ein Fachkräftemangel herrscht (zb gemessen an der Erwerbslosenquote und der Anzahl Erwerbslosen).


### Ziel
Ziel ist ein Tool zu bauen, mit welchem man in Echtzeit abfragen kann, welche Fachkräfte Schweizer und EU Firmen im Ausland suchen.


### Methodik und Vorgehen
Im Kurs  haben wir verschiedene Methoden der Datenbeschaffung kennengelernt: Scrapen mit API, Beautiful Soup und Silenium. Ich will mit vorliegender Arbeit eine weitere Methode kennenlernen und vertiefen: Scrapen mittels POST-Requests. Diese Methode eignet sich insbesondere für dynamische Webseiten und vereinfacht das scrapen. Der POST-Request fordert die Daten im Json-Format an. Mittels Python und dem Modul json lässt sich die Json-Struktur einfach in Python-Dictionarys umwandlen und als csv-Datei abspeichern.

In einem ersten Schritt soll ein Scraper für die Jobinserate von Schweizer Firmen auf EURES entwickelt werden. Gelingt das lässt sich darauf aufbauend ein Scraper für die ganze EURES-Plattform entwickeln.


### Geschätzter Arbeitsaufwand
**TAG 1:** Auslesen der Jobinserate von Schweizer Firmen      
**Tag 2:** Datensatz klassifieren       
**Tag 3:** Visualisierung der Daten          
**Tag 4:** Skizze eines Scrapers für die ganze Plattform    
**Tag 5:** Dokumentation und Storyskizze    
  
Der tatsächliche Zeitaufwand ist unter `Zeitprotokoll.csv` protokolliert. Vorallem die Entwicklung des Scrapers für die Schweizer Firmen und die Klassifizierung der Daten dauerte doppelt so lange wie erwartet.  


### Entwicklung Scraper
Die Jobsuchplattform EURES bietet für Private keine APIs. Die Datenbank muss somit automatisiert ausgelesen (gescrapt) werden um einen Datensatz zu erstellen.

Im Ordner `EURES_CH` sind fünf Jupyter Notebooks mit dem entwickelten Programmiercode sowie der Datensatz und die Visualisierungen abgelegt:

`1_EURES_CH_Entwicklung_Scraper`: In diesem Notebook wird die Webseite analysiert und ein Scraper entwickelt.  
`2_EURES_CH_Scraper`: In diesem Notebook ist der entwickelte Scraper ohne Kommentar abgelegt.  
`3_EURES_CH_Daten_klassifizieren`: In diesem Notebook werden die Daten klassifiziert.  
`4_EURES_CH_Pandas_Plotten`: In diesem Notebook werden die Daten visualisiert.  
`5_EURES_CH_Weitere_Visualisierungen`: In diesem Notebook werden Zahlen des BFS für eine Stroyskizze visualisiert.   


### Ergebnis
Eine Skizze zu einer möglichen journalistischen Story mit den gescrapten Daten findet sich im Dokument `ARTIKEL_CH-Firmen_suchen_Handwerker.pdf`.   


### Skalierung
Der entwickelte Srcaper kann mit nur einer leichten Abänderung dazu genutzt werden die ganze Jobsuchplattform auszulesen. Eine Möglichkeit wird im Ordner `EURES_Total` aufgezeigt. Viele Jobsuchplattformen schicken bei einer Suchanfrage einen Post-Request ab. Die hier erarbeite Methode kann auch zum Scrapen von anderen Suchplattformen angewendet werden wie zum Beispiel https://www.job-room.ch.    



### Weitere Informationen
Im Dokument`INTERVIEW_x28_Seco.pdf` findet sich eine Zusammenfassung der Gespräche mit zwei Briefing-Person.


### Knackpunkte des Projektes
**(1)** Die Plattform Eures erhebt keinen Anspruch auf Vollständigkeit. Es gibt Firmen welche im Ausland direkt rekrutieren (zB über ein persönliches Netzwerk, Plattformen wie Linkedin oder einen Stellenvermittler). Der hier entwickelte Scraper ist lediglich ein Indikator. Aber da keine Zahlen zum Thema Rekrutieren nach Berufen im Ausland existieren kann er doch spannende Trends aufzeigen.  
**(2)** Der Curl für den Scraper muss jedes Mal neu gezogen werden, da sich die mitgegebene Session-ID nach einiger Zeit ändert. Dieser Schritt wird im Scraper noch manuell durchgeführt, könnte aber auch automatisiert werden.    
**(3)** Das Resultat würde an Aussagekraft gewinnen, wenn die offenen Stellen statt nur nach den 10 Berufshauptgruppen (jeder Berufsgruppe ist eine einstellige Nummer zugeordnet, oberste Hierarchiestufe nach der Berufsnomenklatura ISCO) auch nach den Berufsklassen (zweistellige Nummer) kategorisiert werden. Allerdings, bei rund 7000 offenen Stellen in der Schweiz ist die Datenbasis für einen zweistelligen Berufscode zu klein. Bei der Entwicklung eines Scrapers für die ganze Plattform würde es sich aber anbieten.     
**(4)** Wird die ganze Plattform gescrapt, müssen ein paar tausend POST-Requests verteilt über eine gewisse Zeit abgeschickt werden. Dazu braucht es einen externen Server. Die Datensätze müssen anschliessend in ein File gepackt werden. Die Datei dürfte ein paar GB umfassen, was für Jupyter Notebook schwierig zum verarbeiten wäre. Die Daten müssten zB in PyCharms oder der Command Line direkt weiterverarbeitet werden.



### Technische Voraussetzungen
Der Scraper, Datenanalyse und Visualisierung sind in Python 3 programmiert. Die benötigten Libraries sind in `Requirements.txt` aufgelistet.


### Über mich
Ich bin Wirtschaftsjournalistin beim Schweizer Radio und Fernsehen SRF. Bei Fragen Mail an claudia.stahel@srf.ch


### Danksagung
An dieser Stelle möchte ich all jenen danken, die durch ihre fachliche Unterstützung zum Gelingen dieser Abschlussarbeit beigetragen haben. Zuerst gebührt mein Dank Ale Rimoldi von der OpenTechSchool Zürich (http://www.opentechschool.org/zurich/). Ale organisiert zwei Mal wöchentlich (jeweils Dienstag und Sonntag Abend) ein zweistündiges Meetup für Python-Anfänger und fortgeschrittene Programmierer. Für all seine wertvollen Tipps möchte ich mich herzlich bei ihm bedanken!

Ein besonderer Dank gilt auch allen (wechselnden) Teilnehmern der Meetup-Gruppe, welche immer hilfsbereit Auskunft gaben. Hervorheben möchte ich insbesondere Lars Beutler. Ebenfalls möchte ich mich bei meinem Kollegen Timo Grossenbacher von SRF Data für den wertvollen Input zum Scrapen der ganzen Plattform bedanken.