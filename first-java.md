1) Write a program to print whether a number is even or odd, also take input from the user.



import java.util.Scanner;

public class EvenOdd {

    public static void main(String[] args) {

        Scanner reader = new Scanner(System.in);

        System.out.print("Enter a number: ");
        int num = reader.nextInt();

        if(num % 2 == 0)
            System.out.println(num + " is even");
        else
            System.out.println(num + " is odd");
    }
}



2) Take name as input and print a greeting message for that particular name.



import java.util.Scanner;

public class Basic3 {

	public static void main(String[] args) {

		System.out.println("Please enter your name:");

		Scanner input = new Scanner(System.in);
		String name = input.next();

		System.out.println("Hello " + name);

	}

}



3) Write a program to input principal, time, and rate (P, T, R) from the user and find Simple Interest



import java.util.Scanner;

public class KboatCompoundInterest
{
    public static void main(String args[]) {
        Scanner in = new Scanner(System.in);
        System.out.print("Enter Principal: ");
        double p = in.nextDouble();
        System.out.print("Enter Rate: ");
        double r = in.nextDouble();
        System.out.print("Enter Time: ");
        int t = in.nextInt();
        double amt = p;
        for (int i = 1; i <= t; i++) {
            double interest = (amt * r * 1) / 100.0;
            amt += interest;
            System.out.println("Amount after " + i 
                                + " year = " + amt);
        }
    }
}



4) Take in two numbers and an operator (+, -, *, /) and calculate the value. (Use if conditions)



import java.util.Scanner;

class Main {
  public static void main(String[] args) {

    char operator;
    Double number1, number2, result;

    // create an object of Scanner class
    Scanner input = new Scanner(System.in);

    // ask users to enter operator
    System.out.println("Choose an operator: +, -, *, or /");
    operator = input.next().charAt(0);

    // ask users to enter numbers
    System.out.println("Enter first number");
    number1 = input.nextDouble();

    System.out.println("Enter second number");
    number2 = input.nextDouble();

    switch (operator) {

      // performs addition between numbers
      case '+':
        result = number1 + number2;
        System.out.println(number1 + " + " + number2 + " = " + result);
        break;

      // performs subtraction between numbers
      case '-':
        result = number1 - number2;
        System.out.println(number1 + " - " + number2 + " = " + result);
        break;

      // performs multiplication between numbers
      case '*':
        result = number1 * number2;
        System.out.println(number1 + " * " + number2 + " = " + result);
        break;

      // performs division between numbers
      case '/':
        result = number1 / number2;
        System.out.println(number1 + " / " + number2 + " = " + result);
        break;

      default:
        System.out.println("Invalid operator!");
        break;
    }

    input.close();
  }
}



5) Take 2 numbers as input and print the largest number.



import java.util.Scanner;

public class LargestofTwo {
	private static Scanner sc;
	public static void main(String[] args) 
	{
		int number1, number2;
		sc = new Scanner(System.in);
		
		System.out.print(" Please Enter the First Number : ");
		number1 = sc.nextInt();	
		
		System.out.print(" Please Enter the Second Number : ");
		number2 = sc.nextInt();	
		
		if(number1 > number2) 
	    {
			System.out.println("\n The Largest Number = " + number1);          
	    } 
	    else if (number2 > number1)
	    { 
	    	System.out.println("\n The Largest Number = " + number2);        
	    } 
	    else 
	    {
	    	System.out.println("\n Both are Equal");
	    }		
	}	



6) Input currency in rupees and output in USD.



import java.util.Scanner;

public class MathUnitConversions17 {

	public static void main(String[] args) {

		float rupees;

		Scanner in = new Scanner(System.in);

		System.out.println("Please enter rupees:");

		rupees = in.nextLong();

		float dollars = rupees / 75 ;

		System.out.println(dollars + " Dollars");
	}
}



7)To calculate Fibonacci Series up to n numbers.



import java.util.*;
 
class fiboN
{
 public static void main(String args[])
 {
         int i,c=0,n;
 Scanner sc = new Scanner(System.in);
 System.out.println("Enter a number to generate fibonacci series upto nth term");
     n=sc.nextInt();
   int a=0;
   int b=1;
 
 System.out.println("Fibonacci series upto "+n+" is :-");
   while(c<=n)
   {
       System.out.print(c+" ");
       a=b;
       b=c;
       c=a+b;
   }
 }
}



8)To find out whether the given String is Palindrome or not.



import java.util.Scanner;
 
class ChkPalindrome
{
   public static void main(String args[])
   {
      String str, rev = "";
      Scanner sc = new Scanner(System.in);
 
      System.out.println("Enter a string:");
      str = sc.nextLine();
 
      int length = str.length();
 
      for ( int i = length - 1; i >= 0; i-- )
         rev = rev + str.charAt(i);
 
      if (str.equals(rev))
         System.out.println(str+" is a palindrome");
      else
         System.out.println(str+" is not a palindrome");
 
   }
}



9)To find Armstrong Number between two given number.




import java.util.Scanner;
public class ArmstrongBetweenTwoNumbers {
   public static void main(String args[]){
      int num1, num2;
      Scanner sc = new Scanner(System.in);
      System.out.println("Enter the first number ::");
      num1 = sc.nextInt();
      System.out.println("Enter the second number ::");
      num2 = sc.nextInt();

      for (int i = num1; i<num2; i++){
         int check, rem, sum = 0;
         check = i;
         while(check != 0) {
            rem = check % 10;
            sum = sum + (rem * rem * rem);
            check = check / 10;
         }
         if(sum == i){
            System.out.println(""+i+" is an Armstrong number.");
         }
      }
   }
}
