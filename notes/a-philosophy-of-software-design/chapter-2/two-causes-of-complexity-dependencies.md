<p>
  There are three symptoms of complexity: change amplification, cognitive load, and unknown unknowns. What are the causes? Ousterhout gives two: <b>dependencies</b> and <b>obscurity</b>. This post explains dependencies.
</p>

<p>
  <b>Dependencies</b> exist, "when a given piece of code cannot be understood or modified in isolation; the code relates in some way to other code, and the other code must be considered and/or modified if the given code is changed." 
</p>

<p>
  Here's a way to think about this. 
</p>

<p>
  First, dependencies come in pairs. The system has two parts and one part is dependent on the other. Second, Ousterhout points to two kinds of dependencies in his definition, ones that have to do with understanding and ones that have to do with modification. 
</p>

<p>
  Dependencies of understanding exist when in order to understand one part of a system you have to understand another part of the system. Understanding the first part depends on understanding the second part. A common example of this is when you dig down into a module's implementation. You understand what a module does by looking at its API. You understand how it does it by looking at its implementation. And within its implementation, you find all kinds of references to other modules. In these cases, you understand the module because you understand the other modules that it references. 
</p>

<p>
  For example, suppose you see <code>customer.create(data)</code>. It's pretty clear that this is a module that create's customers. But you might need to understand how it does this, so you dig into the code and see 
</p>

<pre><code>
    create(data) {
      api.post('/api/user', data)
    }
</code></pre>

<p>
  Now you understand the <code>customer</code> module in terms of the <code>api</code> module.
</p>

<p>
  Dependencies of modification exist when changes to one module risk breaking another module. You can understand that situation like this. There are two parts of a system and one part consumes the api of the other part. The first is the consumer. The second is the provider. The consumer is dependent on the provider in so far as changes or failures in the provider may cause changes or failures in the consumer. The consumer references the provider with a set of expectations (the API of the provider) and depends upon those expectations being fulfilled. 
</p>

<p>
  For instance, in the above example, the <code>customer</code> module depends on the <code>api</code> module with respect to its modifications. If <code>post</code> is removed or changed, then that will break the <code>customer</code> module.
</p>

<p>
  Dependencies lead to increased change amplification and higher cogntive load. On the one hand, if 10 modules consume a provider module, and therefore depend upon it, then changes in the provider module may require changes in the 10 consuming modules; i.e more change amplification. On the other hand, if a module uses 10 other modules in its implementation, then that increases the cognitive load of understanding how that module works. 
</p>