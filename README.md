# CS487 - Building Secure Computing Systems - AutoPatch

This repository contains the project developed for the CS487 course on Building Secure Computing Systems at the University of Illinois at Chicago (UIC). AutoPatch is a GenAI-assisted tool designed to automatically detect and patch bugs in C code. By combining **Google's Address Sanitizer (ASan)**, **American Fuzzy Lop (AFL)** and **OpenAI's GPT-4o mini**, AutoPatch simplifies the debugging process by identifying and resolving syntactic, runtime and semantic errors in buggy programs.

### Features  
- **Automated Bug Detection:** detects and identifies syntactic errors, runtime crashes and semantic inconsistencies.  
- **Patch Generation:** uses GPT to generate targeted fixes while preserving the program's intended functionality.  
- **Iterative Testing:** retests patched code to ensure bugs are resolved.

## How It Works
1. **Initial Compilation:**  
   The code is compiled with ASan to detect memory-related issues.  
2. **Fuzzing:**  
   AFL tests the program for runtime crashes using mutated inputs.  
3. **Patching with GPT:**  
   Issues detected by ASan and AFL are passed to GPT-4o mini, which generates fixes.  
4. **Iterative Process:**  
   The patched code is retested with AFL to ensure reliability.

