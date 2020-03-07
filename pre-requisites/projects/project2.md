### Introduction

In this project you'll be creating a pretty neat toy for your portfolio to flex your DOM manipulation skills. You're going to make an on-screen calculator using JavaScript, HTML, and CSS.

This project should _not_ be easy for you. You'll probably have to Google frequently to get the right JavaScript methods and CSS to use - in fact, that's the point! You _can_ build this using the tools that you have already learned and there are plenty of resources on the net for learning stuff that we haven't covered yet if you decide you need it. We'll walk you through the basic steps, but it will be up to you to actually implement them.

If you get totally stuck drop by the discord chatroom.. someone will be there to point you in the right direction.

**Important Note:** Before you get started with this calculator project, we need to cover a word of warning. As you look into how to evaluate complex mathematical statements in JavaScript, you will likely come across the tantalizing [`eval()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/eval) function. However, this function can be very dangerous and [should not ever be used](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/eval#Do_not_ever_use_eval!)! You'll need to build your own functions to evaluate expressions as part of this calculator project.

### Assignment

<div class="lesson-content__panel" markdown="1">
Here are some use cases (abilities your project needs to have):

1. Your calculator is going to contain functions for all of the basic math operators you typically find on simple calculators, so start by creating functions for the following items and testing them in your browser's console.
   1. add
   2. subtract
   3. multiply
   4. divide
2. Create a new function `operate` that takes an operator and 2 numbers and then calls one of the above functions on the numbers.
3. Create a basic HTML calculator with buttons for each digit, each of the above functions and an "Equals" key.
   1. Do not worry about wiring up the JS just yet.
   2. There should also be a display for the calculator, go ahead and fill it with some dummy numbers so you can get it looking right.
   3. Add a "clear" button.
   4. Make it look nice using an external CSS sheet!
4. Create the functions that populate the display when you click the number buttons... you should be storing the 'display value' in a variable somewhere for use in the next step.
5. Make the calculator work! You'll need to store the first number that is input into the calculator when a user presses an operator, and also save which operation has been chosen and then `operate()` on them when the user presses the "=" key.
   1. You should already have the code that can populate the display, so once `operate()` has been called, update the display with the 'solution' to the operation.
   2. This is the hardest part of the project. You need to figure out how to store all the values and call the operate function with them. Don't feel bad if it takes you a while to figure out the logic.
6. Gotchas: watch out for and fix these bugs if they show up in your code:
   1. Users should be able to string together several operations and get the right answer: `12 + 7 - 5 * 3` etc. The behavior we're looking for should be something like this https://www.online-calculator.com/.
   2. You should round answers with long decimals so that they don't overflow the screen.
   3. Pressing `=` before entering all of the numbers or an operator could cause problems!
   4. Pressing "clear" should wipe out any existing data.. make sure the user is really starting fresh after pressing "clear"
   5. Display a snarky error message if the user tries to divide by 0... don't let it crash your calculator!
7. Now you should have a working calculator, well done! Now we're going to add a currency converter:
   1. Create 4 new buttons that will convert the number the user has typed into the calculator into different currencies:
      - Shekels into US Dollars
      - Dollars into Shekels
      - Shekels into Euros
      - Euros into Shekels
   2. Create the functions in JavaScript to run these calculations - get the correct conversion rates from google
   3. Wire all the JS up to the HTML!
8. If you have managed to do all that, well done! Now to get them online - follow [these steps](https://help.github.com/en/articles/create-a-repo) to create a repo on GitHub.
9. On GitHub, make new empty files and copy and paste your code into them, making sure you save them by clicking the `commit changes` button.

   </div>
