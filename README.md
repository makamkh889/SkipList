# SkipList
Data Structures and Algorithms Project
"college project"

=====================================================

## Assignment

Many application areas such as computer graphics, geographic information systems, and VLSI design require the ability to store and query a collection of rectangles. In 2D, typical queries include the ability to find all rectangles that cover a query point or query rectangle, and to report all intersections from among the set of rectangles. Adding and removing rectangles from the collection are also fundamental operations.

For this project, you can create a simple spatial database for handling inserting, deleting, and performing queries on a collection of rectangles. The data structure used to store the collection will be the Skip List. The Skip List fills the same role as a Binary Search Tree in applications that need to insert, remove, and search for data objects based on some search key such as a name. The Skip List is roughly as complex as a BST to implement, but it generally gives better performance since its worst case behavior depends purely on chance, not on the order of insertion for the data. Thus, the Skip List provides a good organization for answering non-spatial queries on the collection (in particular, for organizing the objects by name). However, as you will discover, the Skip List performs poorly on spatial queries.


### The program will be invoked from the command-line as:

where:

    Rectangle1 is then name of the program. The file where you have your main() method must be called Rectangle1.java

    commandFile is the name of the command file to read.

The command file may contain any mix of the following additional commands. In the following description, terms in { } are parameters to the command.

    insert {name} {x} {y} {w} {h}

    Insert a rectangle named name with upper left corner (x, y), width w and height h. It is permissible for two or more rectangles to have the same name, and it is permissible for two or more rectangles to have the same spatial dimensions and position. The name must begin with a letter, and may contain letters, digits, and underscore characters. Names are case sensitive. A rectangle should be rejected for insertion if its height or width are not greater than 0. All rectangles must fit within the “world box” that is 1024 by 1024 units in size and has upper left corner at (0, 0). If a rectangle is all or partly out of this box, it should be rejected for insertion.


    remove {name}

    Remove the rectangle with name name. If two or more rectangles have the same name, then any one such rectangle may be removed. If no rectangle exists with this name, it should be so reported.


    remove {x} {y} {w} {h}

    Remove the rectangle with the specified dimensions. If two or more rectangles have the same dimensions, then any one such rectangle may be removed. If no rectangle exists with these dimensions, it should be so reported.


    regionsearch {x} {y} {w} {h}

    Report all rectangles currently in the database that intersect the query rectangle specified by the regionsearch parameters. For each such rectangle, list out its name and coordinates. A regionsearch command should be rejected if the height or width are not greater than 0. However, it is (syntactically) acceptable for the regionsearch rectangle to be all or partly outside of the 1024 by 1024 world box.

    intersections

    Report all pairs of rectangles within the database that intersect.


    search {name}

    Return the information about the rectangle(s), if any, that have name {name}.

    dump

    Return a “dump” of the Skip List. The Skip List dump should print out each Skip List node, from left to right. For each Skip List node, print that node’s value and the number of pointers that it contains (depth).
