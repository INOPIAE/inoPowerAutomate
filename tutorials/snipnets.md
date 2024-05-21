# Code-Schnipzel

## Formatieren von Datumsausgaben

Zur Formatierung von Dateumsausgaben wird die Funktion 
`formatDateTime(Varibale,Formatierungsmuster)` verwendet.

![Screenshot formatDateTime](/sources/formatDateTime.png)

Im Screenshot wird das Element Ende des Schrittes Wenn ein Element erstellt wird im deutschen Datumsformat TT.MM.JJJJ ausgegeben.

`formatDateTime(triggerBody()?['Ende'],'dd.MM.yyyy')`

Für fas Datumsformat muss der englische Syntax mit genutzt werden:
* d - klein geschrieben für den Tag
* M - **groß** geschrieben für den Monat
* y - klein geschrieben für das Jahr

## Prüfen auf leere Eingaben

Zur Prüfen ob eine Variable oder Ausgabe leer ist wird die Funktion `empty(Variable)` innerhalb einer Bedingung als Prüfwert verwendet.

![Screenshot empty](/sources/empty.png)

Das Ergebnis der Prüfung wird dann mit der Funktion `true` oder `false` verglichen.

![Screenshot Bedingung mit Funktion empty](/sources/emptyCondition.png)

