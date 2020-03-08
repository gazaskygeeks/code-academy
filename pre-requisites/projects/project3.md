## JavaScript Library :books:

### Introduction

In this project you'll be creating a pretty neat toy for your portfolio to flex your DOM manipulation skills. You're going to build a browser [bookshelf](https://www.google.com/search?q=bookcase&tbm=isch).

This project should _not_ be easy for you. You'll probably have to Google frequently to get the right JavaScript methods and CSS to use - in fact, that's the point! You _can_ build this using the tools that you have already learned and there are plenty of resources on the net for learning stuff that we haven't covered yet if you decide you need it. We'll walk you through the basic steps, but it will be up to you to actually implement them.

If you get totally stuck drop by the [discord server](https://discord.gg/R6ypSzq), someone there will be able to point you in the right direction.

### Assignment

<div class="lesson-content__panel" markdown="1">

1. Start off by making the files on your computer and opening them in your browser.
2. Create a webpage with a bookshelf :D Don't worry! This just means create a grid of 3 or 4 rows (these are the shelves of your bookshelf).
   1. Create the book divs using JavaScript... don't try making them by hand with copy and pasting in your html file!
   2. Best to put your "shelf" divs inside another "container" div \(that one can go directly in your html\)
   3. Each shelf should appear one on top of the other. Apart from that, you need to add styling. Do this by giving the shelves a class and add class styles in a seperate CSS stylesheet:
      1. They should each be about as wide as the screen
      2. The height should be about 20-30% of the screen height.
      3. Give each one some borders so you can see!
   4. "OMG, Why isn't my grid being created???"
      1. Open your browser's developer tools
      2. Check if there are any errors in the JavaScript console
      3. Check your "elements" pane to see if the elements have actually shown up but are somehow hidden.
      4. Go willy-nilly and add `console.log` statements in your JavaScript to see if it's actually being loaded.
3. Now you need to add the books! First we need the data - each book should have a title, an author, and an image:
   - Go and get this data for as many books as you can (maybe don't get more than 10 books to start with though)
   - In your JavaScript make an object for each book with the keys of `title`,`author` and `image`, with the corresponding values.
   - All of these book Objects should then be stored in an array, like so:

```js
let books = [
   {
      title: "book1",
      author: "John Doe",
      image: "https://img.com/bookimg.jpeg"
   },
   {
     title: "book2",
     ...........
   },
 ..........
]
```

4. Now to put them on the shelves!
   - You should loop through your books array and for each book you should create a new div, which should show the image for the book, along with the title and the author (these could be inside inner divs of the book div).
   - Once you have this book div, you should append it to one of the shelfs (how will you decide which one...)- Don't forget to make new styles for the book div's
5. Add a "NEW BOOK" button that brings up a form allowing users to input the details for the new book: author, title, link to an image.
   - When they submit this form, it should add the book to your array and also render it onto the page.
6. Follow [these steps](https://help.github.com/en/articles/create-a-repo) to create a repo on GitHub.
7. On GitHub, make new empty files and copy and paste your code into them, making sure you save them by clicking the `commit changes` button.

</div>
