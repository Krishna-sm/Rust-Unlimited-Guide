
Control flow statements in programming, such as `if`, `else if`, and `else`, dictate the order of execution. They enable decision-making based on conditions, repetition of tasks, and modification of program flow. These statements offer flexibility for handling diverse scenarios and designing efficient code.


**Note**
- Control flow statements operate based on boolean values (`true` or `false`) and do not directly work with numbers or strings, aligning with common practices in programming languages.



### if statement

- The if statement executes when a condition is `true`. For example, if a user is an admin, I want to grant dashboard access; otherwise, not.
  
`example`:

```rs
        let user:&str= "admin";

        if user == "admin"{
                println!("grant access");
        }

        let user:&str = "user";
         if user == "user"{
                println!("access denied!");
        }

```

### if else statement

- If the condition is `false`, the else block is executed; if `true`, the if block is executed.


`example`:

```rs
        let user:&str= "admin";

        if user == "admin"{
                println!("grant access");
        }else{
             println!("access denied!");
        }


```



### if elseif else statement

- When dealing with multiple conditions, we use the if-else if statement to check each condition sequentially.It also known as else if ladder in other programming languages.


`example`:

```rs
       
       let age = 18;

       if age<18{
        println!("you are not eligible ,please wait {} year",18-age);
       }else if age==18{
        println!("you are not eligible ,please wait 1 year");
else{
    println!("you are eligible for voting");
}
       }

```


### Ternary Operator

- It is also known as a shorthand for the if-else statement; basically, it condenses multiple conditions. However, this shorthand is not present in Rust.

- we use if else in just single line to achive same functionality of ternary operator.


```rs

let user = "admin";

let result = if user =="admin" {"access granted"} else {"access denied"};

println!("result {}",result);

```

### Match Case Statement

- `match` statements in Rust are similar to switch statements in other languages, but the syntax is different. They operate on a single value and allow checking against multiple cases, providing a more flexible and expressive approach.

```rs


const day = "Monday";

match day{
    "Monday" => println!("today is monday"),
    "Tuesday" => println!("today is Tuesday"),
    - =>  println!("Invalid Day")
}

```

`_` : default case , it any conditon not match , it is similar as else statement.


**Imporant**
- In other programming languages, using condtional operators within switch cases is not straightforward. However, in Rust, condtional operators in match statements is quite convenient.

### match statement with Operators

```rs

let age = 18;

match age{
  x if x <18 => println!("you are not eligible"),
  y  if y ==18 => println!("you are eligible, but wait 1 year"),
   x if x > 18 => println!("you are  eligible"),
   _ => println!("invalid age")
}


```

`x` and `y` are used as pattern variables within the match statement to represent the value of the age variable under specific conditions. `x` is associated with ages less than 18, and `y` is associated with `ages` equal to 18. 




