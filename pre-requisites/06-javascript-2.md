## Strings, Arrays & Functions

### Introduction

There are a few extremely common types of data that you will encounter in Javascript, and these fundamentals lessons will give us a really strong foundation in all of them. Before we start digging deep, however, [this article](http://javascript.info/types) will give you a quick overview of the most common ones.

### Learning Outcomes

Look through these now and then use them to test yourself after doing the assignment:

- What are the seven data types of javascript?
- Which data type is NOT primitive?
- What is the difference between single, double, and backtick quotes for strings?
- Which type of quote lets you embed variables/expressions into a string?
- How do you embed variables/expressions into a string?
- How do you escape characters in a string?
- What is the difference between slice/substring/substr?
- What are methods?

### Strings

Depending on what kind of work you're doing, you might end up working more with pieces of text rather than numbers. A **string** is simply a piece of text... and is a fundamental building block of the language.

1. Read and code along with [yet another MDN tutorial](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Strings) on the topic.
2. Go through [this lesson](https://www.w3schools.com/js/js_string_methods.asp) to learn a bit more about what you can do with strings... be sure to do the exercises at the end!
3. Vocabulary time: a **method** is a bit of functionality that is built into the language or into specific data types. In [the previous W3Schools exercise](https://www.w3schools.com/js/js_string_methods.asp), you learned a few methods that can be used on strings, such as `indexOf` and `search`. An exhaustive list of methods that can be used on strings can be found [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String).

### Arrays

Strings and numbers may be our building blocks but as your scripts get more complex you're going to need a way to deal with large quantities of them. Luckily, JavaScript has a couple of data types that are used for just that. An Array is simply an ordered collection of items (Strings, numbers, or other things).

1. [This tutorial](https://www.w3schools.com/js/js_arrays.asp) is a great introduction.
2. [This article](https://www.w3schools.com/js/js_array_methods.asp) covers some of the most useful built-in array methods. These fundamentals are something you'll use every day, so don't rush too much and miss out!

### Functions

Things are about to get _really_ exciting. So far you have been writing an impressive amount of code to solve various problems, but that code has not been as useful as it could be. Imagine taking one of your scripts and bundling it into a little package that you could use over and over again without having to rewrite or change the code. That's the power of functions, and they're used _constantly_ in JavaScript.

1. [This lengthy MDN article](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Functions) is a good place to start. Pay special attention to the sections on 'Function Scope'. Scope is a topic that commonly trips up both beginner and intermediate coders, so it pays to spend some time with it up front.
2. Read this article about [return values](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Return_values).
3. Let's discuss parameters and arguments in the context of the following example function:

   ```javascript
   function favoriteAnimal(animal) {
     console.log(animal + " is my favorite animal!");
   }

   favoriteAnimal("Goat");
   ```

   In JavaScript, parameters are the items listed between the parentheses in the function declaration. Function arguments are the actual values we decide to pass to the function. In the example above, the function definition is written on the first line: `function favoriteAnimal(animal)`. The parameter, `animal`, is found inside the parentheses. We could just as easily replace `animal` with `pet`, `x`, or `blah`. But in this case, naming the parameter `animal` gives someone reading our code a bit of context so that they don't have to guess what `animal` may eventually contain. By putting `animal` inside the parentheses of the `favoriteAnimal()` function, we are telling JavaScript that we will send _some_ value to our `favoriteAnimal` function. This means that `animal` is just a **placeholder** for some future value. But what value are we sending?
   The last line, `favoriteAnimal('Goat')`, is where we are calling our `favoriteAnimal` function and passing the value `Goat` inside that function. Here, `Goat` is our argument. We are telling the `favoriteAnimal` function, "Please send 'Goat' to the favoriteAnimal function and use 'Goat' wherever the 'animal' placeholder is." Because of the flexibility that using a parameter provides, we can declare any animal to be our favorite. Feel free to experiment with the code on your own and replace `Goat` with your favorite animal. Notice how we can change the argument to anything we like? Try changing `animal` in the function declaration and in the function body, too. What happens when you do?

4. Next, read [this article](http://javascript.info/function-basics) from Javascript.info. We've mentioned this before, but JavaScript has changed a bit over the years and functions have recently received some innovation. This article covers one of the more useful new abilities: 'default parameters'. \(NOTE: The last "task" at the end of this lesson uses loops, which you will learn about in the next lesson. Don't worry about that one.\)
5. Finally, read [one more article](https://javascript.info/arrow-functions-basics) about functions in JavaScript that will give you a little more context. Another relatively new feature in modern JavaScript is the `arrow function`, which is introduced in this article. Arrow functions are useful but not crucial, so don't worry about them too much just yet. We include them here because you are likely to encounter them as you move forward, and it's better that you have at least _some_ idea of what you're looking at whenever they crop up.

### Practice

1. Continue on [Free Code Camp Javascript Basics](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-javascript/), up to **Understanding Boolean Values** (don't worry if you do more, we will be assigning that later anyway! :smile:)
