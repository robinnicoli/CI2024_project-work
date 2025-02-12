# Project Work CI 2024-2025

## Overview
This project implements a symbolic regression algorithm using genetic programming (GP). The goal is to approximate mathematical functions given input-output data from multiple datasets. 

## Algorithm Workflow
1. **Initialization**:
   - A population of **random expression trees** is generated.
   - Each tree represents a candidate mathematical expression.

2. **Evaluation**:
   - Each individual is evaluated on the dataset.
   - The MSE is used as the fitness score.
   - Invalid expressions are replaced with a fallback value to maintain robustness.

3. **Selection**:
   - A tournament selection method is used to choose the best individuals.

4. **Crossover and Mutation**:
   - Crossover: Two parent trees swap random subtrees to create new offspring.
   - Mutation: A random subtree is replaced with a newly generated subtree to introduce diversity.

5. **Evolution Process**:
   - The algorithm iterates over multiple generations, refining the population and the best expression is selected based on its fitness score.

6. **Final Output**:
   - The best expression for each dataset is stored in `s335017.py`.

## Performance Considerations
- **Computation Time**: The algorithm is computationally expensive due to the large population size and multiple generations.
- **Parameter Choice**:  I choose to give the values of population size, generations, and mutation/crossover rates high in order to have the best search performance. But as a result, the execution time is quite long (nearly 40min). I couldn't bring the execution time down.

## Results
| Problem | Fitness Value |
|---------|--------------|
| Problem 1 | 3.23e-3 |
| Problem 2 | 2.89e13 |
| Problem 3 | 2.69e3 |
| Problem 4 | 21.6 |
| Problem 5 | 5.57e-18 |
| Problem 6 | 8,27 |
| Problem 7 | 711 |
| Problem 8 | 2,25e7 |
