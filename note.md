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

### bool and char

let booleans: bool = true;
let character: char = 'a';

### unit type

let _unit = ();

like **null** in other languages
if you do not use a varibale, you should name it beginning with an underscore '_'
