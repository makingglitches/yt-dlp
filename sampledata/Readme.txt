As discovered previously years and years and year ago leading to an argument between myself and some guy who supposedly allowed himself to be killd
(TikTok also later did remove some of these fields as well) for whatever stupid reason.

I elected to add two fields to the output, which directly mined the data provided by the site in the rehydratedata section.

The change I suggested to clean the json by removin None fields apparently took.

You wouldn't be able to tell this because they erased me from its history.

Anyway, location, pointOfInterest and contentLocation will not exist if there is no data.

Otherwise there are differences as below.

The code provided does indeed match against a geoname id from the geonames website.

However the Name field is either an arbitrary word or business name, or the most granular level of geotagging eg the town name.
but seemingly not the address.

Note the omission of certain components when differing information is provided.
The only way to keep easily parseable consistency 
is to use 'Name' in conjunction with the 'CityCode' field with the pointofInterest structure.

1st Sample:

"contentLocation": {
    "addressCountry": "",
    "addressLocality": "Youngstown",
    "addressRegion": "",
    "streetAddress": "SUBWAY, 210 W Rayen Ave, Youngstown, United States"
  },

  "pointOfInterest": {
    "name": "SUBWAY",
    "address": "210 W Rayen Ave, Youngstown, United States",
    "city": "Youngstown",
    "province": "",
    "country": "",
    "id": "20319181075334540",
    "fatherPoiId": "",
    "fatherPoiName": "Youngstown",
    "type": 0,
    "category": "Food and Drink",
    "cityCode": "5177568",
    "countryCode": "6252001",
    "ttTypeCode": "05a2a8",
    "typeCode": "",
    "ttTypeNameTiny": "Fast Food Restaurant",
    "ttTypeNameMedium": "Restaurant",
    "ttTypeNameSuper": "Food and Drink"
  },

2nd Sample:

"contentLocation": {
    "addressCountry": "",
    "addressLocality": "",
    "addressRegion": "",
    "streetAddress": "Youngstown, Mahoning County, Ohio, United States"
  },
  "pointOfInterest": {
    "name": "Youngstown",
    "address": "Mahoning County, Ohio, United States",
    "city": "",
    "province": "",
    "country": "",
    "id": "22535865246202332",
    "fatherPoiId": "",
    "fatherPoiName": "",
    "type": 0,
    "category": "Place and Address",
    "cityCode": "5177568",
    "countryCode": "6252001",
    "ttTypeCode": "19a3a0",
    "typeCode": "",
    "ttTypeNameTiny": "City",
    "ttTypeNameMedium": "Places",
    "ttTypeNameSuper": "Place and Address"
  },


3rd Sample:


"contentLocation": {
    "addressCountry": "",
    "addressLocality": "Nago",
    "addressRegion": "",
    "streetAddress": "Camp Schwab, Okinawa, Japan"
  },
  "pointOfInterest": {
    "name": "Camp Schwab",
    "address": "Okinawa, Japan",
    "city": "Nago",
    "province": "",
    "country": "",
    "id": "20442395496014672",
    "fatherPoiId": "",
    "fatherPoiName": "Nago",
    "type": 0,
    "category": "Food and Drink",
    "cityCode": "1856068",
    "countryCode": "1861060",
    "ttTypeCode": "05a2a5",
    "typeCode": "",
    "ttTypeNameTiny": "Cafeteria",
    "ttTypeNameMedium": "Restaurant",
    "ttTypeNameSuper": "Food and Drink"
  },


Anyway this little shit even borrows a name I created heh.