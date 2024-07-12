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
Now our team get to retrieve login attempts outside of Mexico, adn we need to find this information. So to this we will use the  command `SELECT * FROM log_in_attempts WHERE X country LIKE 'MEX%' 

## Retrieve employees in Marketing
[Add content here.]

## Retrieve employees in Finance or Sales
[Add content here.]

## Retrieve all employees not in IT
[Add content here.]

## Summary
[Add content here.]
