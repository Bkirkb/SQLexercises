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

### Question 8: Using IS NOT NULL, ORDER BY, LIMIT, what country has the lowest life expectancy?
   * SELECT Name FROM country WHERE LifeExpectancy is NOT NULL ORDER BY LifeExpectancy limit 1;
   
   * Answer is Zambia at 37.2%
