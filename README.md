# csx730-list

**DUE FRI 2019-02-01 (Feb 1) @ 11:55 PM**

This repository contains the skeleton code for the `csx730-list` project
assigned to the students in the Spring 2019 CSCI 4730/6730 class
at the University of Georgia.

## Intrusive Linked List

## Project Requirements

This assignment is worth 100 points. The lowest possible grade is 0, and the 
highest possible grade is 110 (if you are enrolled in CSCI 4730).

### Functional Requirements

A functional requirement is *added* to your point total if satisfied.
There will be no partial credit for any of the requirements that simply 
require the presence of a function related a particular functionality. 
The actual functionality is tested using test cases.

1. __(80 points) Implement `csx730_list.h` functions in `csx730_list.c`.__
   Each of the functions whose prototype appears in `csx730_list.h` must
   be implemented correctly in `csx730_list.c`. Here is a list of the
   functions:

   * (10 points) `void list_init(struct list_node *);`
   * (10 points) `void list_append(struct list_node *, struct list_node *);`
   * (10 points) `void list_append_all(struct list_node * head, ...);`
   * (10 points) `void list_insert(struct list_node *, struct list_node *, size_t);`
   * (10 points) `struct list_node * list_get(struct list_node *, size_t);`
   * (10 points) `struct list_node * list_remove(struct list_node *, size_t);`
   * (10 points) `size_t list_size(struct list_node *);`
   * (10 points) `size_t index_of(struct list_node *, struct list_node *);

   The documentation for each function is provided directly in
   `csx730_list.h`. Students should not modify the prototypes for these
   functions in any way--doing so will cause the tester used by the
   grader to fail. 

1. __(20 points) Implement `csx730_list.h` macros in `csx730_list.h`.__
   Each of the macros partially defined in `csx730_list.h` must be
   implemented correctly directly in `csx730_list.h`. Here is a list of the
   macros:

   * `list_object(node, type, member)`
   * `list_foreach(head, node)`

   The documentation for each macro is provided directly in `csx730_list.h`. Students will
   need to modify `csx730_list.h` to properly implement the macros. Currently, each
   macro expands to `0`. 

### 6730 Requirements

For the purposes of grading, a 6730 requirement is treated as a non-functional requirement
for students enrolled in CSCI 6730 and a functional requirement for students enrolled in
CSCI 4730. 

1. __(5 points) [PRETTY] Implement pretty printing for your list implementation.__ Add the
   following prototype to `csx730_list.h` (and implement it in `csx730_list.c): 

   ```c
   /**
    * Prints the list to a line in standard output with the help of @p to_string. Assume
    * @p to_string returns a new string representation of the structure a node intrudes upon,
    * formatted similarly to <tt>data(7, 2.0)</tt>. Then, the output that this function produces
    * to standard output might look like the following for a list containing three nodes:
    * <tt>{ data(7, 2.0), data(3, 2.2), data(9, 1.4) }</tt>. You should assume that the memory
    * for the string returned by @p to_string was obtained with @c malloc(3) and should be freed
    * with @c free(3). You may assume that all nodes in the list intrude on the same type of
    * structure. 
    * @param head head of the list
    * @param to_string function that returns a string representaton of a node's enclosing structure
    */
   void list_pretty_print(struct list_node * head, char * (* to_string)(struct list_node *));
   ```

1. __(5 points) [DRIVER] Provide code in `csx730_list_driver.c` that demos your implementation.__
   Provide a commented, functional demo in the `main` function that illustrates each list
   function and macro. This demo should clearly show that each function works correctly. In order
   to recieve points for this requirement, you must include at least one structure that is involved
   with two or more lists. Output to standard output is expected. 

### Non-Functional Requirements

A non-functional requirement is *subtracted* from your point total if not satisfied. In order to
emphasize the importance of these requirements, non-compliance results in the full point amount
being subtracted from your point total. That is, they are all or nothing.

1. __(100 points) Build Compliance:__ Your project must compile on Nike
   using the provided `Makefile` and `gcc` (GCC) 8.2.0. Your code must compile,
   assemble, and link with no errors or warnings. The required compiler
   flags for this project are already included in the provided `Makefile`.

1. __(100 points) `SUBMISSION.md`:__ Your project must include a properly formatted 
   `SUBMISSION.md` file that includes, at a minimum, the following information:

   * __Author Information:__ You need to include your full name, UGA email, and
     which course you are enrolled in (e.g., CSCI 4730 or CSCI 6730).

   * __Implementation Overview:__ You need to include a few sentences that provide an overview
     of your implementation.
     
   * __6730 Requirements:__ You need to include a list of the 6730 requirements that you
     would like the grader to check. These requirements will only be checked if you
     include them in this list. 
     
   * __Reflecton:__ You need to provide answers to the following questions:

     1. What do you think was the motivation behind assigning this project in this class?
     1. What is the most important thing you learned in this project?
     1. What do you wish you had spent more time on or done differently?
     1. What part of the project did you do your best work on?
     1. What was the most enjoyable part of this project?
     1. What was the least enjoyable part of this project?
     1. How could your instructor change this project to make it better next time?

   A properly formatted sample `SUBMISSION.md` file is provided that may be modified to
   help fulfill this non-functional requirement.

1. __(25 points) Memory Leaks:__ Your submission should not result in any memory leaks.
   You an check this with `valgrind(1)`.

1. __(25 points) Code Documentation:__ Any new functions or macros must be properly documented
   using Javadoc-style comments. An example of such comments can be seen in the souce code
   provided with the project.

## Submission Instructions

You will still be submitting your project via Nike. Make sure your project files
are on <code>nike.cs.uga.edu</code>. Change into the parent directory of your
project directory. If you've followed the instructions provided in earlier in this
document, then the name of your project directory is likely `csx730-list`.
While in your project parent directory, execute the following command: 

```
$ submit csx730-list csx730
```

If you have any problems submitting your project then please make a private Piazza
post to "Instructors" as soon as possible. 

<hr/>

[![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC%20BY--NC--ND%204.0-lightgrey.svg)](http://creativecommons.org/licenses/by-nc-nd/4.0/)

<small>
Copyright &copy; Michael E. Cotterell and the University of Georgia.
This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/">Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License</a> to students and the public.
The content and opinions expressed on this page do not necessarily reflect the views of nor are they endorsed by the University of Georgia or the University System of Georgia.
</small>
