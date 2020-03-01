## Twitter Clone :robot:

### Introduction

In this project you'll be creating a pretty neat toy for your portfolio to flex your DOM manipulation skills. You're going to build a basic Twitter Clone :tweet: Don't worry we are not going to do any networking yet! All the tweets will be local to each user on the site (and don't worry if you don't totally understand what that means!)

This project should _not_ be easy for you. You'll probably have to Google frequently to get the right JavaScript methods and CSS to use - in fact, that's the point! You _can_ build this using the tools that you have already learned and there are plenty of resources on the net for learning stuff that we haven't covered yet if you decide you need it. We'll walk you through the basic steps, but it will be up to you to actually implement them.

If you get totally stuck drop by the discord server. someone will be there to point you in the right direction.

### Assignment

<div class="lesson-content__panel" markdown="1">

1. Start off by making the files on your computer and opening them in your browser.
2. Create the basic design of your webpage. You should definitely use the [real twitter page](https://twitter.com) for inspiration, but try to come up with something unique and fun! Make sure you have:
   - A container, "newsfeed", div to hold of the tweets (this will start out as empty)
   - A form with 2 fields for the tweet itself, and the username. There should also be a submit button.
   - A header with the title and a nice logo image of your site :eyes:
   - Use a CSS stylesheet to make everything look pretty :dancer:
3. Now you need to add some functionallity. Firstly, when the user submits the form, the tweet should be added to the "newsfeed"
   - The tweet displayed should contain the tweet itself, as well as the name of the user, and two buttons - like and retweet
   - You will need to create a new div, and then within that div, have more divs for the username, tweet content, and the buttons.
   - Its a very good idea to create seperate functions here:
     - Make a 'createTweet' function which will take tweet text and the author, and then return a the whole div of the tweet, with the buttons and everything. Don't worry about what the buttons will do though, just make sure they are there.
     - Then you should use an `onClick` _event listener_ on your button. When the button is clicked, you should grab the content of the input boxs and then just call your `createTweet` function to make the HTML :tada:
     - you will need to then add this HTML to the newsfeed
     - Don't forget to give everything classes and styles!
   - Try to make sure that each new tweet gets added to the top of the news feed...
   - "OMG, Why isn't my grid being created???"
     1. Open your browser's developer tools
     2. Check if there are any errors in the JavaScript console
     3. Check your "elements" pane to see if the elements have actually shown up but are somehow hidden.
     4. Go willy-nilly and add `console.log` statements in your JavaScript to see if it's actually being loaded.
4. Well done! You've done all the basics now to add the final touches:
   - Make it so that when a user clicks on the "like" button, that tweet changes to a different colour
   - Make it so that when a user clicks on the "retweet" button, that tweet gets repeated at the top of the newsfeed :twins:
5. So far, we've just been adding our tweets directly to the HTML. This is great, however, when you refresh the page all of the tweets will disappear :crying_face:. We are going to use Javascript to fix this!
   - Create an empty array in your javascript file, called something like 'tweets'.
   - When the user submits a new tweet, as well as adding it to the HTML, we want to add it here to the array.
   - We will do this by creating an object for each tweet. The object should have 2 fields - one for the author, and one for the tweet.
   - Add some code to your `onClick` function so that it will create a tweet object, and add that to the tweet array.
   - Great we are now storing the tweets in JavaScript. Try using `console.log` in the onclick function to make sure this is working.
   - The next thing we are going to do is store this tweet array into the local storage. Google what that means! Once you know, add _another_ line to the `onClick` function to save the tweet array into local storage each time.
   - _Finally_ we need to use this! Just below where you defined your empty tweet array, you should add an if statement which will look at the local storage to see if the tweet array has been saved there - if it has, you need to set your tweet array to equal the one in local storage
   - You then also need to _loop_ over the array and _for each_ tweet in the array you should create and add a tweet to the "newsfeed". Luckily for you, you hopefully already made a function to do this! Use your `createTweet` function to create the divs, then append them to the newsfeed :smart:
6. Well done! Now to get them online - follow [these steps](https://help.github.com/en/articles/create-a-repo) to create a repo on GitHub.
7. On GitHub, make new empty files and copy and paste your code into them, making sure you save them by clicking the `commit changes` button.

</div>
