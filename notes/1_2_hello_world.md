Creating a project directory
- make a directory to store the code

Writing and Running a Rust Program
- Rust files always use the `.rs` extention
- multiple words in a file name? use underscores to separate them `hello_world.rs` (snakecase)
- `rustc main.rs` compiles `main.rs` and creates an executable

Anatomy of a Rust program
- `fn main() {}` is always the first code that runs in every executable Rust program
- `{}` are required around all function bodies
- parameters go inside `()` in `fn main()`
- `rustfmt` to format rust code
- indent of 4 spaces is Rust style
- `println!` calls a Rust macro
- a `!` at the end means it's a macro, not a function
- most lines end with a semicolon

Compiling and Running are separate steps
- `rustc main.rs` use rustc to compile by passing it the name of the source file
- Rust is ahead of time compiled vs just in time compiled like javascript and ruby
- rustc is good for small projects, but not for big ones
