# Text
We represent text much as many natural languages do: using sequences of characters. A small number of bytes can represent each character. 
[Unicode](https://www.joelonsoftware.com/articles/Unicode.html) is the best and most ubiquitous method for representing characters as byte sequences. 
It can efficiently represent characters from all living scripts. Some older software uses a representation called ASCII, which uses a single byte per character and only works for a few scripts.

In the parlance of computer science and software development, sequences of characters are known as strings (because we form them by stringing together characters). 
Unlike natural languages, computers do not typically group characters into increasingly more complex sequences like words, phrases, sentences and paragraphs. 
That said, we often refer to smaller segments of a string as substrings.

We store the sequence of bytes that comprise a string in a contiguous chunk of memory known as an array. 
Each element of an array can be addressed by its position in the sequence (typically starting at 0). 
Arrays have one primary downside: once created, their capacity cannot be changed. This means that, once created, strings cannot be lengthened.

Aside from the character representation method, the most important property of a string is its length. 
This may be computed as needed using a special character that marks the end of a string: the string terminator (AKA terminating character). 
Alternatively, the length of the string may be stored along with its content for easy retrieval. This length never needs to be updated if we can never change the number of characters in a string.

Often we want to go even further & never modify the characters in strings at all. The term used to describe data that can never be changed is immutable - as opposed to mutable.
