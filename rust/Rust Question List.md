# Rust Question List



1. `let my_string = String::from("hello world");` vs `let my_string_literal = "hello world";` ?
2. Note that the entire instance must be mutable; Rust doesn’t allow us to mark only certain fields as mutable
    1. 意味着struct里面没有final的字段？
3. 5.3: *automatic referencing and dereferencing*
4. Implementations of a trait on any type that satisfies the trait bounds are called *blanket implementations ？*

[The Rust Programming Language](https://doc.rust-lang.org/book/print.html#using-trait-bounds-to-conditionally-implement-methods)

5. string slices and strings ?

```rust
fn main() {
    let string1 = String::from("long string is long");
    let result;
    {
        let string2 = String::from("xyz");
        result = longest(string1.as_str(), string2.as_str());
    }
    println!("The longest string is {}", result);
}

fn longest<'a>(x: &'a str, y: &'a str) -> &'a str {
    if x.len() > y.len() {
        x
    } else {
        y
    }
}
```

why this is compiled in java

6. println!("{}", var) var为什么是inmutable