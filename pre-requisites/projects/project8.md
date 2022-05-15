# Restaurant Menu :pizza::hamburger:

### Introduction

In this project you'll be creating a pretty neat toy for your Restaurant to flex your DOM manipulation skills. You're going to build a browser [Restaurant Menu](https://www.google.com/search?q=restaurant+menu+page&tbm=isch).

This project should _not_ be easy for you. You'll probably have to Google frequently to get the right JavaScript methods and CSS to use - in fact, that's the point! You _can_ build this using the tools that you have already learned and there are plenty of resources on the net for learning stuff that we haven't covered yet if you decide you need it. We'll walk you through the basic steps, but it will be up to you to actually implement them.

If you get totally stuck drop by the [discord server](https://discord.gg/7QqGtqC9Gy), someone there will be able to point you in the right direction.

### Assignment

<div class="lesson-content__panel" markdown="1">

1. Start off by making the files on your computer and opening them in your browser.
2. Create a webpage with a Menu (Dish Cards) :D Don't worry! This just means create a grid of 3 or 4 dish cards in each row (these are the cards when you show the dish name, image, category, pirce and ingredients).
   1. Create the Dish divs using JavaScript... don't try making them by hand with copy and pasting in your html file!
   2. Best to put your "dish" divs inside another "container" (Menu) div \(that one can go directly in your html\)
   3. Each Dish should appear one on top of the other or on a grid of 3 or 4 dishes on each row. Apart from that, you need to add styling. Do this by giving the dishes a class and add class styles in a seperate CSS stylesheet:
      1. They could each be about as wide as the screen or as a grid (it's your choice)
      2. Give each one some borders so you can see!
   4. "OMG, Why isn't my grid being created???"
      1. Open your browser's developer tools
      2. Check if there are any errors in the JavaScript console
      3. Check your "elements" pane to see if the elements have actually shown up but are somehow hidden.
      4. Go willy-nilly and add `console.log` statements in your JavaScript to see if it's actually being loaded.
3. Now you need to add the dishes! First we need the data - each dish should have a name, image, price, and ingredients:
   - In your JavaScript make an object for each dish with the keys of `name`, `category`,`image`, `price` and `ingredients`, with the corresponding values.
   - All of these dish Objects should then be stored in an array, like so:

        ```js
        let dishes = [
           {
              name: "burger",
              price: 20.99,
              category: "fast food",
              image: "https://img.com/dish_image.jpeg",
              ingredients: "meat, cheese, onion, bread"
           },
           {
             name: "dish2",
              ...........
           },
         ..........
        ]
        ```

4. Now we need to filter and search about dishes!
   
    - you should create and design a filter in the left side or on the top of the menu with these filters (search, category in `dropdown list`, price)
    - You should loop through your dishes array and for each dish you should show the dishes that matches the data in the filters, which should show the `burger` dish  when I type `burger` in the search input , along with the category and the price.
    - you can use some of the [Array Methods](https://www.w3schools.com/js/js_array_methods.asp) as you learnd
5. Add a "New Dish" button that brings up a form allowing users to input the details for the new dish: `name`, `category`, link to an `image`, `price` and `ingredients`.
   - When they submit this form, it should add the book to your array and also render it onto the page.
6. Follow [these steps](https://help.github.com/en/articles/create-a-repo) to create a repo on GitHub.
7. On GitHub, make new empty files and copy and paste your code into them, making sure you save them by clicking the `commit changes` button.

</div>
