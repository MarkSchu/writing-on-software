<p> 
  There are three basic concepts: modules, interfaces, implementations, and abstractions.
</p>

<p>
  A module is a part of a system. In programming, there are many kinds of modules, but the most common are classes and functions and apis. It is, at bottom, something that's consumed; smething that is used. It's a machine that does some kind of work like getting, setting, or transforming.
</p>

<p>
  Modules consist of two parts: an interface and an implementation. An interface is the part of the machine that gets used. You can think about it as the control panel of the machine, filled with buttons and displays, that other things use. I like to think about the interface as a set of affordances; the interface says, "This is what you can do with the machine." You can turn this dial, read this value, or flip this switch. 
</p>


<p>
  The implementation is the how the interface works. An interface might include a button that says, "Turn on." When you press the button, there is an expectation that the machine turns on. The implementation fulfills that promise. The significant bit is that the interface hides the detail of the implementation. It creates a black box. 
</p>


<p>
  The interface stands in a relationship of abstraction to the implementation. The interface hides the details, the nitty-gritty, of how it does it. Another way to say this is that the interface shows the consumer of the module what's relevant. For instance, if the implementation uses a counter variable to get something done, the consumer of the interface doesn't need to know. So it's hidden. 
</p>


<p>
  Interfaces and abstraction are about managing complexity. And they do this in a few ways. 
</p>

<p>
  First, interfaces hide irrelevant complexity. If you can reduce an interface to 3 methods, that is less to remember, less to deal with, less to learn. The complexity is hidden. This is the value of abstraction; you remove the irrelevant from sight. 
</p>

<p>
  Second, interfaces isolate complexity. An implementation is something that fulfills an interface. There are always many different implementations of the same interface. And if you want to change an implementation, all you need to do is make sure that it fulfills the interface. If you do, you can change whatever you like. 
</p>

<p>
  Third, interfaces introduce complexity into a system. The complexity of a module is, relative to the system, the complexity of its interface. Since it's internal, implementation complexity is hidden, all you need to do is worry about the interface. 
</p>


