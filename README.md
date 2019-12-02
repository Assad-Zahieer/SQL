# SQL
* Common query language for relational databases
## Overview
* **RDBMS** - Relational database management system
## Normalisation
* Used to:
  * Reduce duplicate data
  * Simplify queries
  * Reduce data modification issue
* 1st normal form (1NF) each record column only has one value
  * No arrays
  * Potential solution = split arrays into multiple columns
* 2nd normal form (2NF)
  * 1NF satisfied
  * No partial dependency of (non-prime) column on primary
  * Potential solution split partial dependent column into new table
  * e.g. https://en.wikipedia.org/wiki/Second_normal_form
* 3rd normal from (3NF)
  * Satisfy both 1NF and 2NF
  * Every none-prime attribute should depend on primary key
  * none-prime should not depend on none-prime
  * e.g. student-id, name, DOB, Street, City, Postal-code
  * Student-id = primary key but Street and City depend on Postal-code
  * Create two tables - T1 = student-id (p key), name, dob, postal-code (foreign key)
  * T2 = postal-code (p key), Street, City
## Query Categories
* Data definition language (DDL)
 * Deals with schemas (DB and tables)
 * CREATE, SHOW (or DESCRIBE), ALTER, DROP
* Data manipulation language (DML)
 * SELECT, INSERT, UPDATE, DELETE
* Data control language (DCL)
 * Used for permissions
 * GRANT, REVOKE
* Transction control language (TCL)
 * Deals with transactions within a DB
 * COMMIT, ROLLBACK, SAVEPOINT
