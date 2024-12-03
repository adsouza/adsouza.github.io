# Types of data
Data is often used to represent concepts, objects & systems in the real world. 
Computers represent everything (i.e. both data and instructions) as sequences of bits (short for binary digit), 
whose values (like a toggle switch) can be either on or off; 
we use off to represent 0 and on to represent 1. We can group these bits into larger and more complex structures to represent anything else.

The easiest things to represent are dichotomies (e.g. true/false, yes/no, up/down, north/south, etc.) 
because it takes only a single bit to represent them. 
We call these booleans (in honour of [George Boole](http://en.wikipedia.org/wiki/George_Boole), a British Mathematician & Philosopher).

Here are examples of creating a boolean value in different (programming) languages:

<details>
  <summary>C</summary>

  ```c
  #include <stdbool.h>

  bool isAlive = true;
  ```

</details>
<details>
  <summary>Python</summary>

  ```py
  from typing import bool

  is_alive: bool = True
  ```

</details>
<details>
  <summary>Java</summary>

  ```java
  boolean isAlive = true;
  ```

</details>
<details>
  <summary>TypeScript</summary>

  ```ts
  let isAlive: boolean = true;
  ```

</details>

Next up are [numbers](numbers.md).
