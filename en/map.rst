Map
===

Map type of Go is implementation of ``hash table`` data structure.

Operators
---------

- Lookup
- Add
- Delete

Declaration
-----------

map[Ktype]Vtype

Ktype must be comparable type.
Vtype can be anything.

map is reference type, same as pointer and slice.

map retrieval yields a zero value when the key is not present.

Pronunciation
-------------

map[string]int

- Map of int
- map of int values
- map of string to int
- map of string key to int value

map[string]map[string]int

- map of maps
- outer map is a map of string to a map
- inner map is a map of string to int
=> this is map of string to (map of string to int)

var m map[string]int
m['blah']

- retrieve value stored under key 'blah'

m['blah'] = 5

- set key 'blah' to 5

len(m)

- returns number of items in map m

delete(m, 'blah')

- remove entry 'blah' from map m.

Wisdom
------

Using map as value may not a good idea, as zero of a map is ``nil``.
map[X]map[Y]Z is not ideal data structure, map[struct[X,Y]]Z might be better.
Because we can leverage the zero of value for many good cases.
