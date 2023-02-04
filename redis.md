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
