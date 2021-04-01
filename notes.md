# Data Modeling Notes

## Requirements

A client has hired you to build an API for managing `zoos` and the `animals` kept at each `zoo`. The API will be used for `zoos` in the _United States of America_, no need to worry about addresses in other countries.

For the `zoos` the client wants to record:

- name.
- address.

For the `animals` the client wants to record:

- name.
- species.
- list of all the zoos where they have resided.

Determine the database tables necessary to track this information.
Label any relationships between table.


## Remember the principles of good data modeling, and the tennets of Third Normal Form (which is desireable, but not always appropriate or achievable):

* Identify entities that should become tables (look for nouns in requirements
  descriptions.)
* Identify entities that should be properties of records within those tables.
* Identify relationships between the tables.
    - One-to-one (```1:1```) - a record in Table A refers to 0 or 1 records in Table
      B, and a record in Table B is referred to by 0 or 1 records in Table A.
    - One-to-many (```1:*```) - most common type. Foreign key fields are defined in
      the "many" table.
    - Many-to-many (```*:*```) - usually implemented using a "bridge" table (also
      called an "associative" table) - a third table that contains records that
      identify the two records in the related tables that are related. Using
      JOIN statements, you can retrieve any combination of records you need. 


See https://support.microsoft.com/en-us/help/283878/description-of-the-database-normalization-basics

### From the TK:

* Each record has a primary key.
* No fields are repeated.
* All fields relate directly to the key data.
* Each field entry contains a single data point.
* There are no redundant entries.

### From the MS site (for Third Normal Form, a.k.a. 3NF):

* Eliminate repeating groups in individual tables.
* Create a separate table for each set of related data.
* Identify each set of related data with a primary key.
* Create separate tables for sets of values that apply to multiple records.
* Relate these tables with a foreign key.
* Eliminate fields that do not depend on the key.