# SQL_Odev5
lcw bootcamp sql 5.ödev reposudur.

-- 1. Film Tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en uzun (length) 5 filmi sıralama
SELECT title, length
FROM film
WHERE title LIKE '%n'
ORDER BY length DESC
LIMIT 5;

-- 2. Film Tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en kısa (length) ikinci (6, 7, 8, 9, 10) 5 filmi sıralama
SELECT title, length
FROM film
WHERE title LIKE '%n'
  AND length IN (6, 7, 8, 9, 10)
ORDER BY length ASC
LIMIT 5;

-- 3. Customer Tablosunda bulunan last_name sütununa göre azalan yapılan sıralamada store_id 1 olmak koşuluyla ilk 4 veriyi sıralama
SELECT last_name, store_id
FROM customer
WHERE store_id = 1
ORDER BY last_name DESC
LIMIT 4;

