## Weather Observation Station 19

Url: [weather-observation-station-19](https://www.hackerrank.com/challenges/weather-observation-station-19/ "weather-observation-station-19 ")

Consider P1(a,c) and P2(b,d) to be two points on a 2D plane where (a,b) are the respective minimum and maximum values of Northern Latitude (LAT_N) and (c,d) are the respective minimum and maximum values of Western Longitude (LONG_W) in **STATION**.

Query the Euclidean Distance between points P1 and P2 and format your answer to display 4 decimal digits.



**Input Format**

The **STATION** table is described as follows:

[![WOS_14](https://s3.amazonaws.com/hr-challenge-images/9336/1449345840-5f0a551030-Station.jpg "WOS_14")](13-Station "WOS_14")

where LAT_N is the northern latitude and LONG_W is the western longitude.

**Solution** Oracle SQL

    SELECT  ROUND((ABS(MIN(LAT_N)-MAX(LAT_N))+ABS(MIN(LONG_W)-MAX(LONG_W))), 4)
    FROM    STATION;



