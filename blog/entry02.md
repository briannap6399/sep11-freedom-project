# Entry 2: Goal Setting
##### Brianna Peralta on December 15th, 2025 (12/15/25)

## Main Information:
Well, the 2025-2026 Winter Break is pratically right around the corner, as well as the end of Semester 1. My first blog was written more than a month ago, and now this blog is setting up all students of SEP11, including myself, for how they want to tackle work as we take our about 10 day break from classes. If you had asked me what I wanted to do for break right before I had written the 1st Blog, I probably would've said something on the lines of "Break? I need to catch up to everyone as **QUICKLY** as possible!".. To be fair, I'd probably say something similar now but hey, the pressure is not as bad as it was then. Now with that said, after Blog 1 was finished, students were told to continue tinkering with their tool and continue writing their [Learning Logs.](../tool/learning-log.md) I know for those, I tapped into one of the starter games posted in Kaboom and tried my best to recreate it using my IDE as well as the step by step progression guide. However, I tried other things besides just this, but more on that later. Thankfully me and my partner are still partnering for the final result, so for this blog, I plan to not only dig into what I want to personally tackle for Winter Break, but I will also plan some additional things for the future (aka when we start building the final project). So with that, let's get into the progression.


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

This might be a little hard to digest, so let's break it down into something more simple. The `kaboom();` command at top essentially connects Kaboom to your coding project, allowing you to use whatever it has to offer. The variable `moveSpeed` in this context is supposed to represent how fast something will move, with the speed now having a value of 500. `loadSprite()` is, as the name implies, the command that allows for a sprite to feasibly be generated and portrayed on one's game screen. Now `add([])` is really interesting to me, since.. Well, it basically says everything it does in it's name, but it pretty much adds whatever you put in between both set of wraps into your program. This can include sprites, `area()` and `body()`, which establish a hit box for whatever needed, as well as other properties such as `color()`, `scale()`, and `rotate()` (All self explanatory since they were pretty frequent in last year's CSS lessons). Last but not least we also have `onKeyDown(() => {})`. I already explained a bit of what it does but in contrast to `onKeyPress(() => {})`, this command essentially provides a smoother feel compared to the latter as you're supposed to hold the key down and whatever's wrapped inside of it's wraps will happen. Looking back at the example code, note how it includes `spritePlaceHolder.move(moveSpeed,0),`. This means that when the player presses **and** holds a key, the sprite will move towards the right. You can also change the direction the sprite goes by either adding a negative sign by the `moveSpeed`, swapping the position of 0 and `moveSpeed`, or by doing both. There's other properties similar to `.move` such as `.jump` which.. Makes the sprite jump in the air, but for the most part all other parts follow a similar structure. With that said I did mention I spent most of my tinkering time trying to follow that tutorial, creating code segments such as this:

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

## Conclusion/Takeaways:

[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
