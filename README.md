# number-guessing-game
#include<stdio.h>
#include<stdlib.h>
#include<time.h>
int main() {
    int numberToGuess, playerGuess, attempts = 0;
    
    // Seed the random number generator
    srand(time(0));
    
    // Generate a random number between 1 and 100
    numberToGuess = (rand() % 100) + 1;
    
    printf("Welcome to the Number Guessing Game!\n");
    
    do {
        printf("Enter your guess: ");
        scanf("%d", &playerGuess);
        attempts++;
        
        if (playerGuess > numberToGuess) {
            printf("Too high! Try again.\n");
        } else if (playerGuess < numberToGuess) {
            printf("Too low! Try again.\n");
        } else {
            printf("Congratulations! You guessed the number %d in %d attempts!\n", numberToGuess, attempts);
        }
    } while (playerGuess != numberToGuess);
    
    return 0;
    }
