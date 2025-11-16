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


![CSS Properties-Marina](image.png)
<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
