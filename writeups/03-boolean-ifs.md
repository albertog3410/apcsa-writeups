# Process Writeup
## Name: Alberto Gonzalez Jr
## Course: APSCA
## Period: 1
## Concept: If Statements

### Context 
So far in APCSA, I've learned how to use ``if`` and ``else if`` statements to change the flow of a program using mathamatical statements as well as ``&&`` or ``||`` symbols. With ``&&`` stating that two different conditions in an ``if`` statement must be true and ``||`` indicting that either condition in an ``if`` statement should be true. I also learned how to interpret other lines of code that use these statements to identify in what circumstances would a condition be true or false. 

When starting this unit, I thought that I had everything down packed since I have taken lessons that relate to this type of topic before. However, as I went through the <a href="https://courses.projectstem.org/courses/244882">projectSTEM</a> courses and started to learn about **Truth Tables** and **De Morgan's Law**, it started to become more difficult. Which made this unit one of the more eye opener concepts that I really needed to pay attention to despite knowing a little about it already. 

 * **Truth Table** - Helps to simpify certain conditions inside of an if statement. Checks to see what happens in every possible scanario whether one or more conditions will be true or false.  0 = TRUE, 1 = FALSE. 

```js
 A	   B	  A AND B
 
  0      0	     0
 
   0	   1	     1
 
   1	   0	     1
 
  1      1	     1

```

* **De Morgan's Law** - Method created by Augustus De Morgan to provide a systematic way to change boolean expressions. Mainly used to see if a condition can be said either differently or the opposite way around. For example, ``!(x <= 10 || y != 10)`` can be transformed to ``x > 10 && y == 10``.

  


### The Task
One of the ProjectSTEM lessons that I feel that I learned the most from was Lesson 4, where one of the coding activities involved creating a program that takes longitude and latitude inputs and tests if the longitude and latitude inputs are proper coordinates. The program would have to check if the latiude ranges from -90 to 90 and if the longitude ranges from -180 to 180.

### The Progress
After starting by creating the ``Scanner`` values and variables to contain the longitude and latitude coordinates, I formed the conditions to be in the ``if to else if`` format to test first if the longitude was between -180 and 180 and then if the latitude was between -90 and 90.

```js
    Scanner scan = new Scanner(System.in);
    System.out.println("Please enter the latitude:");
    double lat = scan.nextDouble();
    System.out.println("Please enter the longitude:");
    double log = scan.nextDouble();

if(log < -180 && log > 180) {
 System.out.println("longitude is incorrect");
}
else if(lat < -90 && lat > 90){
System.out.println("latitude is incorrect");
} else {
System.out.println("The location: " + lat + ", " + log);
}
```
### The Challenge and Solution
However, when I put this into the program, it would allow for numbers above and below the limited amount to be printed in the ``else`` statement. Due to this road block, I decided to look back into the videos and I noticed that you can use boolean values to change from a true or false statement. Boolean statements are pretty much similar to Strings, but instead of holding an actual String of words, boolean holds true or false statements. Think of it as an on and off switch, If you want to hold the value of what an off switch is, the boolean is set equal to false. But if you want the value to be on, the boolean would have to be set equal to true. Using this, I created two boolean statements that first held true statements for both the ``log`` and ``lat`` double variables. Then I changed the if statements to make each one look out for a decimial number that is either greater than or less than the two desired amounts using **De Morgan's Law**. This way,  I can make the boolean variables become false if either ``if`` statement was true.

```js
    boolean latTrue = true;
    boolean logTrue = true;
        if (lat < -90 || lat > 90) {
            System.out.println("latitude is incorrect");
            latTrue = false;
        } 
        if (log < -180 || log > 180) {
            System.out.println("longitude is incorrect");
            logTrue = false;
        } 
        if(latTrue && logTrue) {
        System.out.println("The location: " + lat + ", " + log);
        }
```    


### Another Challenge 
Another challenge that I had did not have to do with any of the lessons, but instead of with the end of the unit exam. Going into this, I hadn't taken any notes because I thought that I would be fine being that I managed to do alright without them on the previous exam. However, this backfired on me when trying to solve a multiple choice problem that had to do with the truth tables. The problem used the same table that I wrote up in the context section earlier, but the right columns had to be three false and one true at the end( 1 - 1 - 1 0). This question took me so long that I had to use the extra time I had on exam's in order to complete, which meant staying to complete the exam after class ended. It was like my mind just went blank, it which me have a harder time with the other problems. Despite this, I did my best to remain patient and take my time and write down the truth tables method on a piece of paper in order to find the correct answer. Despite not getting the right answer on that question, I took my best guess and used the same method on the other questions.

### Takeaways

* I learned that **De Morgan's Law** is not just another way to simplify ``if`` statements, it also a way to debug and analyze conditions in case of any errors. Which is a method that really helped me when doing Lesson four of ProjectSTEM.
* **Problem Decomposition** - While this is a skill that I usually struggle in, using the truth table method really did help me in analyzing the how and why of boolean conditions. As well as what would it mean if one value comes to be true or false and how it changes the output entirely.
*  **Practice Makes Perfect** - Despite the teacher giving the class practice problems, I did not use them because I thought that I would be fine without them. But after getting 10/20 on the exam, I realized that I needed more practice with this unit than I had anticipated. From this, I learned that even if its just a little while that using the practice was going to be the one thing that could of helped me complete the exam faster.












