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
The lesson that I feel that I learned the most from was a partner project activity. Where me and my partner Brianna had to create a class named ``Fracton`` that will an instance of a ``numerator`` and ``denominator`` in our IDE. Which the class will alter based on a variety of constructors, accessors and mutators. The final solution to the challenge that I have explained below can be seen in this <a href="https://github.com/hstatsep-students/apcsa-2027-assignment5-group-4/blob/main/Fraction.java">github page</a>.

### The Challenge and Solution
When me and Brianna split the work, my task was to create mutator methods that would add and another method that would multiply the current fraction by another fraction based on ``fraction other`` parameters in both methods. Starting with the multiply mutator, I originally thought that I had to use return in order to get the ``numerator`` and ``denominator``. Then call the methods that return the numerator and denominator so that it can be multiplied by ``other``. 

```js
    public void multiply(Fraction other){
      return getNumerator() * other.getNumerator();
      return getDenominator() * other.getDenominator();
    }
```
However, when I put this through the terminal using ``jcar runner_Fraction``, the terminal shows an error when calling the multiply mutator. Due to this, I asked Brianna to see what I was doing wrong and she said that I needed to add the ``this()`` method. Not knowing what that was I asked her and Brianna said that ``this()`` calls a constructor while inside another constructor so that you can use those same variables inside the desired constructor. As a result, I substituted ``return`` for the ``this()`` method so that it can use the numerator and denominator values in the method.
```js
    public void multiply(Fraction other){
         this.setNumerator(this.getNumerator() * other.getNumerator());
         this.setDenominator(this.getDenominator() * other.getDenominator());
    }
```
With the ``multiply`` method done, I then went on to the ``add`` mutator. I originally thought that it was the same form of code, only that we had to add instead of subtract. For a while, I even kept this originial code the same because me and my partner thought that we had done everything the assignment was asking of us.
```js
public void add(Fraction other){
         this.setNumerator(this.getNumerator() + other.getNumerator());
         this.setDenominator(this.getDenominator() + other.getDenominator());
    }
```
However, when I went again to test the code myself through the terminal, I noticed that the fractions were not adding correctly. 

```js
    public void add(Fraction other){
         this.setNumerator((this.getNumerator() * other.getDenominator()) + (other.getNumerator() * this.getDenominator()));
         this.setDenominator(this.getDenominator() * other.getDenominator());
    }
```






### Takeaways
* Learned how to use ``this()`` - Which allows for the constructor to call another constructor within the same class. Being that I never used this method in the ProjectSTEM lessons, I did not think too much of this and did not put it in my notes. Which ended up being a mistake when I had to do this project. 

* **Pay Attention to Detail** - Being that I had to see the project's instructions again, I realize that I am not the most attentive person. Which is a skill that I still need to improve on going forward if I want to understand how to code with not just Java, but also other programming languages. If I hadn't noticed the error before the teacher started grading the assignment, me and my partner probably would of got a lower grade than what we had right now. 
* **Ask for Help When Needed** - Which is something that I do not do a lot  .If it was not for Brianna, I wouldn't have known about the ``this()`` method and how to use it for this project.












