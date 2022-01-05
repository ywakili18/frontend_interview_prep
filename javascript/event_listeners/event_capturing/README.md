# What is event capturing?

(see event bubbling first)
Capturing is the opposite of bubbling, where it goes from the document to the child.

In an event listener, you can add a third parameter called {capture} will "capture" the event. When this is done, it will log from the Document, to parent, to child.

So, event bubbling goes from Child to parent to document

And event capturing goes from document to parent to child!
