# First Normal Form - 1NF

## Rules

-   Each table cell should contain a single atomic value
-   Each record needs to be unique

## How to achieve it

-   Split columns to atomic values
-   If multiple values can be asigned to a record, move them to a new table

# Second Normal Form - 2NF

## Rules

-   A table is in the 2NF if it is in the 1NF and every non-key attribute of the table is depended on the whole (every attribute of the) composite primary key
-   Tables without composite primary key are in the 2NF by default

# Third Normal Form - 3NF

## Rules

-   The table must be in the 2NF
-   3NF applies that every non-prime attribute of the table must be dependent on primary key, meaning, there should no be the case that a non-prime attribute is determined by another non-prime attribute
-   Simply put, every attribute must be dependent on the primary key, if it's not, it must be moved to a a separate table

# Relationship Cardinality

The degree of relationship (also known as cardinality) is the number of occurrences in one entity which are associated to the number of occurrences in another.

There are 3 degrees of relationship:

-   one-to-one (1:1)
-   one-to-many (1:N)
-   many-to-many (N:M)
