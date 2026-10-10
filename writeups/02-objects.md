# Process Writeup
## Name: Alberto Gonzalez Jr
## Course: APSCA
## Period: 1
## Concept: Objects

### Context 
So far in APSCA, I learned how to create **Objects** and use them in order to form more complex forms of structures when it comes to arrays and ``Strings``. I also learned how to apply certain operators in order for the computer to output specific differences between objects and instances. The final <a href="https://courses.projectstem.org/">projectstem.org</a> lessons were tough, but staying on top of my note-taking really helped me understand the unit.

### What are Objects
What makes Objects different from Pritmitives is that Pritmitives are immutable values, or values that cannot be changed after it is created and stores the value directly inside their memory. On the other hand, Objects are the opposite, and stores the memory's address. In other words, Primitive data types can only hold one piece of information at a time. While class data types(reference data types) store the memory address that points to where the data is kept. Which is stored inside of an ``instance``, which is what is formed from a class that is its own unique object. There are also various methods that can be used to call certain parts of a string such as:


* ``.length()`` - returns the number of characters inside of a string. 
* ``.equals()`` - Compares two strings to see if they are equal, uses a boolean(true or false) statement to tell whether the two strings are the same. 
* ``substring()`` - returns the index of the original string.
* ``.compareTo()`` - Compares two strings or objects of the same class and returns a value relative to their order with each other ALPHABETICALLY. 
* ``indexOf()`` - finds a point in a string where a certain letter is used and returns its substring location.

These are all examples of static methods, which are methods that belong to the class of an object.
### Challenge I Had with Math Functions
The real challenge was going through the non-static methods. Which are the methods that are used for mathematic equations. When going into this, I thought that I was going to be alright going through these lessons considering that most of methods were straight forward. Some of those included:

* ``Math.abs()`` - performs an absolute value calculation for either int or double. Takes away the negative sign and puts its positive value. 

* ``Math.pow(double base, double exponent)`` - does exponent math, accepts doubles for both the base and parameter. 

* ``Math.sqrt(double x)`` - calculates the square root. 

The method that confused me the most was ``Math.random()`` which is used to return a random value from two min and max values. The challenge was that I had to use ``math.random()`` in order create three different integers that prints from a minimum value of 2 to a maximum value of a user's input plus 2. What confused me the most was calculating the minimum and maximum integer values so that all three integers will not equal the same number. Originally, I did ``(Math.random() * (n + 2) + 2)`` thinking that since just ``random()`` equals a minimum value of 0, that adding it by 2 would set the minimum to 2 and then the maximum plus that amount. However this ended up not being the case and it took me a long while figuring out how to get the desired result. Due to this, I had to look back at the overview of the lesson to get a better idea. Turns out there was a specific method that involved adding ``(n + 1)`` instead of ``(n + 2)``. The reason that it was ``(n + 1)`` was because that ``Math.random()`` counts for the total amount of possible integer choices. So if I put in 6 as an input with the original code, the computer would think that I was accounting for 8 possible integers instead of the 6 in between 2 and 8. 


###### Solution
```js
Scanner scan = new Scanner(System.in);
System.out.println("Enter a positive integer:");
int n = scan.nextInt();
System.out.println((int) (Math.random() * (n + 1)) + 2);
System.out.println((int) (Math.random() * (n + 1)) + 2);
System.out.println((int) (Math.random() * (n + 1)) + 2);
```



### Takeaways

* I learned how to apply **``Math.random()``** in getting random integers from 0.0 to 1 and understanding its formula using ``Math.floor(Math.random() * (max - min + 1)) + min`` to get the desired minimum and maximum.
  
* **Pay Attention to Detail** Even something that seems minor, like a single line of code, plays a critical role in how the entire system functions. Going through how Math.random() works helped me to recognize not only how it works, but also seeing how code like this works behind the scenes.
* **Ask for Help When Needed** - If I would of asked for help on how to use ``Math.random()`` sooner, I probably would of been done with that lesson sooner. Which was something that I had to learn on my own, but navigating it independently gave me a much deeper understanding of how the logic actually works.

