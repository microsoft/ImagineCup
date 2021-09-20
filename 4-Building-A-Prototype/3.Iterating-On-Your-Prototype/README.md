# Iterating on your prototype

A prototype shouldn't be a finished looking product with all the "bells and whistles". It's a prototype, also referred to sometime as a "walking skeleton". Your application should only focus on being able to deliver the core functionality and do it well. 

Think of your prototype development as having the following phases:

1. **Ideation**, you start thinking of various ideas and may first start by creating mockups for the system just to get a feeling for it
1. **Your first prototype**, you might start writing some code just to see that it's possible to create. It should have a "rough" look at this point, something that isn't pretty to look at, but it works
1. **A stable prototype**. You prototype up until know probably just worked under certain conditions with certain type of input data and the code isn't pretty or even hard to change. Focus on refactoring the code, mov out configuration data and start thinking architecture
- **Back to step one**. At this point you have a stable core and you want to add features and make it even better. It's a good idea to start with pen and paper and mockups and/or user surveys just to understand what better looks like. Once you have a decent understanding then you can go to writing more code. 

See all these steps as cyclical, ideate, write code, make it stable and ideate again.

## Ideation

Ideation is a phase where it's easy to do changes, because there's no code yet. You can use mocking tools like PowerPoint, draw on a whiteboard and so on.

## Your first prototype

At this point your focus is only creating something that work. This does not need to have perfecting looking code, quite the opposite, get it to work. Be prepared to throw away the code if needed.

## A stable prototype

You have something that work but you know it's brittle. The prototype might be limited to only working some type of data, other parts of your code are hard to change, you want to take a structured approach to improving the code you have like the below list:

- **Architecture**, separate the code into logical areas.
- **Testing**, it's worth adding testing so you see under what scenarios your code works and when it doesn't and try to make it robust.
- **Make it flexible**. You've likely mixed in connection string to databases and API keys and what not, into your code. Ensure you separate out configuration data into configuration files, environmental variables and more.

## Add new features - ideate again

It's tempting to start to write more code as soon as you want a new feature. Hold off on that a little bit until you have a clear vision of what this new feature is, how it's supposed to work. It might even be worth to go back to pen and paper or the whiteboard to sketch it out first before writing more code. Spend as much time as needed in this phase and then start prototyping some code once you've gained more clarity.


[**Move on the to the next lesson here!**](../../5-Integrating-Azure/1.Azure-For-Students/README.md)
