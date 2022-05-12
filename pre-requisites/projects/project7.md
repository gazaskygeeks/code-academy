## NAME TAGS GENERATOR :fist: :v: :hand:

### Introduction

In this project, you'll be creating a pretty neat toy for your portfolio to flex your DOM manipulation skills. You're going to build a customizable name tag generator. As a user you will be able to input any name, then the computer will generate a tag for that name.

This project should _not_ be easy for you. You'll probably have to Google frequently to get the right JavaScript methods and CSS to use - in fact, that's the point! You _can_ build this using the tools that you have already learned and there are plenty of resources on the net for learning stuff that we haven't covered yet if you decide you need it. We'll walk you through the basic steps, but it will be up to you to actually implement them.

If you get totally stuck drop by the [discord server](https://discord.gg/R6ypSzq), someone there will be able to point you in the right direction.

### Assignment

<div class="lesson-content__panel" markdown="1">

1. Start off by making the files on your computer and opening them in your browser.

2. We will start off by making the design, which should have these elements, but you decide on how to lay them out. Note, don't worry about the functionality yet, just build the design in this step!:
   - A title for your project `Name Tag Generator`.
   - An input to add the name that we will generate a tag for it.
   - A button titled `Generate Name Tag`(you will add its functionality later!)
   - A section to hold all your tags that you will generate(we will work on these tags later). 
   - You should put these into your HTML file, and use an external CSS stylesheet to make everything look pretty :dancer:
  
3. Create the name tag.
   - Create a function that gets a name as an argument to create a container div to hold the name and a delete icon.
   - Append this container(tag) to your HTML section.

4. Now, let's make the generate button work.
     1. Create a function `generateName` to take the name from your input.
     3. Use the function that you did before to create a tag for the name.
     4. Add a listener to your button to use `generateName` function.

5. Make the delete icon work.
    - Create a function that takes a node name as an argument to delete this node. 
    - Add a listener to the delete icon in the `generateName` function and use your delete function to delete the current tag.

7. Nice, we have all the basics! Now to add some extras:
   - Add a new button titled `Clear All` to delete all tags you already generated.
   - Make your generator generate a random background color for the tags each time you generate a new one.
    - Anything else you can think of!

8. If you have managed to do all that, well done! Now to get them online - follow [these steps](https://help.github.com/en/articles/create-a-repo) to create a repo on GitHub.
9. On GitHub, make new empty files and copy and paste your code into them, making sure you save them by clicking the `commit changes` button.

</div>
