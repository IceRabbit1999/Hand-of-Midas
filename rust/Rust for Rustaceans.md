# Foundations

## Talking About Memory

### Memory Regions

#### The Stack

1. The *stack* is a segment of memory  that your program uses as scratch space for function calls
2. Each time a function is called, a contiguous chunk of memory called a *frame* is allocated at the top of the stack
3. Frame contains all the variables within that function, along with any arguments the function takes
4. When function returns, its stack frame is reclaimed

#### The Heap

1. The *heap* is a pool of memory that isn't tied to the current call stack of the program
2. Values in heap memory live until they are explicitly deallocated 
3. The heap allows you to explicitly allocate contiguous segments of memory
   1. you get a pointer to the start of that segment of memory
   2. That memory segment is reserved for you until you later deallocated it(*freeing*)

## Ownership

1. Rust's memory model centers on the idea that all values have a single *owner*

## Borrowing and Lifetimes

1. Rust allows the owner of a value to lend out that value to others, without giving up ownership, through references
2. *References* are pointers that come with an additional contract for how they can be used

### Shared References

&T

1. each shared reference is **Copy**

### Mutable References

1. The primary difference between owning a value and having a mutable reference to it is that the owner is responsible for dropping the value when it is no longer necessary
2. If you move the value behind the mutable reference, then you must leave another value in its place 

2. try explain this

```rust
fn main() {
    let mut x = Box::new(2);
    let s = &mut x;
    let test = *s; // cannot move out of `*s` which is behind a mutable reference
}
```

### Interior Mutability

