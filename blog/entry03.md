# Entry 3: Progress Report #1
##### Brianna Peralta on February 3rd, 2026 (02/03/26)

## Main Information:

Wow. It hasn't even felt like a long time, but now I'm officially in the big 2026! This is your first look at now 17 Year Old Bri (I officially turned that on January 8th), so.. Woo! Anyways after setting a goal for myself right before WInter Break began, students were now expected to try and pursue it to the best of their capabilities. For a refresher of my goal, I wanted to try and use elements from [Kaboom](https://kaboomjs.com/) (specifically the `onKeyPress({})` command) as well as basic Javascript knowledge in order to randomly generate a question based on a specific topic. This was especially important to me since, depending on the outcome, I might end up implementing this on my final project when the time comes! Now that I think about it, me doing this now just further reflects the overall goal of using a tool for your freedom project, so I suppose good job me? Anyways, did I actually make something that could work as intended? Did I make my dreams come true?.. Short answer, yes. Long answer however.. That'll further be explained in the next session!

## Tinkering Progress:

Before I dive into the exact code, I will say this: Simpler yet efficient is **always** better than elaborate yet convoluted. You might not entirely understand why I'm saying this now, but by the time I'm done demonstrating my progressions, it might be more easy to understand? I hope so anyways. Now, I had already mentioned `onKeyPress({})` and essentially it can become a function of it's own. By giving the command a specific key to look for, it will wait for that key to be pressed and once that happens, certain events could happen such as making a connected sprite move in a certain direction, changing your screen to another scene, or simply changing the apperance of your sprite: It all just depends on your inputs. For a great comparison, think about the `.addEventListener()` programmers can use in the DOM, and it's essentially that but initiated by Kaboom. Since it was my first time using it without any additional backing, I originally hoped to start simple, mainly with planning out how I could even attempt this:

```js
add([
text("Click either 'F' or 'C' to get a surprise!"),
])
```

I already planned out I wanted to start with a few different categories of questions (particularly food and or color themed), but due to external circumstances, I only had time to lock in the 'food' category. For this context, it was represented by the F key and as this small `add()` implies, you just had to click the key for one of it's questions. My original plan for the questions were to have the reader decide which question they wanted to answer, essentially giving them 2 prompts to fill out, though I do recall struggling greatly on making it happen: I'd accidentally trip myself up since I wanted the questions stored in an array in order to store them more efficiently compared to typing them out but I was struggling to make the specific question pop up when it was supposed to. As a result, I decided to remedy this problem with a miniature system that I'm already comfortable with: Random Chance.

```js
var foodQuest = ["What is the most popular food in the world?", "what fruit is claimed to be a berry but ultimately isn't?", "What food is commonly eaten in Japan?"];

onKeyPress("f", () => {
var randomQuest = Math.ceil(Math.random() * (foodQuest.length - 1));
```

Admittedly this might seem a lot more complicated to others, but to me this is genuinely pretty easy for me to understand. It starts with the array that is holding my 3 questions: 'What is the most popular food in the world?', 'what fruit is claimed to be a berry but ultimately isn't?' and 'What food is commonly eaten in Japan?'. Now I know I just said there are 3 questions but with the program Javascript and other programming languages use, 0 is counted alongside the other default numbers, meaning instead of starting at 1, it starts at 0. That is why `(foodQuest.length - 1)` exists, since while length wise there are 3 questions, that last question will only be referred to as the **2nd** Index in the array. Regardless though, that number will represent the highest number the `Math.random()` will generate to, and since it already starts 0 as it's lowest value, all we'd have to do is round since `Math.random()` always generates a decimal rather than a whole number. This is where `Math.ceil()` comes in, as it rounds to the **greatest** whole number. Alternatively, I could've used `Math.floor()` which rounds to the **lowest** whole number
## Skill Reflection:

## Conclusions:

[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
