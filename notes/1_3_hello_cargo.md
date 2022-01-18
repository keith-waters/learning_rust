Hello, Cargo!
- Cargo is rust's build system and package manager.

Creating a Project with Cargo
- `cargo new hello_cargo` creates a new directory `hello_cargo` with a git repo and Cargo.toml
- TOML: Tom's Obvious, Minimal Language
- Cargo.toml `[package]` section are for configuring a package
- Cargo.toml `[dependencies]` section is the list of project dependencies
- crates are rust's packages of code
- cargo new also creates a src folder with a main.rs inside

Building and Running a cargo project
- `cargo build` creates an executable in `target/debug/hello_cargo`
- `./target/debug/hello_cargo` to run the executable
- `cargo run` combines the above two steps, compile and run the code
- `cargo check` checks the code to make sure it will compile
- cargo check is faster than compiling as it does not create an executable
- cargo commands are the same regardless of OS

Building for release
- `cargo build --release` compiles with optimizations and puts it in `target/release`
- takes longer to compile

Cargo as convention

Summary
