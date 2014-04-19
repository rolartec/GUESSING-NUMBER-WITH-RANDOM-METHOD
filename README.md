GUESSING-NUMBER-WITH-RANDOM-METHOD
==================================

LAB # 1 WEEK #9  GUESSING NUMBER WITH RANDOM METHOD


//  	BY REINA OLARTE

//		WEEK # 9	GUESSING NUMBER WITH RANDOM  METHOD


import java.util.Scanner;

// imports the scanner class

public class GuessingMNumberwithRandomMethod 
{
	public static void main( String[]args)
	{
		//Create the Scanner to input the number
		
		Scanner input = new Scanner(System.in);

		//instantiate random number
		
		RandomNumber GuessedNumber = new RandomNumber();

		//		 VARIABLES
		
		int UserNumber;
		
		int computerNumber;
		
		boolean siga = true;
		
		String sino;

		while(siga)
		{
			computerNumber = GuessedNumber.GetANumber_Between_1_and_10();

			System.out.println("Welcome to the game\nPlease enter a digit from 0 to 10:");
			UserNumber = input.nextInt();

			if (computerNumber == UserNumber)
			{
				System.out.println("You Guessed the right number");
				System.out.printf("Your number %d, Random number %d" , UserNumber, computerNumber);
			}

			else
				{
					if (computerNumber < UserNumber)
					{
						System.out.println("You Guessed to High");
						System.out.printf("Your number %d, Random number %d" , UserNumber, computerNumber);
					}
					else
					{	System.out.println("You Guessed to Low");
					System.out.printf("Your number %d, Random number %d" , UserNumber, computerNumber);
					}//end else	
				}//end else
			System.out.println("\nWould you like to continue?\nPress Y for yess N for no");
			sino = input.next();

			if (sino.toUpperCase().startsWith("Y"))
			{
				siga = true;
			}
			else
			{
				siga = false;
			}


		}//end loop
	}//End main

}//End class
