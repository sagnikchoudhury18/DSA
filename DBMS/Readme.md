# Intro and Key concepts

### Super Key
    col or set of cols whihc can uniquely identify a row.

### Candidate Key
    minimal set of cols which can uniquely identify a row.

### Primary Key
    A candidate key which is selected to represent a row uniquely.
    
#### Need for Primary Keys
    1. Generally databases stores data in the order of primary keys. If I have multiple primary keys database would get confused according to which col the data needs to be ordered.
    2. Sorting is required as it makes searching easy
    3. Outputs the data in order of PK
    4. DB creates an index on PK which helps in the optimization.
    5. The user creating the schema decides the PK.
    6. We can have just one PK in the table but this can be a collection of cols eg: CONSTRAINT pk_PersonID PRIMARY KEY (P_Id,LastName) 
    
    Note: Suppose we have 2 cols email_id and student_id the PK would be built on student_id as sorting and comparison is easier on integers. Indexes created on integers take up lesser spaces.

### Foreign Key
    1. FK is not always the PK. But generally it happens like that.
    2. Normally if a col is referred in another table as a FK, it will not allow us to update the value of it as it will cause a data integrity issue.
    
