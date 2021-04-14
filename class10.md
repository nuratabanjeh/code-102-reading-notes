# class10

# Error Handling and Debugging

## Order of execution :

Order of execution in JavaScript is dependent on the following components working together to pass and order information.

* The Callstack.

* The Event Loop.

* The Task Queue.

* WebAPIs/External Resources.

We can think through the order of execution using the (sometimes headache inducing) example of the asynchronous fetch request.

A very simple fetch request might look something like this :

`fetch(url)
.then(res => res.json())
.then(json => {      
this.setFetchResults(json.items)    
}`

You fetch some data, you parse to json, and then you pass that json into another function and do something with it. Fairly straightforward. Now, if this fetch request happens as part of a larger function, at the beginning of that function, JavaScript will essentially put it to the side, and wait for the response (let’s say in this case from an external API), and continue moving down the function. Eventually, hopefully, there is either a response from the external API (whether an error, or the data we’re expecting) or a set timeout. Then, this information is passed to the task queue. As the call stack is cleared, the Event Loop passes information from the task queue back to the call stack to finish executing the function.

## JavaScript Function Scope

In JavaScript there are two types of scope:

* Local scope

* Global scope

 JavaScript has function scope: Each function creates a new scope.Scope determines the accessibility (visibility) of these variables.Variables defined inside a function are not accessible (visible) from outside the function.

 ## Errors :

Runtime errors result in new Error objects being created and thrown.

### Error types :

Besides the generic Error constructor, there are seven other core error constructors in JavaScript. For client-side exceptions, see Exception handling statements.

1. EvalError : Creates an instance representing an error that occurs regarding the global function eval().

2. InternalError : Creates an instance representing an error that occurs when an internal error in the JavaScript engine is thrown. E.g. "too much recursion".

3. RangeError : Creates an instance representing an error that occurs when a numeric variable or parameter is outside of its valid range.

4. ReferenceError : Creates an instance representing an error that occurs when de-referencing an invalid reference.

5. SyntaxError : Creates an instance representing a syntax error.

6. TypeError : Creates an instance representing an error that occurs when a variable or parameter is not of a valid type.

7. URIError : Creates an instance representing an error that occurs when encodeURI() or decodeURI() are passed invalid parameters.

## JavaScript Debugging :

Code Debugging :

Programming code might contain syntax errors, or logical errors.

Many of these errors are difficult to diagnose.

Often, when programming code contains errors, nothing will happen. There are no error messages, and you will get no indications where to search for errors.

Searching for (and fixing) errors in programming code is called code debugging.

## JavaScript Debuggers :

Debugging is not easy. But fortunately, all modern browsers have a built-in JavaScript debugger.

Built-in debuggers can be turned on and off, forcing errors to be reported to the user.

With a debugger, you can also set breakpoints (places where code execution can be stopped), and examine variables while the code is executing.

Normally, otherwise follow the steps at the bottom of this page, you activate debugging in your browser with the F12 key, and select "Console" in the debugger menu.

## The console.log() Method :

If your browser supports debugging, you can use console.log() to display JavaScript values in the debugger window:

Example :

`<!DOCTYPE html>`

`<html>`

`<body>`



`<h1>My First Web Page</h1>`

`<script>`
a = 5;

b = 6;

c = a + b;

console.log(c);

`</script>`

`</body>`

`</html>`

## Major Browsers' Debugging Tools :

Normally, you activate debugging in your browser with F12, and select "Console" in the debugger menu.

Otherwise follow these steps:

- Chrome :

Open the browser.

From the menu, select "More tools".

From tools, choose "Developer tools".

Finally, select Console.

- Safari

Go to Safari, Preferences, Advanced in the main menu.

Check "Enable Show Develop menu in menu bar".

When the new option "Develop" appears in the menu:

Choose "Show Error Console".

**Thankyou**