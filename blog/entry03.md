# Entry 3: Progress Report #1
##### Brianna Peralta on February 3rd, 2026 (02/03/26)

## Main Information:

Wow. It hasn't even felt like a long time, but now I'm officially in the big 2026! This is your first look at now 17 Year Old Bri (I officially turned that on January 8th), so.. Woo! Anyways, after setting a goal for myself right before WInter Break began, students were now expected to try and pursue it to the best of their capabilities. For a refresher of my goal, I wanted to try and use elements from [Kaboom](https://kaboomjs.com/) (specifically the `onKeyPress({})` command) as well as basic Javascript knowledge in order to randomly generate a question based on a specific topic. This was especially important to me since, depending on the outcome, I might end up implementing this on my final project when the time comes! Now that I think about it, me doing this now just further reflects the overall goal of using a tool for your freedom project, so I suppose good job me? Anyways, did I actually make something that could work as intended? Did I make my dreams come true?.. Short answer, yes. Long answer however.. That'll further be explained in the next session!

## Tinkering Progress:

Before I dive into the exact code, I will say this: Simpler yet efficient is **always** better than elaborate yet convoluted. You might not entirely understand why I'm saying this now, but by the time I'm done demonstrating my progressions, it might be easier to understand? I hope so anyways. Now, I had already mentioned `onKeyPress({})` and essentially it can become a function of its own. By giving the command a specific key to look for, it will wait for that key to be pressed and once that happens, certain events could happen such as making a connected sprite move in a certain direction, changing your screen to another scene, or simply changing the appearance of your sprite: It all just depends on your inputs. For a great comparison, think about the `.addEventListener()` programmers can use in the DOM, and it's essentially that but initiated by Kaboom. Since it was my first time using it without any additional backing, I originally hoped to start simple, mainly with planning out how I could even attempt this:

```js
add([
text("Click either 'F' or 'C' to get a surprise!"),
])
```

I already planned out how I wanted to start with a few different categories of questions (particularly food and or color themed), but due to external circumstances, I only had time to lock in the 'food' category. For this context, it was represented by the 'f' key and as this small `add()` implies, you just had to click the key for one of its questions. My original plan for the questions were to have the reader decide which question they wanted to answer, essentially giving them 2 prompts to fill out, though I do recall struggling greatly on making it happen: I'd accidentally trip myself up since I wanted the questions stored in an array in order to store them more efficiently compared to typing them out but I was struggling to make the specific question pop up when it was supposed to. As a result, I decided to remedy this problem with a miniature system that I'm already comfortable with: Random Chance.

```js
var foodQuest = ["What is the most popular food in the world?", "what fruit is claimed to be a berry but ultimately isn't?", "What food is commonly eaten in Japan?"];


onKeyPress("f", () => {
var randomQuest = Math.ceil(Math.random() * (foodQuest.length - 1));
```

Admittedly this might seem a lot more complicated to others, but to me this is genuinely pretty easy for me to understand. It starts with the array that is holding my 3 questions: 'What is the most popular food in the world?', 'what fruit is claimed to be a berry but ultimately isn't?' and 'What food is commonly eaten in Japan?'. Now I know I just said there are 3 questions but with the program Javascript and other programming languages use, 0 is counted alongside the other default numbers, meaning instead of starting at 1, it starts at 0. That is why `(foodQuest.length - 1)` exists, since while length wise there are 3 questions, that last question will only be referred to as the **2nd** Index in the array. Regardless though, that number will represent the highest number the `Math.random()` will generate to, and since it already starts 0 as it's lowest value, all we'd have to do is round since `Math.random()` always generates a decimal rather than a whole number. This is where `Math.ceil()` comes in, as it rounds to the **greatest** whole number. Alternatively, I could've used `Math.floor()` which rounds to the **lowest** whole number, but considering the context of the system, `Math.ceil()` felt much more appropriate.

```js
if (randomQuest == 0) {
 var ansZero = prompt(foodQuest[0]);
   if (ansZero == "rice" || ansZero == "Rice") {
       alert("That's Correct!");
   } else {
       alert(ansZero + " is not the correct answer.. Sorry!");
   }
} else if (randomQuest == 1) {
   var ansOne = prompt(foodQuest[1]);
     if (ansOne == "strawberries" || ansOne == "Strawberries") {
         alert("That's Correct!");
     } else {
         alert(ansOne + " is not the correct answer.. Sorry!");
     }
} else {
   var ansTwo = prompt(foodQuest[2]);
     if (ansTwo == "ramen" || ansTwo == "Ramen") {
        alert("That's Correct!");
     } else {
       alert(ansTwo + " is not the correct answer.. Sorry!");
     }
}
```

With the new system in place, all I had to do was set up some conditionals, stating what would happen if a specific index is called. All indexes upon being called would be given a prompt that states the question, and then they are free to type in their answer. I would've originally asked the reader to insert their answer as fully undercase, but I know that me personally, I'd much rather put in an answer to a question with the first letter as uppercase, hence why there is an `||` (or statement) in between the lowercase and uppercase variations of the correct answer. Regardless of how the answer is inserted however, they'll either be told they answered correctly or not. If the reader wants, they can type in the 'f' key once again in hopes of taking on the question they failed to get correct or get a new one altogether. In each case however, I feel deeply proud of this bit of progress, since it confirms my original thoughts about combining javascript with kaboom!

## Yet another Revisit to the EDP: 

Welcome back old friend as they would say. Now, here's a quick refresher of the different Engineering Design Process stages:

* **1) Define the Problem**
 * **2) Research the Problem**
 * **3) Brainstorm possible solutions**
 * **4) Plan the most promising solution**
 * **5) Create a Prototype**
 * **6) Test and Evaluate the prototype**
 * **7) Improve as needed**
 * **8) Communicate the Results**

In a similar vein to what was said in the last blog, I think it's safe to say I'm in between Stage 3 of the EDP, also known as **Brainstorm Possible SOlutions**, and Stage 4, also known as **Plan the most promising solution**. It's clear to me that the platformer is already set in stone for what my partner and I want to work on, but how it'll be structred is still up to debate. Based on what I've  
## Skill Reflection + Conclusion:

Now with that said, what about the skills? Also as previously stated, the 2 skills I wanted to try and enhance ended up being **Embracing Failure** and **Organization** and once again, **Embracing Failure** received the most development, something I'm not surprised by as this whole process is obviously going to take trial and error. Yet with that said, I wanted to pinpoint my original failure with the `foodQuest` array as a prime example of me taking accountability for my failures but not dwelling on it for too long and instead striving to find a more efficient method to the madness (the `Math.random()` solution that ended up working phenomenally). If I had to think of an example for **Organization**, then I suppose the best example could be the fact that I was considerate when it came to how I wanted my javascript structured: I specifically created the array of questions first, then wrote the code that randomly generated 0-2, then typed out the if + if else statement. I hope to try and further focus on **Organization** by the time the next blog is due. Perhaps to do so, I can shift my focus onto creating my own scenes upon clicking a certain button, rather than a random question so I can heavily focus on using comments as well? I feel confident in that plan, so I think that's what I'll be doing! I can already see the timeline that this ends up bringing in for me, so I can't wait to show you what happens next. Thank you so much for taking the time to write this shorter blog, and I hope to see you in the future for Blog 4. Take care now!

-Bri

[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
