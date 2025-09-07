# README: Activation Functions and Financial Calculations Project

## Overview

This repository demonstrates Python programming for:

1. **Deep Learning Activation Functions**: sigmoid, tanh, ReLU, and Leaky ReLU.
2. **Financial Calculations using NumPy**: revenue, expenses, profit, and total sales calculations.

The project combines mathematical concepts and coding practices, showcasing professional skills suitable for a portfolio.

## Activation Functions

* **Sigmoid**: Converts any number into a value between 0 and 1.
* **Tanh**: Converts numbers into a value between -1 and 1.
* **ReLU**: Returns 0 for negative numbers, and the number itself if positive.
* **Leaky ReLU**: Similar to ReLU but allows a small value for negatives.

### Examples

```python
sigmoid(100)
sigmoid(-56)
tanh(-56)
tanh(1)
relu(-100)
relu(8)
leaky_relu(-100)
leaky_relu(8)
```

## Financial Calculations

* Calculate **profit** by subtracting expenses from revenue.
* Calculate **total sales per product** and **total revenue per row** using NumPy dot product.

### Examples

```python
revenue = np.array([[180,200,220],[24,36,40],[12,18,20]])
expenses = np.array([[80,90,100],[10,16,20],[8,10,10]])
profit = revenue - expenses

price_per_unit = np.array([1000,400,1200])
units = np.array([[30,40,50],[5,10,15],[2,5,7]])
total_per_product = price_per_unit * units
total_revenue_rows = np.dot(units, price_per_unit)
```

## Key Features

* Modular, professional code.
* Combines **math, programming, and NumPy usage**.
* Suitable for portfolio projects and professional demonstration.

## How to Run

1. Clone the repository.
2. Run `activation_financial_calculations.py` in a Python environment.
3. Observe outputs for activation functions and financial calculations.

---

# Code File: activation\_financial\_calculations.py

```python
import math
import numpy as np

# Activation Functions
def sigmoid(x):
    return 1 / (1 + math.exp(-x))

def tanh(x):
    return (math.exp(x) - math.exp(-x)) / (math.exp(x) + math.exp(-x))

def relu(x):
    return max(0, x)

def leaky_relu(x):
    return max(0.1*x, x)

# Examples
print("Sigmoid:", sigmoid(100), sigmoid(-56))
print("Tanh:", tanh(-56), tanh(1), tanh(50))
print("ReLU:", relu(-100), relu(8))
print("Leaky ReLU:", leaky_relu(-100), leaky_relu(8))

# Financial Calculations
revenue = np.array([[180,200,220],[24,36,40],[12,18,20]])
expenses = np.array([[80,90,100],[10,16,20],[8,10,10]])
profit = revenue - expenses
print("Profit:")
print(profit)

price_per_unit = np.array([1000,400,1200])
units = np.array([[30,40,50],[5,10,15],[2,5,7]])
total_per_product = price_per_unit * units
print("Total Revenue per Product:")
print(total_per_product)
total_revenue_rows = np.dot(units, price_per_unit)
print("Total Revenue per Row:")
print(total_revenue_rows)
```
