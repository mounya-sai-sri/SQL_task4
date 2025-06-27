# SQL_task4
Aggregate functions like sum,avg,max,count on numeric columns:
______________________________________________________________
SELECT SUM(user_id) AS total_quantity FROM Users;
SELECT AVG(category_id) AS average_ategories FROM BookCategories; 
SELECT MAX(cost) AS max_cost FROM Books;  
SELECT SUM((book_id-100) * cost) AS expenditure FROM Books; 
SELECT COUNT(user_id) AS no_of_users FROM Users;  

GroupBy column using on IssuedBooks table:
__________________________________________
SELECT 
  user_id,
  COUNT(book_id) AS total_books_issued
FROM IssuedBooks
GROUP BY user_id; 

Using Having on Books table:
____________________________
SELECT 
  publisher,
  SUM(cost) AS total_cost
FROM Books
GROUP BY publisher
HAVING SUM(cost) > 5000;
