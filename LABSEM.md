-----------------------------------------------------------------------------------------------
EX 1(a) :
Imagine you're a software developer working on a project in a remote village. One day, an
elderly villager approaches you, intrigued by your work. They share stories of their youth,
when converting temperatures required complex calculations. Curious, they ask how your
program, which converts Celsius to Fahrenheit, might have impacted their past.

import java.io.*;
import java.util.*;
class Main
{
  public static void main (String[]args)
  {
	double a, b;
	Scanner inp = new Scanner (System.in);
	  a = inp.nextDouble ();
	  b = (a * 9 / 5 + 32);
	  System.out.println ("Temperature in Fahrenheit: " + b);
  }
}

-----------------------------------------------------------------------------------------------
EX 1(b) :
You are developing a BMI calculator for a health app. During the onboarding process, users
are prompted to input their weight and height. Implement a program where users can enter
their weight in kilograms and height in meters. Your program should then compute and
display their Body Mass Index (BMI). This tool helps users track their health and fitness
progress.

import java.io.*;
import java.util.*;
class Main
{
  public static void main (String[]args)
  {
	double weight, height;
	Scanner sc = new Scanner (System.in);
	  weight = sc.nextDouble ();
	  height = sc.nextDouble ();
	double bmi = weight / (height * height);
	  System.out.println ("Your BMI is: " + (int) bmi);
  }
}

--------------------------------------------------------------------------------------------------
EX 1(c) :
A group of friends explores an ancient code-breaking game. Each player inputs a single
character, unveiling hidden messages encoded in ASCII. As they decipher symbols, they
uncover clues to an ancient treasure. Help them by Implement a code to find a ascii value of
a character.

import java.io.*;
import java.util.*;
class Main
{
  public static void main (String[]args)
  {
	char a;
	Scanner sc = new Scanner (System.in);
	  a = sc.next ().charAt (0);
	int b = (int) a;
	  System.out.println ("Character: " + a);
	  System.out.println ("ASCII value: " + b);
  }
}

--------------------------------------------------------------------------------------------------
EX 1(d) :
You're tasked with developing a Java program for a binary-to-decimal converter tool. The
program expects users to input a binary number as a string. After receiving the input, it
converts the binary number to its decimal equivalent and prints the decimal value as an
integer.

import java.io.*;
import java.util.*;
class Main
{
  public static void main (String[]args)
  {
	Scanner sc = new Scanner (System.in);
	String st = sc.nextLine ();
	int a = Integer.parseInt (st, 2);
	  System.out.println ("Decimal value: " + (int) a);
  }
}

------------------------------------------------------------------------------------------------
EX 1(e) :
You're tasked with developing a simple currency converter tool. The program should prompt
users to input an amount in USD and convert it to EUR using a predefined exchange rate.
Upon input, it calculates and displays the converted amount in EUR. This tool facilitates
quick currency conversions, aiding users in international financial transactions and budget
planning.

import java.io.*;
import java.util.*;
public class Main
{
  public static void main (String[]args)
  {
	int a;
	Scanner sc = new Scanner (System.in);
	  a = sc.nextInt ();
	double b = (a * 0.92);
	  System.out.println ((int) b);
  }
}

-----------------------------------------------------------------------------------------------
EX 2(a) :
You're developing a retail billing system. Develop a program that calculates the total cost of
a purchase after applying discounts. If the purchase is over $1000, apply a 10% discount;
between $500 and $1000, apply 5%; otherwise, no discount. Prompt users for the purchase
amount, then display the total cost after discount.

import java.io.*;
import java.util.*;
class Main
{
  public static void main (String[]args)
  {
	Scanner sc = new Scanner (System.in);
	int a = sc.nextInt ();
	if (a > 1000)
	  {
		System.out.print ("Total cost after discount: " + (float) (a - (a * 0.1)));
	  }
	else if (a >= 500)
	  {
		System.out.print ("Total cost after discount: " + (float) (a - (a * 0.05)));
	  }
	else
	  {
		System.out.print ("Total cost after discount: " + (float) a);
	  }
  }
}

--------------------------------------------------------------------------------------------------
EX 2(b) :
You've created a simple program that prompts users to input a number. Once the number is
entered, the program analyzes it to determine if it's positive, negative, or zero. Based on this
analysis, it provides immediate feedback to the user regarding the nature of the number.

import java.util.Scanner;
public class Main
{
  public static void main (String[]args)
  {
	Scanner sc = new Scanner (System.in);
	double num = sc.nextDouble ();
	if (num > 0)
	  {
		System.out.println ("The entered number is positive.");
	  }
	else if (num < 0)
	  {
		System.out.println ("The entered number is negative.");
	  }
	else
	  {
		System.out.println ("The entered number is zero.");
	  }
  }
}

--------------------------------------------------------------------------------------------------
EX 2(c) :
You're building a geometry tool for analyzing triangles. Design a program that prompts users
to input the lengths of three sides of a triangle, determines if it's equilateral, isosceles, or
scalene using if statements, and displays the result.

import java.util.Scanner;
public class Main
{
  public static void main (String[]args)
  {
	Scanner sc = new Scanner (System.in);
	double a = sc.nextDouble ();
	double b = sc.nextDouble ();
	double c = sc.nextDouble ();
	if (a == b && b == c)
	  {
		System.out.println ("The triangle is equilateral.");
	  }
	else if (a == b || b == c || a == c)
	  {
		System.out.println ("The triangle is isosceles.");
	  }
	else
	  {
		System.out.println ("The triangle is scalene.");
	  }
  }
}

-------------------------------------------------------------------------------------------------
EX 2(d) :
You're developing a calendar utility to translate numerical representations of weekdays into
their respective names. Design a program prompting users to input a number representing a
day (1 for Monday, 2 for Tuesday, …, 7 for Sunday), and output the corresponding day name
using a switch statement.

import java.util.Scanner;
public class Main
{
  public static void main (String[]args)
  {
	Scanner scanner = new Scanner (System.in);
	int dayNumber = scanner.nextInt ();
	String dayName;
	switch (dayNumber)
	  {
	  case 1:
		dayName = "Monday";
		break;
		case 2:dayName = "Tuesday";
		break;
		case 3:dayName = "Wednesday";
		break;
		case 4:dayName = "Thursday";
		break;
		case 5:dayName = "Friday";
		break;
		case 6:dayName = "Saturday";
		break;
		case 7:dayName = "Sunday";
		break;
		default:dayName = "Invalid day number";
		break;
	  }
	System.out.println ("The corresponding day is " + dayName);
	scanner.close ();
  }
}

----------------------------------------------------------------------------------------
EX 3(a) :
Imagine you're a teacher creating a fun learning tool. With your program, generate
multiplication tables from 1 to 10 for each number entered. Every loop iteration reveals a
new set of answers, fostering a deeper understanding of multiplication.

import java.util.Scanner;
public class Main
{
  public static void main (String[]args)
  {
	Scanner sc = new Scanner (System.in);
	int num = sc.nextInt ();
	  System.out.println ("Multiplication table for " + num + ":");
	for (int i = 1; i <= 10; i++)
	  {
		System.out.println (num + " C " + i + " = " + (num * i));
	  }
  }
}

-------------------------------------------------------------------------------------------------
EX 3(b) :
Imagine you're a mathematical consultant assisting clients with number inquiries. A user
enters a positive integer, seeking its factors. Implement a program to help the user to find the
factors the numbers.

import java.io.*;
import java.util.*;
class Main
{
  public static void main (String[]args)
  {
	int num, fact = 1;
	Scanner sc = new Scanner (System.in);
	  num = sc.nextInt ();
	if (num > 0)
	  {
		System.out.print ("Factors of " + num + ": ");
		for (int i = 1; i <= num; i++)
		  {
			if (num % i == 0)
			  {
				System.out.print (i + " ");
			  }
		  }
	  }
  }
}

----------------------------------------------------------------------------------------------
EX 3(c) :
In a school competition, students are participating in a relay race. The race organizer needs
to arrange batons for each team. They have batons in sets, where each set contains a
certain number of batons. However, they need to find out the minimum number of sets
required to distribute an equal number of batons to each team. Implement a program to help
the race organizer find the minimum number of sets required to distribute batons equally
among all teams. Assume that each team requires the same number of batons, and the
number of batons in each set and the number of teams are provided as inputs

import java.util.Scanner;
public class Main
{
  public static int findLCM (int num1, int num2)
  {
	int lcm = (num1 > num2) ? num1 : num2;
	while (true)
	  {
		if (lcm % num1 == 0 && lcm % num2 == 0)
		  {
			return lcm;
		  }
		lcm++;
	  }
  }
  public static void main (String[]args)
  {
	Scanner scanner = new Scanner (System.in);
	int num1 = scanner.nextInt ();
	int num2 = scanner.nextInt ();
	int lcm = findLCM (num1, num2);
	System.out.println (+lcm);
	scanner.close ();
  }
}

-------------------------------------------------------------------------------------------
EX 3(d) :
You're tasked with developing a tool that computes squares of numbers within specified
limits. Imagine you're embarking on a journey through the realm of numbers, exploring their
squares. Implement a program using a do-while loop to iterate through these numbers,
uncovering their squares along the way.

import java.io.*;
import java.util.*;
public class Main
{
  public static void main (String args[])
  {
	Scanner sc = new Scanner (System.in);
	int lim = sc.nextInt ();
	  System.out.print ("Squares of numbers from 1 to " + lim + ": ");
	for (int i = 1; i <= lim; i++)
	  {
		System.out.print ((i * i) + " ");
	  }
  }
}

-----------------------------------------------------------------------------------------------
EX 4(a) :
Imagine you're a curious explorer delving into the world of prime numbers. Envision seekers
inputting their chosen numbers eagerly. Implement a program to traverse through each
number's factors up to its square root, determining its primality. Each iteration brings you
closer to unraveling the mysteries of prime numbers.

import java.io.*;
import java.util.*;
class Main
{
  public static void main (String[]args)
  {
	int num, div;
	Scanner sc = new Scanner (System.in);
	  num = sc.nextInt ();
	for (int i = 2; i < num - 1; i++)
	  {
		div = num % i;
		if (div == 0)
		  {
			System.out.println (num + " is not a prime number.");
			break;
		  }
		else
		  {
			System.out.println (num + " is a prime number.");
			break;
		  }
	  }
  }
}

-------------------------------------------------------------------------------------------
EX 4(b) :
Imagine you're a software developer creating a tool for numerical transformations. A user,
fascinated by number manipulation, inputs a positive integer. Implement a program to
gracefully reverse the digits of their number using a while loop, providing them with the
mirror image of their input for exploration

import java.util.*;
class Main
{
  public static void main (String[]args)
  {
	Scanner sc = new Scanner (System.in);
	int a = sc.nextInt ();
	int rev = 0;
	if (a > 0)
	  {
		while (a != 0)
		  {
			int rem = a % 10;
			  rev = rev * 10 + rem;
			  a /= 10;
		  }
		System.out.println ("Reversed number: " + rev);
	  }
	else
	  {
		System.out.println ("Error: Please enter a positive integer.");
	  }
  }
}

----------------------------------------------------------------------------------------
EX 5(a) :
Imagine you're developing software for a weather monitoring station. You're tasked with
creating a program to analyze temperature data stored in an array of doubles. Your goal is to
determine the maximum temperature recorded and its corresponding time index.

import java.util.*;
class Main
{
  public static void main (String[]args)
  {
	Scanner sc = new Scanner (System.in);
	int a = sc.nextInt ();
	double[] arr;
	int b = 0;
	  arr = new double[a];
	for (int i = 0; i < a; i++)
	  {
		arr[i] = sc.nextDouble ();
	  }
	double max = arr[0];
	for (int i = 0; i < a; i++)
	  {
		if (max < arr[i])
		  {
			max = arr[i];
			b = i;
		  }
	  }
	System.out.println ("Maximum Temperature: " + max);
	System.out.println ("Index of Maximum Temperature: " + b);
  }
}

------------------------------------------------------------------------------------------
EX 5(b) :
You're developing software for a temperature monitoring system. Your task is to create a
program that analyzes temperature data stored in an array of integers. The program finds
the highest recorded temperature, along with its index.

import java.util.*;
class Main
{
  public static void main (String args[])
  {
	int a;
	Scanner sc = new Scanner (System.in);
	  a = sc.nextInt ();
	int[] n = new int[a];
	for (int i = 0; i < a; i++)
	  {
		n[i] = sc.nextInt ();
	  }
	int y = 0, x = n[0];
	for (int i = 0; i < a; i++)
	  {
		if (n[i] > x)
		  {
			x = n[i];
			y = i;
		  }
	  }
	System.out.println ("Maximum Element: " + x);
	System.out.println ("Index of Maximum Element: " + y);
  }
}

--------------------------------------------------------------------------------------------
EX 5(c) :
Suppose you are building a leaderboard for a gaming competition. You need to determine
the player who achieved the second-highest score. Develop a program to find the
second-highest score from an array of player scores. Ensure that your program handles
scenarios where there might be ties for the highest score and ensures that the
second-highest score is accurately identified. Test your program with various test cases to
verify its correctness.

import java.util.Scanner;
public class Main
{
  public static int findSecondLargest (int[]arr)
  {
	int max = Integer.MIN_VALUE;
	int secondMax = Integer.MIN_VALUE;
	for (int num:arr)
		{ if (num > max)
		  {
		   secondMax = max;
		   max = num;}
		   else if (num > secondMax && num != max)
		   {
		   secondMax = num;}
		   }
		   return secondMax;}
		   public static void main (String[]args)
		   {
		   Scanner scanner = new Scanner (System.in);
		   int n = scanner.nextInt (); int[]arr = new int[n];
		   for (int i = 0; i < n; i++)
		   {
		   arr[i] = scanner.nextInt ();}
		   int secondLargest = findSecondLargest (arr);
		   System.out.println (+secondLargest); scanner.close ();       
	 }
    }
-----------------------------------------------------------------------------------------------
EX 6(a) :
You're developing software for a financial analytics tool. Your task is to design a program to
process a dataset stored in a 2D array of integers. The program calculates the total value of
all entries in the dataset and prints the result.

import java.util.*;
class Main
{
  public static void main (String[]args)
  {
	Scanner sc = new Scanner (System.in);
	int sum = 0;
	while (sc.hasNextLine ())
	  {
		String line = sc.nextLine ();
		if (line.isEmpty ())
		  {
			break;
		  }
		String[] n = line.split (" ");
	  for (String num:n)
		  {
			sum += Integer.parseInt (num);
		  }
	  }
	System.out.println ("Sum of all elements in the 2D array: " + sum);
  }
}

------------------------------------------------------------------------------------------------
EX 6(b) :
You're developing a data analysis tool for financial data. Your task is to develop a program to
process a dataset stored in a 2D array of doubles. The program identifies the highest value
in the dataset, along with its corresponding row and column indices.

import java.util.*;
class Main
{
  public static void main (String[]args)
  {
	Scanner sc = new Scanner (System.in);
	int a = sc.nextInt ();
	int b = sc.nextInt ();
	double[][] arr;
	int n = 0, m = 0;
	  arr = new double[a][b];
	for (int i = 0; i < a; i++)
	  {
		for (int j = 0; j < b; j++)
		  {
			arr[i][j] = sc.nextDouble ();
		  }
	  }
	double max = arr[0][0];
	for (int i = 0; i < a; i++)
	  {
		for (int j = 0; j < b; j++)
		  {
			if (max < arr[i][j])
			  {
				max = arr[i][j];
				n = i;
				m = j;
			  }
		  }
	  }
	System.out.println ("Maximum Element: " + max);
	System.out.println ("Row Index of Maximum Element: " + n);
	System.out.println ("Column Index of Maximum Element: " + m);
  }
}

-----------------------------------------------------------------------------------------
EX 6(c) :
You're developing software for a scientific data analysis tool. Your task is to design a
program to process matrices. The program initializes a 2D array representing a matrix and
computes its transpose, providing both the original and transposed matrices for further
analysis.

import java.util.*;
class Main
{
  public static void main (String args[])
  {
	int m, n;
	Scanner sc = new Scanner (System.in);
	  n = sc.nextInt ();
	  m = sc.nextInt ();
	int[][] a = new int[n][m];
	for (int i = 0; i < n; i++)
	  {
		for (int j = 0; j < m; j++)
		  {
			a[i][j] = sc.nextInt ();
		  }
	  }
	System.out.println ("Original Matrix:");
	for (int i = 0; i < n; i++)
	  {
		for (int j = 0; j < m; j++)
		  {
			System.out.print (a[i][j] + " ");
		  }
		System.out.println ("");
	  }
	System.out.println ("Transposed Matrix:");
	for (int i = 0; i < m; i++)
	  {
		for (int j = 0; j < n; j++)
		  {
			System.out.print (a[j][i] + " ");
		  }
		System.out.println ("");
	  }
  }
}

-------------------------------------------------------------------------------------------------
EX 7(a) :
As a linguistic data analyst, you're developing a Text Refinement Tool to process text inputs.
Users expect the tool to remove duplicate characters and count occurrences of vowels for
linguistic analysis. The tool accepts a string as input and redefines it, presenting the refined
text without duplicate characters and providing counts of vowels. Design a program that
meets these requirements efficiently.

import java.util.*;
public class Main
{
  public static void main (String[]args)
  {
	Scanner sc = new Scanner (System.in);
	String st = sc.nextLine ();
	int a = 0, e = 0, ii = 0, o = 0, u = 0, c = 0;
	for (int i = 0; i < st.length (); i++)
	  {
		char ch = st.charAt (i);
		if (ch == 'A' || ch == 'a')
		  a++;
		else if (ch == 'E' || ch == 'e')
		  e++;
		else if (ch == 'I' || ch == 'i')
		  ii++;
		else if (ch == 'O' || ch == 'o')
		  o++;
		else if (ch == 'U' || ch == 'u')
		  u++;
		else
		    c++;
	  }
	String str = " ";
	for (int i = 0; i < st.length (); i++)
	  {
		int f = 0;
		for (int j = 0; j < str.length (); j++)
		  {
			if (st.charAt (i) == str.charAt (j))
			  {
				f += 1;
			  }
		  }
		if ((f == 0) && (st.charAt (i) != ' '))
		  {
			str = str + st.charAt (i);
		  }
	  }
	System.out.println (str);
	if (c != st.length ())
	  {
		if (a > 0)
		  System.out.println ("a" + a);
		if (e > 0)
		  System.out.println ("e" + e);
		if (ii > 0)
		  System.out.println ("i" + ii);
		if (o > 0)
		  System.out.println ("o" + o);
		if (u > 0)
		  System.out.println ("u" + u);
	  }
	else
	  {
		System.out.println ("No vowels found.");
	  }
  }
}

--------------------------------------------------------------------------------------------------
EX 7(b) :
You are tasked with enhancing a popular text-editing app with a new feature to stylize text for
a more captivating presentation. With the app's extensive user base, efficiency and
performance are critical considerations. Users desire a feature that reverses the word order
of their input sentence while alternating the case of each letter, starting with uppercase for a
visually engaging effect.

import java.util.*;
class Main
{
  public static void main (String[]args)
  {
	Scanner sc = new Scanner (System.in);
	String n = sc.nextLine ();
	String w[] = n.split (" ");
	for (int i = w.length - 1; i >= 0; i--)
	  {
		for (int j = 0; j < w[i].length (); j++)
		  {
			if (Character.isUpperCase (w[i].charAt (j)))
			  System.out.print (Character.toLowerCase (w[i].charAt (j)));
			else if (Character.isLowerCase (w[i].charAt (j)))
			  System.out.print (Character.toUpperCase (w[i].charAt (j)));
		  }
		System.out.print (" ");
	  }
  }
}

------------------------------------------------------------------------------------------------
EX 7(c) :
You're developing a tool that reverse a given string S, such that the reversed string does not
contain any repeated characters or spaces. The program should eliminate any duplicate
characters and spaces while reversing the string.

import java.util.*;
class Main
{
  public static void main (String[]args)
  {
	Scanner sc = new Scanner (System.in);
	String n = sc.nextLine ();
	String w[] = n.split (" ");
	for (int i = w.length - 1; i >= 0; i--)
	  {
		for (int j = 0; j < w[i].length (); j++)
		  {
			if (Character.isUpperCase (w[i].charAt (j)))
			  System.out.print (Character.toLowerCase (w[i].charAt (j)));
			else if (Character.isLowerCase (w[i].charAt (j)))
			  System.out.print (Character.toUpperCase (w[i].charAt (j)));
		  }
		System.out.print (" ");
	  }
  }
}

--------------------------------------------------------------------------------------
EX 9(a) :
Imagine you're developing a utility to determine users' current ages for a registration
platform. Develop a program that prompts users to input their birth year.

import java.util.*;
import java.time.*;
class Main
{
  public static void main (String[]args)
  {
	int year;
	Scanner sc = new Scanner (System.in);
	  year = sc.nextInt ();
	if (year < 0)
	  {
		System.out.println ("Invalid input. Birth year cannot be negative.");
	  }
	else
	  {
		int cd = LocalDate.now ().getYear ();
		System.out.print (cd - year);
	  }
  }
}

---------------------------------------------------------------------------------------------
EX 9(b) :
In a financial application, Your task is to implement a function to round transaction amounts
to the nearest integer to ensure accurate representation of monetary values in reports and
accounting records.

import java.util.*;
class Main
{
  public static void main (String[]args)
  {
	Scanner sc = new Scanner (System.in);
	float a = sc.nextFloat ();
	int b = Math.round (a);
	  System.out.print ("Rounded number: " + b);
  }
}

-----------------------------------------------------------------------------------------------
