## ALarm clock ⏰

### Introduction

In this project you'll be creating a clock to display the local time on your screen, You can add an alarm by selecting the time you want to play the alarm, specifying hours and minutes, and time period `AM` OR `PM`

*AS a stretch goal*, It's good to run audio when current time match on of the alarms user saved.

This project should _not_ be easy for you. You'll probably have to Google frequently to get the right JavaScript methods and `html` elements to use - in fact, that's the point! You _can_ build this using the tools that you have already learned and there are plenty of resources on the net for learning stuff that we haven't covered yet if you decide you need it. We'll walk you through the basic steps, but it will be up to you to actually implement them.

If you get totally stuck drop by the [discord server](https://discord.gg/XBgJHZDJP8), someone there will be able to point you in the right direction.

### Assignment

<div class="lesson-content__panel" markdown="1">

1. Start off by making the files on your computer and opening them in your browser.
2. We will start off by making the design, which should have these elements, but you decide on how to lay them out. Note, don't worry about the functionality yet, just build the design in this step!:
   - A container div to hold the clock that will display the current time on screen.
   - A container div to hold the form to add new Alarm.
   - A form should contain an input to select hour, an input to select minute, and a drop down to select `am`|`pm`time period and a button to add Alarm.
   - A section `alarms` to contain all your alarms you have.
   - an [audio](https://www.w3schools.com/html/html5_audio.asp) that will run when the time match any of the alarms user have.
   - You should put these into you html file, and use an external CSS stylesheet to make everything look pretty :dancer:
3. Create a function `renderClock` to render the time to your screen.
   - You will use the `Date Api` to get the current time.
   - Time will change every second so try to run the `renderClock` function very seconed, `setInterval` might help you.
 
4. Its a time to display alarms we have:
     - Start up with adding a static data that simulate the alarms you have. So create an array of `fakeAlarms` to start with.
     ```js
     // Maybe it's good to store the new Alarm in this way
      const fakeAlarms = [{hour: 5, minute: 50, period: 'am'}]
     ```
     - Make a 'renderAlarm' function which will take the alarm time then return the whole div of the alarm.
     - you will need then add this HTML to the `alarms` section By DOM manpulation.
     - Don't forget to give everything classes and styles!
     - Now as we have a function to display specific alarm, and we already having the alarms array, So we need to loop on the array we have to `renderAlarm`.
4. We will work on the add alert form submit.
   - We need a function to add alert.
   - In the function itself we have to get the input values alarm time`hours`, `minutes` and `period`!
   - the function at the end should add the the new alarm time to the `fakeAlarms` array we have.
5. Nice, we have all the basics! :
   - try to style every thing
   - maybe you want to add extra feature.
   - Anything else you can think of!
   - if you want to activate audio follow steps bellow. 
6. Now it's a time to run the audio if time match one of the alarms times we have.
   - create a function to check If one of the `fakeAlarms` match with the local time.
   - we have the hour and minute for every alarm. So we need to get the `hour` and `minute` for the `Date.now()`
   - If time match one of the stored alarms, we should play the audio we have in the html file.
   - we need to check this every second!   

7. If you have managed to do all that, well done! Now to get them online - follow [these steps](https://help.github.com/en/articles/create-a-repo) to create a repo on GitHub.
8. On GitHub, make new empty files and copy and paste your code into them, making sure you save them by clicking the `commit changes` button.

</div>
