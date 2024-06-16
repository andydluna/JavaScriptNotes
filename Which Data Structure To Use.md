**Data Structures Overview**
- Sources of Data:
	1. **From the program itself:** Data written directly in source code (e.g. status messages)
	2. **From the UI:** Data input from the user or data written in DOM (e.g. tasks in todo app)
	3. **From external sources:** Data fetched for example from web API (e.g. recipe objects)
- 👇 Collection of data
- 👇 Data Structure
	- Simple List?
		- Arrays or Sets
	- Key/Value Pairs? (keys allow to describe values)
		- Objects or Maps (JSON files)


| **OTHER BUILT-IN** | **NON-BUILT IN** |
| ------------------ | ---------------- |
| 👉 WeakMap         | 👉 Stacks        |
| 👉 WeakSet         | 👉 Queues        |
|                    | 👉 Linked lists  |
|                    | 👉 Trees         |
|                    | 👉 Hash tables   |

**Arrays vs. Sets and Objects vs. Maps**


| **ARRAYS**                                                              | **SETS**                                            |
| ----------------------------------------------------------------------- | --------------------------------------------------- |
| Use when you need **ordered** list of values (might contain duplicates) | Use when you need to work with **unique** values    |
| Use when you need to **manipulate** data                                | Use when **high-performance** is *really* important |
|                                                                         | Use to **remove duplicates** from arrays            |


| **OBJECTS**                                                                       | **MAPS**                                        |
| --------------------------------------------------------------------------------- | ----------------------------------------------- |
| More "traditional" key/value store ("abused" objects)                             | Better performance                              |
| Easier to write and access values with . and []                                   | Keys can have **any** data type                 |
|                                                                                   | Easy to iterate                                 |
|                                                                                   | Easy to compute size                            |
| Use when you need to include **functions** (methods) that need the `this` keyword | Use when you simply need to map key to values   |
| Use when working with JSON (can convert to map)                                   | Use when you need keys that are **not** strings |
