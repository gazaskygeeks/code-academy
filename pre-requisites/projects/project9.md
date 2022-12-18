# Dice Game 🎲 

## Introduction
In this project you'll be creating a Dice Game to flex your DOM manipulation skills.

This project should not be easy for you. You'll probably have to Google frequently to get the right JavaScript methods and CSS to use - in fact, that's the point! You can build this using the tools that you have already learned and there are plenty of resources on the net for learning stuff that we haven't covered yet if you decide you need it. We'll walk you through the basic steps, but it will be up to you to actually implement them.

If you get totally stuck drop by the [discord](https://discord.gg/XBgJHZDJP8) server, someone there will be able to point you in the right direction.

### Description
Dice game a simple game. Players take turns to roll a single dice as many times as they wish, adding all roll results to a running total, but losing their gained score for the turn if they roll a 1.

### Gameplay
Each turn, a player repeatedly rolls a die until either a 1 is rolled or the player decides to "hold":

If the player rolls a 1, they score nothing and it becomes the next player's turn.
If the player rolls any other number, it is added to their turn total and the player's turn continues.
If a player chooses to "hold", their turn total is added to their score, and it becomes the next player's turn.
The first player to score 30 or more points wins.

### For example
The first player, Mohammed, begins a turn with a roll of 5. Mohammed could hold and score 5 points, but chooses to roll again. Mohammed rolls a 2, and could hold with a turn total of 7 points, but chooses to roll again. Mohammed rolls a 1, and must end his turn without scoring. The next player, Fadi, rolls the sequence 4-5-3-5-5, after which she chooses to hold, and adds her turn total of 22 points to her score.



### Assignment
1. Start off by making the files on your computer and opening them in your browser.

3. We will start off by making the design, which should have these elements, but you decide on how to lay them out. Note, don't worry about the functionality yet, just build the design in this step!:

    * Two sections titled "Player1 - Player2 ". This section will be include:- 
        * Title (Player1).
        * Total Score.
        * Current Score.
    * A container div to hold the buttons which will be the player decision  (but don't code the buttons!)
        * Roll Dice button.
        * Hold button.
        * New Game Button.

    * You should put these into you html file, and use an external CSS stylesheet to make everything look pretty 💃


3. We will now add the actual game logic. For this we need a few things:

* We need a function which will tell us who wins. This should check the total score for each player after rolling the dice, If the Score equal 30. It should return the **WINNER** as a string below the title of the player.

* We need a function to get a random number between 1 and 6, and add the result to the current score.

* We need a function to check if the player got One as a result, it will end his turn  and move the turn to the next player after reset the current score for the player got 1.

* When current Player decide to hold his current score, we must add his current score to his total score unless he got one as result.

* after Player 1 click on Hold Button we must move the turn to Player 2.


* we need a function will be run when the Player click on New Game button, this function will reset total score for each player, and move the turn to Player 1.



4. Nice, we have all the basics! Now to add some extras, see if you can do any of these things:
    * CSS Animations! maybe you can reveal the winner in a fun animated way 👀
    * Can you add an input that take a number as A final score, so instead of check total score against 30, we will check it against the value of this input.
    * Anything else you can think of!
5. If you have managed to do all that, well done! Now to get them online - follow [these steps](https://docs.github.com/en/get-started/quickstart/create-a-repo) to create a repo on GitHub.

6. On GitHub, make new empty files and copy and paste your code into them, making sure you save them by clicking the commit changes button.


