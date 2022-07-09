### II.	STACKS

####  Introduction
 A Stack is a data structure determined by the order a piece of data is entered and the order that leaves the structure. It is contrary to what is known as queues( similar to a bank queue). In a Stack the last data entering the structure is the first to exit. This is known as LIFO(Last in, first out). 
####  Stack of Pancakes 
To understand this concept more clearly, it will be represented with a tray of pancakes. At the moment that the tray is filled, the last one that is added is the first to be taken to eat. This means that the first one that came out of the oven is going to be the last one to be eaten. 

	
####  Stacks in Python
A Stack in Python can be represented with a list. Where default functions will be used to add, get, and calculate their size. In the following table you can see the functions that are used to handle a list.
Push(value).- Adds “value” to the back of the stack.
Pop().- Removes and returns the item from the back of the stack.
Size().- Return the size of the stack.
Empty().- Returns true if the length of the stack is zero.
####  Example
def reverse_string(strValue):
    strNew = Stack()
    For i  in strValue:
        strNew.push(i)
    strReverse= “”
    while not strNew.is_empty():
        strReverse += strNew.pop()
    return strReverse
####  Problem to Solve
Create a program using a stack data structure to convert a decimal number to binary.


