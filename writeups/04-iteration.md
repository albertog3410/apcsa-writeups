# Process Writeup
## Name: Alberto Gonzalez Jr
## Course: APSCA
## Period: 1
## Concept: Iteration

### Context 
So far in APCSA, I have learned how to use **Loops** to keep a condition true until it is proven false. Which is called **Iteration**, repeating a process to get a series of possible outcomes. In order to do this, I learned how to use two different forms of loops that I have learned last year when learning about Javascript, ``while()`` and ``for()`` loops. Similar to if statements, I also learned how to interpret the outputs for these kinds of loops. I had a difficult time with this unit considering that I struggled with knowing how to use loops, but as I broke down how the code iterates through the loops using the <a href="https://courses.projectstem.org">ProjectSTEM lessons</a>, it became a little easier to understand. 

* ``while()`` - Repeats a condition as long as it is true, used when you need your loop to be controlled by user input.
* ``for()`` - Sets a variable that either increases or decreases based condition, used when you want to output the number of times something appears or if you want to do a said amount of things a certain amount of times. 

### The Task
The ProjectSTEM lesson that I feel that I learned the most from was the **String Shortener** lesson. Where me and my partner, Tina had to create two sets of Algorithms that were meant to change the inputted string based on the number of vowels it has using ``for()`` loops. With the first algorithm removing vowels and repeated non-vowels if they were not at the start of the string. Followed by the second algorithm creating a string by taking each unique character in the message in the order they first appear and putting that letter and the number of times it appears in the original message into the shortened string. The challenge that we had run into mainly focused on the first algorithm. To see the solution of how we solved both algorithms, <a href="https://github.com/albertog3410/apcsa-writeups/blob/main/writeups/04-iteration.md">here</a> is the link.

### The Progress 
We started off by creating the ``for()`` statements to loop through each and every character of the string ``message`` and creating ``int`` values to hold the number of ``vowels`` and ``repeats`` in the string. As well as an empty string named ``result`` so that we can add any string in message that was not a vowel or repeated non-vowel. Then we created if statements that checked to see if any of the indexes in the string was a vowel or had repeated letters. 

```js
    for(int i = 0; i < message.length() - 1; i++) {
    String letter = message.substring(i, i + 1); // letter = a letter in the string
     if(i != 0 && !message.substring(i,i-1).equals(" ") && (letter.equals("a") || letter.equals("e") || letter.equals("i") || letter.equals("o") || letter.equals("u")) ) {
       vowels++;
     }
     else if(i != 0 && letter.equals(message.substring(i-1,i))) {
       repeats++;
     }
      else {
        result += letter;
      }
      
      
     }
    System.out.println("\nAlgorithm 1");
    System.out.println("Vowels removed: " + vowels);
    System.out.println("Repeats removed: " + repeats);
    System.out.println("Algorithm 1 message: " + result);
    System.out.println("Algorithm 1 characters saved: " + (message.length() - result.length() ));
    

```


### The Challenge
However, when I put this into the program, the error would print out as an error that said that the length of the string was extended. 



Even when I fixed this, the amount of characters saved was one more than the desired amount.









### Takeaways
**.length() vs .length() - 1** - I learned that ``.length() - 1`` gives the index of the very last character in a string. While ``.length()`` returns the total count of strings, which was the required output for the assignment. I would have never known this if Tina hadn't pointed it out considering that I originally thought that they meant the same thing.
**Patience** - While trying to solve the first algorithim, I was not having the patience to just sit there with the problem knowing that I had other assignments to complete for other classes. But using the strategy to help break down the ``for()`` loop to see where I went wrong really helped me to think with a clear head. 
**Pay Attention to Detail** - I did not even notice that I had ``.length() - 1`` in the loop at first. Even when I did notice it, I did not care due to me thinking that were the same thing, but were not. Now I realized that in future units, I should really pay attention to what I type in code because one number that change the entire algorithm as a whole. 

