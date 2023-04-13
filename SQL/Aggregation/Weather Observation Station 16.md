## Weather Observation Station 16

Url: [weather-observation-station-16](https://www.hackerrank.com/challenges/weather-observation-station-16/ "weather-observation-station-16")

Query the smallest *Northern Latitude* (*LAT_N*) from **STATION** that is greater than 38.7780. Round your answer to 4 decimal places.

**Input Format**

The **STATION** table is described as follows:

[![WOS_14](https://s3.amazonaws.com/hr-challenge-images/9336/1449345840-5f0a551030-Station.jpg "WOS_14")](13-Station "WOS_14")

where LAT_N is the northern latitude and LONG_W is the western longitude.

**Solution 1** Oracle SQL

    SELECT   *
    FROM    (
                SELECT  ROUND(MIN(LAT_N), 4)
                FROM    STATION
                WHERE   LAT_N > 38.7780
                ORDER BY LAT_N Asc
        )
    WHERE    ROWNUM = 1;


**Solution 2** Oracle SQL

    SELECT  ROUND(LAT_N, 4)
    FROM    STATION
    WHERE   LAT_N IN (
                        SELECT MIN(LAT_N) FROM STATION
                        WHERE LAT_N > 38.7780
                        );

