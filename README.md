# Rock-paper-scissor-game

import random

# List of possible choices
choices = ['rock', 'paper', 'scissors']

def game():
    # Generate a random choice for the computer
    computer_choice = random.choice(choices)
    
    # Prompt the user to choose Rock, Paper, or Scissors
    print("Choose Rock, Paper, or Scissors.")

    # Take input from the user
    user_choice = input("Enter your choice: ").lower()

    # Check if the user's choice is in the list of valid choices
    if user_choice in choices:
        print(f"Your choice: {user_choice}")
        print(f"Computer's choice: {computer_choice}")

        # Compare the user's choice with the computer's choice
        if user_choice == computer_choice:
            print("It's a draw!")
        elif (user_choice == 'rock' and computer_choice == 'scissors') or \
             (user_choice == 'scissors' and computer_choice == 'paper') or \
             (user_choice == 'paper' and computer_choice == 'rock'):
            print("You win!")
        else:
            print("You lose!")

        # Ask if the user wants to play again
        play_again = input("Do you want to play again? (yes/no): ").lower()
        if play_again == 'yes':
            game()  # Recursively call the game function to play again
        else:
            print("Thanks for playing!")
    else:
        print("Invalid choice. Please choose either rock, paper, or scissors.")

# Start the game
game()
