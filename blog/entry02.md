# Entry 2: Goal Setting
##### Brianna Peralta on December 15th, 2025 (12/15/25)

## Main Information:
Well, the 2025-2026 Winter Break is practically right around the corner, as well as the end of Semester 1. My first blog was written more than a month ago, and now this blog is setting up all students of SEP11, including myself, for how they want to tackle work as we take our about 10 day break from classes. If you had asked me what I wanted to do for the break right before I had written the 1st Blog, I probably would've said something on the lines of "Break? I need to catch up to everyone as **QUICKLY** as possible!".. To be fair, I'd probably say something similar now but hey, the pressure is not as bad as it was then. Now with that said, after Blog 1 was finished, students were told to continue tinkering with their tool and continue writing their [Learning Logs.](../tool/learning-log.md) I know for those, I tapped into one of the starter games posted in Kaboom and tried my best to recreate it using my IDE as well as the step by step progression guide. However, I tried other things besides just this, but more on that later. Thankfully me and my partner are still partnering for the final result, so for this blog, I plan to not only dig into what I want to personally tackle for Winter Break, but I will also plan some additional things for the future (aka when we start building the final project). So with that, let's get into the progression.

## Tinker Progression:
In Blog 1, I already established that I wanted to work on Kaboom, and I can recall the struggle to actually try and use [Kaboom](https://kaboomjs.com/), but now that I don't need to worry about trying to set up Kaboom, I genuinely spent a lot of time trying to tinker and play with Kaboom has to offer. Since it's the ideal type of game for the tool is a platformer, it featured a good amount of commands and keys that suits a "2D Scale" such as `onKeyPress(() => {})` and `onKeyDown(() => {})`, which triggers an event to occur depending on what Keyboard key gets used. For example, take a look at this strand of Javascript:

```js
kaboom();


const moveSpeed = 500;
loadSprite("Placeholder", placeholder.png);


const spritePlaceHolder = add([
sprite("Placeholder),
area(),
body(),
])


onKeyDown("r", () => {
spritePlaceHolder.move(moveSpeed,0),
})
```
This might be a little hard to digest, so let's break it down into something more simple. The `kaboom();` command at top essentially connects Kaboom to your coding project, allowing you to use whatever it has to offer. The variable `moveSpeed` in this context is supposed to represent how fast something will move, with the speed now having a value of 500. `loadSprite()` is, as the name implies, the command that allows for a sprite to feasibly be generated and portrayed on one's game screen. Now `add([])` is really interesting to me, since.. Well, it basically says everything it does in its name, but it pretty much adds whatever you put in between both sets of wraps into your program. This can include sprites, `area()` and `body()`, which establish a hit box for whatever needed, as well as other properties such as `color()`, `scale()`, and `rotate()` (All self explanatory since they were pretty frequent in last year's CSS lessons). Last but not least we also have `onKeyDown(() => {})`. I already explained a bit of what it does but in contrast to `onKeyPress(() => {})`, this command essentially provides a smoother feel compared to the latter as you're supposed to hold the key down and whatever's wrapped inside of it's wraps will happen. Looking back at the example code, note how it includes `spritePlaceHolder.move(moveSpeed,0),`. This means that when the player presses **and** holds a key, the sprite will move towards the right. You can also change the direction the sprite goes by either adding a negative sign by the `moveSpeed`, swapping the position of 0 and `moveSpeed`, or by doing both. There's other properties similar to `.move` such as `.jump` which.. Makes the sprite jump in the air, but for the most part all other parts follow a similar structure. With that said I did mention I spent most of my tinkering time trying to follow that tutorial, creating code segments such as this:

```js
const spriteMarina = add([
   sprite("marina"),
   pos(80,50),
   scale(.75),
   area(),
   body(),
])


onKeyPress("space", () => {
   if (spriteMarina.isGrounded()) {
   spriteMarina.jump()
   }
})


add([
   rect(width(), 48),
   pos(0, height() - 48),
   outline(2),
   area(),
   body({ isStatic: true }),
   color(127, 200, 225),
])


function spawnTree() {


       add([
           rect(48, rand(32, 96)),
           area(),
           outline(4),
           pos(width(), height() - 48),
           anchor("botleft"),
           color(255, 180, 255),
           move(LEFT, 300),
           "tree",
       ]);
       wait(rand(1, 2), spawnTree);
   }
   spawnTree();
})

```

There's other things I could absolutely refer to but for the sake of this blog potentially being way too long, I'll cut off this segment here. As you can clearly tell however, I've been pretty busy when it comes to setting this portion up.


## Revisiting the EDP:
As a reminder, these are the steps behind the Engineering Design Process, or EDP:


* **1) Define the Problem**
 * **2) Research the Problem**
 * **3) Brainstorm possible solutions**
 * **4) Plan the most promising solution**
 * **5) Create a Prototype**
 * **6) Test and Evaluate the prototype**
 * **7) Improve as needed**
 * **8) Communicate the Results**

I feel like with all of our focus on the consistent learning logs and from what I mentioned in the 1st Blog, I'd say with confidence that we are past step 1, and instead we're onto step 3, **Brainstorming possible solutions**. My partner and I already agreed that we'd be creating a platform that, on random occurrences, project spanish problems at a player and if they answer correctly they'd receive a reward, but what has been on my mind the most was: How can we account for the different needs of people and how can we make the questions appear frequently but not overwhelmingly often? I know in the 1st Blog I confirmed I wanted to take Junior's opinions for what they would want to see in the platformer the most, but right before that part I stated that I mentioned how I wanted to include different types of problems (i.e., Translations back and forth, conjugation, vocabulary, fill in the blanks, etc) in order to strengthen different needs. In context of the game itself, I had this concept of putting some buttons on the home screen that, when clicked, will ask someone the questions that connect to what was on the button, as well as having the platformer level that the part is connected to feel unique from the others (probably a different background, different enemies, etc). With that said, I also had this idea of putting certain questions into an array and having a random question from that list be displayed in `prompt()`. I think that's what I'd like to work on over the break; Testing this system with much simpler questions but still categorized to see if it could work for the game. I want to give the different types of questions a different corresponding keyboard key; For example Historical Questions would be attached to the "h" key, while questions about food can be attached to "f", video games "v", books, "b", etcetera. Of course there won't be a lot of categories, but I want enough categories (likely 4 or 5) that could potentially work alongside one another, even if the code for one set isn't called just yet. I'm super excited to tackle this over the Winter Break, and I know that it's definitely a good time to tackle it now because this can decide arguably the biggest portion of the game rather than the player progression itself!

## Conclusion/Takeaways:
Before we wrap up the Blog for this session, I must bring up the 2 skills I had wanted to work on throughout this development project as mentioned in Blog 1, those of course being **Embracing Failure** and **Organization**. So far into this project, I definitely feel like one skill got the most attention out of these 2, that of course being **Embracing Failure**. Throughout my tinkering process, I would consistently run into little mistakes in my code (such as a certain thing not being defined, or something missing from the code resulting in the entire system not functioning as intended) so I'd try to patch up any errors as quickly and efficiently as possible. FOr example when creating `spriteMarina` as shown in the 2nd Portion of this blog, I almost forgot to give her gravity using `gravity()`, hence why when I tried to run what I had created, I couldn't get the sprite to jump whatsoever. There are other problems that I ran into for sure, but I feel like that one probably would've been the most catastrophic if not fixed, so that's progress! Now for **Organization**, and this is a problem that I've noticed myself having throughout Javascript. Organizing code chunks has always been a little tricky for me as I tend to write something, but then add something extremely important to a segment into a space where it won't receive much attention. The biggest example of that is with this other command I did not mention: `scene(() => {})`. When using this, you'd need to have a trigger for it and when that trigger happens, it should take you to a new screen. This is something I know I will not just utilize during my sessions of tinkering but also in my final project, but I keep accidentally putting it towards the bottom of my script, making me forget all about it and when I try to add something else, I end up running into an error screen. My teacher has also pushed for the implementation of comments with our code, so that is something I want to begin pushing more aggressively for myself during this process in order to be more organized. Now with both of my skills mentioned, I must say that I cannot wait to begin progression towards this new goal; I already established how important it'd be if successful, and if it doesn't work out, then that's completely alright! It just means I have to think deeper. I'm going to bring up this goal to my partner, see what he thinks and change what I do accordingly. Thank you so much for reading this blog (and I deeply apologize for its length), now with that said, have a good day and I'll see you all in Blog 3!

-Bri

[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
