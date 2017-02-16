# googlemaps
Google maps code sample for KML 

* Flat file tab delimited source file with no geo location data: lat/lng 
* Read the address, city state, zip data into a url safe string value
* call the google maps geocode json address url with KEY 
* update the tab delimited file with new goecode lat/lng data coordinates (and zip +4 extensions) 
* Create a marker for address to include on personal maps for the address with notes & data. 


Read the address into a URL friendly string variable and HTTP GET the json-response. 
URL: 
https://maps.googleapis.com/maps/api/geocode/json?address=157+ADELAIDE+AVE+SE,+WARREN+OH+44483&key=YOUR_API_KEY
```
{
   "results" : [
      {
         "address_components" : [
            {
               "long_name" : "157",
               "short_name" : "157",
               "types" : [ "street_number" ]
            },
            {
               "long_name" : "Adelaide Avenue Southeast",
               "short_name" : "Adelaide Ave SE",
               "types" : [ "route" ]
            },
            {
               "long_name" : "Warren",
               "short_name" : "Warren",
               "types" : [ "locality", "political" ]
            },
            {
               "long_name" : "Trumbull County",
               "short_name" : "Trumbull County",
               "types" : [ "administrative_area_level_2", "political" ]
            },
            {
               "long_name" : "Ohio",
               "short_name" : "OH",
               "types" : [ "administrative_area_level_1", "political" ]
            },
            {
               "long_name" : "United States",
               "short_name" : "US",
               "types" : [ "country", "political" ]
            },
            {
               "long_name" : "44483",
               "short_name" : "44483",
               "types" : [ "postal_code" ]
            },
            {
               "long_name" : "6107",
               "short_name" : "6107",
               "types" : [ "postal_code_suffix" ]
            }
         ],
         "formatted_address" : "157 Adelaide Ave SE, Warren, OH 44483, USA",
         "geometry" : {
            "location" : {
               "lat" : 41.235732,
               "lng" : -80.791372
            },
            "location_type" : "ROOFTOP",
            "viewport" : {
               "northeast" : {
                  "lat" : 41.23708098029149,
                  "lng" : -80.79002301970849
               },
               "southwest" : {
                  "lat" : 41.2343830197085,
                  "lng" : -80.79272098029149
               }
            }
         },
         "place_id" : "ChIJm46GGuHfM4gRMmkiNwSL__0",
         "types" : [ "street_address" ]
      }
   ],
   "status" : "OK"
```
