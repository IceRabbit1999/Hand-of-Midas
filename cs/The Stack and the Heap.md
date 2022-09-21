# The Stack and the Heap

Created: August 11, 2022 8:52 PM
Last Edited Time: August 11, 2022 9:18 PM
Status: In Progress 🙌
Type: cs

# A brief explanation from *The Rust Programming Language*

1. Both the stack and the heap are parts of memory available to your code to use at runtime
2. stack: 
    1. last in, first out
    2. all data stored on the stack must have a known, fixed size
3. heap:
    1. allocating: The memory allocator finds an empty spot in the heap that is big enough, marks it as being in use, and returns a *pointer*, which is the **address of that location**
    2. the pointer to the heap is a known, fixed size, you can store the pointer on the stack
4. pushing to the stack is faster than allocating on the heap because the allocator never has to search for a place to store new data (that location is always at the top of the stack)
5. accessing data in the heap is slower than accessing data on the stack because you have to follow a pointer to get there
6. when your code calls a function
    1. the values passed into the function and the function’s local variables get pushed onto the stack
    2. when the function is over, those values get popped off the stack