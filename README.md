# ps5-scrapper-api-sort-of
 
## JSON model example

``` 
{
  "country" : "fr-fast",
  "country_name" : "France",
  "found" : "MAYBE SOMETHING HERE! GO AND CHECK!!!",
  "name" : "Auchan - Standard",
  "timestamp" : 1611133806446,
  "type" : "standard",
  "url" : "https://www.currys.co.uk/gbuk/gaming/console-gaming/consoles/sony-playstation-5-825-gb-10203370-pdt.html"
}

```

## Description

`country` is associated to the country flag and country listing, use `fr-fast` and `fr-accessories` to list separately console OR accessories.
`found` one of : `TIMEOUT` or `MAYBE SOMETHING HERE! GO AND CHECK!!!` (I know it's bad...) or `NO STOCK`
`timestamp` date and time at nanosecond resolution in UTC Epoch time : 13 digits ex: `1611133806446`
`type` of product `standard`, `digital`, `bundle`. Future reference to a logo to put on the app and later for notification filtering.

## Firebase

Login as the user transmitted and update reference named ps5 with following key structure

reference Key: [country] - [name]
Object: 
``` 
{
  "country" : "fr-fast",
  "country_name" : "France",
  "found" : "MAYBE SOMETHING HERE! GO AND CHECK!!!",
  "name" : "Auchan - Standard",
  "timestamp" : 1611133806446,
  "type" : "standard",
  "url" : "https://www.currys.co.uk/gbuk/gaming/console-gaming/consoles/sony-playstation-5-825-gb-10203370-pdt.html"
}

```
