# Code-Schnipzel

## Formatieren von Datumsausgaben

Zur Formatierung von Dateumsausgaben wird die Funktion 
`formatDateTime(Varibale, Formatierungsmuster)` verwendet.

![Screenshot formatDateTime](/sources/formatDateTime.png)

Im Screenshot wird das Element Ende des Schrittes Wenn ein Element erstellt wird im deutschen Datumsformat TT.MM.JJJJ ausgegeben.

`formatDateTime(triggerBody()?['Ende'], 'dd.MM.yyyy')`

Für fas Datumsformat muss der englische Syntax mit genutzt werden:
* d - klein geschrieben für den Tag
* M - **groß** geschrieben für den Monat
* y - klein geschrieben für das Jahr
* h - klein geschrieben für 12 Std Uhrzeit
* H - groß geschrieben für 24 Std Uhrzeit

## Umrechnen von Zeiten

Power Automate arbeitet intern mit UTC Zeit. Auch in dem Connector 'Aktuelle Uhrzeit' wird mit UTC Zeit gearbeitet.

Zur Ausgabe der Aktuellen Uhrzeit in CET muss die Zeit mit entweder mit dem Connector 'Zeitzone konvertieren' oder der Funktion 

`convertTimeZone(timestamp: string, sourceTimeZone: string, destinationTimeZone: string, format?: string)`

Beispiel für die Zeit in Deutschland

`convertTimeZone(utcNow(), 'UTC', 'Romance Standard Time')`

![Screenshot Zeitzone konvertieren](/sources/zeitkonvertieren.png)

## Prüfen auf leere Eingaben

Zur Prüfen ob eine Variable oder Ausgabe leer ist wird die Funktion `empty(Variable)` innerhalb einer Bedingung als Prüfwert verwendet.

![Screenshot empty](/sources/empty.png)

Das Ergebnis der Prüfung wird dann mit der Funktion `true` oder `false` verglichen.

![Screenshot Bedingung mit Funktion empty](/sources/emptyCondition.png)

## Datei auf Sharepoint beim Anlegen überschreiben

Damit eine Datei im Connector 'Datei erstellen' überschrieben werden kann, muss in den Einstellungen des Connectors bei Networking die 'Segmentierung zulassen' ausgeschaltet werden.

![Screenshot Datei überschreiben](/sources/dateiueberschreiben.png)
