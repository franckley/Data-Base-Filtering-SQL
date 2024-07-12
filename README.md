# Data-Base-Filtering-SQL

## Project description
My organisation needs to obtain specific information aobut employees, their machines, and the departments they belong to from the database. In order for the team to investigate potential security issues and to update computers. My responsability is to filter the required information from the database.

## Retrieve after hours failed login attempts
First, we will retrieve information about the failed login attempts that were made after business hours (18:00). We need to execute the command `SELECT *` to search the entire `log_in_attempts` and we will use the boolean value of 0 which is `FALSE` since we are looking for the failed attempts. So we will use the command `SELECT *` to search the entire database.

![Screenshot (105)_proc](https://github.com/user-attachments/assets/98be21da-d1c4-4baf-9c45-1da21f1b934b)

## Retrieve login attempts on specific dates
My team is investigating a suspicious event that occured on `2022-05-09`. We want to retrieve all login attemps that occured on this day `2022-05-09` and the day before `2022-05-08`. Using the `SELECT *` to search the entire database `log_in_attempts` while taking in count `the login_date` column. Also we got to use the commnad operator `OR`to retrieve the failed login attemps on the specified dates.

![Screenshot (106)_proc](https://github.com/user-attachments/assets/f440fd77-cb79-4063-8bfb-66ebb16d852c)
![Screenshot (107)_proc](https://github.com/user-attachments/assets/904da667-203e-4e33-9ba1-d676bb7fdae1)

## Retrieve login attempts outside of Mexico
Now our team get to retrieve login attempts outside of Mexico, and we need to find this information. So to this we will use the  command `SELECT * FROM log_in_attempts WHERE NOT country LIKE MEX%` to which the output of this command will only take in count the countries that are not MEXICO.
![Screenshot (108)_proc](https://github.com/user-attachments/assets/5323e809-1212-4c10-a495-e432fa6db603)
![Screenshot (109)_proc](https://github.com/user-attachments/assets/238dd029-1d3b-4831-986f-377475d36262)

## Retrieve employees in Marketing
Our team is updating employee machines, and we need to obtain the information about employees in the `Marketing` department who are located in all offices in the East building (such as `East-170` or `East-320`). So in order to do that we will have to write down the following command 'SELECT * FROM employees WHERE department = 'Marketing' AND office LIKE 'EAST-%';' which filters the database for all the employees from the Marketing departement working in a East office.
![Screenshot (112)_proc](https://github.com/user-attachments/assets/13e99432-e8c8-474e-9506-45d55e30d4c6)

But since we want to find the ones who are either in  office `East-170` or office `East-320`. We can readjust our command in the following order to do so: `MariaDB [organization]> SELECT *   FROM employees   WHERE department = 'Marketing'   AND (office LIKE 'East-170%' OR office LIKE 'East-320%');`.

![Screenshot (112)_proc](https://github.com/user-attachments/assets/b1a15641-f973-4419-b983-ac2d893988e0)

## Retrieve employees in Finance or Sales
[Add content here.]

## Retrieve all employees not in IT
[Add content here.]

## Summary
[Add content here.]
