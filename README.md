
<h1>1.What is scope in JavaScript, and why is it important?</h1>

-Scope in JavaScript refers to the context or environment in which variables are declared and can be accessed.
-It dictates the visibility and lifetime of a variable, determining where in your code a particular variable is valid and accessible.

<h1>2.Can you explain the difference between global scope and local scope?</h1>

Global variables are declared outside all the function blocks while Local Variables are declared within a function block.

Global Scope:

Variables defined outside of any function or code block have global scope.
They can be accessed and modified from anywhere within the program, including inside functions or blocks.
Global variables are typically declared at the beginning of the program or in a shared module that multiple parts of the program can access.

var globalVar = 10;

function foo() {
    console.log(globalVar);  // Accessing globalVar inside function
}

foo();  // Output: 10

 Local Scope:

Variables defined inside a function or a block (like a loop or conditional statement) have local scope.
They can only be accessed and modified.

def my_function():
    local_var = 20
    print(local_var)  # local_var is accessible within my_function

my_function()

<h1>3. How does JavaScript handle scope in functions compared to block-level scope?</h1>

Function-scoped variables (var) are accessible throughout the entire function, including nested blocks.
Block-scoped variables (let and const) are only accessible within the block they are declared in, providing more controlled access and preventing unintended variable reuse or modification.

<h1>4. How do var, let, and const differ in terms of scope?</h1>

VAR- It can be updated and re-declared in the same scope.

    -Variables declared with var are function-scoped or globally scoped.

LET-It can be updated but cannot be re-declared in the same scope.

    let variables are not initialized until their declaration is evaluated during runtime. They are in a "temporal dead zone" until the execution reaches their declaration.

CONST-It can neither be updated or re-declared in any scope.

   constants declared with const are also block-scoped, like let.
They differ in that their value cannot be reassigned after declaration. However, the binding (or reference) it points to is still mutable if it is an object or array.
<h1>5. What are the implications of declaring a variable without any keyword (i.e., no var, let, or const)?</h1>

Declaring a variable without var, let, or const inside a function or a block (like in a loop or an if statement), JavaScript will treat it as a global variable.
Global variables are accessible throughout your entire JavaScript code, which can lead to unintended consequences and potential issues with variable name clashes or unintentional overwriting.

<h1>6.What is the scope chain, and how does JavaScript use it to resolve variable access?</h1>

Scope Chain means that one variable has a scope (it may be global or local/function or block scope) is used by another variable or function having another scope (may be global or local/function or block scope).

-JavaScript engine uses scopes to find out the exact location or accessibility of variables

<h1>7. What are some differences between lexical scope and dynamic scope? Which one does JavaScript use?</h1>

Lexical scope is defined by the placement of functions, blocks, and modules in the code.It is determined at compile time or when the code is parsed.
Variables are resolved based on the location of the variables in the source code (the lexical environment) where they are defined.

Dynamic scope determines variable scope based on the call stack or runtime context.Variables are resolved based on the current flow of execution.
The scope can change dynamically as the program runs, depending on which functions are called.

Javascript uses lexical scoping rules to resolve variable bindings


<h1>8.What is a closure, and how does it relate to scope in JavaScript?</h1>

A closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment).A  closure gives you access to an outer function’s scope from an inner function. In JavaScript, closures are created every time a function is created, at function creation time.

Closure leverages the scope chain in JavaScript. Functions close over the variables they use from their surrounding lexical environment,
