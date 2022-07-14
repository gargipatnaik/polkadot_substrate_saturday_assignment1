Binding and mutability

1.
// Fix the error below with least amount of modification to the code
fn main() {
    let x: i32=5; // Uninitialized but used, ERROR !
    let y: i32; // Uninitialized but also unused, only a Warning !

    assert_eq!(x, 5);
    println!("Success!");
}

OUTPUT - Success!

2.

// Fill the blanks in the code to make it compile
fn main() {
    let mut x =  1;
    x += 2; 
    
    assert_eq!(x, 3);
    println!("Success!");
}

OUTPUT - Success!

3.

// Fix the error below with least amount of modification
fn main() {
    let x: i32 = 10;
    {
        let y: i32 = 5;
        println!("The value of x is {} and value of y is {}", x, y);
    }
    println!("The value of x is {}", x); 
}

OUTPUT - The value of x is 10 and value of y is 5
The value of x is 10 

4.
// Fix the error with the use of define_x
fn main() {
    let x = define_x();
    println!("{}, world", x); 
}

fn define_x() -> String {
    let x = "hello".to_string();
    x
}

OUTPUT - hello, world

5. // Only modify `assert_eq!` to make the `println!` work(print `42` in terminal)
fn main() {
    let x: i32 = 5;
    {
        let x = 12;
        assert_eq!(x, 12);
    }

    assert_eq!(x, 5);

    let x =  42;
    println!("{}", x); // Prints "42".
}

OUTPUT - 42 
6. // Remove a line in the code to make it compile
fn main() {
    let mut x: i32 = 1;
    x = 7;
    // Shadowing and re-binding
    let x = x; 
    let y = 4;
    let y = "I can also be bound to text!";


 

    println!("Success!");
}
OUTPUT - SUCCESS

7. 
fn main() {
    let x = 1; 
    println!("{}",x)
}

// Warning: unused variable: `x`
OUTPUT - 1 
8.
// Fix the error below with least amount of modification
fn main() {
    let (mut x, y) = (1, 2);
    x += 2;

    assert_eq!(x, 3);
    assert_eq!(y, 2);

    println!("Success!");
}
OUTPUT - SUCCESS 
9. 
fn main() {
    let (x, y);
    (x,..) = (3, 4);
    [.., y] = [1, 2];
    // Fill the blank to make the code work
    assert_eq!([x,y], [3,2]);

    println!("Success!");
} 
OUTPUT -  SUCCESS











