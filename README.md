# Undefined Behavior Example in Rust
This repository demonstrates a common source of undefined behavior in Rust: modifying a vector through a raw pointer after potential capacity changes.  The code modifies the vector's first element using a raw pointer obtained via `as_mut_ptr()`. However, this approach is unsafe and can lead to unexpected behavior if the vector's internal memory is reallocated or otherwise altered.

## How to Reproduce
Clone this repository and run `cargo run`.

## Solution
The solution avoids raw pointers and instead uses safe Rust methods to modify the vector.