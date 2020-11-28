## Sakila Excercises

### Question 1: Select all actors from the table
   * SELECT * FROM actor
    * Answer is list of 200 total actors

### Question 2: Find the actor with the first name of 'John'
   * SELECT * FROM actor WHERE first_name LIKE 'John'
    * Answer is John Suvari, ID of 192.
  
### Question 3: Find all actors with the surname 'Neeson'
   * SELECT * FROM actor WHERE last_name LIKE 'Neeson'
    * Answer is Christian Neeson, Jayne Neeson

### Question 4: Find all actors with Id numbers divisible by 10
   * SELECT * FROM actor WHERE actor_id LIKE '%0'
    * Answer is all actors with ID ending in 0, 20 total actors.

### Question 5: What is the description of the movie with ID of 100?
   * SELECT description, name, film_id FROM film WHERE film_id = '100'
    * Answer is "A Beautiful Drama of a Dentist And a Composer who must Battle a Sumo Wrestler in The First Manned Space Station ", title = BROOKLYN DESERT, film_id = 100

### Question 6: Find every movie with a rating of 'R'
   * SELECT COUNT(film_id) FROM film WHERE rating = 'r'
    * Answer is 195 total r rated films, Select * can be used to see the full list

### Question 7: Find every movie except those with a rating of 'R'
   * SELECT COUNT(film_id) FROM film WHERE rating != 'r'
    * Answer is 805 total non-r rated films, Select * can be used to see the full list

### Question 8: Find the 10 shortest movies
   * SELECT length FROM film ORDER BY length LIMIT 10
    * Answer is 46 (5) and 47 (5), List is automatically sorted into ascending order via ORDER BY command

### Question 9: Now return only the movie titles
   * SELECT title FROM film ORDER BY length LIMIT 10
    * Answer is | RIDGEMONT SUBMARINE |
                | IRON MOON           |
                | ALIEN CENTER        |
                | LABYRINTH LEAGUE    |
                | KWAI HOMEWARD       |
                | DOWNHILL ENOUGH     |
                | HALLOWEEN NUTS      |
                | HANOVER GALAXY      |
                | DIVORCE SHINING     |
                | HAWK CHILL 

### Question 10: Find all movies with Deleted Scenes
   * SELECT COUNT(*) FROM film WHERE special_features LIKE 'Deleted_Scenes'
    * Answer is 61 total films with deleted scenes.

### Question 11: Which last names are not repeated?
   * SELECT DISTINCT * last_name FROM table_name
    * Using actors, there are 121 Rows in the set, meaning 121 distinct last names from the 200 total.

### Question 12: Which last names appear more than once?
   * SELECT COUNT(last_name), last_name FROM actor GROUP BY last_name HAVING COUNT(last_name) > 1
    * Answer is 51 Total last names which appear more than once within the actor table

### Question 13: Which actor has appeared in the most films?
   * SELECT actor_id, COUNT(actor_id) AS total_films FROM film_actor GROUP BY actor_id ORDER BY total_films DESC
     Returns actor_id 107 as the top of the list with 42 total films,
     SELECT actor_id, first_name, last_name FROM actor WHERE actor_id = 107
    * Answer is Gina Degeneres

### Question 14: Is 'Academy Dinosaur' available for rent from Store 1?

### Question 15: When is the above due?

### Question 16: What is the average running time of all the films in the database?

### Question 17: What is the average running time of films by category?

### Question 18: How many movies have Robots in them?

### Question 19: Find the movie(s) with the longest runtime

### Question 20: Count how many movies were released in 2010

### Question 21: Find the titles of all horror movies.

### Question 22: Rturn the full name of the staff member - in a column named full_name with the ID of 1

### Question 23: Retrieve all the movies that Fred Costner has appeared in.

### Question 24: Find out which location has the most copies of BUCKET BROTHERHOOD

### Question 25: How many distinct countries are there?

### Question 26: What are the names of all the languages in the database sorted alphabetically?

### Question 27: Return the full names of actors with 'son' in their last name, ordered by their first name.

### Question 28: Create a list of categories and the number of films for each category

### Question 29: Create a list of actors and the number of movies by each actor


