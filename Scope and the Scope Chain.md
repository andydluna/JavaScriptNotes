**Scope Concepts**
- **Scoping**: How our program's  variables are **organized** and **accessed**. *"Where do variables live?"* or *"Where can we access a certain variable, and where not?"*
- **Lexical scoping:** Scoping is controlled by **placement** of functions and blocks in the code
- **Scope:** Space or environment in which a certain variable is **declared** (*variable environment in case of functions*). There is **global** scope, **function** scope, and **block** scope
- **Scope of a variable:** Region of our code where a certain variable can be **accessed**.

**The Three Types of Scope**
- **Global Scope:** 
	- Outside of **any** function or block
	- Variables declared in global scope are accessible **everywhere**
- **Function Scope:** 
	- Variables are accessible only **inside function, NOT** outside
	- Also called local scope
- **Block Scope (ES6):**
	- Variables are accessible only **inside block** (block scoped)
	- **HOWEVER,** this only applies to `let` and `const` variables!
	- Functions are **also block scoped** *(only in strict mode)*

**The Scope Chain**
Variables do not get copied from one scope to another, instead they use the **Scope Chain** to access variables in the scope.

![[Scope Chain Example.png]]

In the upper example, we can see how the scope chain works. In the case of the `if` block scope and the `second()` scope, they do not share variables as their lexical scope is separated since they are in different blocks.

**Scope Chain vs. Call Stack**
![[Scope Chain vs. Call Stack Example.png]]

Even though the `third()` function was called in once all the variables were declared, since the function was declared outside the scope of the variables, it will give an error as the variables cannot be accessed.

**Summary! 🙉**

- Scoping asks the questions *"Where do variables live?"* or *"Where can we access a certain variable, and where not?"*
- There are three types of scope in JavaScript: the global scope, scopes defined by function, and scopes defined by blocks
- Only `let` and `const` variables are block-scoped. Variables declared with `var` end up in the closest function scope
- In JavaScript, we have lexical scoping, so the rules of where we can access variables are based on exactly were in the code functions and blocks are written
- Every scope always has access to all the variables from all its outer scopes. This is the scope chain!
- When a variable is not in the current scope, the engine looks up in the scope chain until it finds the variable it's looking for. This is called variable lookup
- The scope chain is a one-way street: a scope will never, ever have access to the variables of an inner scope
- The scope chain in a certain scope is equal to adding together all the variable environments of all the parent scopes
- The scope chain has nothing to do with the order in which functions were called. It does not affect the scope chain at all!