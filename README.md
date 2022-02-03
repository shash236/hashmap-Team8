# Hashmap-Team8
Designing a concurrent hashmap

## Introduction
#### What are Hashmaps  
Hashmap is a widely used data structure which performs constant time insertion and retrieval of key-value pairs. This is done using hash functions

#### Why Concurrency  
If different threads try to modify the hashmap at same time, we might run into race conditions and deadlocks. The data might also be incorrect based on order of operations. Hence in a multi-threaded scenario it is better to use concurrent hashmaps.

#### Disadvantages  
A concurrent hashmaps performance can be lower than traditional implementation due to the locks acquired while inserting/updating keys. This can be mitigated by locking some sequences instead of complete hashmap.

## Implementation
#### Implement Hashmap
- should support get, put and remove operations
- Hash function

#### Collisions
- Handle using [separate chaining](https://www.geeksforgeeks.org/hashing-set-2-separate-chaining/?ref=lbp)
- Add new node to linked list for each key

#### Concurrency
- `Synchronized` Keyword? Has low performance due to locks
- Refer to [this link](https://softwareengineering.stackexchange.com/questions/401503/implementing-a-hash-table-with-true-concurrency) for more approaches