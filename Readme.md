# Mongo DB

- It came From huMongOus word
- Open Source
-  Document oriented
-   Flexible
-   Schema-less Data Struture (not defined field)
- Stored in Json like Bson Documents  unlike Table structure of SQL.
- 

## SQL -Relational DBMS
 -  Structured predefined, fixed row and colums with a unique id.

 ## No SQL: Mongo DB , Cassandra
  -

- DataBase
    - Students(Collection)  
        - Multiple Documents
            -Field(Different)
    - Teachers(collection)
          - Multiple Documents
             -Field(Different)


## How MongoDb works?

Frontend Request => Backend (Nodejs) => MongoDB Server => Storage Engine(WiredTiger) => Read/Write files => Database 
 then reverse the process to fetch the files

 - Storage eNGINE: Converts Json to BSon format , BSOn is binary Json Format.
 - By using Bson , Mongo Db can achieve higher read and write speed.

[!Working](./Resources/working.png)

 ## Installation
 - Mongo DB community
 - Mongo DB Shell
 - Mongo DB tools

-  for checking mongodb 
    -   mongod --version
-   For mongo shell
    -  mongosh


## Managing Database

### Show all DBs
    - show dbs
### Creating database
    - use <DaTabase Name>

### Delete Database
    - db.dropDatabase();
 
### Show Collections
    - show collections

