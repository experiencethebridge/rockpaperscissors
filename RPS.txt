/*Sean O'Brien 
Rock Paper Scissors
*/

#include <stdio.h>/*is a statement which tells the compiler to insert the contents of stdio 
at that particular place. In C/C++ we use some functions like printf(), scanf(), cout,cin. 
These functions are not defined by the programmer. These functions are already defined 
inside the language library.*/

#include <windows.h>/* is a Windows-specific header file for the C and C++ programming 
languages which contains declarations for all of the functions in the Windows API, all 
the common macros used by Windows programmers, and all the data types used by the various 
functions and subsystems.*/

#include <time.h>/*time.h (used as ctime in C++) is a header file defined in the C 
Standard Library that contains time and date function declarations to provide standardized 
access to time/date manipulation and formatting.*/

#include <stdlib.h>/*is the header of the general purpose standard library of C 
programming language which includes functions involving memory allocation, process 
control, conversions and others. It is compatible with C++ and is known as cstdlib 
in C++. The name "stdlib" stands for "standard library".*/
 
int main()
{
	  //local variable definitions	
      int x = 0; 
	  /*In order to use a do/while as was instructed, I need an exit argument.  
	  I will only allow 5x's*/
	  do{
		x = x + 1;
		//nested variable definitions
		int Selection = 0;
		int Random = 0;
		Random = (rand() % 3) + 1;
		
		//Messages and prompts to players
		printf("\nSean's Rock, Paper, Scissors!  You have 5 chances.");
		printf("\n1\tRock\n");
		printf("2\tPaper\n");
		printf("3\tScissors\n");
		printf("\nPlease enter a selection: ");
		scanf("%d", &Selection);/*scanf() returns total number of Inputs Scanned successfully*/
		
			//beginning of the nested if loops
			if (Selection < 1 || Selection > 3) {
			printf("\nPlease enter a valid choice!\n");
			}
     
			if (Selection == 1 && Random == 1) {
			printf("\nYou picked %d\n", Selection);
			printf("\nThe Computer picked %d\n", Random);
			printf("\nIt's a tie!\n");
			}
			       /*&& is a boolean operator, which means "and". For it to become true, 
					both of the statements must be true. If one of them is false, it 
					becomes false. if you want true and false to return true, 
					you should use ||, which means or.*/
       
			if (Selection == 1 && Random == 2) {
			printf("\nYou picked %d\n", Selection);
			printf("\nThe Computer picked %d\n", Random);
			printf("\nLooser!!\n");
			}
       
			if (Selection == 1 && Random == 3) {
			printf("\nYou picked %d\n", Selection);
			printf("\nThe Computer picked %d\n", Random);
			printf("\nYou Win!\n");
			}
       
			if (Selection == 2 && Random == 1) {
			printf("\nYou picked %d\n", Selection);
			printf("\nThe Computer picked %d\n", Random);
			printf("\nYou Win!\n");
			}
       
			if (Selection == 2 && Random == 2) {
			printf("\nYou picked %d\n", Selection);
			printf("\nThe Computer picked %d\n", Random);
			printf("\nIt's a tie!\n");
			}	
       
			if (Selection == 2 && Random == 3) {
			printf("\nYou picked %d\n", Selection);
			printf("\nThe Computer picked %d\n", Random);
			printf("\nLooser!!\n");
			}
       
			if (Selection == 3 && Random == 1) {
			printf("\nYou picked %d\n", Selection);
			printf("\nThe Computer picked %d\n", Random);
			printf("\nLooser!!\n");
			}
       
			if (Selection == 3 && Random == 2) {
			printf("\nYou picked %d\n", Selection);
			printf("\nThe Computer picked %d\n", Random);
			printf("\nYou Win!\n");
			}
       
			if (Selection == 3 && Random == 3) {
			printf("\nYou picked %d\n", Selection);
			printf("\nThe Computer picked %d\n", Random);
			printf("\nIt's a tie!\n");
			}
	  }while ( x < 5 );	
	  //The game will end after 5 times through.
       
      return 0;
}