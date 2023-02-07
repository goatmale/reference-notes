# Redis Cardinality
`LLEN` List cardinality
`SCARD` - Set cardinality
`ZCARD` - Sorted set cardinality

## Deleting or "trim"ing list element
`LTRIM key start stop`
ie. 

`LTRIM 0 -1` - Entire list

`ZREMRANGEBYRANK`
ZREMRANGEBYRANK 5 -1
Keep only top 5
cap cardinality

## Set operations

Intersection

ZINTERSTORE

The set operations for sorted sets have a unique capability. They can operate on
both sorted sets and sets

zunionstore - aggregation - scores - ie. sum

## Set use case - Faceted Search
* Secondary index
  * single value - storage and mainteance -
  * compound indexes
* full text search
  * lucene
  * compelxity / eventual consistency
* Faceted search:
  * inverted index

How to find?
## Object inspection
Time complexity of o(n)
* Retreieve all
* scan
* get each

## Set intersection
* Create sets for each attribute and use a primary key like SKU
* `sinter` - based on cardinality on the smallest set
* o(1) for gets
* beats the time complexity of the object inspection if the card of one set is be low and the number of sets were checking are also low.
* SINTER - time complexity of O(N * M)

## Hashing
Consistent hashing
o(1) - 
