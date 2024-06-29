# Product types

## Collections
Often it is necessary to represent many items of the same type. This is called a collection (AKA container). 
There are various types of collections, each of which have properties that make them suitable for particular uses: 
lists provide order, sets provide uniqueness, dictionaries (AKA maps, symbol look-up tables or key→value stores) provide access to items by name, 
trees provide hierarchy, etc. The size of a collection is dynamic: it can change over the course of execution.

While each cat can only have two parents, they can have a large number of children. 
Thus, a list would let us store references to the children of each cat in birth order, 
while a dictionary would let us store the list of children each cat has with specific other cats. 
Taken together, these lists of children would form a tree representing the genealogy of some feline population.
