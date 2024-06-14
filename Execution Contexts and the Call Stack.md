**What is an Execution Context?** 

Environment in which a piece of JavaScript is executed. Stores all the necessary information for some code to be executed. 

![[Execution Context Example.png]]

- Exactly **one** global execution context (EC): Default context, created from code that is not inside any function (top-level).
- One execution context **per function**: For each function call, a new execution context is created (All together make the call stack)

- Compilation ->
	- Execution
		- Creation of **global execution context** (for top-level code) *Not inside a function* ->
		- Execution of **top-level code** (inside global EC) ->
		- Execution of **functions** and waiting for **callbacks**  *Example: click even callback*

**What's Inside Execution Context?**
1. Variable Environment [[Hoisting In JavaScript]]
	1. `let`,`const`,and `var` declarations
	2. Functions
	3. `arguments` objects ~
2. Scope chain [[Scope and the Scope Chain]]
3. `this` keyword ~
Generated during "creation phase", right before execution.
~ NOT in arrow functions!

![[Inside Execution Context Example.png]]

**The Call Stack**
- "Place" where execution contexts get stacked on top of each other, to keep track of where we are in the execution.
- Combined with the heap, makes up the JavaScript Engines.
- As compiled code gets executed, they will be added to the call stack, and will get popped following a stack behavior **(FIFO)** until the stack is empty.



