# 📘 Assignment: Games in Python

## 🎯 Objective

Build a simple Hangman game in Python to practice working with strings, loops, conditionals, and user input while creating an interactive game experience.

## 📝 Tasks

### 🛠️	Create the Game Setup

#### Description
Set up the game by choosing a secret word and preparing the display that shows the player which letters have been guessed so far.

#### Requirements
Completed program should:

- Use a list of words and randomly select one for the player to guess
- Display the hidden word as underscores, such as `_ _ _ _ _`
- Track the letters the player has already guessed
- Keep the game organized and easy to read in the console

### 🛠️	Handle Player Guesses

#### Description
Allow the player to guess letters one at a time and update the hidden word based on whether the guess is correct or incorrect.

#### Requirements
Completed program should:

- Ask the player to enter a single letter
- Check whether the letter is in the secret word
- Reveal matching letters in the correct positions
- Count incorrect guesses and reduce the remaining attempts
- Prevent duplicate guesses from being counted twice

### 🛠️	End the Game

#### Description
Finish the game when the player either guesses the word correctly or runs out of attempts, then display a final result message.

#### Requirements
Completed program should:

- Show a win message when the word is fully guessed
- Show a lose message when the player runs out of attempts
- Display the secret word at the end of the game
- Print a clear message explaining whether the player won or lost
