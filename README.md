Joshua Price  
CS 4343 Numerical Methods for Digital Computing  
Oklahoma State University  
Creation Date: 11-11-2025  

# Linear System Solver Comparison

A Java program that solves systems of linear equations using three different numerical methods and compares their performance.

## What This Does

This program solves a 5x5 system of linear equations using three different approaches:

1. **Cramer's Rule**: Uses determinants to find each variable by computing ratios of determinants
2. **Gaussian Elimination**: Transforms the augmented matrix into row echelon form through forward elimination, then uses back substitution
3. **LU Decomposition**: Factors the coefficient matrix into lower and upper triangular matrices, then solves two simpler systems

The program runs each method 100 times to measure average execution time and compares the performance against expected computational complexity.

## The Linear System

The program solves this system of equations:
```
x₁ + 2x₂ + 3x₃ + 4x₄ + 5x₅ = 15
2x₁ + 3x₂ + 4x₃ + 5x₄ + 6x₅ = 34
3x₁ + 4x₂ + 5x₃ + 6x₄ + 7x₅ = 55
4x₁ + 5x₂ + 6x₃ + 7x₄ + 8x₅ = 78
5x₁ + 6x₂ + 7x₃ + 8x₄ + 9x₅ = 103
```

## Linear Algebra Background

**Cramer's Rule** computes each variable xᵢ as the ratio det(Aᵢ)/det(A), where Aᵢ is the coefficient matrix with column i replaced by the constant vector. This has O(n!) complexity due to determinant calculations.

**Gaussian Elimination** systematically eliminates variables by adding multiples of one equation to another until reaching a triangular form. This has O(n³) complexity.

**LU Decomposition** factors matrix A into A = LU where L is lower triangular and U is upper triangular. Once factored, you can solve Ly = b and then Ux = y. This also has O(n³) complexity but is more efficient for solving multiple systems with the same coefficient matrix.

## How to Run

Compile the program:
```bash
javac LinearSystemSolver.java
```

Run the program:
```bash
java LinearSystemSolver
```

The program will output the solution vector for each method, timing information, and performance analysis comparing actual results to theoretical complexity.

## Course Information

This project was completed for CS 4343 Numerical Methods for Digital Computing at Oklahoma State University.
