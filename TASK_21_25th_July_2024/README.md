SQLBolt
Learn SQL with simple, interactive exercises.

SQL Lesson 1: SELECT queries 101
Exercise 1 — Tasks
1.Find the title of each film
2.Find the director of each film
3.Find the title and director of each film
4.Find the title and year of each film
5.Find all the information about each film
Answers:
--SELECT * FROM movies
--SELECT TITLE FROM MOVIES
--SELECT DIRECTOR FROM MOVIES
--SELECT TITLE,DIRECTOR FROM MOVIES
--SELECT TITLE,YEAR FROM MOVIES
SELECT * FROM MOVIES

SQL Lesson 2: Queries with constraints (Pt. 1)
Exercise 2 — Tasks
1.Find the movie with a row id of 6
2.Find the movies released in the years between 2000 and 2010
3.Find the movies not released in the years between 2000 and 2010
4.Find the first 5 Pixar movies and their release year
Answers:
--SELECT * FROM MOVIES WHERE ID=6
--SELECT * FROM MOVIES WHERE YEAR BETWEEN 2000 AND 2010
--SELECT * FROM MOVIES WHERE YEAR NOT BETWEEN 2000 AND 2010
SELECT * FROM movies WHERE year LIMIT 5

SQL Lesson 3: Queries with constraints (Pt. 2)
Exercise 3 — Tasks
1.Find all the Toy Story movies
2.Find all the movies directed by John Lasseter
3.Find all the movies (and director) not directed by John Lasseter
4.Find all the WALL-* movies
Answers:
--SELECT TITLE FROM MOVIES WHERE TITLE LIKE "%TOY STORY%"
--SELECT * FROM MOVIES WHERE DIRECTOR LIKE "%John Lasseter%"
--SELECT TITLE,DIRECTOR FROM MOVIES WHERE DIRECTOR NOT LIKE "%John Lasseter%"
SELECT TITLE FROM MOVIES WHERE TITLE LIKE "%WALL-%"

SQL Lesson 4: Filtering and sorting Query results
Exercise 4 — Tasks
1.List all directors of Pixar movies (alphabetically), without duplicates
2.List the last four Pixar movies released (ordered from most recent to least)
3.List the first five Pixar movies sorted alphabetically
4.List the next five Pixar movies sorted alphabetically
Answers:
--SELECT DISTINCT DIRECTOR FROM MOVIES ORDER BY DIRECTOR
--SELECT DISTINCT TITLE FROM MOVIES ORDER BY YEAR DESC LIMIT 4
--SELECT TITLE FROM MOVIES ORDER BY TITLE LIMIT 5
SELECT TITLE FROM MOVIES ORDER BY TITLE LIMIT 5 OFFSET 5

SQL Review: Simple SELECT Queries
Review 1 — Tasks
1.List all the Canadian cities and their populations
2.Order all the cities in the United States by their latitude from north to south
3.List all the cities west of Chicago, ordered from west to east
4.List the two largest cities in Mexico (by population)
5.List the third and fourth largest cities (by population) in the United States and their population
Answers:
--SELECT CITY, POPULATION FROM north_american_cities WHERE country = "Canada"
--SELECT CITY FROM north_american_cities WHERE COUNTRY = "United States" ORDER BY latitude DESC
--SELECT CITY FROM north_american_cities WHERE longitude < -87.629798 ORDER BY longitude;
--SELECT CITY FROM north_american_cities WHERE COUNTRY = "Mexico" ORDER BY POPULATION DESC LIMIT 2;
SELECT CITY FROM north_american_cities WHERE COUNTRY = "United States" ORDER BY POPULATION DESC LIMIT 2 OFFSET 2;

SQL Lesson 6: Multi-table queries with JOINs
Exercise 6 — Tasks
1.Find the domestic and international sales for each movie
2.Show the sales numbers for each movie that did better internationally rather than domestically
3.List all the movies by their ratings in descending order
Answers:


































