##  SQL Questions
### Question 1: How many cities in the US using Count function?
   * SELECT COUNT(CountryCode) FROM city WHERE CountryCode = 'USA';

   * Answer is 274

### Question 2: Find out the Population and Life expectancy of Argentina
   * SELECT LifeExpectancy FROM country WHERE Name='Argentina';
     SELECT Population FROM country WHERE Name='Argentina';

   * Life Expectancy : 75.1 , Population : 37032000

### Question 3: Using IS NOT NULL, ORDER BY, LIMIT, what country has the highest life expectancy
   * SELECT Name FROM country WHERE LifeExpectancy is NOT NULL ORDER BY LifeExpectancy desc limit 1;

   * Answer is Andorra at 83.5%

### Question 4: Using JOIN … ON, what is the capital of Spain (ESP)?
   * SELECT y.id AS 'City ID', y.name AS 'Capital City', y.countrycode AS 'Country/Region', y.Population
     FROM city y INNER JOIN country c ON c.capital = y.id WHERE id LIKE '653';
    
    * Answer is Madrid, 653 found via previous query.

### Question 5: Using JOIN … ON, list all the languages spoken in the 'Southeast Asia' region.
   * SELECT l.language, c.code, c.region FROM countrylanguage l 
     LEFT JOIN country c ON c.code = l.countrycode WHERE c.region LIKE '%east Asia';

    * Answer is 65 rows, so 65 languages within the SEA region.
### Question 6: SELECT 25 Cities around the world that start with the letter F in a single Query
   * SELECT Name, CountryCode FROM city WHERE Name LIKE 'F%';

### Question 8: Using IS NOT NULL, ORDER BY, LIMIT, what country has the lowest life expectancy?
   * SELECT Name FROM country WHERE LifeExpectancy is NOT NULL ORDER BY LifeExpectancy limit 1;
   
    * Answer is Zambia at 37.2%

### Question 9: Using Aggregate find the total number of countries in the database
   * SELECT COUNT(Code) FROM country;
   
    * Answer is 239

### Question 10: What are the top 10 countries with the highest population
   * SELECT * FROM country ORDER BY POPULATION DESC LIMIT 10;
    * Answer is 1. China, 2. India, 3. United States, 4. Indonesia, 5. Brazil
      6. Pakistan, 7. Russian Federation, 8. Balngladesh, 9. Japan, 10. Nigeria 

### Question 11: List the top 5 cities by population in Japan
   * SELECT * FROM city WHERE CountryCode LIKE 'JPN' ORDER BY Population DESC LIMIT 5;

    * Answers are 1. Tokyo, 2. Yokohama, 3. Osaka, 4. Nagoya, 5. Sapporo

### Question 12: List the names and country codes of every country which has Elizabeth II as it's     head of state.

   * SELECT Code, Name, HeadOfState FROM country WHERE HeadOfState LIKE '%lisabeth %';

    * Answer is: 35 Rows in set,
	 +------+----------------------------------------------+--------------+
	| Code | Name                                         | HeadOfState  |
	+------+----------------------------------------------+--------------+
	| AIA  | Anguilla                                     | Elisabeth II |
	| ATG  | Antigua and Barbuda                          | Elisabeth II |
	| AUS  | Australia                                    | Elisabeth II |
	| BHS  | Bahamas                                      | Elisabeth II |
	| BLZ  | Belize                                       | Elisabeth II |
	| BMU  | Bermuda                                      | Elisabeth II |
	| BRB  | Barbados                                     | Elisabeth II |
	| CAN  | Canada                                       | Elisabeth II |
	| CCK  | Cocos (Keeling) Islands                      | Elisabeth II |
	| COK  | Cook Islands                                 | Elisabeth II |
	| CXR  | Christmas Island                             | Elisabeth II |
	| CYM  | Cayman Islands                               | Elisabeth II |
	| FLK  | Falkland Islands                             | Elisabeth II |
	| GBR  | United Kingdom                               | Elisabeth II |
	| GIB  | Gibraltar                                    | Elisabeth II |
	| GRD  | Grenada                                      | Elisabeth II |
	| HMD  | Heard Island and McDonald Islands            | Elisabeth II |
	| IOT  | British Indian Ocean Territory               | Elisabeth II |
	| JAM  | Jamaica                                      | Elisabeth II |
	| KNA  | Saint Kitts and Nevis                        | Elisabeth II |
	| LCA  | Saint Lucia                                  | Elisabeth II |
	| MSR  | Montserrat                                   | Elisabeth II |
	| NFK  | Norfolk Island                               | Elisabeth II |
	| NIU  | Niue                                         | Elisabeth II |
	| NZL  | New Zealand                                  | Elisabeth II |
	| PCN  | Pitcairn                                     | Elisabeth II |
	| PNG  | Papua New Guinea                             | Elisabeth II |
	| SGS  | South Georgia and the South Sandwich Islands | Elisabeth II |
	| SHN  | Saint Helena                                 | Elisabeth II |
	| SLB  | Solomon Islands                              | Elisabeth II |
	| TCA  | Turks and Caicos Islands                     | Elisabeth II |
	| TKL  | Tokelau                                      | Elisabeth II |
	| TUV  | Tuvalu                                       | Elisabeth II |
	| VCT  | Saint Vincent and the Grenadines             | Elisabeth II |
	| VGB  | Virgin Islands, British                      | Elisabeth II |
	+------+----------------------------------------------+--------------+

### Question 13: List the top 10 countries which have the smallest population-to-area ratio.

   * SELECT Name, Population / SurfaceArea AS 'PopDensity' FROM country ORDER BY PopDensity LIMIT 10;

    * Answer is 10 rows,
    	+----------------------------------------------+------------+
	| Name                                         | PopDensity |
	+----------------------------------------------+------------+
	| Antarctica                                   |   0.000000 |
	| Bouvet Island                                |   0.000000 |
	| South Georgia and the South Sandwich Islands |   0.000000 |
	| British Indian Ocean Territory               |   0.000000 |
	| Heard Island and McDonald Islands            |   0.000000 |
	| United States Minor Outlying Islands         |   0.000000 |
	| French Southern territories                  |   0.000000 |
	| Greenland                                    |   0.025853 |
	| Svalbard and Jan Mayen                       |   0.051264 |
	| Falkland Islands                             |   0.164298 |
	+----------------------------------------------+------------+

### Question 14: List every unique world language, according to the World database.

### Question 15: What are the top 10 richest countries by GDP?

### Question 16: What are the top 10 largest countries by surface area?

### Question 17: List every country where over 50% of its population can speak French

### Question 18: Which country has the worst life expectancy? (Lowest)

### Question 19: What is the most common government form?

### Question 20: How many countries have gained independance since records began?
