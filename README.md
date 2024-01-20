# Battleships

Battleships is a Python game that runs on the Code Institute mock terminal on Heroku. Players can win the game by finding the computer’s battleships before the computer finds theirs. The players take turns to guess spots on a map and try to hit all the spots where their enemy's ships are hiding! 

[More information about Battleships](embedded_link)

[Live version of the project](embedded_link)

## How to play

In our version, the player will be greeted with some text art, alongside some instructions/rules for how to play. The game works like this: you’ll be asked to input your name, and two boards will be shown, yours and the computer's. You will be guessing on your board, and the computer on theirs. You have ten turns to guess all six of the spots. If you succeed, you win; if the computer does it before you, you lose. If you find all the ships at the same time as your opponent, or if you run out of turns, it’s a draw!

### Existing features

#### Text art and instructions

The player is met with some art and instructions to read through to play the game.

![Enter image](image_link)

#### Enter your name

The player has the chance to enter their name. The game cannot start without this, and there is code in place to ensure the entered data is valid.

![Enter image](image_link)

#### Boards being printed

Two boards will be printed, players and computers, with coordinates from 0-4 on the row and the column.

![Enter image](image_link)

#### Enter a guess

The player is then asked to enter a row and a column to select. If you select a letter or a number out of the range, you’ll be asked to enter it again.

![Enter image](image_link)

#### Board print & scores updated

Now you’ll see the boards being printed, with the points updated too. For example, if you guessed 22 and it was a miss, the point that is 22 will now be represented by a “x” and no longer a “_”. You will also see the computer's guess and board the same, alongside two lines which tell you where each guess was and if it was a miss or a hit. Then if applicable, you’ll know if all the ships were sank, and who won, or if the turns have run out, that you can start the game again, or simply just moving onto the next turn and being asked for another row and column.

![Enter image](image_link)

#### Play again

You’ll get an option to play the game again if it comes to an end. This will restart the game if you wish. It is also able to handle input data that is not valid and keep going until it gets the correct data.

![Enter image](image_link)

### Future features

- Let players change the board size, and how many ships they want to use.
- Let players place the ships themselves.
- Add a player v player mode. 

## Data model

I used the Board as my class, this sets the size of the board, lets us know who’s playing and has a type, which assists with later parts of the code. This class also has a print method, which shows us each player's board and updates the boards after each guess. I used this class as it was the most fitting when it came to this project, as both players have a board.

## Testing

I have manually tested this project by:

1. Passing code through a PEP linter, the only errors I received were about lines in the code being too long, but needed to stay in the project as they were important for the logic.
2. Implemented validation for inputs when it comes to wrong inputs (like numbers off the board or too many characters).
3. Tested the logic in the Code Institute terminal.

### Stories from user experience testing

#### User one

##### First time user

When I first arrived on the terminal I was greeted with text art and instructions to read for the Battleships game, which were slightly long, but I knew I could come back to them at any time if I needed them.

![Enter image](image_link)

Next, I was able to enter my three-letter username, and I accidentally put in less than three characters and got a response saying I needed to try again. To make sure there were no errors here, I tried more than three letters and also numbers, but all did not work until I entered the right amount.

![Enter image](image_link)

Then I saw the boards, mine and the computers. I noticed that my name had been capitalized which was a nice touch. Looking at the boards, I noticed the coordinates started from 0-4, like the instructions said, so it was clear what column or row I would select.

![Enter image](image_link)

Next, I was asked to enter a row and a column to make a guess. Again I tried to put in data other than what was asked, but again I was unable to do so due to the validation requirement of the code.

![Enter image](image_link)

After I saw the boards printed again with “@” symbols on my board which let me know where my ships were, and if my guess was a hit or a miss, and the same for my opponent, I could see their guess on my board. The last thing I could see was the notes telling me where I had guessed and where the computer had guessed to make the game clearer. There was also a turn counter so I knew how many turns I had left.

![Enter image](image_link)

Next, I was asked to put in another guess, so I tried my last one, and it told me that I already had made that guess. I was able to enter another guess and see if it landed.

![Enter image](image_link)

Lastly, when the game was over I was asked if I wanted to continue. After trying more inputs than I was meant to, I was again met with more errors until I put in the right data and I was able to play the game again. Next time when I said I didn’t want to play again I was left with a goodbye.

![Enter image](image_link)

#### User stories

##### First time visitor

Overall, I found the game to be very straightforward and easy to use. I thought there was a lot of reading for the instructions, but if I had no idea what the game was, I would need them. The input features, the name being displayed and the turn counter were features I thought were helpful. To improve the website, I would like to see the instructions being minimized in some way.

##### Returning visitor

When I returned to the site, I could see the instructions and was hoping for a way to make them smaller or even disappear, maybe to make them show at the start and then disappear. I found using the program very straightforward and would have appreciated if the functions had some delay so when the next stage was happening it had some more bounce to it.

##### Frequent visitor

As a frequent visitor, I now would like to have the instructions hidden and have a way to ask for them if needed. I would also look for a mode where you can make the grid wider, change the turn counter, place your ships, and play against another person.

### Bugs

#### Solved bugs

When running the program, I had an issue with the hits, misses, and boats only showing up on one of the boards. I fixed this by changing the way the program received the data for updating the board in the print board function within the Board class.

#### Remaining bugs

When the program starts, the player isn’t able to see where their ships are until after they’ve made their first turn.

### Validator testing

#### PEP8

The only errors that came back were saying that certain lines were too long, but they’re needed for the code, so I left them in.

## Deployment

The project was deployed using Code Institute mock terminal for Heroku. Here are the steps for deployment:

1. Fork or clone this repository.
2. Create a new Heroku app.
3. Set the buildbacks to Python and NodeJS in that order.
4. Link the Heroku app to the repository.
5. Click on Deploy.

## Credits

I would like to credit Code Institute for the deployment terminal as well as their support and guidance on this project. Wikipedia for the battleship game details. My mentor for their support and guidance. This YouTube tutorial which helped in understanding some of the logic [YouTube Tutorial](https://www.youtube.com/watch?v=Ej7I8BPw7Gk&list=PLpeS0xTwoWAsn3SwQbSsOZ26pqZ-0CG6i).
