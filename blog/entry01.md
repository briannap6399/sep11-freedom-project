# Entry 1: Tool Solidification 
#### Brianna 'Bri' Peralta on November 3rd, 2025 (11/03/25) 

## Main Information:
Going into SEP11, I already knew we'd be covering Javascript and how to use it, but what I did not expect was to write the 1st Blog so late compared to last year, let alone with it talking about Tools for the final Freedom Project (FP). Enough of mentioning time however, this FP is definitely way different compared to SEP10's which was all about Web-Design. For this one, we need to create a running and functional program; This program could be anything, from small games to alarm clocks and digital to-do lists. It all just depends on something you as a creator feel passionate about, and the necessary materials needed in order to actually create your final project. Just like SEP10's FP, we are given a tool (typically a website that uses Javascript and website specific commands in order to make something) that will be able to help us along our creation progress and get more comfortable in the world of Javascript, but you do need to be mindful that your tool actually needs to be at least relevant towards your end project. A tool that is much better for game development for example should not be paired with someone who wants to make an app for finding music taste, and a tool that gives people outside information on any topic would not be good for someone who wants to create something personal like a to-do list. As a result, proper selection is absolutely key. Even before coming into SEP11, I always knew I wanted to develop a game for this year's FP. My only problem was I wasn't confident on what game to create, but I did have an idea what would be in my top 2; either a Wordle based game for Geography that runs with **[JSON APIs](https://github.com/public-apis/public-apis)**, or a 2D Platformer that helps educate people on Spanish and runs with **[Kaboom](https://kaboomjs.com/)**. These 2 ideas would have to run on different tools, so by determining which tool I would use, I was also determining what idea I'd use. Eventually though, I decided on using Kaboom and the 2D Platformer Idea, but more on why later. Before we get into that though, I do also want to add that I'm going to be working with a partner for this blog. In particular, I'm going to work with a close friend named Alberto Gonzalez Jr as we both do have similar visions for this project. 

<img width="300" margin-left="100" height="168" alt="download" src="https://github.com/user-attachments/assets/b8f79f9f-2850-4608-9147-13bbda0b018b" />

## Tinker Progression:
Even before we had to make a final selection as to what tool we were to use, we were given about a week to begin tinkering and experimenting with a tool we were interested in. Since I was still split on what I wanted to focus on, I decided to first work with the APIs, and if I enjoyed it, I'd pursue; Otherwise, I'd switch to Kaboom. I remember trying it for that week as planned, but for the first few days (Monday-Thursday), I admittedly got stuck real quick. The APIs did not make any sense to me whatsoever, and I started to doubt if I even wanted to continue with the APIs. I decided to give myself a break on Friday to think, taking Saturday and Sunday to finish my learning log. Unfortunately though, I remember trying to boot up my laptop on Saturday, but my password didn't work at all! I think I might've been cyberattacked, but that extension to my break (even if I didn't want that extension in the first place) made me realize there was no way I'd stick to the APIs, so Kaboom ended up being my selected tool, and the 2D Platformer won out overb the API!

Now, onto the 2nd Learning Log. I decided to focus on initiating the website and attempted to recreate a small section of some code listed as a part of a Kaboom tutorial, particularly one that would load a "sprite" (a movable image/set of images made to represent the player). Before that however, I did have some issues with properly bringing Kaboom into my code. The website did offer a tutorial on how to do exactly that and I followed it to the best of my abilities, but the problem was that whenever I tried to connect a Javascript file to the main `index.html` file and check it, I'd always be met with a white screen. 

  <img width="613" height="306" alt="image" src="https://github.com/user-attachments/assets/3d6646fa-e878-4490-89b7-4db249aafc9c" />

I'm happy I got this problem at the beginning however, because if I had to deal with this when we're really supposed to focus on creating our project, that wouldn't be good at all would it? I've tried to put the initiating code and a small bit of JS on an `.html` file, and that seemed to work? However, I do want to bring this up with my teacher or a senior mentor and see if I can get help with this. Maybe even make it a **skill** for this Freedom Project. With that said, I started to work on the small section from Kaboom, and this was the piece I was able to create: 

  ```js
loadSprite("bean", "sprites/bean.png");
add ([
	sprite("bean");
	pos(75,50)
])
```
The different bits of code is rather self explanatory, but just in case.. `loadSprite();`, as the command implies, is all about loading an image into your game and deeming it as a sprite. For this, keep in mind that you must **name** the sprite, then properly **link where the sprite's image comes from**. Next up, `add([]);`: This command adds things such as sprites to the main screen. Then we have `pos();`, which places the sprite in a specific location based on coordinates (x,y). Just keep in mind that the horizontal placement must come **1st**, and the vertical placement comes **2nd**. This might end up becoming another **skill** I'd need to develop, but I'm ready to face the challenge whenever it happens. 

## Re-Visiting the Engineering Design Process (EDP):
  With everything said, say hello once again to the Engineering Design Process, or just EDP! For a refresher, the EDP works in 8 steps;

  * **1) Define the Problem**
  * **2) Research the Problem**
  * **3) Brainstorm possible solutions**
  * **4) Plan the most promising solution**
  * **5) Create a Prototype**
  * **6) Test and Evaluate the prototype**
  * **7) Improve as needed**
  * **8) Communicate the Results**

Considering the fact that we're not solidifying what we want to focus on for the rest of the year, I'd say my partner and I are on Step 1. However, we both have acknowledged the needs our platformer could potentially fulfill. I've already mentioned how this was targeted towards learning how to speak Spanish, but to go into more detail, this game is supposed to be a hybrid of the typical language learning app and something like Mario; As the player progresses in the game, they will be given different problems they have to solve, such as translating basic English sentences into Spanish and vice versa, as well as giving proper definitions to Spanish vocabulary and learning how to properly conjugate verbs, normal or irregular. In theory, this should help your brain remember what you'd need in order to hold a basic Spanish conversation, and especially since this year there is a big Spanish exam in June for most Juniors, I feel like this game would not only help me, but also help out my fellow Spanish learners! Before we get too ahead of ourselves however, I do want to determine what portion of Spanish Juniors struggle with the most, that way my partner and I can cater to that need the most (Of course there will be other needs that won't get much attention, but they will be met nevertheless). Maybe this could be done through some quick polling? It would be the best way to get information from everyone, but more on that another day.

## Conclusions / Take-Aways:
Phew! That's everything for this Blog.. Right? Not exactly. Remember how I mentioned 2 skills I could potentially try to develop throughout my progress on the Freedom Project? I'd hope so, because before I go, I would like to talk to them. Considering my skills for the last Freedom Project were all about managing time, being flexible and doing research more efficiently, I thought it would be nice to try and come up with new skills that'll reflect my progress this time! Considering the fact I struggled with accurately downloading the initiating code for Kaboom, I feel like the 1st skill I should try to develop would be **Embracing Failure**. For this, I'm also including self-advocacy in this skill as well, since I do plan to speak with my teacher for his help in the future. As for the 2nd skill, this is more so a prediction into the future, but I think I should be prepared for times where I will have to sift through my code and debug any unfortunate situations that may pop up. As a result, my 2nd skill would be **Organization**. Considering me as a person, one who really likes to let all the knowledge in her head spill out without realizing I might be making a mistake, I think this would be a great skill to try and develop. Now, we've reached the end of this blog entry. I'm excited to continue on with the 2D Platformer, as well as the Freedom Project as a whole and the different kinds of problems that could potentially follow. Thank you so much for reading, and I hope to see you in the 2nd Blog!

-Bri 


[Next](entry02.md)
[Home](../README.md)
