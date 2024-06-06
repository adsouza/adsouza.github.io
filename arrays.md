# Arrays
The second-smallest grouping of bits used by modern computers is known as a word, which is typically a power-of-two (e.g. 2, 4, 8) multiple of a byte. 
Today we commonly use words composed of eight bytes (i.e. 64 bits), although 32-bit words aren’t that rare & we still use 16-bit words on many embedded systems.

Modern computers tend to have many gigabytes (i.e. billions of bytes) of RAM (memory). This vast memory can be easily accessed as a giant sequence of words. 
We refer to the content of words in memory using their (0-indexed) position in the sequence. Such a fixed-size sequence that can be indexed by position is called an array.

The best thing about an array in RAM is that we can trivially & very quickly inspect or change a word anywhere within it as long as we know its position. 
This makes arrays ideal for analysing or editing large quantities of identically structured data that have an obvious natural ordering.

We can sometimes exploit the fact that arrays are guaranteed to contain data of the same type in order to perform identical computations or manipulations on an entire array in parallel. This technique is known as [SIMD](https://www.wikiwand.com/en/Single_instruction,_multiple_data) (single instruction, multiple data).

Common examples of array data include statistical records, images (grids of pixels), and text corpora. Speaking of which, let's see [how we represent text on computers](text.md).
