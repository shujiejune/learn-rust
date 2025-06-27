## Basic Rust

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
