Write a query identifying the type of each record in the TRIANGLES table using its three side lengths. Output one of the following statements for each record in the table:

Equilateral: It's a triangle with  sides of equal length.
Isosceles: It's a triangle with  sides of equal length.
Scalene: It's a triangle with  sides of differing lengths.
Not A Triangle: The given values of A, B, and C don't form a triangle.
Input Format

Solution:
select case
when (A+B>C) and ((A=B) and (A=C)) then 'Equilateral'
when (A+B>C) and ((A=B) or (B=C) or (A=C)) then 'Isosceles'
when (A+B>C) and ((A<>B) and (B<>C) and (A<>C)) then 'Scalene'
else 'Not A Triangle' 
end as typeOfTriangle
from triangles
