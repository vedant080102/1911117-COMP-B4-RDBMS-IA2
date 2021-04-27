# RDBMS-IA2

### Name: VEDANT SARNOBAT
### Class: SY COMP B4
### Course: COMPUTER
### Faculty name: PRADNYA BHANGALE and VAIBHAV VASANI
### College name: KJ SOMAIYA COLLEGE OF ENGINEERING

***

- ### WHAT IS DONE IN THIS PROJECT:

Aim of the project is to realize the fully homomorphic encryption to a certain extent. By combining the additive and multilpicative homomorphic encryption
Algorithms used here are rsa and paillier homomorphic encryption.

---

- ### IMPORTANT LIBRARIES TO BE INSTALLED:

Libnum
```
  pip install libnum
 ```

---

- ### INSTRUCTIONS:

You can run the code in any IDE
But you need to modify the details (config) for the MySQL database that you would be using.

Database:
```
CREATE database homomor_encyptionDB;
CREATE TABLE `homomor_encyptionDB`.`table1` (
  `col1` INT NOT NULL,
  `col2` INT NOT NULL);

CREATE database plain_text;

CREATE TABLE `plain_text`.`table1` (
  `col1` INT NOT NULL,
  `col2` INT NOT NULL);
```
The MySQL structured procedure used for updating the cipher text in the database:
```
DROP PROCEDURE IF EXISTS updateTable;
delimiter &&

CREATE PROCEDURE updateTable(IN c1 integer, c2 integer, c00 integer, c01 integer)
begin
	UPDATE `homomor_encyptiondb`.`table1`
		SET `col1` = c1,
			`col2` = c2
		WHERE `col1`= c00
			AND `col2` = c01;

end &&

delimiter ;
```

---

- ### WHAT TO DO AFTER RUNNING THE CODE:

  You must input whatever choice you wish from the options provided.
  First of all inserting data would be recommended
  Then there are two other options tha you can choose those are the two queries for which the execution time and functionalities are checked.

***
**THANK YOU!**
