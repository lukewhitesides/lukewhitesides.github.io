---
layout: post
title: My First Vibe Coding Experiment
subtitle: I built a specialized language learning routine for free in 20 minutes
cover-img: /assets/img/nguyen-truong-JdWdHdkkRec-unsplash.jpg
thumbnail-img: /assets/img/nguyen-truong-JdWdHdkkRec-unsplash.jpg
share-img: /assets/img/path.jpg
author: Luke Whitesides
---

### Background
Recently, I've been hearing more and more about "vibe coding." As defined by [Wikipedia]([https://en.wikipedia.org/wiki/Vibe_coding), "Vibe coding is an AI-dependent programming technique where a person describes a problem in a few sentences as a prompt to a large language model (LLM) tuned for coding. The LLM generates software, shifting the programmer's role from manual coding to guiding, testing, and refining the AI-generated source code."
Having spent the last 7 years of my career as a product manager, this sounds not too dissimilar to the interactions I have with engineering teams building new technology products. As a product manager, much of the quality of my contributions depends on the accuracy and specificity of how I communicate context, requirements, and use cases to my engineering team. Based on my experience doing this, I assumed I'd be a pretty good vibe coder and wanted to put it to the test.
### Step 1 - Use Case Selection
The first step to my vibe coding project was identifying a problem or need that I had that had not yet been met by any existing app, website, or software. Fortunately, I had something in mind.
To give some background, I would consider myself proficient, but not fluent, in speaking and understanding Spanish. From 8th grade through my final year of college, I took Spanish classes for about 7 years. I have retained a pretty good understanding of grammar and basic vocabulary, but more advanced vocabulary has often drifted from my memory. So far, I have never been able to find a good solution to practice advanced Spanish vocabulary, as language learning apps like DuoLingo and Babbel are too easy for my current ability with the language. I needed a more targeted way that would help me focus on learning vocabulary that I did not know.
### Step 2 - Solutioning
Based on the problem described above, my core user need was a way to learn Spanish vocabulary in a more time-effective way. A simple solution I identified was through a flashcard-style study/review method, but one based on the relative frequency of each word in the Spanish language.
Rather than being presented with random words to study, the most common words would be presented for study first—a stack rank of the most common words in the Spanish language. This would ensure I have a grasp on the most foundational vocabulary first before getting to esoteric words I am unlikely to encounter. However, in order to not waste time, if a word is already known, it will be skipped in future study sessions so that time is not wasted reviewing basic vocab over and over (a la Duolingo). The goal of the solution is to as efficiently as possible identify words in Spanish that 1) I do not already know and 2) am most likely to encounter in various situations.
Note: I am aware there are language learning platforms that use this approach, but I also mostly wanted to use this solution as a test bed for vibe coding independent of other use cases.
###Step 3 - Vibe Coding
Now that I had a problem in mind and the concept of a solution, it was time to vibe code. I started by searching DuckDuckGo for "best vibe coding tool." After looking through a couple of links, I selected [Replit](https://replit.com/) (which is powered by Claude Sonnet 3.5 at the time of writing this) and signed up for a free account using my Github account.
This is the starting prompt I gave it:

![Screenshot of a prompt](/assets/img/vibecoding-1.png)

After a few minutes, it developed the first version of the app with this output. It named the app "VocabLearn Spanish," so I guess the LLMs haven't mastered marketing yet. Additionally, it decided to implement the user authentication system anyway. I would have preferred an initial prototype to just use browser storage/cookies to track progress for a simpler overall system.

![Screenshot of a prompt](/assets/img/vibecoding2.png)

There were a few obvious bugs I noticed during my first time testing it, with certain buttons not working. I reported these in a single prompt, and it fixed 2 of the 3 bugs. Similar to real engineers, it possibly does better when each bug is reported and investigated individually.
I tested the app again and noticed a functionality issue in which the app would only recognize one possible translation as correct, when it is possible for a word in Spanish to have multiple translations or vice versa. For example, when prompted for the Spanish word for "her," I responded "ella" and it registered this as incorrect, with the correct translation being "su." "Su" would be the correct translation when the word is used as a possessive, but "ella" would be correct when it is used as a direct object or object of a preposition. E.g., "her dog" vs. "speak with her" both use the same word in English but would have a different word for "her" in Spanish for each context.
I reported this to Replit, and it understood the problem and started implementing a solution. 

![Screenshot of a prompt](/assets/img/vibecoding3.png)

It took about 10 minutes for it to solve this problem, but the new version of the app handled this very gracefully. For example, the word "were" can have a number of different translations in Spanish.
At this point, I ran out of my free usage of Replit, but the app was in a pretty good state - MVP level that I was able to "build" in about 20 minutes.

![Screenshot of a website](/assets/img/vibecoding4.png)

![Screenshot of a website](/assets/img/vibecoding5.png)

### Takeaways
1. **Vibe Coding is going to be a game changer for Proof of Concepts and Prototypes**  I was able to create a working MVP level app for free within about 20 minutes. This is less than the time it took me to write this article about the vibe coding. This will unlock tons of potential for building prototype and MVP level software to validate a market, or even a new feature within an existing product.
2. **It is not ready to replace modern engineers** I would guess the app that I "built" likely could have existed around 25 years ago (While I was only 6 years old at that time, it seems less complicated than Neopets, which is my main experience with early 2000s web tech). Any new software solution with a mid-highly skilled engineering team working on it will be a much more difficult problem to solve or involve much more complicated technology. I doubt a vibe coding system would be capable of this.
3. **Vibe coding is going to be most beneficial for business-savvy engineers and tech-savvy product people** While LLMs are quickly abstracting away coding to prompting, there will still be a need for people who can identify customer problems and solutions. In my experience, the best software engineers do not just write code but are systems thinkers who can truly solve user and customer problems. Similarly, great product managers do not just write requirements but are synthesizers who can identify user pain points and validate ways to solve them. While LLMs may level the playing field for coding, the best software products in this new era will be differentiated by human creativity.
