## Rock, Paper, Scissors

### Introduction

In this project you'll be creating a pretty neat toy for your portfolio to flex your DOM manipulation skills. You're going to build a customisable game of Rock, Paper, Scissors :fight: As a user you will be able to choose one of the 3 options, then the computer will randomly pick one, and then the wbesite will tell you who won.

This project should _not_ be easy for you. You'll probably have to Google frequently to get the right JavaScript methods and CSS to use - in fact, that's the point! You _can_ build this using the tools that you have already learned and there are plenty of resources on the net for learning stuff that we haven't covered yet if you decide you need it. We'll walk you through the basic steps, but it will be up to you to actually implement them.

If you get totally stuck drop by the discord server. someone will be there to point you in the right direction.

### Assignment

<div class="lesson-content__panel" markdown="1">

1. Start off by making the files on your computer and opening them in your browser.
2. We will start off by making the design, which should have these elements, but you decide on how to lay them out. Note, don't worry about the functionality yet, just build the design in this step!:
   - A container div to hold the buttons which will be the player choices (but don't code the buttons!)
   - A section titled "Players's Choice". This will show the players choice, but will start off empty.
   - A section titled "Computer's Choice" which will show the computers choice.
   - A section titled "Result" which will show who is the winner.
   - A button titled "Play again"
   - You should could these into you html file, and use an external CSS stylesheet to make everything look pretty :dancer:
3. Now let's add the option buttons for the players to choose, using JavaScript.
   - create an array in JavaScript of strings, of each option
   - Loop over that array and for each element, create an HTML button with the string text on it, and then add it to the container div you made in step 2.
   - Make sure you give the button a class, and use your style sheet to make it look good :eyes:
4. We will now add the actual game logic. For this we need a few things:
   - We need a function which will tell us who wins. This should take 2 arguments - the player choice and the computer choice. It should return the winner as a string, either "computer" or "player"
   - We need a function which will give us the computer's choice, randomly. This function should take an array of choices, and then randomly return a string of one of them. Google how to randomly select from an array in javascript!
   - Once you have created those 2 functions we have all the pieces we need! You now need to some _event listeners_ to the choice buttons so the following will happen when they are clicked:
     1. Add the the players choice into the the players choice container you made in step 2 (using dom manipulation).
     2. Use your "computer choice" function to get a random choice from the computer. Then update the computer's choice container with this value.
     3. Using the player choice and computer choice as values in your "decide the winner" function, to find out who the winner is. Using dom manipulation, add this result as text to your "result" section - eg: "You lose, sucker!"
     4. Add a listener to your reset button to empty the divs in steps 1-3 so the player can play again!
5. Nice, we have all the basics! Now to add some extras, see if you can do any of these things:
   - Pictures! add some logic so that instead of just showing text, you show images.For example, when someone clicks the rock button, it will show a rock.
   - CSS Animations! maybe you can reveal the winner in a fun animated way :eyes:
   - Can you add some inputs to customise the game... Try to add three inputs, so that the player could replace rock, paper and scissor with 3 other choices - for example "Water, Fire, Wood" water beats fire, fire beats wood, wood beats water. You could add more inputs so the player can add their own images.
   - Anything else you can think of!
6. If you have managed to do all that, well done! Now to get them online - follow [these steps](https://help.github.com/en/articles/create-a-repo) to create a repo on GitHub.
7. On GitHub, make new empty files and copy and paste your code into them, making sure you save them by clicking the `commit changes` button.

</div>
