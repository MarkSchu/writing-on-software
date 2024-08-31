First, what is a layer? Ousterhout describes layers like this:

  "Software systems are composed in layers, where higher layers use the facilities provided by lower layers." 

This describes layers as modules that invoke the types, methods, and properties of other modules. Consider, for instance, the DOM API as a layer and a UI component called `CreatePostButton`.

```javascript
  function CreatePostButton() {
    const el = document.createElement('button');
    const post = getSomeData();
    
    el.onclick = () => {
      createPost();
    }

    return el;
```

`CreatePostButton ` is a layer above the DOM API. Indeed, you can imagine a whole design system of components created with the DOM API. The design system would be the layer above the DOM API. 

Second, what is an abstraction? Earlier in the book, Ousterhout characterizes an abstraction as, “a simplified view of something.”I think that there are probably multiple, overlapping forms of abstraction. In the case of layers, I think we’re dealing with two. I’m going to call them formal abstraction and conceptual abstraction. And both are forms of composition, where you combine many things to create one thing. The one thing is a simplified view of the many things. 

Formal abstraction is, more or less, combining code - function calls and properties - into a single block that runs as once. For instance, `CreatePostButton` combines references to different functions and properties and hides them behind the name `CreatePostButton `. This is called “Formal” because we don’t actually need to know what the code means. It’s purely mechanical. It’s just composing functional calls. It’s symbolic. We don’t have to understand it. 

The second kind, conceptual abstraction, is the composition of meanings into a larger meaning. For instance, a molecule is a collection of atoms held together by atomic bonds. The concept molecule is a composition of the concepts atom, bond, held together, etc. 

In the case of the principle, “Different Layer, Different Abstraction,” I think we’re dealing with conceptual abstraction. In effect, the principle says that the meaning of a layer should be consistent. It should have a consistent domain of discourse. 

Meaning has to do with responsibility. To me, the responsibility of a layer is, ideally, identical to the meaning of the layer. The domain of discourse of the DOM API contains HTML elements and events in the document. In other words, the responsibility of the DOM API is to manage HTML elements. The responsibility of a design system is to provide basic building blocks for a consistent user interface. It would be strange if either of those modules managed something else. It would see "off topic." 