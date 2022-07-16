### Introduction

Sets in Python are known to be an unordered collection of data, in other words they have no index for storage. When entering the data you cannot choose the position where it will be stored. Something important to note is that there are no repeated values within a set.
#### Characteristics of Sets
Sets in Python come by default just like lists, tuples, and dictionaries. Sets are regularly used for logic and mathematics because you can take advantage of their properties by creating more efficient and easier to understand code.
There is a very useful technique in Python to apply to sets. This tool is called hashing and it allows adding, removing and testing an element within a set in O(1) time.
#### Hashing and Sets
Operations using Hashing are similar to Linked List. Thanks to this technique you can work efficiently creating sets, checking if an element is within the set, adding elements, joining sets, intersecting sets, subtraction between sets, and symmetric difference. Best of all, these processes are performed in O(1) time.
#### Applications with Sets in Python
* Speed to add, remove and search for an element.
* Does not allow duplicate items. This avoids errors when entering repeated data.
* The elements entered do not have an order dependent on an index. This means that they do not maintain an entry order.
The main uses of sets in Python are as follows:
* Search for a single value in a list.
* Provide quick access to a single value after a calculation process.
* Improvement in processes between sets such as union, intersection, differentiation, etc.
#### Example
set1 = {1, 2, 3, 4, 5}

set2 = {4, 5, 6, 7, 8}

set3 = intersection(set1, set2)  # This will result in {4, 5}

set3 = set1 & set2               # Alternate way of writing an intersection

set4 = union(set1, set2)  # This will result in {1, 2, 3, 4, 5, 6, 7, 8}

set4 = set1 | set2        # Alternate way of writing a union
#### Problem to Solve
Assume you have been asked in an interview to describe how you would write a function to find the intersection of two sets and a function to find the union of two sets. An intersection will return a set containing items that are common between the two sets. A union will return a set containing all items from both sets. Do not use the set operators (+, -, *, &, |) and functions (intersection, union) that are built-in to Python. You will need to use a set to to implement these functions.

