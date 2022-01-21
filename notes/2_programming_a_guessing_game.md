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



