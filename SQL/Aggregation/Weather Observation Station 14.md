## Weather Observation Station 14

Url: [weather-observation-station-14](https://www.hackerrank.com/challenges/weather-observation-station-14/ "weather-observation-station-14")


Query the greatest value of the Northern Latitudes (LAT_N) from **STATION** that is less than 137.2345. Truncate your answer to 4 decimal places.

**Input Format**

The STATION table is described as follows:

[![WOS_14](https://s3.amazonaws.com/hr-challenge-images/9336/1449345840-5f0a551030-Station.jpg "WOS_14")](13-Station "WOS_14")

where LAT_N is the northern latitude and LONG_W is the western longitude.

**Solution** Oracle SQL

    SELECT  TRUNC(MAX(LAT_N), 4)
    FROM    STATION
    WHERE   LAT_N < 137.2345;
