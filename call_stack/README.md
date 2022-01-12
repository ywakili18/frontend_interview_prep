# What is call stack?

Call stack is a "mechanism" behind the scenes. The JS interpreter keeps tracking of multiple functions running, essentially keeping track of where it is during execution. 

A "stack" is a basic data structure (commonly known within data structures and algorithms)

## So how does it work then?

When a script calls a function, the interpreters adds it to the call stack, and then starts carrying out the function.

Any functions that are called by that function are added to the call stack further up and run where their calls are reached.

When the current function has successfully executed, the JS interpreter takes it off the stack and resumes execution where it left off. 

Let's take a look at the following example: 

        function add(a, b) {
            return a + b;
        }

        function average(a, b) {
            return add(a, b) / 2;
        }

        let x = average(10, 20);

When the script runs, the JavaScript engine places the global execution context (typically main() or global())

The average() will be added to call stack, then add() will be added on TOP of the average().

After the add() executes and returns that value, it will be removed from the top of the call stack. The average() will finish executing its function with the value being passed in from the add(), and then it will be removed from the call stack. 

The call stack is now empty, so the JS engine will stop executing.

Visual example:

<img src="https://www.javascripttutorial.net/wp-content/uploads/2019/12/JavaScript-Call-Stack.png">
