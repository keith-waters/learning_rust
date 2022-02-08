Variables and Mutability
- variables are immutable by default
- immutable: you cannot change the value after it's set
- Experienced Rustaceans still get compiler errors
- compiler guarantees that variables will not change unless you say they can with `mut`

Constants
- constants are always immutable, you cannot use `mut`
- `const` instead of `let` like javascript
- constants can be declared in any scope, including the global scope
- compiler can evaluate a limited set of operations at compile time
	- so `const THREE_HOURS_IN_SECONDS: u32 = 60 * 60 * 3;` is evaluated at compile time, not at runtime

Shadowing
- you can declare another variable with the same name as one above it
- must use the `let` keyword
- this is effectively creating a new variable
- can change variable types when shadowing
