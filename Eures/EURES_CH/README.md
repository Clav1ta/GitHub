# Data-Scraper für Jobinserate von Schweizer Firmen auf EURES

In diesem Ordner finden sich folgende Files:

### Jupyter Notebooks
In folgenden Notebooks wird der Programmiercode für den Scraper entwickelt und die einzelnen Arbeitsschritte dokumentiert. Die Notebooks der Nummerierung entsprechend durchgehen.

`1_EURES_CH_Entwicklung_Scraper`: In diesem Notebook wird die Webseite analysiert und ein Scraper entwickelt.    
`2_EURES_CH_Scraper`: In diesem Notebook ist der entwickelte Scraper ohne Kommentar abgelegt.    
`3_EURES_CH_Daten_klassifizieren`: In diesem Notebook werden die Daten klassifiziert.    
`4_EURES_CH_Pandas_Plotten`: In diesem Notebook werden die Daten visualisiert.  
`5_EURES_CH_Weitere_Visualisierungen`: In diesem Notebook werden Zahlen des BFS für eine Stroyskizze visualisiert. 


### Daten 
`Data_EURES_CH_17022019.csv`: Dieser Datensatz erhält sämtliche Jobinserate und offene Stellen inklusive allen Informationen welche Schweizer Firmen am 17.2.2019 auf Eures publiziert haben. 
`Data_jobCodes10_17022019.csv`: Dieser Datensatz erhält sämtliche 4831 Jobinserate und 7'670 Stellen vom 17.2.2019. Jedem Jobinserat wurde ein Berufscode nach ISCO (oberste Hirarchiestufe) zugeteilt.
`BFS_ISCO-08_dt.xlsx`: Die Excel-Datei enhält die Berufssystematik International Standard Classification of Occupations (ISCO) in Deutsch.
`BFS_Erwerbslosenquote_Berufsgruppe_ISCO.csv`: Die CSV-Datei enthält die Erwerbslosenquote in der Schweiz gemäss ILO nach Berufsgruppen ISCO-08 als Jahresdurchschnittswert und in Prozent.**ACHTUNG** Die Erwerblosenquote nach Berufsgruppen gibt es nur als Jahresdurchschnittswert und nicht als Quartalswert. Entsprechend müssen auch bei den Erwerbstätigen die Jahreswerte genommen werden (Quelle https://www.bfs.admin.ch/bfs/de/home/statistiken/arbeit-erwerb/erwerbslosigkeit-unterbeschaeftigung-offene-stellen.assetdetail.7206156.html)
`BFS_Erwerbstätige_Erwerbslose_nach_Berufsgruppen_ISCO.csv`: Die CSV-Datei enthält die Zahl der Erwerbstätigen und Erwerbslosen in der Schweiz gemäss ILO nach Berufsgruppen ISCO-08 als Jahresdurchschnittswert und in 1'000. (Quelle: https://www.bfs.admin.ch/bfs/de/home/statistiken/kataloge-datenbanken/tabellen.assetdetail.7206130.html)

### Visualisierung
`EURES_CH_Anzahl_Stellen_nach_Berufen.png`: Der Barchart zeigt die Anzahl gesuchten Fachkräfte nach Berufsgruppen gemäss ISCO.
`BFS_Erwerbslosenquote.png`: Der Barchat zeigt die Erwerbslosenquote in Prozent in der Schweiz für das Jahr 2018 nach Berufsgruppen gemäss ISCO.
`BFS_Erwerbstätige_Erwerbslose.png`: Der Barchat zeigt die Zahl der Erwerbstätigen und Erwerbslosen in der Schweiz für das Jahr 2018 in 1'000 nach Berufsgruppen gemäss ISCO.


