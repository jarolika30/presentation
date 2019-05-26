# presentation

##Slides 1-2

Hello, my name is Ekaterina. I`ve prepared an introductory report about MongoDB database. I`ll try to answer following questions:
      -	What is MongoDB?
      -	What is difference between SQL and NoSQL databases?
      -	Also, we will talk about CRUD operations in MongoDB.

##Slide 3

MongoDB is a free, open-source, cross-platform document-oriented database
program. It belongs to non-relational databases, also known as NoSQL. 

##Slide 4

In general, a database is a collection of data that is stored on a machine. We can divide databases on SQL and NoSQL. 
SQL-databases are relational and always table based. It means, that data is organized in tables and every record is a row in a table.
NoSQL-databases can have a variety of different structure. For example, they can be graph-based or document based. MongoDB uses document structure. 
In SQL databases tables have a fixed schema defined by creation. After that, all rows will have the same attributes.
NoSQL schema is not predefined. In MongoDB data is stored in separate documents. Each document is independent from others and even more, documents 
in one collection can have different fields and data types!

##Slide 5

Let’s compare how data looks in SQL and in NoSQL. 
In a SQL database each row is one record and each column represents an attribute of this record. The examples of SQL databases are Oracle, MySQL, MS SQL Server. 
In NoSQL, data looks like JSON and has keys and values. That representation is very similar to real object-oriented programming. The examples of NoSQL are Redis, Cassandra, Titan, MongoDB.

##Slide 6
MongoDB is a relatively new database technology, it was created in 2009. It became popular in the IT-industry in the recent years.
The results of DB-Engines Ranking shows that MongoDb is one of the leading NoSQL databases in May 2019. It is in the top among NoSQL databases and on the fifth position among all rated DBs. 
The ranking score of MongoDB grows last several years. 
The following companies utilize MongoDb: Adobe, Bosch, Cisco, facebook, SAP.

##Slide 7

In comparison with SQL-databases MongoDB has the following advantages:
-	First of all, MongoDB is object-oriented, it uses JSON-like documents, that is very convenient for those developers who knows JavaScript;
-	Secondly, because documents are independent of each other, the document add / edit / delete operation do not affect the other documents;
-	Finally, the MongoDB provides the elastic scalability and high performance
But MongoDB has some disadvantages too:
-	It doesn`t support transactions and join operations and also has a high memory usage.
 
##Slide 8

MongoDB has the next structure:  every database consists of collections, every collection consists of documents. Each document has fields and every field consists of key and value. Fields can store different data types. The key has to be always a string and value can be string, integer, Boolean, double, 
array, date or object. So, these are main data types that MongoDB supports.

## Slide 9

Now we will talk about CRUD operations.
CRUD acronym stands for create, read, update and delete. These are 
4 basic functions used for data manipulation in the database.

## Slide 10

Create operations add new documents to a collection, if the collection does not exist, it will be created. 

There are 2 primary ways to create a document: 
-	.insertOne() for adding a single document
-	and .insertMany(). for adding multiple documents

## Slide 11

In this example the new document is inserted into the moviesScratch collection. Note, that the pasted document 
looks like JSON-object.

## Slide 12

In the next example .insertMany() adds 2 documents into the collection. This function takes 2 arguments - an array with the pasted documents and an object with the key “ordered”. By default, MongoDB guarantees the insertion of documents in the order in which they are specified. In case of error, this function stops its work. But when the ‘ordered’ para
meter is set to false, .insertMany() will try to insert the other documents.

## Slide 13

Let’s proceed to the read operations…
Read operations retrieve documents from a collection. The main methods for this operations are find() and find().pretty().
The method find() views and returns documents of the collection, the pretty method  makes the same but prints result in a more readable form. 
The commands show dbs, show collections, db, use and the method count are used for displaying information about existing databases, collections and documents.


## Slide 14

The example demonstrates the output of mentioned commands. On the first 
line, show dbs lists all available databases. The next command use video 
selects the database named ‘video’. The show collections command returns 
all existing collections. The db command retrieves the current database. 
Finally, the db.movieDetails.count() execution displays the number
 of all documents in the movieDetails collection in the video database.
 
## Slide 15

Next slides demonstrate find() function results with and without pretty call. Please, pay attention how the documents displayed. The .find().pretty() returns result in 
human-readable form while the result of pure find() is difficult to read.

## Slide 16

Let’s roll to the update operations
Update operations modify existing documents in a collection. There are 3 main methods for it:
-	.updateOne() for updating a single document;
-	.updateMany() – to update multiple documents;
-	.replaceOne() – for replacing a document.
All these methods require a filter for selecting the necessary documents. See the next examples…


## Slide 17

Here is the example of single document update. The filter is “title”: ”The Martian” .updateOne() will modify the first document matching the filter. The $set block specifies how to
 update the document - add field poster or if such field exists – modify it. 

 
 ## Slide 18
 
 The .updateMany() example selects  documents with key “rated”  and value “null”, then the $unset 
 operator removes this field.
 
 ## Slide 19
 
 
 The .replaceOne() example will select  the first document matching the filter (“name”:”Pavel”) and 
 then will replace keys “name”, “password”, “hasCar” with specified values.
 
 
 ## Slide 20
 
 
 MongoDB supports following delete operations:
-	 .deleteOne()  to delete single document 
-	and .deleteMany() – to delete multiple documents. 
The first argument is a filter that defines what to delete. 

## Slide 21

The example of .deleteOne() shows how to delete the 
first document with a key “name” and value “Pavel”.

## Slide 22

.deleteMany()  example deletes all documents, with a 
key “name” and value “Pavel”. The last example demonstrates 
deletion of all documents from the collection inventory.



## Slide 23

This ends my short introduction into the MongoDB. 

Let me remind you key points:

-	MongoDB is a NoSQL database;
-	It is document-oriented;
-	MongoDB uses JSON-like documents;
-	It has a flexible schema;
-	MongoDB has next structure: database -> collections->documents -> fields;
-	To create documents we use .insertOne() or .insertMany();
-	To read document we use .find() or .find().pretty();
-	To update documents we can use .updateOne(), .updateMany(), .replaceOne();
-	And to delete documents use .deleteOne(), .deleteMany().

Thank you for attention!!!







