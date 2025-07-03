## Basic Rust

### compile and run

compile: rustc filename.rs
run: ./filename

#### cargo

cargo new project-name: create a new project
cargo build: build your cargo project by producing an executable
cargo run: build and run, storing the build result in ./target/debug/
cargo check: check if your project has any compile error without creating an executable
cargo build --release: compile with optimizations for final release, storing in ./target/release/

### print

println!("Hello World");

println!("Hello {}", "Jha");

println!("Hey {0}, is this your sister, {1} {0}?", "Jha", "Lily");

println!("This is {}", 2025);

println!("Hexa {:X}", 2025); // hexadecimal

println!("Octa {:o}", 2025); // octadecimal

println!("Binary {:b}", 2025); // binary

println!("{num}", num = 2025);

println!("{num:>5}", num = 1); // 4 spaces before 1, 1 is shifted to right by 4 digits

println!("{num:0>5}", num = 1); // 00001

println!("{num:0<5}", num = 1); // 10000

println! calls a Rust macro instead of a function.

when printing variables, put variable name in {};
when printing the result of evaluating an experssion, put {} in the format string, and follow the format string with a comma-separated list of expressions.

### let

let a = "abc";
println!("Hexa for pointer {:p}", &a);

### numbers

#### integer

signed
- i8: [-128, 127]
let num: i8 = -1;

unsigned
let num: u8 = 1;

default is i32 and u32

#### float

float
let num: f32 = 1.324567

default is f64

if you wanna change its value afterwards, add "mut":
let mut num = 1.234324569798023576;
println!("{}", num);

you can mutate every variable declared with **let**

#### random number

how to get a random number in [1, 100]:

use rand::Rng;

let random_number = rand::thread_rng().gen_range(1..=100);

gen_range() function takes a range expression (start..=end) as argument and returns a random number in this range.

run "cargo doc --open" to build a documentation provided by all the specified dependencies in Cargo.toml locally and open in the browser.

### bool and char

let booleans: bool = true;
let character: char = 'a';

### unit type

let _unit = ();

like **null** in other languages
if you do not use a varibale, you should name it beginning with an underscore '_'

### receive user input

use std::io; // io is a **prelude** in the standard library

io::stdin()
    .read_line(&mut varname)
    .expect();

call functions from io module
- stdin() has the return type std::io::Stdin, representing a handle to the standard input to the terminal.
- read_line() takes whatever user types into standard input and append that to a string (passed as an argument), returns a Result value of type enumeration (Ok and Err, encoding error-handling information).
- expect() is an error-handling function defined on Result values:
  - Result == Err, crash the program and display the message that passed as an argument to expect().
  - Result == Ok, take the return value held by Ok and just return it.

### loop

switch-case:
match a.cmp(&b) {
    pattern1 => conduct1,
    pattern2 => conduct2,
    pattern3 => conduct3,
}
each line in match {} is an arm.

infinite loop:
loop {
    /* code snippet to conduct */
}


