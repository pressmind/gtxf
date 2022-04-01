
#gtxf-final-offer-v1

### Beispiel
````json
{
  "format": "gtxf-final-offer-v1",
  "language": "DE",
  "product-type": "P",
  "id": "2106607",
  "code": "Aktiv-S22-006",
  "active": true,
  "valid": {},
  "name": "Rügen-Stralsund Radreise",
  "url": "https://xxxx.de//?id=2106607",
  "teaser": {},
  "images": [],
  "attributes": [],
  "descriptions": [],
  "locations": [],
  "links": [],
  "services": {},
  "offers": []
}
````

## Objektbeschreibung gtxf-final-offer-v1
| Property| Type | Beschreibung |   
|---|---|---| 
|id|string | eindeutige ID|
|code|string | Artikelnummer bzw. sprechender Reisecode des Veranstalters|
|format|enum('gtxf-final-offer-v1') | |
|language|string | ISO-639-1, z.B. DE, EN oder FR|
|product-type|string | |
|active|boolean | Status des Reise, wenn true dann ist das Produkt frei für die Vermarktung |
|valid|[DateRange](#DateRange) | In Kombination mit active, der Gültikeitszeitraum für die Vermarktungsfreigabe |
|name|string | interner Produktname, sollte nicht veröffentlicht werden|
|url|string | URL zur Website. Die URL muss einen Link zur Buchung des Produktes enthalten|
|teaser|[Teaser](#Teaser) | Kurzversion des Produktes, z.B. für die Ausgabe in Suchergebnissen|
|images|[Image[]](#Image) | Bilder des Produktes, alle Bilder müssen die Rechte für die Veröffentlichtung im Ausgabekanal haben. Die ist im Einzelfall zu prüfen|
|attributes|[Attribute[]](#Attribute) | variable Liste an Produkteigenschaften, z.B. Zielgebiet, Reisearten usw.|
|descriptions|[Description[]](#Description) | Beschreibungsblöcke, die Blöcke müssen in Lesereihenfolge aufgebaut sein.|
|locations|string | Liste an Orten bzw. Geopunkten die in dieser Reise besucht werden. |
|links|string | Links, z.B. auch Videos |
|services|[Services](#Services) | Leistungen, bzw. Inklusivleistungen|
|offers|[Offer[]](#Offer) | die buchbaren Angebote bzw. Reisetermine |



Vollständiges Beispiel:
[example-gtxf-final-offer-v1.json](example-gtxf-final-offer-v1.json)


## DateRange
| Property| Type | Beschreibung |   
|---|---|---|
|from|DateTime | |
|to|DateTime | |

## Image
| Property| Type | Beschreibung |   
|---|---|---|
|url|string | URl zu Bild. Das Bild darf von dieser URL aus niemals produktiv eingebinden werden. Es ist zu cachen.|
|caption|string | Bildunterschrift|
|copyright|string | Copyright |

## Teaser
| Property| Type | Beschreibung |   
|---|---|---|
|title|string | |
|content|string ||
|images|[Image[]](#Image) | |

#Attribute
| Property| Type | Beschreibung |   
|---|---|---|
|name|string | |
|items|[AttributeItem[]](#AttributeItem) | |


## AttributeItem
| Property| Type | Beschreibung |   
|---|---|---|
|id|string | |
|name|string | |
|code|string | |
|childs|[AttributeItem[]](#AttributeItem)| |

## Description
| Property| Type | Beschreibung |   
|---|---|---|
|name|string | Bezeichner des Beschreibungblocks|
|content|string | Inhalt des Beschreibungsblocks als HTML, [siehe HTML Markup](#HTML Markup) |

## Services
| Property| Type | Beschreibung |   
|---|---|---|
|included|string | Inkludierte Leistungen als HTML, [siehe HTML Markup](#HTML Markup)|

##Offer
| Property| Type | Beschreibung |   
|---|---|---|
|departure|DateTime | Anreisedatum|
|return|DateTime | Rückreisedatum|
|transport|[Transport](#Transport) | Transportart, z.B. Busreise|
|room|[Room](#Room) | Zimmerleistung samt Verpflegugung des Angebotes|
|price|string | Brutto-Endpreis |
|booking|[Booking](#Booking) |Sammlung der Leistungscode welche zur Buchung des Angebotes benötigt werden.|


## Room
| Property| Type | Beschreibung |   
|---|---|---| 
|occupancy|int | Belegung|
|board|string | Verpflegung, z.B. "Vollpension"|
|label|string | Zimmer, z.B. "Doppelzimmer mit Meerbliock" |

## Transport
| Property| Type | Beschreibung |   
|---|---|---| 
|type|enum('BUS', 'PKW', 'FLIGHT') | Die Transportart |

## Booking
| Property| Type | Beschreibung |   
|---|---|---|
|key|string | Variabler Key zur Identifizierung der Leistungart|
|id|string | optional ID |
|code|string | Leistungscode|


## HTML Markup
Folgendes HTML Markup ist zulässig: <br>
``<span> <p> <br> <i> <ul> <li> <b> <strong> <table> <tr> <th> <td>`` sowie innherlab der Elemente das Attribut ``class``
