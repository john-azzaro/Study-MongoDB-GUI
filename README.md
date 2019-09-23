# MongoDB GUI Management Tools Study

<br>

## What is the MongoDB GUI Management Tools Study?
The default interface for MongoDB is a CLI command line which can be difficult at times to use. But unlike using mongo shell to work with your databases locally or on the cloud with a tool such as Atlas (formerly mLab), you can also use *management tools* that are built specifically to for working with databases like MongoDB.  These tools can help improve productivity in your MongoDB development and admin tasks as well as make it easier to work with larger amounts of data.

Here's some questions covered in the study:

* [What is MongoDB Compass Community?](#What-is-MongoDB-Compass-Community)

<br>

## What is MongoDB Compass Community?
MongoDB Compass is a simple GUI that allows users to explore, insert, modify, and delete from your database (i.e. fill CRUD functionality) visually as well as run ad hoc queries. Compass uses inbuilt schema visualization to help the user analyze documents and display rich structues.  Additionally, Compass offers real time statistics of database operations

<br>

### How do you use Compass?
To use compass, you need to install MongoDB Compass Community: https://www.mongodb.com/download-center/community.  However, make sure to install Compass AFTER you install MongoDB because some issues can occur that make it a pain to get working correctly.

When you open Compass, you will see a list of your databases.  For example, testDB in the example below represents a database that holds *collections* of *documents*.
```
    > admin
    > config
    > local
    > testDB
```

Inside those databases, you can see collections within those databases, how many documents in each collection, and 
other information such as document size, number of indexes, and total index size. 
```
    Collection Name    Documents   Avg. Document Size   Total Document Size    Num. Indexes    Total Index Size    Properties
    _______________    _________   __________________   ___________________    ____________    ________________    __________
        books            3,950          451.2 B               1.8 MB                1               45.1 KB             
```