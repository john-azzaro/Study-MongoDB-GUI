# MongoDB GUI Management Tools Study

<br>

## What is the MongoDB GUI Management Tools Study?
The default interface for MongoDB is a CLI command line which can be difficult at times to use. But unlike using mongo shell to work with your databases locally or on the cloud with a tool such as Atlas (formerly mLab), you can also use *management tools* that are built specifically to for working with databases like MongoDB.  These tools can help improve productivity in your MongoDB development and admin tasks as well as make it easier to work with larger amounts of data.

Here's some questions covered in the study:

* [What is MongoDB Compass Community?](#What-is-MongoDB-Compass-Community)
    * [How do you use Compass?](#How-do-you-use-Compass)
* [What is Robo 3T?](#What-is-Robo-3T)
    * [How do you use Robo 3T?](#How-do-you-use-Robo-3T)

<br>

## What is MongoDB Compass Community?
MongoDB Compass is a simple GUI that allows users to explore, insert, modify, and delete from your database (i.e. fill CRUD functionality) visually as well as run ad hoc queries. Compass uses inbuilt schema visualization to help the user analyze documents and display rich structues.  Additionally, Compass offers real time statistics of database operations

<br>

### How do you use Compass?
First, download MongoDB Compass Community: https://www.mongodb.com/download-center/community.  However, make sure to install Compass AFTER you install MongoDB because some issues can occur that make it a pain to get working correctly.

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

And inside each each collection are documents, which are essentially key/value pairs.
```
    {
        "_id":"59074c7c057aaffaafb0da64",
        "Author": Object,                      
        "genre":"fiction",
        "cuisine":"Italian",
        "reviews" Array:
        "name":"Making Bread the Easy Way",
        "book_id":"40365784"
    }
```

<br>

## What is Robo 3T?
With functionality similar to compass, Robo 3T also lests use work more directly with queries and documents.  However, Robo 3T is one of the few GUI management tools available that embeds the orginal MongoDB shell, uses minimal machines resources, as well as having all operations performed with MongoDB asynchronously.


<br>

### How do you use Robo 3T?
After installing Robo 3T, you will need to connect with your database which will then be displayed on a sidebar to the left of your window.
```
    > New Connection
        > System
        > config
        > testDB
```

And to give you an example of what you would see if you had a database to look through, when you click on a database such as "testDB", you will see a folder named "collections" which will
expand in the right window with all the documents associated with that collection.  
```
    (1) ObjectId("563097824igf876e42)
    (2) ObjectId("ghfe65678fhkjlhf7")
    (3) ObjectId("57689hkjbhjkhnhj3")
    ...
    ...
    ...
```
Be sure to note that at the top of the right window you will see the query used to retrieve the documents.  This line can be edited to make your query function how you want.
```
    db.getCollection('myCollection').find({})
```