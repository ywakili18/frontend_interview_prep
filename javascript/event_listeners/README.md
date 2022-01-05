# Event listeners

In Javascript, event listeners is a function/procedure that waits for an event to occur.

Another term for understanding Event listners is "Event Propagation" which describes the "stack" of events.

The phases of event propagations are:

1.) Event Capturing
2.) Event Delegations
3.) Event Bubbling

Most commonly, you would have event listeners to "listen" for a click, mouse hover, keyboard enter, etc.

Example:

    const button = document.querySelector('#button')

    (This will select the button you define in your HTML document, adding an Id of 'button' to it)

    button.addEventListener('click', function(e){
      console.log(e.target.value)
    })

    (This will perform an event listener for a click, then performing the function after the click has executed. We can then pass in the 'e' or 'event' parameter to see a list of methods such as target to grab the value and work with that data.)
