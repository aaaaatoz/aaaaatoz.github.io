# Redis Introduction

## What is Redis
Radis is a Key-Value based data store and it is widely used as high performance temporary date set.

## Key Feature
-  memory based: disk is only used for consistent storage
-  rich data structure
-  master - slave deployment
-  high performance IO
-  atom data operations, Thread safety

## Installation and Start(skipped)

## Redis Data Structure
- string: the value is a single string. common operations get/set
- hash table: the value is a hash table. common operations mset/mget
- list: (linked list in Redis internal), insert and get is O(1) cost. common operations: lpush, rpush, lrange,
- set: unsorted/ordered set. common operations: sadd/smembers/sismember
- ZSets: sorted-set: common operations:zadd/zrange/zrevrange
 