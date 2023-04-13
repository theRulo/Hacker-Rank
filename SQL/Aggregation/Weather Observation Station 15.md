## Weather Observation Station 15

Url: [weather-observation-station-15](https://www.hackerrank.com/challenges/weather-observation-station-15/ "weather-observation-station-15")

Query the *Western Longitude* (*LONG_W*) for the largest *Northern Latitude* (*LAT_N*) in **STATION** that is less than 137.2345. Round your answer to 4 decimal places.

**Input Format**

The **STATION** table is described as follows:

**Input Format**

The STATION table is described as follows:

[![WOS_14](https://s3.amazonaws.com/hr-challenge-images/9336/1449345840-5f0a551030-Station.jpg "WOS_14")](13-Station "WOS_14")

where LAT_N is the northern latitude and LONG_W is the western longitude.

**Solution 1** Oracle SQL

    SELECT   *
    FROM    (
                SELECT	ROUND(LONG_W, 4)
                FROM	STATION
                WHERE	LAT_N < 137.2345 
                ORDER	BY LAT_N Desc
    )
    WHERE	ROWNUM = 1;


**Solution 2** Oracle SQL

    SELECT  ROUND(LONG_W, 4)
    FROM    STATION
    WHERE   LAT_N IN (
                        SELECT MAX(LAT_N) FROM STATION
                        WHERE LAT_N < 137.2345
                        );

