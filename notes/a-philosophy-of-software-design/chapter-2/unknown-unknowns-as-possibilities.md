<p>
  Ousterhout thinks that <b>unknown unknowns</b> are one of the three symptoms of complex software systems. There are different ways to characterize unknown unknowns; one way is in terms of <i>what's possible</i>. 
</p>

<p>
  When you design a system, you have to think about what's possible and what's not possible. This often comes in the form of thinking about cases you need to account for. For example, suppose you design a function that makes api requests and receives HTTP responses. In accounting for the response, you have to consider the different HTTP response codes: 200, 404, 500, etc. These are possibilities. And the function needs to know what to do in the case of each one.  
</p>

<p>
  You can think about an <b>unknown</b> as a known possibility. You don't know if it's going to happen, but you know it <i>might</i> happen. You know the possible cases, the possible options. 
</p>

<p>
  On the other hand, an <b>unknown unknown</b> is an unknown possibility. You don't know if it's going to happen and you don't know that it <i>might</i> happen. For instance, suppose you don't know that there are HTTP response codes between <code>100</code> and <code>199</code>. You thought it was <code>200</code> and up. In this case, you don't know what's going to happen and you also don't fully understand what <i>might</i> happen. 
</p>