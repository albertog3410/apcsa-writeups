import java.util.Scanner;
// worked with Tina 
class Assignment4 
{
  public static void main(String[] args) 
  {
        
    /* Write your code here */
    Scanner scan = new Scanner(System.in);
    
    System.out.println("Type the message to be shortened");
    String message = scan.nextLine().toLowerCase();
    int vowels = 0;
    int repeats = 0;
    String result = "";
    for(int i = 0; i < message.length(); i++){
    String letter = message.substring(i, i + 1);
     if(i != 0 && !message.substring(i - 1, i).equals(" ") && (letter.equals("a") || letter.equals("e") || letter.equals("i") || letter.equals("o") || letter.equals("u")) ) {
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
    
    
    String a2space = "";
    String a2part = "";
    String a2message = "";
    int u = 0;
    for (int i = 0; i < message.length(); i++)
    {
    String letter = message.substring(i, i + 1);
      if (!(letter.equals(" "))) // if there is a space
      {
        a2space += letter;
      }
    }
    for (int i = 0; i < a2space.length(); i++) // checks to see if there are any spaces
    {
      if (a2part.indexOf(a2space.substring(i, i + 1)) == -1)
      {
        a2part += a2space.substring(i, i + 1);
      }
    }
    for (int i = 0; i < a2part.length(); i++)
    {
      for (int i2 = 0; i2 < a2space.length(); i2++)
      {
        if ((a2part.substring(i, i + 1)).equals(a2space.substring(i2, i2 + 1)))
        {
          u++; 
        }
      }
      a2message += u + a2part.substring(i, i + 1);
      u = 0;
    }
    int a2unique = a2part.length();
    int a2saved = message.length() - a2message.length();


    /// Algorithm 2
    System.out.println("\nAlgorithm 2");
    System.out.println("Unique characters found: " + a2unique);
    System.out.println("Algorithm 2 message: " + a2message);
    System.out.println("Algorithm 2 characters saved: " + a2saved);

    
    
    
    

  }
}
