# Numbers
Humans typically have 10 digits on our hands so we use a decimal numbering system. 
Computers have only 2 digits with which to form numbers so they use a [binary numbering system](https://en.wikipedia.org/wiki/Binary_number). 
But they can translate to decimal when interacting with humans.

The smallest grouping of bits used by modern computers is a sequence of bits known as a byte. 
By far the most common size for a byte is 8 bits, also known as an octet.
Treating an 8-bit byte as a binary whole number gives us a range of possible values from 00000000 to 11111111. 
In decimal we would express this range as 0 to 255 - every number system expresses zero as all zeros.
To represent negative values, we can reserve one of those bits (generally the first one) for the sign (i.e. positive or negative). 
This halves the magnitude of our range so that the maximum value is now 127 but the minimum is now -128 (instead of 0).

As you might expect, we need to represent larger numbers than this! 
The easiest way to do that is by grouping bytes together into even larger sequences. 
Each additional bit doubles the range of possible values: four octets give us 32 bits, which can represent numbers on the order of billions - 
good enough for most things - while eight octets give us 64 bits, which can represent truly enormous numbers (e.g. grains of sand on Earth).

That works for integers but we often also need to represent fractional values. Humans typically represent these using a decimal point. 
As it turns out, we can also represent these using a more complex approach known as [floating point](https://en.wikipedia.org/wiki/Floating_point). 
That gives us the 2 types of numbers commonly used in computing: integers and floating point numbers. 
Doubling the number of bits used to store an integer increases its capacity; doing the same with floating point numbers increases their precision instead. 
Floating point numbers have some odd [quirks](https://floating-point-gui.de/basic/) you’ll want to keep in mind.

For both types of numbers, it is often up to the programmer to decide how many bytes to use to store them, based on what they need to represent. 
For instance, while an 8-bit integer will suffice to count the number of days in a month, it will not suffice for counting the days in a year. 
Using too many bytes may be inefficient but using too few can have far worse consequences if you need to store numbers too large to fit in the space you allocated for them 
(e.g. the infamous [Y2K](https://en.wikipedia.org/wiki/Year_2000_problem) debacle); therefore it is better to err on the side of generosity.

Numbers are great & all that but we also need [text](text.md).
