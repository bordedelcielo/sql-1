-- Christopher's homework problems for week 4 day 1 of Coding Temple.

-- 1. How many actors are there with the last name ‘Wahlberg’?
-- A: 2
SELECT COUNT(*)
FROM actor
WHERE last_name = 'Wahlberg';

-- 2. How many payments were made between $3.99 and $5.99
-- A: 5607
SELECT COUNT(*)
FROM payment
WHERE amount BETWEEN 3.99 AND 5.99;

-- 3. What film does the store have the most of? (search in inventory)
-- A: Multiple instances of films tied at 8 copies. Select film title from film where film id is 193. Etc.
SELECT film_id, COUNT(film_id)
FROM inventory
GROUP BY film_id
ORDER BY COUNT(film_id) DESC;

-- 4. How many customers have the last name ‘William’?
-- A: 0
SELECT COUNT(*)
FROM customer
WHERE last_name = 'William';

-- 5. What store employee (get the id) sold the most rentals?
-- A: staff_id = 1 sold 8040 rentals.
SELECT staff_id, COUNT(rental_id)
FROM rental
GROUP BY staff_id
ORDER BY COUNT(rental_id) DESC;

-- 6. How many different district names are there?
-- A: 378
SELECT COUNT(DISTINCT(district))
FROM address;

-- 7. What film has the most actors in it? (use film_actor table and get film_id)
-- A: film_id 508 has 15 actors in it.
SELECT film_id, COUNT(DISTINCT(actor_id))
FROM film_actor
GROUP BY film_id
ORDER BY COUNT(DISTINCT(actor_ID)) DESC;

-- 8. From store_id 1, how many customers have a last name ending with ‘es’? (use customer table)
-- A: 13 customers in store_id 1 with last name ending in 'es'.
SELECT COUNT(DISTINCT(customer_id))
FROM customer
WHERE store_id = '1' AND last_name LIKE '%es';

-- 9. How many payment amounts (4.99, 5.99, etc.) had a number of rentals above 250 for customers
-- with ids between 380 and 430? (use group by and having > 250)
-- A: 3. The amounts are 0.99, 2.99, 4.99
SELECT amount
FROM payment
WHERE customer_id BETWEEN 380 and 430
GROUP BY amount
HAVING COUNT(rental_id) > 250;

-- 10. Within the film table, how many rating categories are there? And what rating has the most
-- movies total
-- A: There are 5 distinct ratings. PG-13 is the most common rating at 223 film_ids.
SELECT COUNT(DISTINCT(rating))
FROM film;
SELECT COUNT(DISTINCT(film_id)), rating
FROM film
GROUP BY rating
ORDER BY COUNT(DISTINCT(film_id)) DESC;