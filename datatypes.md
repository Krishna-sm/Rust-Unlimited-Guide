- Data types are common in all programming languages; they are used to inform variables about the type of value they hold.

# Primitive Datatype   
  
Primitive data types are core data types that are predefined by Rust.

types:
 1. ## integer
    - Integers are decimal numbers, and in Rust, integers are represented by `i32`, `i64`, and `i128`.

    - syntax to use integer
    ```js
        let num:i32 = 12;
        let num:i64 = 12;
        let num:i128 = 12;
    ```

    - let understand differce between `i32` `i64` `i128`.
     
      The `i` represents an integer, and `32, 64, and 128` denote the number of bits each integer type uses to store numerical values. Each of these types has its own limit for storing numbers.

      - `i32` it store number between - `-2147483648..=2147483647`.
    
      - `i64` it store number between - `9223372036854775808..=9223372036854775807`.
  
       - `i128` it store very large number like `23345678345678945678345678934567823456`. it unable to store `233456783456789456783456789345678234562345623451234523452345`.
 
 2. ## string
   - A string is a collection of characters.
    In Rust we can create string by two methods

        - String Datatype           
        ```js
            let user =  String::from("Krishna");
            let user:String =  String::from("Krishna");
        ```
        In the first example, String::from("Krishna") creates a String object, allocating memory on the heap to store the string "Krishna". This allows for dynamic resizing and modification of the string.

        - using simple way
        
        ```js
                let user = "Krishna";
                let user:&str = "Krishna";
        ```
        The type of user is inferred to be a string slice (&str). String literals in Rust have the type &str, representing a reference to a slice of a string stored in the program's binary. String slices are immutable views into a string and do not allow modifications.


 3. ## boolean
    boolean values are also represent either `true` or `false`;

    ```js
            let is_admin = true;
            let is_admin:bool = true;
            let is_user:bool = false;
            let is_user = false;
    ```

 4. ## float
Float values in Rust represent decimal point numbers, such as 1.2 or 15.9. Similar to integer data types in Rust where we use i32 for integers, for floats, we use f32 for smaller precision and f64 for higher precision. However, Rust does not support f128.

example:
```js
    let marks:f32 =45.6;
    let marks:f64=458.6;
```

It's important to note that when dealing with float values, there can be precision limitations. In situations where the decimal portion exceeds the limit, Rust automatically replaces the numbers beyond the limit with zero, helping to eliminate long decimal numbers.




# NON - Primitive Datatypes

- these are user define datatype , which based on primitive types.

## Array
- array

    array is are used to store similar type of data.
    example:
    1. names of array which contain strings.  
    2. marks of array which contain numbers.
    3. users array which contain users information. 

to create array in rust we use `[]` square brackets. 

```js
    let arr = ["krishna","harish","Radha"];

```

- Note: 
   array allow single type of data, i you provide 1 element in string so it must to all elements are string.

example:
```js
    let arr = ["krishna",23,45.4];
    // invalid array
``` 

for doing this instead of using array you can tuples. 


-  Define type of an array
```js
    let array_name:[type;size] = [element1,element2];
    // type = datatype,size = no of elements
``` 

example:
```js
let names:[&str;3] = ["krishna","harish","sita"];
```

if you mention size of array so it is compulsary the numbers element are euqal than size;

example:
```js
let names:[&str;2] = ["krishna","harish","sita"];
// invalid array throw an error
```


#### access array values
example:
```js
let names:[&str;3] = ["krishna","harish","sita"];
println!("{:?}",names);
```
   - `"{}"` - default formatter; 

   - `"{:?}"` - debug formatter;

- ### indexing

```js
let names:[&str;3] = ["krishna","harish","sita"];
println!("{:?}",names[0]);
println!("{:?}",names[1]);
println!("{:?}",names[2]);
```


```js
let names:[&str;3] = ["krishna","harish","sita"];
println!("{:?}",names[0]);
println!("{:?}",names[1]);
println!("{:?}",names[2]);
println!("{:?}",names[3]); //Err: index out of bound
```

# tuples
- in rust tuple are used to hold different type values.


syntax:
```js

let tuple_name= (val1,val2,val3);
// with types
let tuple_name:(type1,type2,type3) = (val1,val2,val3);

```
example:

```js
    let tuple_name = (10,true,59.8,"krishna");
       
    let tuple_name:(i32,bool,f32,&str) = (10,true,59.8,"krishna");

```

#### access tuple values
example:
```js
  let tuple_name:(i32,bool,f32,&str) = (10,true,59.8,"krishna");
println!("{:?}",tuple_name);
```
   - `"{}"` - default formatter; 

   - `"{:?}"` - debug formatter;

- ### indexing

```js
 let tuple_name:(i32,bool,f32,&str) = (10,true,59.8,"krishna");
println!("{:?}",tuple_name.0);
println!("{:?}",tuple_name.1);
println!("{:?}",tuple_name.2);
println!("{:?}",tuple_name.3);
```


```js
 let tuple_name:(i32,bool,f32,&str) = (10,true,59.8,"krishna");
println!("{:?}",tuple_name.0);
println!("{:?}",tuple_name.1);
println!("{:?}",tuple_name.2);
println!("{:?}",tuple_name.4);
println!("{:?}",tuple_name.3); //Err: Element not found
```


# struct
In Rust, a struct is a data structure that allows you to group related data together. 

```rs
    struct User{
        name:String,
        age:i32
    }

let user_1:User= User{
    name:String.from("Krishna"),
    age:23
}
let user_2:User= User{
    name:"harish".to_string(),
    age:56
}



```

### access items values

```rs
        println!("{:?}",user_1.name);
        println!("{:?}",user_1.age);
        println!("{:?}",user_2.name);
        println!("{:?}",user_2.age);
```




# enum

In Rust, an enum is a data type that represents a value which can be one of several possible variants.

```rs
enum Direction {
    Up,
    Down,
    Left,
    Right,
}

let my_direction = Direction::Up;
match my_direction {
    Direction::Up => println!("Moving up!"),
    _ => println!("Not moving up."),
}

```

# pointers

In programming, a pointer is a variable that stores the memory address of another variable.

```rs


let num =2; // Declare a variable
let refer:&i32 = &num; // Declare a pointer and assign the address of my_variable
  print!("num reference {:p}",refer );// Access the value at the memory address stored in the pointer
```