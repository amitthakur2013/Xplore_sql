Ending with vowel:--
select distinct city from station where REGEXP_LIKE(LOWER(CITY), '[aeiou]$');

Does not start and end with vowel
SELECT DISTINCT city
FROM   station
WHERE REGEXP_LIKE(city, '^[^aeiouAEIOU].*[^aeiouAEIOU]$')
