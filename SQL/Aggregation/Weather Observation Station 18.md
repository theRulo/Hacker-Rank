## Weather Observation Station 18

Url: [weather-observation-station-18](https://www.hackerrank.com/challenges/weather-observation-station-18/ "weather-observation-station-18 ")

Consider  and  to be two points on a 2D plane.

  - **a** happens to equal the minimum value in Northern Latitude (LAT_N in STATION).
 - **b** happens to equal the minimum value in Western Longitude (LONG_W in STATION).
 - **c** happens to equal the maximum value in Northern Latitude (LAT_N in STATION).
 - **d** happens to equal the maximum value in Western Longitude (LONG_W in STATION).

Query the Manhattan Distance between points P1 and P2 and round it to a scale of  4 decimal places.


**Input Format**

The **STATION** table is described as follows:

[![WOS_14](https://s3.amazonaws.com/hr-challenge-images/9336/1449345840-5f0a551030-Station.jpg "WOS_14")](13-Station "WOS_14")

where LAT_N is the northern latitude and LONG_W is the western longitude.

**Solution** Oracle SQL

    SELECT  ROUND((ABS(MIN(LAT_N)-MAX(LAT_N))+ABS(MIN(LONG_W)-MAX(LONG_W))), 4)
    FROM    STATION;



