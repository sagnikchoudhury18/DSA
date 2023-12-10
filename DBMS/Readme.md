# Intro and Key concepts

### Super Key
    col or set of cols that can uniquely identify a row.

### Candidate Key
    minimal set of cols that can uniquely identify a row.

### Primary Key
    A candidate key is selected to represent a row uniquely.
    
#### Need for Primary Keys
    1. Generally databases stores data in the order of primary keys. If I have multiple primary keys, the database would get confused according to which col the data needs to be ordered.
    2. Sorting is required as it makes searching easy
    3. Outputs the data in order of PK
    4. DB creates an index on PK which helps in the optimization.
    5. The user creating the schema decides the PK.
    6. We can have just one PK in the table but this can be a collection of cols eg: CONSTRAINT pk_PersonID PRIMARY KEY (P_Id,LastName) 
    7. PK in nature is unique and not null.
    
    Note: Suppose we have 2 cols email_id and student_id the PK would be built on student_id as sorting and comparison is easier on integers. Indexes created on integers take up lesser spaces.

### Foreign Key
    1. FK is not always the PK. But generally, it happens like that.
    2. Normally if a col is referred to in another table as a FK, it will not allow us to update its value as it will cause a data integrity issue. Suppose there are 2 tables: Students and years where the reference table is years whose col is being referred in the students' table. We can make modifications in the students' table but we will not be allowed to make changes in the years table.
    3. For foreign key we usually pick up a unique col from a table. It need not be a primary key but it has to be unique.
    4. We can also have a composite key acting as a foreign key.

    This behavior mentioned in point 2 is the default behavior where we are not allowed to DELETE or UPDATE values of the col of the table that is being referenced.
    Therefore there are 4 properties:
    a. No Action: Scenario mentioned above.
    b. Cascade: Reflecting the changes in the table which contains the foreign key
    c. Set Null: The Fk col should not have NOT NULL on it for this.
    d. Set Default
    
