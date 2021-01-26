Ending with vowel:--
select distinct city from station where REGEXP_LIKE(LOWER(CITY), '[aeiou]$');
