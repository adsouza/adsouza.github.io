# Text
We represent text, at a high level, much as many natural languages do: 
using sequences of "_characters_" (e.g. A, €, Ñ, Æ, ﬃ, क्ष, 공, นั่, 鬱, ♬, ⭐, 🇨🇦, 𓂀, 👩🏻‍❤️‍💋‍👨🏾, Ǫ̵̹̻̝̳͂̌̌͘, ﷺ) 
that are in turn composed of _graphemes_ (the smallest distinct meaningful units of writing); 
some characters consist of a single grapheme (e.g. A, €, ♬, ⭐, 𓂀) while 
others combine two (e.g. Ñ, Æ, อ์, 🇨🇦), three (e.g. ﬃ, क्ष, 공, นั่) or even several (e.g. 鬱, 👩🏻‍❤️‍💋‍👨🏾, Ǫ̵̹̻̝̳͂̌̌͘, ﷺ).

[Unicode](https://www.joelonsoftware.com/articles/Unicode.html) is the best and most ubiquitous _character set_: 
a method for mapping between graphemes (and some precomposed characters) and integers (AKA scalar values). 
It contains integer mappings for graphemes that can represent all living scripts as well as many historical ones, 
various symbols (e.g. math, music, transport, science, games), emoji, etc. 
Each of the integers can be encoded by a small number (up to 4) of bytes. 

Some older software uses a legacy mapping called ASCII, which uses a single byte per character and only works for a few scripts - 
it doesn’t even allow mixing text from multiple scripts. 

In the parlance of computer science and software development, sequences of characters are known as **strings** 
(because we form them by _stringing_ together characters). 
Unlike natural languages, computers do not typically group characters into increasingly more complex sequences like phrases, sentences and paragraphs. 
That said, we often refer to smaller segments of a string as substrings.

We store the sequence of bytes that comprise a string in an _array_ (contiguous chunk of memory). 
_Recall that each element of an array can be addressed by its position in the sequence (typically starting at 0)._
Arrays have one primary downside: once created, their capacity cannot be changed. 
This means that, once created, strings cannot be lengthened in-place.

Aside from the grapheme representation method, the most important property of a string is its _length_. 
This may be computed as needed using a special character that marks the end of a string: the string terminator, which is a null byte (integer value 0). However, because characters may be composed of a variable number of graphemes, which in turn may be composed of a variable number of bytes, 
computing the number of characters (or even graphemes) in a string is a complex operation. 

Alternatively, the length of the string may be stored along with its content for easy retrieval. 
This length never needs to be updated if we can never change the number of characters in a string.
Often we want to go even further & never modify the bytes in strings at all. 
The term used to describe data that can never be changed is **immutable** - as opposed to mutable.
