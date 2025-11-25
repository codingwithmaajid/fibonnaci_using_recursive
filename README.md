# Fibonacci Program in C

This repository contains a simple C program to calculate the **nth Fibonacci number** using recursion.  
The program accepts user input via `scanf` and prints the result.

---

## 🚀 Features
- Accepts user input for `n`.
- Uses recursion to compute Fibonacci numbers.
- Handles base cases (`fib(0) = 0`, `fib(1) = 1`).
- Demonstrates recursion in C programming.

---

## 📂 Code Explanation
1. **Function Declaration**  
   `int fib(int n);` declares the recursive function.

2. **Main Function**  
   - Prompts the user for input.  
   - Calls the `fib()` function.  
   - Prints the result.

3. **Recursive Function**  
   - Base cases:  
     - `fib(0) = 0`  
     - `fib(1) = 1`  
   - Recursive case:  
     - `fib(n) = fib(n-1) + fib(n-2)`

---

## 🖥️ Example Run
```c
Enter a number to find its Fibonacci value: 7
The Fibonacci of 7 is 13
```c
#include <stdio.h>

// Function prototype
int fib(int n);

int main() {
    int n;

    // Prompt user for input
    printf("Enter a number to find its Fibonacci value: ");
    scanf("%d", &n);

    // Display the result
    printf("The Fibonacci of %d is %d\n", n, fib(n));
    return 0;
}

// Recursive function to calculate Fibonacci
int fib(int n) {
    // Base cases
    if (n == 0) {
        return 0;
    }
    if (n == 1) {
        return 1;
    }

    // Recursive case: fib(n) = fib(n-1) + fib(n-2)
    return fib(n - 1) + fib(n - 2);
}
