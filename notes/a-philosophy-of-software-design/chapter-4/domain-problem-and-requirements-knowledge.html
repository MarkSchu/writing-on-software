<p>
  One way to describe the role that the interface of a module plays is, "The interface describes what the module does." In some ways, this is true. For consider a module like this (taking functions as examples of modules): 
</p>

<pre><code>
  reverse: Array -> Array
</code></pre>

<p>
  The interface of the module is <code>Array -> Array</code>. And that does, in a way, describe what the module does: it inputs an array and outputs an array. But it provides very little information. There are loads of functions that input arrays and output arrays. It describes the input/output types, but it doesn't describe what relationship the output has to the input. 
</p>

<p>
  In this case, the name indicates what it does: it inputs the array and then reverses it. But that's a human readable name. You have to speak English and know what "reverse" means in the context of arrays. And that is not always obvious. Consider the function <code>WebGLRenderingContext.bindFramebuffer()</code> from WebGL. Even if you know the function's interface (its signature), you also need to know what a <code>frameBuffer</code> is and what it means to <code>bind</code> it. 
</p>

<p>
  In short, there's a whole world of relevant information left out of the interface. Ousterhout points this out with his distinction between the formal and informal information of an interface. The formal aspects of an interface are specifiable in code, i.e. the signature. The informal aspects of an interface describe high-level behavior and cannot be specified in code (though perhaps specified with comments).
</p>

<p>
  I think there are probably three kinds of informal knowledge associated with an interface: domain knowledge, problem knowledge, and requirements knowledge. The boundaries between these three groups are not completely clear, but I find the distinction helpful. 
</p>

<p>
  <b>Domain knowledge</b> is knowledge that consists of the domains of discourse you need to be familiar with in order to understand the module's use. It consists of things like concepts, ideas, relationships, jargon, and business applications. If you're writing web service code, then you need to be familiar with HTTP responses and requests, clients, and web servers. If you're writing code that simulates a black hole, then you need to know something about gravity, space, and the math that goes along with it. Domain knowledge is what the code is talking about; it's the context. 
</p>

<p>
  For instance, in order to understand the module:
</p>

<pre><code>
  class User {
    login,
    logout,
    inviteFriend
  }
</code></pre>

<p>
  you need to have a general understanding of the concept of a user and the context in which a user operates. You need to know what logging in and logging out are. And in this particular case, you need to know what "inviting a friend" means.
</p>

<p>
  It's common that several different areas of domain knowledge are required to understand an interface. WebGl, for instance, requires domain knowledge about computer storage (buffers), rendering, and 3D graphics. 
</p>

<p>
  <b>Problem Knowledge</b> is knowledge about the specific problem or problems that the module solves. If domain knowledge is about the context, then problem knowledge concerns the specific problem that the module is trying to solve in that context. The <code>reverse</code> function above solves the problem of generating an array with the opposite sequence of the input. The <code>User</code> module solves problems having to do with accessing the application.
</p>

<p>
  <b>Requirements Knowledge</b> consists of the specific conditions that a module must fulfill in order to consider the problem solved. It isn't enough, for instance, that <code>reverse: Array -> Array</code> inputs and outputs an array, it has to do it in a particular way. The first member of the input, for example, has to be the last member of the output. These are the specific conditions under which the implementation is successful.
</p>

<p>
  Requirements Knowledge is expressed in the form of expected behavior: when this happens, that happens. And it is enforced by unit tests; they codify expected behavior. At bottom, you can think about requirements knowledge as something like a formalization of problem knowledge. 
</p>

<p>
  In summary, the formal interface only provides partial understanding for what a module does. In addition to knowing the interface, the literal type signatures, you need to have domain knowledge, problem knowledge and requirements knowledge. In short, they are the context of the problem, the specific problem you're trying to solve, and the specific conditions of a successful solution. 
</p>
 
