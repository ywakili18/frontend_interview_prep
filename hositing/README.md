# What is hositing?

Hoisting is the concept of how JavaScript calls a function or variable based on where it is being called. 

Example:

        1.)
        console.log(dog)
        var dog = "Rover"
        <!-- This will return undefined. -->

        2.)
        var dog = "Rover"
        console.log(dog)
        <!-- This will return "Rover" -->

        3.)
        console.log(dog)
        <!-- With no value being declared, this will return NOT DEFINED. (not undefined! big difference.) -->

What's going on above? 

At number 1, we are not getting an error? Javascript is "aware" of the variable dog. It creates the variable dog BEFORE intizalizing the value of "dog" or the console.log(dog) 
(This is done in memory)


How would this work in a function?

        var num1 = 1;
        var num2 = 2;

        function checkNum(){
            if(!num1){
                var num1 = num2;
            }
            return num1
        }
        console.log('Your number is: ', checkNum())


In that console.log, ideally it should not run since a number is not being passed in to the function or is called within its local scope. However, if you run it as is: it does work and performs that function!

Why is that? This is due to the "var" keyword. Var has a global scope meaning it can be called **anywhere in the javascript file**. This is bad practice hence the reason why ES6 introduced the "let" and "const" keywords. (use that instead to fix the issue!)
