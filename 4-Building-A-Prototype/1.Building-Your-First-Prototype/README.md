# Building your first prototype

Ok so you want to build a prototype, there are things to consider. Some considerations can be made after a while and some are habits you want to adopt as early as possible.

## Use code revision

One of the earliest habits you want to adopt is using code revision. Code revision enables you to do many things like:

- **Revise your code**. Create various saving points in your code that you can go back to
- **Collaboration**. Using an established code revision like Git and GitHUb makes it easy to collaborate on the same code repository
- **Release management**. You are likely to go in and out of periods in your code development when the code feels stable to move to a point where it's less stable because you are doing changes like refactoring or you are adding more functionality. You want to have the ability to point out a time in your code where it works well and _tag_ it as a candidate that can be released. The earlier you think about this, the more prepared you are to demo your system should you suddenly need to demo it to a jury or prospective customers.
- **CI/CD**. Code revision systems usually integrate well with various systems to make it easy for you to produce releaseable code. So what is releaseable code? It's code that's well-tested and does what it's supposed to. You want to automate this process as early as possible so you focus on developing code and pushing it to a repository and then code is then tested and deployed to some system where it can be demoed. 

## Keep configuration separate

You start out, the code works well, and the features as well, but you notice it's hard to change things because configuration information like APIs and database information is part of your code.

To mitigate this problem, ensure to separate configuration information from application code. By doing this separation, it makes you flexible if you later need to change from your local machine to a more production like environment.

## Testing

You want to think about testing early on. As your prototype becomes more and more complex, it makes sense to consider how to test it. There are various testing approaches you can use like. As you are likely to demonstrate your prototype to someone sooner or later, like a jury. You want to make sure you know under what circumstances it works.

- **Integration testing**, testing that various larger parts of your prototype works together.
- **Unit testing**. At this level you are testing that smaller units do what they should.
- **Manual testing**. Having someone manually run through major test scenarios is a good idea. It can catch things that your other test types isn't able to.

## Instructions for running various parts of your code

Although it sounds like documentation is something you can do much of at a later point. It make sense to think about documentation early. What you want to capture is how you start up various parts of your system or if there is configuration that makes the system behave differently. Also think about onboarding a new team member, what parts would they want to know to be able to run the prototype. Consider that this person could be anything from a technical to a non technical person, how would you explain your system differently to these types of roles?

## Use established frameworks and approaches

Depending on your choice of technology, you want to go with established frameworks and programming languages. The benefit to such an approach is that you can find help on pages like Stack Overflow, or official docs, where you to get stuck. 

## Implement gradually, start with core functionality

it's easy to think that you want to add all these features to your prototype. Take a step back, and focus on the core functionality the prototype and make sure you implement those features first and make sure they work really well.

## Accessibility

Can your prototype be used by anyone? Maybe your prototype is only meant to be used be a certain type of user but if not you've got everything to gain by thinking about accessibility early. At least consider how you would implement support for screen readers, translation and so on. It will definitely count in your favor towards a future jury and your users will thank you.
