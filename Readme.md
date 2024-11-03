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
    or
    - show databases

### Creating database
    - use <DaTabase Name>

### Delete Database
    - db.dropDatabase()
 
### Show Collections
    - show collections

### Create Collections
    - db.createCollection('<Collection-name>')

### Delete Collections
    - db.<collection-name>.drop()

- Untill a single collection in not present in the created database , show dbs will not show the name of created datbase.

### Example

````
use Students
switched to db Students
Students> db.createCollection('DATA')
{ ok: 1 }
Students> show collections
DATA
Students> show dbs
Students    8.00 KiB
admin      40.00 KiB
config    108.00 KiB
local      40.00 KiB
Students> show collections
DATA
Students> db.DATA.drop()
true
Students> show dbs
admin    40.00 KiB
config  108.00 KiB
local    40.00 KiB
Students> show dbs
admin    40.00 KiB
config  108.00 KiB
local    40.00 KiB
Students> db.dropDatabase()
{ ok: 1, dropped: 'Students' }
````

### Inserting one Document
    - db.<collection-name>.insertOne({
        field1: value1,
        field2: value2,
        ...
    })

### Insert Multiple Documents
    - db.<collection-name>.insertMany([
        {
        field1: value1,
        field2: value2,
        ...
        },
        {
        field1: value1,
        field2: value2,
        ...
        },
    ...
    ])