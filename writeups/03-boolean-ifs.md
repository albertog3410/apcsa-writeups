# Process Writeup
## Name: Alberto Gonzalez Jr
## Course: APSCA
## Period: 1
## Concept: If Statements

### Context 
So far in APCSA, I've learned how to use ``if`` and ``else if`` statements to change the flow of a program using mathamatical statements as well as ``&&`` or ``||`` symbols. With ``&&`` stating that two different conditions in an ``if`` statement must be true and ``||`` indicting that either condition in an ``if`` statement should be true. I also learned how to interpret other lines of code that use these statements to identify in what circumstances would a condition be true or false. When starting this unit, I thought that I had everything down packed since I have taken lessons that relate to this type of topic before. However, as I went through the <a href="https://courses.projectstem.org/courses/244882">projectSTEM</a> courses and started to learn about **Truth Tables** and **De Morgan's Law**, it started to become more difficult.


**Truth Table** - Helps to simpify certain conditions inside of an if statement. Checks to see what happens in every possible scanario whether one or more conditions will be true or false.  0 = TRUE, 1 = FALSE. 

``js
 A	   B	  A AND B
 0     0	     0
 0	   1	     1
 1	   0	     1
1      1	     1
``

**De Morgan's Law** - Method created by Augustus De Morgan to provide a systematic way to change boolean expressions. Mainly used to see if a condition can be said either differently or the opposite way around. For example, ``!(x <= 10 || y != 10)`` can be transformed to ``x > 10 && y == 10``.


### The Task 
One of the ProjectSTEM lessons that I feel that I learned the most from was Lesson 4, where one of the coding activities involved creating a program that takes longitude and latitude inputs and tests if the longitude and latitude inputs are proper coordinates. The program would have to check if the latiude ranges from -90 to 90 and if the longitude ranges from -180 to 180.

### The Progress




