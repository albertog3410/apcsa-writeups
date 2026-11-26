# Process Writeup
## Name: Alberto Gonzalez Jr
## Course: APCSA
## Period: 1
## Concept: Classes

### Context 
So far in APCSA, I have learned how to create **Classes** in java to seperate code for specific purposes. Classes are able to serve as blueprints or templates when creating objects. I also learned how to create various nested classes such as methods, accessors, constructors and mutator methods. The goal for this unit was to better understand classes and know how to create our own classes and nested classes moving forward. When starting this unit, looking at the concept of classes sounded simple to me. However, as I went through the <a href="https://courses.projectstem.org/courses/244882">projectSTEM</a> lessons I have seen that classes have a variety of complex algorithms based on what variables get returned. As well as new pieces of code that are used for nested classes to call other nested classes. Some of the definitions and code that I have used for this challenge are shown below:

* **Method** - Behavior of an object
* **Field/Attribute** = The state of an object
* **Parameter** - Variables that get declared inside of nested classes.
* **Constructors** - sets up instances of classes. They are inside the class, but are declared public with parameters. 
* ``public`` methods can be accessed from outside of the class
* ``private`` methods are restricted to only the class itself. 
* ``.toString()`` - returns a string representation of the object.
* ``this()`` - allows for the constructor to call another constructor within the same class.
* ``extends`` - can pass on whatever private variable to all new classes inside of a class. Creates a sub class.

```js
Public class Dog(String b) // parameter is String b
{
private String breed; // field
private int weight; // field
private String name; // field

public Dog(String b, int w, String n) { // constructor
breed = b;
weight = w;
name = n;
  }

Public class Dog extends Animal { // every animal has a breed, weight and name

  }
}
```

### The Task
The lesson that I feel that I learned the most from was a partner project activity. Where me and my partner Brianna had to create a class named ``Fracton`` that will an instance of a ``numerator`` and ``denominator``. Which the class will alter based on a variety of constructors, accessors and mutators. The final solution to the challenge that I have explained below can be seen in this <a href="https://github.com/hstatsep-students/apcsa-2027-assignment5-group-4/blob/main/Fraction.java">github page</a>.

### The Challenge and Solution




### Takeaways















