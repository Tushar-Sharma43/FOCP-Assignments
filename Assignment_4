#include <stdio.h>
#include <stdlib.h>
#include <time.h>
#include <string.h>

int main()
{
    char user_choice[10], comp_choice[10];
    srand(time(0));
    int random_number = rand() % 100;

    printf("Choices: Stone, Paper, and Scissors\n");
    printf("Enter your choice: ");
    scanf("%s", user_choice);

    if(random_number >= 0 && random_number < 33){
        strcpy(comp_choice, "Stone");
    }
    else if(random_number >= 33 && random_number < 66){
        strcpy(comp_choice, "Paper");
    }
    else{
        strcpy(comp_choice, "Scissors");
    }

    printf("Computer chose: %s\n", comp_choice);

    if((strcmp(user_choice, "Stone") == 0 && strcmp(comp_choice, "Scissors") == 0) ||
       (strcmp(user_choice, "Paper") == 0 && strcmp(comp_choice, "Stone") == 0) ||
       (strcmp(user_choice, "Scissors") == 0 && strcmp(comp_choice, "Paper") == 0)) {
        printf("You won!\n");
    }
    else if((strcmp(comp_choice, "Stone") == 0 && strcmp(user_choice, "Scissors") == 0) ||
            (strcmp(comp_choice, "Paper") == 0 && strcmp(user_choice, "Stone") == 0) ||
            (strcmp(comp_choice, "Scissors") == 0 && strcmp(user_choice, "Paper") == 0)) {
        printf("Computer won!\n");
    }
    else {
        printf("It's a draw!\n");
    }

    return 0;
}
