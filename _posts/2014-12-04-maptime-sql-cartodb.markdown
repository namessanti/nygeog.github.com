---
layout: post
title:  "Maptime SQL for CartoDB"
date:   2014-12-04 11:31:10
categories: Maptime CartoDB SQL
---


Jeff F. ( aka [@zingbot](https://twitter.com/zingbot)) gave a solid presentation during the [@MaptimeNYC](http://www.meetup.com/Maptime-NYC/) session last night (2014-12-03). The Maptime was at [CartoDB's](http://cartodb.com/) Williamsburg, Brooklyn office. 

Below are my notes:

## MaptimeNYC's SQL for CartoDB

#### Creating Lines from Points

#### ST_Makeline

	SELECT ST_MakeLine (the_geom_webmercator ORDER BY _order ASC)
	AS the_geom_webmercator, route
	FROM maptimesql_points
	GROUP BY route
	
<iframe width='100%' height='900' frameborder='0' src='https://dms2203.cartodb.com/tables/maptimesql_points/public/map' allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen></iframe>
	
#### ST_Contains (Spatial Join)

	SELECT 
	us_counties.the_geom_webmercator,us_counties.cartodb_id, count(quakes.the_geom)
	AS total
	FROM us_counties JOIN quakes
	ON st_contains(us_counties.the_geom,quakes.the_geom)
	GROUP BY us_counties.cartodb_id
	
#### CDB_LatLng

	SELECT * FROM table 
	ORDER BY the_geom <->
	CDB_LatLng(42.5,-73) LIMIT 10
	
	#In POSTGIS it is the command ST_Point	
	
Check out ST_BUFFER (METERS) search it'll do the DIST or BUFFER in Meters


#### lag()

Access the previous row of data and get value (time, value,number,etc)