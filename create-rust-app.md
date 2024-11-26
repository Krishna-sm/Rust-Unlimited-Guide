- ### To Create First Program Rust so, follow some steps

- step 1. create rust app/project using  
  

  ```bash
    cargo new my-app # replace my-app with your project name
   ```

- step 2. change directory 
        
    ```bash
            cd my-app
    ```
- step 3. modify `src/main.rs` file
   - by the way rust default project provide a hello world program . 

    ```rs
            fn main(){
                println!("Radhey Radhey !");
            }
    ```
        
 
- step 4: generate .exe by build app
  ```bash
    cargo build
    ```  
 after build the app it generate .exe file in `myapp/target/debug/{project-name}.exe`

- step 5: excute .exe file by run app 

  ```bash
    cargo run
    ```  

🎉 congratulation, your first app is created .


#### Let understand `Hello world` Program.

- `fn` : to define or declare function
- `main` : It is a main function that is automatically called by the Rust compiler.
- `{}` : `curly brackets`  are code blocks that help define the scope of code.
- `println!()` : `println!()` is a macro used to print statements in the console. It is similar to the `printf` statement in C. 🎉 installed in your local machine.

