# SQL-DAY-1-HW-CTRL-ALT-ELITE-82-JAYDEN-SZAKMARY

-- QUESTION 1 ANS: 2
SELECT  *
FROM actor
WHERE last_name = 'Wahlberg';
-- QUESTION 2 ANS: 5607
SELECT COUNT(AMOUNT) 
FROM payment
WHERE amount BETWEEN 3.99  aND 5.99;
-- QUESTION 3 ANS:
SELECT film_id , COUNT(*)
FROM inventory
GROUP BY film_id;
-- QUESTION 4 ANS: NONE
SELECT last_name 
FROM customer
WHERE last_name = 'William';
-- QUESTION 5 ANS: STAFF_ID 2 
SELECT staff_id , COUNT(*) 
FROM payment
GROUP BY staff_id;
--QUESTION 6 ANS: 378
SELECT district , COUNT(*)
FROM address
GROUP BY district;
-- QUESTION 7 ANS: 508
SELECT film_id , COUNT(*)
FROM film_actor
GROUP BY film_id;
-- QUESTION 8 ANS: none
SELECT store_id
FROM customer
WHERE last_name = '%es' and store_id = 1;
-- QUESTION 9 ANS:
SELECT amount
FROM payment
WHERE customer_id BETWEEN 380 AND 430
GROUP BY amount
HAVING COUNT(RENTAL_ID) > 250;
--QUESTION 10 ANS:5 AND PG-13
SELECT COUNT( DISTINCT rating)
FROM film;
SELECT rating , COUNT(*)
FROM film
GROUP BY rating
