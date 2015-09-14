1. spatial join parcels polygons to building polygons
2. spatial join CAD points (addresses) to building polygons
3. delete unnecessary columns  
4. re-project data to epsg:4326; wgs 84 
5. simplify geometry to 0.25
6. remove buildings less than 500 sqft
7. concatenate & format parcel addresses to OSM address format
8. concatenate & format CAD points to OSM address format
9. delete unnecessary columns
10. remove addresses from shed types


###Building Footprints  
Buildings will be simplified to ```0.25``` using common geometry simplification tools. Attributes from the ```CODE``` column will be mapped to OSM tags:  

| Code  | Type | Count |  Note |
| ------------- | ------------- |------------- |------------- |
| 1  | NULL  | 127  | ---  |
| 2  | Apartment / Townhouse / Condo  | 1431  | Apartments  |
| 3  | Church  | 88  | Church  |
| 4  | Federal / State / Local  | 420  | Will Split By Name If Possible  |
| 5  | Garage / Shed  | 9954  | Will Split By Name If Possible  |
| 6  | HOA (Homeowners Assoc)  | 151  | Need to look into  |
| 7  | Schools  | 29   | School   |
| 8  | Residential  | 21714  | House  |
| 9  | Timeshares  | 224  | Need to look into  |
| 7  | Trailers  | 1353   | Mobile Home   |

###Addresses 
Points were provided as parcel centroids. Will need to run some processes to conflate addresses to building polygons. There are some attributes that will provide additional info:  
```BUSNAME (name of business) : 446 points```  
The ```ex_land_us``` field will provide some further classifications:  

| Code  | Type | Count |  Note |  
| ------------- | ------------- |------------- |------------- |
| 1  | null  | 2838  | --- |
| 2  | Heavy Industrial  | 59 | Industrial  |
| 3  | Historic  | 37  | Historic  |
| 4  | Light Industrial  | 145  | Industrial  |
| 5  | local commercial  | 596  | commercial  |
| 6  | low-dens residential  | 18187  | house  |
| 7  | med-dens residential  | 6240  | Need to look into   |
| 8  | military  | 4  | building  |
| 9  | mixed use  | 661  | Need to look into |
| 10  | neighborhood commercial  | 45 | commercial  |
| 11  | parks and rec  | 95  | govt. building?  |
| 12  | aviation  | 4  | airport bldg  |
| 13  | public/semi public  | 117  | Need to look into  |
| 14  | regional commercial  | 1083  | commercial  |
| 15  | rural residential  | 2092  | residential   |
| 16  | small agriculture  | 243  | farms? |
| 17  | transportation network  | 14  | Need to look into  |
| 18  | utilities  | 76  | Need to look into  |
| 19  | vacant  | 3151  | will not map   |
