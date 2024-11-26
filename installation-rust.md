- To install rust visit official documentation of rust  
[click here](https://www.rust-lang.org/)
```bash
https://www.rust-lang.org/
``` 

- Navigate to the "Install" section.

- Download `rustup-init.exe` for Windows. If you are using another operating system, install it using the following `curl` command:


```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

```

-  After downloading rustup-init.exe 
   -  excute .exe
   -  Choose option 2 for manual setup (this may take 20-30 minutes)
   -  During manual setup, it will prompt you to install `Visual Studio C++ Build Tools`. Close this prompt.

- After finishing the `rustup-init.exe` installation, check if Rust is installed on your local machine:
```bash
        rustc --version
        cargo --version  # just like npm
```
- Once you have checked Rust , install ` Visual Studio C++ Build tool` 
  - visit 
  ```bash
    https://visualstudio.microsoft.com/visual-cpp-build-tools/
   ```
  - Download the build tools .exe


- Excute `vs_buildTools.exe ` and allow to install tools , after install  select `Desktop development with C++`  . 
    - this process take 20-40 minutes

- after install build tools . rust successfully 🎉 installed in your local machine.

