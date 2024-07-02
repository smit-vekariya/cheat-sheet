# Reference Python
> 1. Python interview questions:\
    https://www.interviewbit.com/python-interview-questions/
    https://www.geeksforgeeks.org/python-interview-questions/


# Revision Questions

> 1. What are the data types in the Python programming language:

* List : A collection which is ordered and changeable. Allows duplicate members.
* Tuple : A collection which is ordered and unchangeable. Allows duplicate members.
* Set : A collection which is unordered, unchangeable*, and unindexed. No duplicate members.
* Dictionary : A collection which is ordered** and changeable. No duplicate members.

*Set items are unchangeable, but you can remove and/or add items whenever you like.

> 2. what is diffrent beetween list and tuple and how tuple is faster then list.

Mutability:

Lists are mutable, meaning their elements can be changed, added, or removed after the list has been created.\
Tuples are immutable, meaning once they are created, their elements cannot be changed, added, or removed.

Use Cases:

Lists are typically used when you have a collection of items that may need to change, such as a collection of objects that might grow or shrink.\
Tuples are used for fixed collections of items, often to represent a single object or a set of related values that should not change, such as coordinates or fixed settings.

Performance:

Tuples are generally faster than lists. This is primarily because tuples are immutable, which allows Python to make certain optimizations that are not possible with mutable data structures like lists.\
For example:\
Tuples can be stored in a more compact and efficient way, saving memory.\
The immutability of tuples allows Python to cache and reuse tuples, reducing the need for repeated memory allocation.\
Operations on tuples are generally faster due to the fixed size and immutability, which can lead to reduced overhead in certain scenarios.