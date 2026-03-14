# Entry 4: Progress Report #2
##### Brianna Peralta on March 10th, 2026 (03/10/26)

## Main Information:

Ladies, gentlemen, and everyone in between, welcome to the homestretch of SEP (Technically it's not really the homestretch, but it's one of the peaks of the Freedom Project since this is where the main project is getting closer to being finished)! As of writing, the main project will be due on ***April 13th***, basically right after Spring Break. I know that'll be a little hazardous for me personally since I'll be away from the States during the Spring Break (Dominican Republic representation, we love to see it), but I'm confident in my partner and myself's capabilities. With that being said, this portion of my blog is going to end up shorter than usual as most of the information will be in the `Current Events:`, but for a brief summary of what's going on: I've been working on my part of the project; Creating Arrays that'll hold all of the Spanish questions, laying out the format of the different platformer stages and making sure the player's sprite (right now it's a cursor, but I'm fairly confident my partner and I will be changing it so it's just a placeholder) activates and interacts with it's environment correctly. Now with that said, onto the more juicy portion of the blog.

## Current Events:

Now. I've already given the summary, but it's time to focus on the details of what's been going on! Before getting a solid piece of progress, I did some minor experimentations regarding how the code could look. From the little experiments I've done while starting to put everything together, I realized that traditional Javascript and ***[Kaboom](https://kaboomjs.com/)*** do not exactly work well together. I can make variables and such, which have been a lifesaver with Kaboom, but whenever I try to use `Math.random()` for example, I end up facing an error, with Kaboom considering it a function. I'm fairly confidence this is mainly because of `rand()` and `randi()` having a much similar purpose, but even moving past Javascript, Kaboom doesn't mesh all too well with HTML either, loading with the game screen right below some `<h1></h1>` for example. That won't be all too much of a problem however, as Kaboom does provide a good chunk of programs and commands to work with! With that being said, I decided to dedicate the top part of the file into creating some global variables that'll be important later down the line:

```js
var conListQues = ["Hablar; Yo (Present Tense)", "Vivir; El (Present Tense)","Salir; Nosotras (Present Tense)","Beber; Ella (Present Tense)","Pintar; Ustedes (Present Tense)"];
var conListAns = ["Hablo","Vive","Salemos","Bebe","Pintan"]
console.log(conListQues);
var movSpeed = 500;
```

The first 2 variables, `conListQues` and `conListAns`, go hand in hand with each other, acting as 'cards' that'll hold answers and questions for practicing. For this example, they represent verbs that can be conjugated depending on who's using the verb in a sentence, and who the target for the sentence is. For example, if someone wanted to say 'I am 17 years old' in Spanish, their sentence would end up looking like: 'Yo tengo diecisiete (17) años'. When talking about yourself in present tense, you'd take a verb (Tener in this case), and replace the suffix '-er' with '-o'. However, Tener is an irregular verb and it has different changes to it based on whoever's speaking. An example of a regular verb would be 'El bebe jugo de manzana', which translates to 'He drinks apple juice'. In this case, the verb 'Beber' drops the suffix '-er', and since we aren't referencing oneself in this sentence, and instead another person, '-e' would be the replacement. I will show a chart regarding how present tense conjugation works, but there are other types of conjugations, such as imperfect, past tense, and conditionals. For more information, please check out websites such as ***[Spanish Academy](https://www.spanish.academy/blog/master-the-18-spanish-tenses-and-take-our-cheat-sheet-with-you).*** With that said, we also have the variable `movSpeed`, which will basically be how fast the player will be able to move upon loading into the different levels. For example let's take one of the future pieces of code which establishes the player's movement.

```js
  onKeyDown("right",() => {
        cursSprite.move(movSpeed,0);
    })
```

In this portion, the sprite moves right every time the the right-arrow key is down, with the variable `movSpeed` having a value of 500 as established before. I hope that makes sense since the logic is very similar to how left movement works, albeit there is a minus sign right in front of `movSpeed`. This doesn't apply to jumping, but due to the fact we briefly covered left and right movements it felt appropriate to show it here:

```js
onKeyDown("space",() => {
        if(cursSprite.isGrounded()) {
          cursSprite.jump();
        }
    })
```

Essentially as long as the player is on stable ground while hitting the space button, they will jump into the air. Their jump length can be altered based on an established number beforehand using `setGravity()`. Out of preference, I decided to do `setGravity(1000);`, so the sprite doesn't jump into the atmosphere.

```js
add([
    text("Click here to play!"),
    pos(500,250),
    area(),
    "title-card"
])
onClick("title-card", () => go("option-sect")),

scene("option-sect",() => {
    add([
        text("Vocabulary"),
        pos(250,250),
        area(),
        "vocab"
    ])

    add([
        text("Conjugation"),
        pos(800,250),
        area(),
        "conjugation"
    ])
```

While creating the code, I also learned something called `onClick()`, which to me reminds me of the DOM Event Listener: `.addEventListener('click', function(){})`. Essentially when a mouse clicks on an indicated entity, such as "title-card", an action will happen. It's another Kaboom function, and in this case I use it to go to the next scene, which have the 2 topics I wanted to cover. Using the same function, I'll transition the player into another screen, which will hold one part of a level, as seen here.

```js
onClick("vocab", () => go("plat-one"));

scene("plat-one",() => {
 loadSprite("cursor", "/project-images/cursor.png");
 var cursSprite = add([
        sprite("cursor"),
        scale(.10),
        area(),
        body(),
        pos(0,100),

    ])
    add([
      rect(width(), 48),
      pos(0,height() - 48),
      area(),
      body({isStatic: true}),
    ])
```

This is essentially the progress I have so far, but I assure you, there will be more in right before April comes around. Now with that said, stay tuned for any updates!

## The Engineering Design Process(EDP):

For the rest of the blogs, I will not repeat the steps of the ***EDP***, so for the last time, here are the different steps:

* **1) Define the Problem**
* **2) Research the Problem**
* **3) Brainstorm possible solutions**
* **4) Plan the most promising solution**
* **5) Create a Prototype**
* **6) Test and Evaluate the prototype**
* **7) Improve as needed**
* **8) Communicate the Results**

This is certainly an easier call compared to the last 2 Blogs, especially since this whole blog is all about my progress on the project as awhole. Right now, my partner and I are on ***Step 5: Create a Prototype***, though we do also alternate with ***Step 6: Test and Evaluate the Prototype*** as, at least in my opinion, it would be much better to test as we go along with creation. I know that conjugation tends to be the part of spanish that people struggle with the most besides of course pronounciation so I wanted to focus on creating it's cards the most. Here is the conjugation chart as mentioned beforehand:

* ***Yo (I): -o (For all verbs ending in -ar, -er, and -ir)***
* ***Tu (Informal You): -as (For all verbs ending in -ar) or -es (For all verbs ending in -er and -ir)***
* ***El/Ella/Usted (He/She/Formal You): -a (For all verbs ending in -ar) or -e (For all verbs ending in -er and -ir)***
* ***Nosotros/Nosotras (We/We (Female Exclusive)): -amos (For all verbs ending in -ar), -emos (For all verbs ending in -er), or -imos (For all verbs ending in -ir)***
* ***Ellos/Ellas/Ustedes (They/They (Female Exclusive)/ You All): -an (For all verbs ending in -ar) or -en (For all verbs ending in -er and -ir)***

For this project, I really decided to research (especially using notes from past spanish classes), in order to give accurate data as to what the correct answers should be. I've been continiously testing the questions and their respective answers to make sure they run smoothly upon booting up the program. In addition I will also be adding in information about vocabulary, as well as a portal at the end which will serve as a sort of 'Checkpoint'. To pass it, players would need to answer a question correctly in order to pass. How I'll be checking them since `Math.random()` no longer works? Well, I previously mentioned something called `rand()` and `randi()`, so using `randi()` specifically since it asks for specific integers, I've been able to create this:

```js
var quesNum = randi(0,4);
       var ques = prompt(conListQues[quesNum]);
        if(ques == conListAns[quesNum]) {
        console.log("That's correct!");
    } else {
        console.log("Study Harder Bozo.")
```

Of course this exact piece won't be in the final project, but it serves as a basis for what SHOULD happen.

## Skill Reflection & Conclusion:



[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
