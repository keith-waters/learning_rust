Setting up a new project
- `cargo new guessing_game` 
	- I know what this does!
	- sets up a project folder named `guessing_game`
- `cargo run` builds and runs the executable

Processing a guess
- lets process some user input with `std::io`
- `use std::io` brings the input/output library into scope
- prelude: Rust has a few items in the standard library that it brings into scope of every program (called prelude) it's listed in the standard lib docs
- `fn` declares a new function
- `()` indicates there are no params
Storing values with variables
- `let` statements create variables: `let apple = 5;`
- Variables are immutable by default
- `//` indicates a single line comment
- `mut` makes a variable mutable: `let mut apple = 5;`
- `=` binds something to a variable
- `String::new()` creates a new instance of a string
- `String` type is a growable, UTF8 encoded piece of text
- `::` indicates that `new` is an _associated function_ of `String`
- an associated function is one that's implemented on a type
- `let mut guess = String::new();` creates a mutable variable that is currently bound to a new, empty instance of String

Recieving User Input
- `stdin` module from `io` allows uf to handle user input
- `stdin` is the same as `std::io::Stdin` 
  - it's a type that represents a handle to the standard input for the terminal
- `readline` takes whatever is typed into standard input and appends it to a string
- the `&` in `&mut guess` indicates the argument is a reference

Handling potential failur with the Result Type
- `read_line` will returns an `io::Result`
- Rust has lots of Result types
  - the are all enumerations
  - this one has Ok and Err variant
- `.expect` will handle the Err variant by crashing the program and display the string passed to it
  - if it gets an Ok, it will return the value in Ok

Printing Values with `println!` placeholders
- `println!('hello {}, how do you {}', x, y);` 
  - x is connected to the first {}
  - y is connected to the second {}

Testing the first part
- My code works so far. :D


Generating a secret number
- using the `rand` crate

Using a crate to get more functionality
- crate is a collection of Rust source code files
- the guessing game project is a _binary crate_ or executable
- `rand` is a _library crate_ which is intended to be used in other programs, and can't be executed alone
- crates use semantic versioning
- external dependecies are pulled from the _registry_: a copy of data from Crates.io

Ensuring reproducable builds with the Cargo.lock file
- saves the exact versions of dependencies
- cargo build will use this in the future to figure out dependencies

Updating a crate to get a new version
- `cargo update` will figure out the latest version of the crates that fits into the spec in Cargo.toml, ignoring Cargo.lock

Generating a random number
- `use rand::Rng` brings the `Rng` trait into scope. 
  - it defines methods for us to use
- `rand::thread_rng` function gives us the generator to use
  - one that is on the current thread and seeded by the OS
- `gen_range` takes a range expression `1..101` 
- `cargo doc --open` builds documentation for all crates in the project as a webpage!

Comparing the guess to the secret number




























