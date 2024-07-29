In chapter 4, Ousterhout identifies one of his main principles for developing software: modules should be deep. That means that modules should have simple interfaces that hide complex implementations. Here's a real world example.

Last week, I used an ice machine at a hotel. Its interface had two parts: a button labeled "push for ice" and an opening labeled, "catch ice here." That’s dead simple.

Presumably, however, the box hid a lot of complexity. I'm guessing that it pumps water in from the plumbing, freezes it to some specific temperature, creates cubes, stores cubes, stops making ice when the storage is full, starts making ice when the storage isn’t full, and moves ice over to the opening when the button is pushed. 

The two-part interface hides all that complexity from me. I have no idea what really goes on between pressing the button and catching the ice. 

Now imagine that same machine with a more complex interface. What would it look like? I imagine that it would expose some of the functions above, but leave it to the consumer to operate those functions. In that case, using the machine might like look this: Press a button to pump in water. Press a button to freeze the water. Press a button to turn the frozen water into cubes. Push a button to store the cubes. Press a button to move the cubes toward the opening. And press another button to drop them out. 

That is definitely more complex. Specifically, it would increase cognitive load and introduce unknown unknowns. First, there would be more buttons to learn. Second, I would have to know the order in which to push the buttons. Third, I wouldn’t know the consequences of getting the order wrong. 

And there’s an additional problem: the complex interface hands the problem solving back to the consumer. At bottom, the consumer has to solve the problem of making ice all over again. Figuring out the right sequence to making ice just is solving the problem of making ice. The only difference is that the complex interface provides a new set of tools for solving the problem. 