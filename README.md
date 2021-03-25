# Pre-work - *Memory Game*

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program. 

Submitted by: **Maximilian Aquino**

Time spent: **5** hours spent in total

Link to project: (https://glitch.com/edit/#!/charm-habitual-glade)

## Required Functionality

The following **required** functionality is complete:

* [X] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
* [X] "Start" button toggles between "Start" and "Stop" when clicked. 
* [X] Game buttons each light up and play a sound when clicked. 
* [X] Computer plays back sequence of clues including sound and visual cue for each button
* [X] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess. 
* [X] User wins the game after guessing a complete pattern
* [X] User loses the game after an incorrect guess

The following **optional** features are implemented:

* [X] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
* [X] Buttons use a pitch (frequency) other than the ones in the tutorial
* [X] More than 4 functional game buttons
* [X] Playback speeds up on each turn
* [X] Computer picks a different pattern each time the game is played
* [X] Player only loses after 3 mistakes (instead of on the first mistake)
* [X] Game button appearance change goes beyond color (e.g. add an image)
* [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
* [X] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

- [ ] List anything else that you can get done to improve the app!

## Video Walkthrough

Here's a walkthrough of implemented user stories:
3 Strikes + 10 second timer: http://g.recordit.co/sMDtT1Bp2w.gif  

Winning the game: https://recordit.co/6SGUcdRjMF  



## Reflection Questions
**1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here.**
I used w3Schools to figure out how to use the setInterval() and clear() functions.

**2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words) **
I would say the main challenge I had to overcome was not knowing JavaScript. However I did have the advantage of working with languages like Java and Python so things weren't entirely foreign to me. I had many smaller problems throughout my code, the most challenging being the implementation of the user turn clock and the guess method. For the guess method I initially wanted to have separate if statements, one checking to see if all the win conditions were met to end the game on a win. (if statement with &&) The other checking to see if the user made a wrong move to end the game. Unfortunately, I couldn't get this approach to work and I found myself getting slightly frustrated. One thing that's helped me in the past, is writing my ideas and organizing my thoughts on a piece of paper so I did just that however this time, I moved forward with the nested if statement approach. It took some trial and error but finally ,after many console.logs and some tweaking, I had an implementation that worked. My next obstacle was finding where to start and stop the interval timer that would end the game if run all the way through. I made two functions, startClock() that started the timer and stopClock() that cleared it so that I would easily be able to start and stop the interval timer while making it easier to read. At first I had both startClock() and stopClock() inside of the guess function but I was running into some timing issues and realized the clock needed to be started at the end of the automatic pattern. I didn't figure this out right away but when I did, I put the function at the end of playClueSequence() and had the stopClock() setup() in guess so that the clock would stop when the user inputs the correct pattern. I also made a global var clock so that all the functions would be able to have access to the timer.

**3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words)**
I would like to know if professional web developers run into problems with their codes as well, and how they respond to those problems. What do they do when they run into an issue that they can't remedy right away? Another thing I've always wondered with web design is how multiple people can come together and work on one project. By myself, I made some mistakes and bounced all around the documents. I can't imagine having multiple people doing that. At times, I had trouble finding the source of one small problem so when I think of a group webdev project, It's hard to envision where to find the source of a problem with so many people working at the same time.

**4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words)** 
If I had more time to work on this project, I would've loved to have learned how to implement a visible clock on the website that displayed how much time the user had left in their turn. I ran into some confusion after doing some online research because the countdown clock implementations I was seeing were independently written in the HTML file using the script tag while I had my JavaScript code in a separate file. Another thing I came across was "new JavaScript". Apparently there are better ways to implement and write the functions in my script.js file so I would use that extra time to explore "new JavaScript" and make potential conversions.



## License

    Copyright Maximilian Aquino

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.