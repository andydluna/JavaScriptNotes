**Hoisting:** Makes some types of variables accessible/usable in the code before they are actually declared. "Variables lifted to the top of their scope".

**BEHIND THE SCENES**

**Before execution,** code is scanned for variable declarations, and for each variable, a new property is created in the **variable environment object**.

|                                   | Hoisted?                              | Initial Value                               | Scope                                 |
| --------------------------------- | ------------------------------------- | ------------------------------------------- | ------------------------------------- |
| `function` declarations           | YES                                   | Actual function                             | Block *(strict mode)* else: function! |
| `var` variables                   | YES                                   | `undefined`                                 | Function                              |
| `let` and `const` variables       | NO (well, yes, but not in practice)   | `<uninitialized>`, TDZ (Temporal Dead Zone) | Block                                 |
| `function` expressions and arrows | Depends if using `var` or `let/const` | <                                           | <                                     |
![[Hoisting Example.png]]