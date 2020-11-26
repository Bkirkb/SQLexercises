##  SQL Questions
### Question 1: How many cities in the US using Count function?
   * SELECT COUNT(CountryCode) FROM city WHERE CountryCode = 'USA';

   * Answer is 274

### Question 2: Find out the Population and Life expectancy of Argentina
   * SELECT LifeExpectancy FROM country WHERE Name='Argentina'
     SELECT Population FROM country WHERE Name='Argentina'

   * Life Expectancy : 75.1 , Population : 37032000

### Question 3: Using IS NOT NULL, ORDER BY, LIMIT, what country has the highest life expectancy
   * SELECT Name FROM country WHERE LifeExpectancy is NOT NULL ORDER BY LifeExpectancy desc limit 1;

   * Answer is Andorra at 83.5%

### Question 4: Using JOIN … ON, what is the capital of Spain (ESP)?


### Question 5: Using JOIN … ON, list all the languages spoken in the 'Southeast Asia' region.

### Question 6: SELECT 25 Cities around the world that start with the letter F in a single Query
   * SELECT Name, CountryCode FROM city WHERE Name LIKE 'F%';

### Question 8: Using IS NOT NULL, ORDER BY, LIMIT, what country has the lowest life expectancy?
   * SELECT Name FROM country WHERE LifeExpectancy is NOT NULL ORDER BY LifeExpectancy limit 1;
   
   * Answer is Zambia at 37.2%

### Question 9: Using Aggregate find the total number of countries in the database
   * SELECT COUNT(Code) FROM country;
   
   * Answer is 239
