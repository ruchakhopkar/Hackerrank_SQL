Query the list of CITY names from STATION that either do not start with vowels or do not end with vowels. Your result cannot contain duplicates.

Input Format

The STATION table is described as follows:
<br />

![alt text](https://github.com/ruchakhopkar/Hackerrank_SQL/blob/main/1449345840-5f0a551030-Station.jpg)

<br />
where LAT_N is the northern latitude and LONG_W is the western longitude.

Solution:
select distinct city from station
where not city like '[A,E,I,O,U]%[a,e,i,o,u]';
