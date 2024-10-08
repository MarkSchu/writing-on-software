<p>John Ousterhout explains that the fundamental problem of software design is Problem Decomposition: How do you take a problem and divide it into independently solvable parts.</p>

<p>When you solve a problem, you almost always have to break it into parts. For instance, if you want to build a feature that displays economic data on a browser, you might break it down like this: </p>

<ol>
    <li>fetch data from api </li>
    <li>transform data</li>
    <li>display data in UI</li>
</ol>

<p>Since you know how to solve each part, you now know how to solve the whole.</p>

<p>This feels like common sense, but there are a lot of interesting things to think about. Here are a few initial thoughts.</p>

<p>First, there's an important distinction to make between the problem, the solution, the implementation of the solution, and the process of implementation. The problem is a description of what you want: display economic data on the browser. The solution is how you're going to do that: fetch data from an api and display it using a web app. The implementation of the solution gets into specifics: use this technology and call those methods on these classes. The process of implementation are the steps that the team is going to take to implement the solution.</p>

<p>Problem decomposition shows up in the transition from problem to solution. In a way, problem decomposition is problem solving. You take a large problem and break it into small problems that are already solved, and then you recombine them into one, large, solved problem. </p>

<p>That said, the transition from solution to implementation and the process of implementation itself are also problems in their own right, so problem decomposition shows up everywhere. </p>

<p>Second, why is it necessary to break the problem into parts? Why can't a developer solve the whole problem at once? For two reasons I think: (1) the entire problem is too much for the programmer to think about at once, and (2) it identifies places where the programmer can start. In other words, problem decomposition is about human psychology, it's about the limitations and shape of the human mind. Because of that, vague senses and feelings are an active ingredient. Why does one problem decomposition feel like the right problem decomposition? Because it gives the feeling of being able to wrap your head around the problem.</p>

<p>Third, problems have many possible decompositions. You can break down the problem in many different ways. For the problem above - display economic data on the browser - you could use:</p>

<ol>
    <li>fetch data</li>
    <li>display data </li>
</ol>

<p>or</p>  

<ol>
    <li>fetch data from www.economicdata.com/api/summary</li>
    <li>receive data</li>
    <li>transform data</li>
    <li>add data to client state </li>
    <li>render display using new state</li>
</ol>

<p>Different compositions have different levels of specificity, different levels of formality, and make different assumptions.</p>

<p>Fourth and finally, different decompositions resonate with different programmers. Not only are we dealing with the limitations and shape of the human mind, we're dealing with the limitations and shape of particular human minds. Different people associate different levels of cognitive load with the same decomposition as a result of their own personal experience. What helps one programmer may not help another. </p>

<p>There's a lot more to think about here, but this is a start. Problem decomposition may be matter of common sense, but it's really rich. </p>