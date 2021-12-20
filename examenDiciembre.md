# Examen BBDD Diciembre

**Replica Set:** a few connected machines that store the same data to ensure that if something happens to one of the machines the data will remain intact. Comes from the word replicate - to copy something.

**Instance:** a single machine locally or in the cloud, running a certain software, in our case it is the MongoDB database.

**Cluster:** group of servers that store your data.

### CHAPTER I

**Why is MongoDB a NoSQL database?:**
- Because it uses a structured way to store and access data.
- Because it doesn't utilitze tables, rows and columns to organize data.

**Select the statements that together help build the most complete definition of the MongoDB database:**
- The MongoDB database is an organizated way to store and access data.
- MongoDB is a NoSQL database that uses documents to store data in an organizated way.

**In MongoDB how does a document relate to a collection?:**
- Collections consist of one or many documents.

**In a MongoDB Document what is the role of fields and values?:**
- Each field has a value associated with it.
- A field is a unique identifier for a specific datapoint.

**How is MongoDB Atlas related to MongoDB the Database?:**
- Atlas has many tools and services within in that are built specifically for the MongoDB Database.
- They both are MongoDB products.

### CHAPTER II

**Which of the following documents is correct JSON?:**

- {"name" : "Devi", "age": 19, "major": "Computer Science"}

**Write BSON or JSON:** 
- MongoDB stores data in BSON, and you can then view it in JSON
- BSON is faster to parse and lighter to store than JSON.
- JSON supports fewer data types than BSON.

### ACTIVITIES

**See in a database:**
```
show dbs
```
**Use a database:**
```
use db_name
```
**See collections:** 
```
show collections
```
**Create a collection:**
```
db.createCollection("name")
```
**Insert a document:**
```
db.collection.insertOne({name: "Juan})
db.collection.insertMany({name: "Juan}, {name: "Pedro"}, {name:"Maria"})
```
**Find a document:**
```
db.collection.find()
db.collection.findOne()
```
**Delete a document:**
```
db.coleccion.delete({})
db.coleccion.deleteOne({name:"Pedro"})
db.coleccion.deleteMany({name:"Maria"})
```
**Compare values:**
```
db.coleccion.find({age: {$gt: 18}})
db.coleccion.find({age: {$gte:18}})
db.coleccion.find({age: {$gte: 40, $lte: 51}})
```
**Update values:** 
```
db.coleccion.update({name:"eze"}, {$set: {name:"Luis"}})
```
**Different to X:**
```
db.coleccion.find({name: {$ne: "Pedro"}})
```
**Between X and Y:**
```
db.customer.find({age: {$in: [47, 48, 49]}})
db.customer.find({age: {$gte: 47, $lte: 49}})
```