## -linear_regression_mode


Reflection on My First Experience with Rust and Burn Library

Introduction

This was my first time working with Rust and the Burn library, and my goal was to 
implement a simple linear regression model. The experience provided valuable lessons, 
even though I encountered multiple challenges. This reflection outlines the steps I took, the 
failures I faced, and what I learned from the experience.


Steps Taken

1. 
o 
I created a new Rust project using:
o 
I then modified the Cargo.toml file to include the required dependencies:
o 
After saving the file, I proceeded to build the project using cargo build.
o 
When I ran cargo build, I received multiple "unresolved import" errors, 
meaning Rust could not recognize some dependencies.
o 
I checked my Rust installation and verified that I had rustc and cargo 
installed correctly.
o 
The Burn library requires a proper backend setup, and I suspected that my 
system might be missing some dependencies.
Setting Up the Rust Project
cargo new linear_regression_model

cd linear_regression_model

[dependencies]

burn = { version = "0.16.0", features = ["wgpu", "train"] }

burn
-ndarray = "0.16.0"

rand = "0.9.0"

rgb = "0.8.50"

textplots = "0.8.6"

2. 
Encountering Errors During Compilation
3. 
Issues with Rust Dependencies
o 
I tried running cargo clean and then cargo build again, but the errors 
persisted.
o 
One of the biggest failures was the "link.exe not found" error.
o 
I learned that Rust (when using the MSVC toolchain) requires Visual Studio 
with C++ Build Tools
.
o 
Even though I had Visual Studio Code, I later realized that VS Code is NOT 
the same as Visual Studio
.
o 
Installing Visual Studio with C++ Build Tools is necessary, but due to time 
constraints, I could not fully set it up.
o 
I tried reinstalling Rust and switching to the gnu toolchain using:
o 
I considered using WSL (Windows Subsystem for Linux) to compile the 
project in a Linux environment, but I lacked prior experience setting it up.
4. 
Encountering Linker Errors (link.exe not found)
5. 
Trying Alternative Solutions
rustup default stable-gnu

However, this did not fully resolve my issues.


Reasons for Failure

1. 
o 
This was my first time using Rust, so I was still learning the syntax, package 
management, and toolchain requirements.
o 
The Burn library is also relatively new, and there aren’t many beginner-
friendly resources available.
Lack of Experience with Rust
2. 
o 
I initially assumed that Visual Studio Code was enough, but I later learned 
that Rust requires Visual Studio with C++ Build Tools
.
o 
Since link.exe was missing, I was unable to compile the dependencies 
properly.
Incomplete Setup for Rust on Windows
3. 
Library Dependencies and Compatibility Issues
o 
The Burn library requires specific versions of dependencies, and I 
struggled with ensuring all were correctly installed.
o 
The NdArray backend also requires proper configuration, which I was unable 
to complete.
o 
Due to the deadline for this assignment, I did not have enough time to fully 
troubleshoot all issues.
o 
Setting up Rust properly (including link.exe) and debugging dependency 
errors took longer than expected.
o 
While I tried various solutions (cargo clean, reinstalling Rust, switching 
toolchains), I did not have the debugging experience to quickly diagnose 
and fix issues.
4. 
Time Constraints
5. 
Limited Debugging Experience

What I Learned from This Experience

1. 
o 
Unlike some other languages, Rust (especially when using MSVC) needs 
Visual Studio with C++ Build Tools to compile certain crates.
o 
If I had known this earlier, I would have set up Visual Studio before starting.
Rust Requires a Proper Development Environment
2. 
o 
The Cargo.toml file must be configured correctly, and certain libraries (like 
Burn) may require additional setup.
Dependency Management in Rust Can Be Tricky
3. 
o 
Understanding error messages like "link.exe not found" is crucial.
o 
I learned how to check Rust toolchains and switch between MSVC and GNU
versions.
Debugging and Error Messages Are Important
4. 
o 
If I had researched Rust’s system requirements beforehand, I could have 
avoided some of these issues.
The Importance of Proper Research Before Starting

Conclusion

Even though I was unable to fully complete the assignment due to toolchain setup issues 
and lack of Rust experience, I gained valuable insights into Rust’s development 
environment. This experience helped me understand the importance of proper setup, 
dependency management, and debugging skills
.

If I were to attempt this again, I would:

• 
Install Visual Studio with C++ Build Tools first.
• 
Start with a smaller Rust project to understand Cargo and dependencies.
• 
Use Rust’s official documentation and community resources to troubleshoot 
errors.
This assignment, though challenging, has deepened my understanding of Rust and 
