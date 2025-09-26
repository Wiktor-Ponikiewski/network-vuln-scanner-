#guess-the-number
import random

print("Welcome to the game! Try to guess a number between 1 and 100.")
print("The computer has chosen a number – can you find it?")

secret = random.randint(1, 100)   # computer chooses the number
guessed = False                   # game runs until guessed = True
attempts = 0                      # counter of attempts

while not guessed:
    guess = input("Enter your guess: ")

    if not guess.isdigit():
        print("This is not a number. Please enter a valid number!")
        continue   # go back to the loop if input is invalid

    guess = int(guess)
    attempts += 1

    print(f"This is your {attempts} attempt(s)")

    if secret == guess:
        print(f"You won!!! It took you {attempts} attempts.")
        guessed = True
    elif secret < guess:
        print("The number is smaller, try again!")
    else:
        print("The number is bigger, try again!")
