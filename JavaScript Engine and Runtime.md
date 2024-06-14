
**JS Engine** is the program that *executes* JavaScript code. Like V8 Engine.

Every engine contains both:
- Call Stack: Where our code is executed [[Execution Contexts and the Call Stack]]
- Heap: Where objects are stored

**Compilation vs. Interpretation**
- Compilation: The entire code is converted into machine code at once, and written to binary file that can be executed by a computer
	- Source code -> Compilation -> Portable file: machine code -> Execution *(can happen way after compilation)* -> Program running
- Interpretation: Interpret runs through the source code and executes it line by line. **Much Slower** than compiled languages  
	- Source code -> Execution line by line *(Code still need to be converted to machine code)* -> Program running
- Just-in-Time (JIT) compilation: Entire code is converted into machine code at once, then executed immediately. *(what modern JavaScript uses)*
	- Source code -> Compilation -> Machine code (**NOT** a portable file) -> Execution (**Immediately** after)-> Program running

**Modern Just-In-Time Compilation of JavaScript**
- Parsing
	- Converts code into a Abstract Syntax Tree (AST)
- Compilation
	-  Just-In-Time compilation utilizing the AST
- Execution
	- Executes the compiled code. Happens in the Call Stack
- Optimization
	- The code first executes in a unoptimized machine code just to get the program running. Then, it optimizes and repeats the process of compilation which keeps happening as the code is running!

All of these happen in a special thread that we can't access from code!

**JavaScript Runtime**
Runtime in the browser:
- JS Engine
	- Heap
	- Call Stack
- WEB APIs (Functionalities provided to the engine, accessible on *window* object)
	- DOM
	- Timers
	- Fetch API
	- ...
- Callback Queue (**Event Loop** takes functions from here to place them in the **Call Stack**!)
	- onClick
	- timer
	- data
	- ...

Runtime in Node.js:
- Basically the same as in the browser, with the difference that **WEB APIs** are replaced with **C++ Bindings** and a **Thread Pool**.