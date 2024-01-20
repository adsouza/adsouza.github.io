# Abstraction

There are two kinds of constraints imposed upon software:
1. At run-time (i.e. when the software is executing on a machine) the constraints are imposed by the limits of physical hardware resources:
CPU cycles, memory, storage, I/O bandwidth & latency.
1. At design-time (i.e. while the software is being written by programmers) the constraints are imposed by the maximum amount of complexity a human mind is capable of holding:
most people can hold items in [chunks](https://en.wikipedia.org/wiki/Chunking_(psychology)) of at most three within their working memory;
any useful software is likely to have more than three instructions & highly likely to have far more than three pieces of data;
therefore our only hope for being able to reason about non-trivial software is by using [abstraction](https://tomstu.art/a-lever-for-the-mind)
to encapsulate software into modules that interact with each other.

The fundamental theorem of software engineering: any problem can be solved by adding another layer of indirection, 
except the problem of having too many layers of indirection. 
When you get the humour behind that aphorism, you will truly understand how to build software. 
For now, just keep in mind that a very common approach to solving problems involves decomposing them into a set of simpler problems.
