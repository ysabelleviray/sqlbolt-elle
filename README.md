SELECT city, population
FROM north_american_cities
WHERE country="Canada";
---------------------------
SELECT city
FROM north_american_cities
WHERE country="United States"
ORDER BY latitude DESC;
---------------------------
SELECT city
FROM north_american_cities
WHERE longitude < -87.6298
ORDER BY longitude;
---------------------------
SELECT city
FROM north_american_cities
WHERE country="Mexico"
ORDER BY population DESC
LIMIT 2;
---------------------------
SELECT city
FROM north_american_cities
WHERE country="United States"
ORDER BY population DESC
LIMIT 2 OFFSET 2;
