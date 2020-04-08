## What is call stack in node JS?
- The **call stack**, event *loop* and *callback* queue, its a mechanism in Javascript used to *keep track* of where it is in a program, it knows which functions are currently being run and which to call next, the catch with the **call stack** is that you *can only add things to the top of the stack*.
## How does call stack work?
-  Since the call stack is **organized** as a stack, the caller pushes the *return address* onto the stack, and the **called subroutine**, when it finishes, *pulls or pops* the return address off **the call stack** and transfers control to that address.
## How stack is used in function call?
- Each computer program that runs uses a **region of memory** called the stack to enable *functions* to work properly, machine uses the stack to pass function *arguments*, to store return information, to save registers for later restoration, and for *local variables*.
## What causes a stack overflow?
- The most-common cause of **stack overflow** is excessively deep or **infinite recursion**, in which a function calls itself so many times that the space needed to store the *variables* and *information* associated with each call is more than can fit on the stack.
## Types of error messages
1. ***Reference errors:***  
    - When we try to use a variable that is not yet declared you get this type os errors:   
    - **THE ERROR**


            1.console.log(foo) // Uncaught ReferenceError: foo is not defined


            2.foo = 'Hello' // Uncaught ReferenceError: foo is not defined
            let foo
    - **THE FIX OF ERROR**

        let foo;
        foo = 'Hello'
2. ***Syntax errors:***
- is occurs when you have something that cannot be parsed in terms of syntax, like when we try to parse an invalid object using JSON.parse.
    - **THE ERROR**

            JSON.parse( {'foo': 'bar'} ) // Uncaught SyntaxError: Unexpected token o in JSON at position 1
    - **THE FIX OF ERROR**


            JSON.parse('{"foo":"bar"}')

## Debugging
- If we encounter a general issue with any of the Toolset plugins, there are two main types of debugging you can use to debug the issue: **PHP Debugging** and **JavaScript debugging**. These two types of debugging provide you with some very *technical information*.
### Tools to avoid runtime errors
- **quokka** to evaluate your code as you type. 
- **eslint** to make sure your style guide is consistency and it will grab you an error or two along the way and




