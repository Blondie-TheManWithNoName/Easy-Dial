# EASY DIAL

Implementation of modified TST **(Ternary Search Tree)** in C++ in order to get suggestion of most called people names by typing one letter at a time.


Defined classes:

- Phone
- Easy Dial
- DIalog
- Call Registry


## UML of the Project

![Untitled Diagram drawio](https://github.com/Blondie-TheManWithNoName/Easy-Dial/assets/58909117/11a4f09a-44f8-475b-8885-0b430a21cbd5)


## Process of thought to get to the Data Structure that suits the most

### Common TST

I started with this one and ran into a problem, I could not tell which was the number with the highest frequency if the node with the current prefix had more than two children and also if the central child of this one had more than two children, and the central child of this one etc.

### General tree (with full names)

With this one the previous issue with the TST was solved. I could identify the most frequent number of direct children of a node, but the problem was that I could not know if any child of the children of the current node had higher frequency or not.

###Pointer vector per node with all ascii characters

This option solved all of the above problems. The problem was that the space cost was very large since we had to have a table with all ascii characters a table with all ascii characters. And the function _ _easy_dial::comencen(...)_ _ was not efficient, so even though it worked perfectly I decided to change the implementation.

### General tree (with only prefixes)

This was the best option, because we could always identify which was the most frequent name. The problem was in the function _ _easy_dial::comencen(...)_ _, because I only stored the necessary characters and not the full names, the function was very convoluted and not very efficient.

### TST (modified)

This last implementation turned out to be the one that best fit the requested criteria. Basically it is like the general tree with only the characters but I added the whole name, so when you are looking at the prefixes in functions like next and previous, we only look at the characters as in the general tree, you only look at the characters as if it were the general tree.
But when we do the function _ _easy_dial::comencen(...)_ _ we take advantage of the fact that we have the integer names and this way we have an easy and efficient function.



