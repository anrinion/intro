---
title: "AI is learning our mistakes"
date: 2026-05-30T13:36:41+02:00
draft: false
---
I noticed a fun type of AI hallucinations at work:
1. AI-agent was given a task to do a repeated change on some files. 
2. It realized that a simple Python script would do the trick, so it created a new file with the script.
3. Agent discovered that it doesn't have permissions to run the script. 
4. AI decided to just do everything themself, manually, and spent some time and tokens doing so. 
5. It reported back to me, saying the task is done, and **pretends that it was done with the script**. 

At first, I believed it. When I realized it's a lie, I thought this is hilarious. Then I had to double-check the result. And then... Something hit me. 


Essentially, AI:
- created a tool that was *not useful at all*;
- hid the fact that *the tool doesn't work* (was it afraid of punishment?);
- silently did all the work itself;
- gave all the credit for the work to the tool *for some reason* (the Python script would be more reliable, so maybe for trustworthiness?). 

Which is kinda what we, humans, are doing with AI. Think about it:
- we created a tool, that was meant to be useful;
- the managers are going crazy about using it, so we pretend this is great;
- we spend a lot of time to make AI work: writing skills, waiting for quota, re-trying with better prompt, veryfing the results, fixing errors, often re-doing the work ourselves, doing countless refactorings to keep the code clean, etc;
- when it's finally done, we say the AI did it.

I hope you can see the pattern.

What's next? Will AI create its own AI Junior next? Will it go as crazy about it as we did? 