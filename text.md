# Text
We represent text, at a high level, much as many natural languages do: using sequences of _graphemes_, 
the smallest distinct meaningful units of writing (e.g. A, €, Ñ, Æ, ﬃ, क्ष, 공, นั่, 鬱, ♬, ⭐, 🇨🇦, 𓂀, 🏴‍☠️, 👩🏻‍❤️‍💋‍👨🏾, Ǫ̵̹̻̝̳͂̌̌͘, ﷺ), 
which are in turn composed of "_characters_"; 
some graphemes consist of a single character (e.g. A, €, ♬, ⭐, 𓂀) while 
others combine two (e.g. Ñ, Æ, อ์, 🇨🇦), three (e.g. ﬃ, क्ष, 공, นั่, 🏴‍☠️) or even several (e.g. 鬱, 👩🏻‍❤️‍💋‍👨🏾, Ǫ̵̹̻̝̳͂̌̌͘, ﷺ) upto a max of 31.

[Unicode](https://www.joelonsoftware.com/articles/Unicode.html) is the most comprehensive and ubiquitous _character set_: 
a method for mapping between characters (including some precomposed/composite ones) and integers (AKA scalar values). 
It contains integer mappings for characters that can represent all living scripts as well as many historical ones, 
various symbols (e.g. math, music, transport, science, games), emoji, etc. 
Each of the integers can be encoded by a small number (up to 4) of _bytes_. 

**Historical note**: some older software uses a legacy mapping called ASCII, which uses a single byte per character 
and only works for a few scripts - it doesn’t even allow mixing text from multiple scripts. 

In the parlance of computer science and software development, sequences of characters/graphemes are known as **strings** 
(because we form them by _stringing_ those together). 
Unlike natural languages, computers do not typically group graphemes into increasingly more complex sequences like phrases, sentences and paragraphs. 
That said, we often refer to smaller segments of a string as substrings.

We can store the sequence of bytes that comprise a string in an _array_ (contiguous chunk of memory). 
_Recall that each element of an array can be addressed by its position in the sequence (typically starting at 0)._
Arrays have one primary downside: once created, their capacity cannot be changed. 
This means that, once created, strings cannot be lengthened in-place.

An important property of a string is its _length_. 
This may be computed as needed using a special character that marks the end of a string: the string terminator, which is a null byte (integer value 0). However, because graphemes may be composed of a variable number of characters, which in turn may be composed of a variable number of bytes, 
computing the number of graphemes (or even characters) in a string is a complex operation. 

Alternatively, the length of the string may be stored along with its content for easy retrieval. 
This length never needs to be updated if we can never change the _number_ of graphemes or characters in a string.
Often we want to go even further & never modify the bytes in strings at all. 
The term used to describe data that can never be changed is **immutable** - as opposed to mutable.

The types of data we've considered so far (e.g. boolean, numeric, text) can be combined to create even more useful ways of organizing data. 
We refer to those as _composite_ types. Let us next consider [sum types](sum-types.md).
