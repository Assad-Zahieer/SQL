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
  * Poential solution = split arrays into multiple columns
| Name | Age |
|------|-----|
| Adam | 15  |
| Adam | 17  |
* 2nd normal form (2NF)
  * 1NF satisfied
  * No partial dependency of (non-prime) column on primary
  * Potential solution split partial dependent column into new table
  * e.g. https://en.wikipedia.org/wiki/Second_normal_form
