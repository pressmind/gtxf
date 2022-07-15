# GTXF
![](logo_300.png)

## Was ist GTXF? 
GTXF steht für Group Travel Exchange Format. 
Ziel ist es, Produktdaten aus der Bus- und Gruppentouristik standardisiert abzubilden.
Daten sollen systemübergreifend les- und austauschbar sein. 

### Subformate
Je nach Bestimmungszweck sind verschiedene Subformate vorgesehen: 

### Format: gtxf-final-offer-v1
Dieses Format ist für die Vermarktung bestimmt. Es enthält eine vollständige Produktbeschreibung einer Reise sowie 
ausmultiplizierte Angebote mit Brutto-Endpreisen. Jedes Angebot ist mit Buchungsparameter markierbar, 
sodass der Aufruf einer Buchungsstrecke möglich ist. 

Es bildet jedoch in der aktuellen Ausprägung keine Detailinformationen wie Zusatzleistungen und Zustiege ab. 
Hiermit wird bewusst die Komplexität zurückgehalten und somit die Integration vereinfacht. 

Das Format standardisiert die Produktstruktur. Attribute wie Reiseart oder Zielgebiete sind nicht zwingend normiert.

#### Links
* [Formatbeschreibung](gtxf-final-offer-v1.md)

* [Beispieldokument](example-gtxf-final-offer-v1.json)

### GTXF Attributes DRAFT
Zur Standardisierung von Produkteigenschaften sind im ersten Schritt Destination und Travel Types normiert worden. 
Ziel ist es, durch standardisierte Produkteigenschaften, im Zielsystem Produktsilos von 
unterschiedlichen Veranstaltern in den entsprechenden Kategorien wie Destinationen und Reisearten bilden zu können.
In weiteren Schritten können diese Eigenschaften verwendet werden um eine Vergleichbarkeit zwischen den Leistungen 
herstellen zu können.

[Details zu den GTXF Attributes](gtxf-attributes-v1.md)

# Repräsentation
Die Daten werden stets im ``JSON Format`` bereitgestellt.

# Kann ich am Projekt mitwirken?
Ja, jeder mit Erfahrung in der Branche kann am Projekt mitwirken.

