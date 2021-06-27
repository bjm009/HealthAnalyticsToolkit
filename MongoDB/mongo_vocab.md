# MongoDB Vocabulary!
Here we will explore the key concepts and terms you will likely encounter as you learn about MongoDB. 

## Documents
The documents are the records in a document database. MongoDB stores data as JSON documents. 

## Collections
A collection is a group of documents. A collection can be thought of as a table, like we see in relational databases, such as SQL. However, the collections are more flexible in that they documents in the same collection can have different fields. 

## Replica Sets
When you create a database in MongoDB, the system creates at least two additional copies of the data, which is referred to as a replica set. A replica set is a group of at least 3 MongoDB instances that continuously replicate data between them, ensuring high availablility and protection against downtime. 

## Sharding
Sharding is the term for distributing data intelligently across multiple machines. With MongoDB, it shards data at the collection level. This distributes documents in a colleciton across the shards in a cluster, resulting in a scale-out architecture that supports large applications.

## Indexes
Indexes are designed to imporve query speed. 

## Aggregation Piplines
MongoDB has a flexible framework for the creation of data processing pipelines, which are called aggregation pipelines. The aggregation pipelines feature dozens of stages and more than 150 operators and expressions which enables you to process, transform, and analyze data of any structure at scale. 

## Programming Languages
MongoDB supports the following languages: Node.js, C, C++, C#, Go, Java, Perl, PHP, Python, Ruby, Rust, Scala, and Swift. 

### Reference
This information was obtained from [mongoDB](https://www.mongodb.com/basics). Visit their website to explore more! 
