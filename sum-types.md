# Sum types

## Enumerations
Sometimes we have a _fixed set of named entities_ (e.g. days of the week, months of the year, cardinal directions) that we want to use as values. 
We could just represent these as strings but that's sloppy.
Ideally, we can model that our use of a named entity (e.g. Friday) in one place refers to the exact same thing as our use of it in another place. 
To address this need we use a construct called an _enumeration_, which defines a fixed set of named entities. 
We can then refer to members of this set by name anywhere and the computer will know we are referring to the same thing in each case.

You could even think of booleans as a very simple enumeration that has only two possible values: true & false.

Note: The elements of an enumeration will often have an obvious sequence (e.g. months) but this is not always applicable (e.g. cardinal directions).

## Tagged Unions
Beyond just offering a set of unique names, we can even allow some of the named entities to include additional data.
Such a data type is called a tagged union; the unique named values are the tags.

### Option types
Often we want to represent a type that may or may not actually have a value.
While it may be tempting to always have a default value (e.g. 0 for integers or the empty string), 
there isn’t always a reasonable default value that can be used; 
moreover, sometimes it is actually necessary to distinguish between the default value & the absence of one. 

Historically, people have tried to deal with this by using a global constant value (typically called null or nil) to represent the lack of a value. 
However, this tends to cause problems when code isn’t expecting the value of something to be missing. 

A better way to handle this situation is by using an explicitly nullable type that forces people to always handle the case of a missing value. 
This is usually called an _option_; it is a tagged union with exactly two tags, 
one of which is a global constant (typically called none) while the other (usually called some) holds the actual data when present.
