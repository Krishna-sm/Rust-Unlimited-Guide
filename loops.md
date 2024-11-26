A loops in programming is a control structure that repeatedly executes a block of code as long as a specified condition is true or for a specified number of iterations. It helps in automating repetitive tasks and iterating over collections of data.

## Types of Loops in Rust

- loop keyword 
- while loop 
- for loop 


Before starting loop , let understand `break` and `continue` statement.

### Break Keyword

- It used to break the statement based on a desired condition.

syntax:
```rs

           fn main(){
             if(num ==5){
                break;
            }
            println!("Hello world {num}");
           }

```
- n this code, when the `num` variable equals 5, it breaks the block of code.



### Continue keyword

- The `continue` keyword is used to skip or bypass a particular statement based on a specified condition.

syntax:
```rs

            fn main(){
                if(num ==5){
                continue;
            }
            println!("Hello world,{num}");

            }

```
- n this code, when the `num` variable equals 5, it bypass the block of code.


## Loop Keyword

- In Rust, the `loop` is used to create an infinite loop that continues to execute a block of code until manually stopped. In other programming languages, it is similar to a `do-while` loop, where the condition is provided within the `while` function. In Rust, it is simply used with the `loop` keyword, and the loop is interrupted with the `break` keyword.

`syntax`:

```rs
        fn main(){
            loop{
                // code
            }
        }
```

`example`:

 - print a table of the number num;
  
```rs
                fn main(){

            let num:i32 = 4;
            let mut index:i32 =1;

            loop{
                if index == 11 {
                    break;
                }
                println!("{num}X{index} => {}",num*index);
                i=i+1;
            }

                }

```


## while loop

- The `while` loop is also known as an entry-control loop. It is used to execute a block of code based on a specified condition.

+ syntax
  
```rs
        fn main(){
            while(condition){
                        // code
            }
        }
```

> ### print a table of the number num;
+ example

```rs
        fn main(){
            let:i32 = 4;
            let mut i:i32 = 1;
            while i<=10 {
             println!("{num}X{i} => {}",num*i);
                    i=i+1;
            }
        }
```
- it excute untill `i <= 10 `.
   

## range operator 

- `Exclusive Range (..)`

syntax:
  
```rs
 startNum..endNum;

// example
0..4 // 0,1,2,3
```


- `InExclusive Range (..=)`
  
syntax: 

```rs
    startNum..=endNum;
    // example
    0..=4 // 0,1,2,3,4
```


## For loop 

#### examples

- print table of the 5

```rs
        fn main(){
            let num:i32 = 5;

        for i in 1..=10{
            println!("{num}X{i} => {}",num*i);
        }

        }
```
- access index 

```rs
            fn main(){
                for (index,i) in (1..=10).enumerate(){
            println!("{index} {num}X{i} => {}",num*i);

                }
            }
```



## For loop with array

#### by index

```rs
    fn main(){
        let arr = [10,20,30,40,50,60,70];

for  i in 0..arr.len(){
      println!("{:?}",arr[i]);
}
    }
```


### by array 

```rs
        fn main(){
        let arr = [10,20,30,40,50,60,70];

        for  i in arr{
        println!("{:?}",i);
        }
        } 

```

### access array index


```rs
fn main(){

    let arr = [10,20,30,40,50,60,70];

    for  (index,i) in arr.iter().enumerate(){
    println!("{:?} {index}",i);
    } 
    
} 

```