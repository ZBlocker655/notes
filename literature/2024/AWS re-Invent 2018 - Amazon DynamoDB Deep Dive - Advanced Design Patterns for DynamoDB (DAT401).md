---
type: video
url: https://www.youtube.com/watch?v=HaEPXoXVf2k&ab_channel=AmazonWebServices
channel: Amazon Web Services
year: 2018
subjects:
- [[nosql data modeling]]
- [[dynamodb]]
---

# History of databases

5:00 

## NoSQL data modeling optimizes for CPU at the expense of storage

One of the drivers behind the development of relational databases was that in the late 1970s, storage was the most expensive component in the computer system, so it made sense to minimize it when possible.  Relational modeling involves normalizing data, so that any given piece of information appears only in one place (one table, one row).  On the other hand, this means the CPU has to work harder (to join tables, compute result views, etc.)

On the other hand, in today's world, the CPU is the more expensive resource, whereas storage has become much cheaper. This has been one of the drivers behind the development of NoSQL databases, which minimize CPU time (since we don't generally do joins or other expensive query computation) but maximize storage through denormalized modeling, duplication of data, etc.

# DynamoDB modeling

20:13
## The DynamoDB partition key should have high cardinality

In order to distribute data access evenly throughout the key space, the table partition key should have a very high cardinality, or number of distinct keys. This helps avoid a "hot key", which is a key that is accessed far more often than other keys.  If this is allowed to occur, it can negate many of the performance benefits of NoSQL.