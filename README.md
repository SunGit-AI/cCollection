# cCollection

Idea:
if someone uses the array and he has the index, he can access the value with O(1). 
Goal: use the array efficiency advantage to suit keys in a size-fixed array. use that keys for key-value pairs.

solution:
1. for each key in keys: array-indexes = key mod array-size.
2. arrange all collision array-indexes in the free indexes.
3. save all keys in the array with indexes.

allocate array with array_size: map->ids = allocate_array (array_size).

for (    array_index = key_x mod array_size; 
	map->ids[array_index] != free; //if this index is free, use this, if not, try array_index + 1
	array_index = ( array_index + 1) mod array_size; );


problem: if there too many collision array-indexes? Solution: generate hash-codes with the keys.
