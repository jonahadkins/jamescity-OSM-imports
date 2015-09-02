1. spatial join parcels polygons to building polygons
2. spatial join CAD points (addresses) to building polygons
3. delete unnecessary columns  
4. re-project data to epsg:4326; wgs 84 
5. simplify geometry to 0.25
6. remove buildings less than 500 sqft
12. calculate building [ptype2] codes to text -> new [ptype] column (readme)
13. calculate address [type] codes to text -> new [ptype] column (readme)
14. calculate street prefix abbr to long-from
15. calculate road type abbr to long-form (usps suffixes)
16. concatenate street names
17. calculate city = york county
18. calcualte state = virginia
19. spatial join with zipcodes
21. final column clean-up
