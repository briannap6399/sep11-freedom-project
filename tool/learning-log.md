# Tool Learning Log

## Tool: JSON APIs (Geogle)
## Project: Wordle-Inspired Geography Game (Geogle)
### 09/29/25 - 10/06/25:

* [Main source of Data = GeographQL](https://geographql.netlify.app/)

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Tool: Kaboom
## Project: Spanish based Platformer
### 10/27/25 - 11/03/25:

**[Entrance to Kaboom:](https://kaboomjs.com/)**

* Kaboom is a good Javascript Supported software in order to make things such as platformers. I've decided to change from my original idea and instead shift to a platformer that emphasizes the knowledge of Spanish.

For my session of Tinkering, I'm trying to, using the tutorials Kaboom provides, create something that takes on the basics of what Kaboom offers. For this, I've chosen to try and code a bit of a Chrome Dinosaur game found in oje of Kaboom's tutorials, one that doesn't need a lot of effort, but enough to show what could be done with the tool. As of now I've been trying to initiate the tool, and here's my code right now:

```js
kaboom();

loadSprite("bean", "sprites/bean.png");
add ([
	sprite("bean");
	pos(75,50)
])
```
The little indicators or simple enough, but just in case I forget `kaboom();` is what gets the code in it's necessary context and `loadSprite();`, as the name says, loads up whatever sprite you choose for your game. I think what I find the most interesting so far is the fact that `add([])` in Kaboom seemingly functions a little similarly to Functions, whereas they both usually take code inside of themselves and act upon it when fully declared. Neat. However, I must stress that in order to use Kaboom more easily, you need to make sure to initalize usage properly. Admittedly I struggled on that a little, trying to see why I wouldn't find the checkered background associated with Kaboom when using `http-server`, but I was able to figure out that the initalizing code must be placed in an `.html` file, so that helped with making the code function.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Tool: Kaboom
## Project: Spanish based Platformer
### 11/10/25 - 11/17/25:

**[Entrance to Kaboom:](https://kaboomjs.com/)**

So, good news! I think it might be best if I forgo using a `.js` file for this tool as I can load everything perfectly on a `.html` file. Anyways, I decided to continue on with the progress I was making before, with the chrome dinosaur game. Last time I managed adding the default sprite to the default checkerboard pattern background using `add([])` as well as `loadSprite()`, but since I decided to shift to a `.html` file for Kaboom's code, I decided to try and add in my own sprite using the same code, so with that, I present Marina!

<img src="marina-sprite.png"></img>

The woman in this sprite isn't my own creation admittedly, and instead she's from one of my favorite video game franchises (Splatoon), but I thought it would be cool to tinker with her sprite! With that said, the next part of this tutorial gives insight on using some properties you'd actually see in CSS:

```js
loadSprite("marina", "marina-sprite.png");
add([
    sprite("marina"),
    pos(80,50),
    scale(.5),
    rotate(30),
    color(25,25,25),
]);
```
I never knew that Kaboom includes CSS Properties, but now that I do know I'm certainly more than impressed! Now, the 3 new properties as seen in this miniature chunk of code functions just how you'd expect:

* `scale(),` - *Input a scale size of your choosing on a sprite. Any values > 1 will make the sprite dilate in size, while any values < 1 but more than 0 (such as .5 for half or .25 for a quarter) will make the sprite compress.*
* `rotate(),` - *Makes the sprite rotate on a simple degree scale. What I've noticed for this command is the fact that the sprite seemingly moves in a wider circle while also making it point in a different direction. For example, if I make Marina rotate about 180 degrees, not only will she be upside down, but most of her will also be off the screen.*
* `color(),` - *Simply changes the color of a sprite based on an RBG system. You can add 3 numbers and based off the colors you add, you will see the sprite change.*

With the meanings of these properties listed, here is what they make Marina look like when all put together:

![CSS Properties-Marina](image.png)

Pretty cool in all honesty. But before we wrap up this session of tinkering, I want to mention one more chunk of code that while not mentioned exactly in the tutorial, I think it'd be nice to jot down now. To be specific, it's a chunk of code that lets you move your sprite:

```js
const spriteMarina = add([
    sprite("marina"),
    pos(80,50),
    scale(.5),
    area(),
    body(),
])
const moveSpeed = 230;
onKeyPress("right", () => {
    spriteMarina.move(moveSpeed,0)
})
onKeyPress("left", () => {
    spriteMarina.move(-moveSpeed,0)
})
```
In order to make your sprite can actually move, you'd need to make a variable that holds your sprite. In this case, I used `spriteMarina` as my variable since it lets me know that what I'm doing is for, well.. Marina. Before I can think of using the movement code, I need to make sure I not only define how fast she'd move (using another vairable called `moveSpeed`) but I also need to consider what key on a keyboard will make her move. For this test, I decided to use only the left and right arrow key and plugged it into `onKeyPress`, which has a self explanatory name. I cannot stress how important it is to imagine the checkerboard as a coordinate plane, as a `moveSpeed` with a negative sign attached to it will make it go left, while a poisitive `moveSpeed` will make it move right. I know you can also make your sprite jump by using similar code and instead of including the movement speed variable as well as `.move()`, you use `.jump()`.

## Tool: Kaboom
## Project: Spanish based Platformer
### 11/17/25 - 11/24/25:

**[Entrance to Kaboom:](https://kaboomjs.com/)**

As mentioned last time, 

<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
