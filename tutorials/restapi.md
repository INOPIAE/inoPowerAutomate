# REST API

Erstellen eines API Abrufes am Beispiel des Abrufes der aktuellen Wetterdaten von openweather.org 
[https://home.openweathermap.org/](https://home.openweathermap.org/)

Dort muss zunächst ein Account angelegt werden, der aber für die Basisfuntktionen kostenfrei ist.

Die Dokumentation der genutzten API findet sich unter [https://openweathermap.org/current](https://openweathermap.org/current).

Der fertige manuelle Flow sieht so aus:

![Screenshot API Flow](/sources/api_flow.png)

Der entscheidende Schritt findet sich bei HTTP:

![Screenshot Flow](/sources/api_weather.png)

Der allgemeine Abruf kann durch diese URL erfolgen:
`https://api.openweathermap.org/data/2.5/weather?lat=44.34&lon=10.99&appid={API key}`

Dieser wird dann wie im Bild oben umgesetzt und enthält diese Angaben. Die Parameter in der URL werden durch die Einträge bei Queries gefüllt.

* URI - enthält die Basisadresse 
* Method - muss in diesem Fall GET sein
* appid - ist der Key, der in openweathermap.org hinterlegt ist.
* lat - ist der Breitengrad des Ortes für die Vorhersage
* lon- ist der Längengrad des Ortes für die Vorhersage
* units - steuert, welche Temperaturskala verwendet wird. metric gibt ° C zurück.

Der fertige Flow steht auch in den Samples zum Download zur Verfügung [WetterDemo.zip](/samples/WetterDemo.zip).

Im importierten Flow müssen die Einträge der Parameter so wie die Angaben zum Sharepoint für 'Datei erstellen' angepasst werden.
