<h1 align="center">Hangman 😵𓍯</h1>
  
------------

This file contains code for the famous hangman game. It is a version where an English word will be chosen randomly and the user can choose a level for solving this game.

## Explanations
------------

__**Line 1-8**__:

Importing an English dictionary.

__.text__ transforms the data into only the text, otherwise things like headers etc are included \
__.splitlines()__ splits the text by lines, since it was a string divided by returns\
__.isalpha()__ only use words, which consist of letters from the alphabet\

------------

**__Line 9-46__**:

Hangman dictionary with the figures.

------------

__**Line 47-66**__:

The user chooses a level between 1-3. The input is controlled, whether it is one of those numbers. If that is the case. the level is logged in. A random word is chosen from the imported English dictionary (take from GitHub). The random word is printed by replacing every letter with a dash.

------------

**__Line 68-99__**:

The hangman function is defined. Important notion here: The user has a mistake count equal to 6, which decreases by one with every wrong guess. The user chooses a variable which is controlled for being a single letter from the alphabet. Then a loop checks every letter in the hidden word and replaced the location of the dash through slicing, with the letter if it is correct. The loop runs once through the word. If no letter in the word is equal to the chosen letter, the mistake count decreases by one. This continues, until either the user identifies the word, or there are no mistakes left and he is 'Hanged'.

------------

**__Line 100-118__**:

Here we define the help function, which comes into play when the user decides to have either level 1 or 2. Here a hint, a letter, is given to the user, when his mistake count = 2. For level 1, he even gets two hints. That is only if the mistake counts do not complete the word. Accordingly, the function checks for the remaining unsolved letters. When there are enough, the function replaces the dash(es) with the hint(s), and the user continues playing.

------------

**__Line 120- End__**:

Lastly we put it all together in an if function, which checks for the level chosen and the executes the hangman and if necessary, the help function.
