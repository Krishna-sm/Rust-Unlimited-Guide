- Variables are containers that store values. In Rust, variables are a bit different from other programming languages.

1. By default, variables are immutable, which means we cannot change the value or assign a new value to the same variable.

2. Rust is quite smart; it automatically detects the type of a variable.

### Some Concept To impliment variables in `Rust` :- 

1. `let` Keyword
    - `let` keyword is used to declear variable in rust 

syntax: 

```js

let variable_name = value;

```

example:

```js

let user ="Krishna";
let num =23;
let is_admin =true;
let marks =23.5;

```
Note:
 - rust does not follow camel case , it follow snake case , 
   - example:
    ```js
        let userName="Krishna"; // does not follow cancel case

        // alternate
        let user_name = "Krishna";

    ```
#### To Print any variable value in rust we use `println!()` macro.

```rs
    println!("{}",variable);
```

- `{}` this is default place holder.

2. `mut` keyword
    - as we know in rust we can not change variable directly 
    ```js
        let user= "Krishna";

        user = "harish";
        
        user = "Radha";

    ```
    like this we can not do , for doing this we use `mut` keyword

    syntax
     ```js 
    let mut variable = value;
    ```

    example:
    ```js
        let mut user= "Krishna";

        user = "harish";
        
        user = "Radha";

    ```
    
    Note: 
        If I assign a string for the first time, then the next time, I can also assign a string, and not any other data type, to the variable using the `mut` keyword.

3. Shadow Variable

- As you know, we cannot reassign a variable with a different type of value. To address this, the solution is to reuse the same memory after the variable has been used. Once the work is done, we can reuse the variable.
  
- example:
    ```js
        let user = "Krishan";

        let user = 23;

        let user = true;

        let user = 45.9;
    ```

4. Type Annotation
    
- we can define types .     
    
    syntax

    ```js
        let variable:type = value
    ```

    example : 

    ```js
        let user:&str ="Krishna";
        let num:i32 = 34;
        let marks:f32 = 56.9;
        let is_admin:bool = true;

    ```
5. assign mutiple variable in single line

- in rust we can define multiple variables in single line using tuple.

    - syntax
    ```js
        let (var1,var2,var3):(type1,type2,type3) = (val1,val2,val3);

        println!("{}",val1);
        println!("{}",val2);
        println!("{}",val3);

    ```

6. Constant Variables

- Constant variables in Rust are essentially used to define constant data that cannot be changed at any time. 

- we can define constant variables with `const` keyword.
- In Rust constant variable are always follow `UPPERCASE`.
syntax:

```js
        const PI = 3.14;

        const USER = "Krishna";
```