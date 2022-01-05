# What is event bubbling?

#####

As an example, let's say we have a HTML document with three divs in it.

    <div id="grandparent">
      <div id="parent">
        <div id="child"></div>
      </div>
    </div>

In your js file select each div

    const grandparent = document.querySelector(".grandparent")

    const parent = document.querySelector(".parent")

    const child = document.querySelector(".child")

And add event listeners for each parent and child, console.log the specified family name.

What do you notice if you click on the child element? It will log not _only_ the logged value of the child, but also the _parent and grandparent_. This is event bubbling. This goes as far as the document itself.
