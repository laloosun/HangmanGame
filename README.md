# HangmanGame
This code sets up a simple Hangman game (Python) where the player needs to guess letters to reveal a randomly chosen word from a predefined list. The player has 6 lives to guess the word correctly. The game will continue until the player either guesses the word or runs out of lives. Each line of code is explained below.        
1. `import random`: Imports the random module to generate random choices.
2. `word_list = ["ardvark", "baboon", "camel"]`: Defines a list of words for the game.
3. `chosen_word = random.choice(word_list)`: Randomly selects a word from the word list.
4. `word_length = len(chosen_word)`: Determines the length of the chosen word.
5. `display = []`: Initializes an empty list to store the displayed word.
6. `for _ in range(word_length): display += "_"`: Fills the display list with underscores based on the word length.
7. `end_of_game = False`: Initializes a variable to control the game loop.
8. `lives = 6`: Sets the number of lives for the player.
9. `while not end_of_game:`: Starts a loop that continues until the game ends.
10. `guess = input("Guess a letter: ").lower()`: Prompts the user to guess a letter and converts it to lowercase.
11. `if guess in display: print(f"You've already guessed {guess}")`: Checks if the guessed letter was already guessed.
12. `for position in range(word_length):`: Iterates over the positions of the chosen word.
13. `letter = chosen_word[position]`: Retrieves a letter from the chosen word at a specific position.
14. `if letter == guess: display[position] = letter`: Updates the display if the guessed letter matches.
15. `if guess not in chosen_word:`: Checks if the guessed letter is not in the chosen word.
16. `print(f"{guess} is not in the word. You lose a life.")`: Informs the player about losing a life for an incorrect guess.
17. `lives -= 1`: Decreases the number of lives left for the player.
18. `if lives == 0: end_of_game = True; print("You lose.")`: Ends the game if all lives are used up.
19. `print(' '.join(display))`: Displays the current state of the word with guessed letters.
20. `if "_" not in display:`: Checks if all letters have been correctly guessed.
21. `end_of_game = True; print("You win.")`: Ends the game and declares victory if all letters are revealed correctly.
