# Codsoft1
#include <iostream>
#include <cstdlib>
#include <ctime>

int main() {
    // Initialize random seed based on the current time
    std::srand(std::time(0));

    // Generate a random number between 1 and 100
    int randomNumber = std::rand() % 100 + 1;
    int guess = 0;

    std::cout << "Guess the number (between 1 and 100): ";

    // Loop until the user guesses the correct number
    while (guess != randomNumber) {
        std::cin >> guess;

        if (guess > randomNumber) {
            std::cout << "Too high! Try again: ";
        } else if (guess < randomNumber) {
            std::cout << "Too low! Try again: ";
        } else {
            std::cout << "Congratulations! You guessed the correct number." << std::endl;
        }
    }

    return 0;
}

