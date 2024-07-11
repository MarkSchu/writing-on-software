<header>
    <h1>Reading <i>A Philosophy of Software Design</i> - Chapter 2</h1>
    <h2>Three Symptoms of Complex Systems</h2>
</header>

Ousterhoff presents three symptoms of complexity. When a system is complex, the complexity manifests in three ways: 

    1. Change Amplification 
    2. Cognitive Load 
    3. Unknown Unknowns 

Change Amplification is when a small change requires modifications in many places. When a system is complex, the developer has to touch multiple files or functions in order to implement the simple difference. 

Cognitive load is the amount that the developer needs to know to make a change. When the system is complex, the change requires the developer to know a lot. 

Unknown Unknowns are the things that the developer needs to know in order to make the change, doesn't know, and doesn't know that they don't know! For instance, suppose you're using TypeScript and don't know that TypeScript comes with a config file. Not knowing how to configure TypeScript is an unknown. Not knowing that you don't know how to configure TypeScript is an unknown unknown.  

You can think about each of these symptoms as relative to particular changes in specific systems. Given a change and a system, you can ask about it's change amplification, cognitive load, and unknown unknowns. 

Now, here are a few thoughts on each. 

Change Amplification is measured in effort, the effort of keystrokes, thinking, switching files, and switching contexts. It is an answer to the question, "How much does the programmer need to do during the implementation?" If you have to change 10 files for a simple change, then you might be dealing with change amplification. 

Hardcoding the same value over and over generates this problem. When you want to change the value, you have to change it everywhere. In contrast, if you assign the value to a variable and reference the variable in multiple locations, then changing the value means changing it in a single place. 

Cognitive load is the number of things that the developer has to remember or keep in mind to make the change; it is a quantity of knowledge. It's an answer to the question, "What do I need to know to make the change?" And like any load, the larger it is, the harder it is to hold. If, in order to make a change, you have to consider an api, three modules, two configuration files, and a set of conventions, then the change will be harder.

Cognitive load is really about attention and relevance. It's an answer to the question, "What is relevant?" Systems can be very large and contain an incredible amount of detail (to say nothing about the ecosystems that they exist in). As a developer, you have to know which parts of that huge system are relevant to your change and which are not. And as humans, we can only attend to so many things as one time. If many things are relevant to the change then it is hard to think about. 

A large set of unknown unknowns leave you with two ugly possibilities. First, that you can't get things working. And second, that you do get things working, but introduce bugs. Both happen because there are things you don't know. In the first case, there are missing pieces to the puzzle. And in the second case, there are side effects that you don't know about. 

Another way to think about unknown unknowns is in terms of cognitive load. Cognitive load is an answer to the question, "What do I need to know?" Unknown unknowns make answering that question difficult. That is, unknown unknowns are associated with the question, "How hard will it be find out what's relevant?" If there are many unknown unknowns, then it's going to be very hard. 

In short, you can sum up the three like this: 

    1. how difficult is it to implement the change? 
    2. what's relevant to the change?
    3. how hard is it to find out what's relevant? 
