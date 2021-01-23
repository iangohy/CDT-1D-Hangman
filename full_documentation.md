# Computational Thinking for Design 1D Project - PyHangman

F05 Group 03

```
Naurana Badalge Axel
Ian Goh Yiheng
Hayden Ang Wei En
Carvalho Andrea Roby
Mandis Loh Zhi Cheng
```



## Description

This game is known as Hangman, an overview of the game can be found here http://gambiter.com/paper-pencil/Hangman_game.html.

The objective of this game is to guess a randomized word and to score as many points as possible with a limited number of guesses. 

A category is given and its word length along with some visible letters and dashes, and the player is to guess the word.  If the letter is present in the word, all instances of that letter will appear in its place in the word. If the letter is not found in the word given, the number of strokes for the hangman figure will increase by one. Players can continue to guess until all their 9 chances have been used up (ie. when the hangman is fully drawn) . After which, the answer will be revealed and the game is over. 

This game can also be played with two players where instead of the algorithm, Player 1 will choose a category and word for Player 2 to guess. The game then continues the same way if there was only one player except in this case, Player 2 acts as the computer. The game will continue with each player taking turns to guess the word entered by the other player until the game is exited. 


 ### Resources Referenced

Hangman Game: http://gambiter.com/paper-pencil/Hangman_game.html

https://stackoverflow.com/questions/24816237/ipython-notebook-clear-cell-output-in-code

ASCII Art generated from http://patorjk.com/software/taag/#p=display&f=Doom&t=PyHangMan



## Documentation

### Running the game

To play the game, ensure that the file `words.csv` is in the same directory as the python file. To start the game, enter `python 1d_project_ctd.py` in a terminal and run.

 

### Libraries used

This game makes use of the `randint()` and `sample()` functions from the `random` library and `os` library to clear the terminal.

 

### Testing

The global variable `test` enables/disables the unit tests for each function.

 

### Functions

`clear_terminal()` - Clears the terminal.



`header()` - Displays the game header.

 

`how_to_play()` - Displays instructions on how to play the game.

 

`main_menu()` - Displays the main menu and returns the option selected by the user.

 

`generate_answer()` - Generates an answer from a list of words found in `words.csv`. Returns a tuple containing `(category, answer)`.

 

`user_answer()` - Gets user input to set the category and answer. Returns a tuple containing `(category, answer)`.

 

`starting_letters(answer)` - Generates the starting hints. Returns a list representing the partially filled guess.

 

`hangman(num_wrong_guess)` - Displays the hangman based on the current number of wrong guesses.

 

`display_interface(category, guess, num_wrong_guess, max_wrong_guess)` - Displays the main game interface.

 

`get_guess(answer)` - Gets guess from user and ensures that it is a valid input. Returns a lowercase string containing a single letter guess or a full word guess of length equal to that of the answer.

 

`check_guess(answer, guess, user_input, num_wrong_guess)` - Takes the user's letter guess and returns the updated guess and number of wrong guesses based on the user input.

 

`check_solved(answer, guess)` - Checks if the player has solved the hangman question. Returns 0 if not solved and 1 if solved.

 

`game(category, answer, max_wrong_guess)` - Runs one round of hangman. Returns 0 if round was not solved and 1 if it was solved.

 

`single_player(max_wrong_guess)` - Starts the game for single player.

 

`two_player(max_wrong_guess)` - Starts the game for two players.

 

`main()` - Starts the full hangman game.

 