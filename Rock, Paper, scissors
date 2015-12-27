
/*                          Kevan Wiegand
                          Copyright 12/27/2015

      This program prompts the user to enter a number from 1 to 4, where:
            1 = Rock
            2 = Paper
            3 = Scissors
            4 = Quit
     The program then assigns a random value from 1 to 4 to the variable computeChoice and depending 
       on the programs switch statement determines the outcome of the game.
*/

//Preprocessor Commands
#include <stdlib.h>
#include <stdio.h>


int main(void){  

//Define Variables here
  int rock, paper, scissor, computeChoice, userWins = 0, compWins= 0, draw = 0; 
  int t = 0;
  int playerChoice;
  char term;
 

//Prompt User with information about the program
   printf("\n\nLets play rock, paper, scissors.. shoot!\n\n");
   printf("Rock = 1\nPaper = 2\nScissors = 3\n");
   puts("Quit = 4\n\n");
   

//While loop to keep the game continuous 
 while(t==0)
  {

//Do while statement to prevent user from entering wrong inputs
 do
  {
    printf("Enter an integer from 1 to 4\n");

  }while(((scanf("%d%c", &playerChoice, &term) != 2 || term != '\n') 
              && reset_stdin()) || playerChoice < 1 || playerChoice > 4);


//Quit if user enters 4
   if(playerChoice == 4)
 {
 
   return 0;

 }else{

  //Seed Random Number Generator & define rock, paper, scissors
  srand(time(NULL));  
  computeChoice = rand()%3 + 1;
  rock = 1;
  paper = 2;
  scissor = 3;

  //Show to the user what the computer has randomly picked
   printf("The computer picked:%d\n" , computeChoice);

  //Start Switch Statement
     switch(playerChoice)
    {
                //Case #1 = ROCK
      case 1:  

           if(computeChoice == 3){
            printf("Rock Smashes the scissors.\nThe user wins!\n");
            userWins++;}

            else if(computeChoice == 1){
             printf("\nThe game is a draw.\n");
             draw++;}

           else if(computeChoice == 2){
            printf("Paper Wraps Rock\nThe computer has won!\n");
            compWins++;}
            printf("\nLet's play again!\n\n");
           

      break;

               // Case #2 Paper
      case 2:

           if(computeChoice == 1){
            printf("Paper Wraps Rock\nThe user wins!\n");
            userWins;}

            else if(computeChoice == 2){
             printf("\nThe game is a draw.\n");
             draw++;}

          else if(computeChoice == 3){
            printf("Scissors cut paper\nThe computer has won!\n");
            compWins++;}
            printf("\nLet's play again!\n\n");
           
      break;

              // Case #3 Scissors
      case 3:

           if(computeChoice == 2){
             printf("Scissors cuts paper\nThe user has won!\n");
                userWins++;}

        	else if(computeChoice == 3){
        	  printf("\nThe game is a draw!\n");
                draw++;}

           else if(computeChoice == 1){
            printf("The rock smashes the scissors\nThe computer has won!!\n");
            compWins++;}
            printf("\nLet's play again!\n\n");
            
      break;

     }// END Switch Statement
   //print the current score
    printf("\nScore:\nUser wins: %d\nComputer Wins: %d\nDraws: %d\n\n\n", userWins, compWins, draw);
 
  }//End Else Statement
    
 }//End While Loop

}// End Main Method

/* This function resets the scanf in the while loop 
    in the top of the program when the user enters 
     the wrong statement
*/
 int reset_stdin()
 {
    while (getchar()!='\n');
    return 1;
 }

