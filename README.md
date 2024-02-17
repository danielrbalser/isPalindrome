/*
Daniel Balser
COM 210: isPalindrome Assignment
 */
package ispalindrome;

import java.util.Scanner;

public class IsPalindrome {
    
    public static void main(String[] s) {
      
      Scanner palindrome= new Scanner(System.in);
      
      System.out.println("Input a word: ");
      String input= palindrome.nextLine();
          
      if(palindrome(input)){
          System.out.println("it is a palindrome");   
      }
      else{
          System.out.println("it is not a palindrome");
      }
      palindrome.close();
    }
    
    
    public static boolean palindrome (String str){
        
      char[] palindromeArray= str.toCharArray();
      int pdlength= palindromeArray.length;
      
      for (int i=0; i< pdlength/2; i++ ) {
          
            if ((Character.toLowerCase(palindromeArray[i])  !=  Character.toLowerCase(palindromeArray[pdlength - i - 1]))){               
                return false;
          }
    }
          return true;
  }
}
