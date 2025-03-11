# 📅 Week 1  

## 💻 Programming Languages  

- A way to communicate with computers using instructions.  
- In the beginning, closely linked to how computers work internally.  
- Computers store values in memory and use registers for calculations.  
- **Basic steps:**  
  1. Load a value from memory into a register.  
  2. Perform an operation (like addition).  
  3. Store the result back in memory.  
- ⚠️ This process was complex and prone to errors.  
- 🚀 High-level languages were created to make coding easier.  

## 🧠 Abstraction in Programming  

- **What is Abstraction?**  
  - A way to simplify complex concepts in computational thinking.  

- **Common Abstractions:**  
  - Assigning values to **variables**.  
  - Using **conditional statements** (if-else).  
  - **Loops** for iteration (for, while).  
  - 🛠️ **Functions & recursion** to reuse code.  
  - 📦 **Data structures** like arrays, lists, and dictionaries.  

- **From High-Level to Low-Level:**  
  - Programming languages express these abstract ideas.  
  - 🔄 **Compilers & interpreters** translate high-level code into machine language.  
  - ⚖️ **Trade-off:** More abstraction means less control over hardware but fewer errors.  


### Styles of Programming  

#### ⚡ Imperative vs. Declarative  

| Feature             | 🏗️ Imperative Programming | 🎯 Declarative Programming |
|---------------------|--------------------------|----------------------------|
| **Focus**          | How to compute            | What the computation should produce |
| **Approach**       | Step-by-step instructions | Defines results in terms of smaller computations |
| **Usage**          | Uses loops, conditionals  | Uses functions and transformations |
| **Intermediate Variables** | Commonly used | Typically avoided |
| **Example**        | Procedural languages (C, Java) | Functional languages (Haskell, SQL) |

## Imperative vs Declarative Programming, by Example  

### 📝 Adding Values in a List  

#### 🏗️ Imperative Approach  

```python
def sum_list(l):
    sum = 0
    for x in l:
        sum += x
    return sum
```
- **Intermediate values:** `sum`, `x`  
- **Explicit iteration:** Examines each element in the list.

### 🎯 Declarative (in Python)  

```python
def sum_list(l):
    if l == []:
        return 0
    else:
        return l[0] + sum_list(l[1:])
```
- **Base case:** An empty list sums to `0`.  
- **Inductive step:** Add the first element to the sum of the rest.  
- **No extra variables used.**  

### 🏗️ Imperative Approach (Python)  

```python
def sum_square_even(n):
    sum = 0
    for x in range(n + 1):
        if x % 2 == 0:
            sum += x * x
    return sum
```
- **Uses loops and conditions** to find even numbers and square them.  
- **Can be written in a functional style** to improve reusability.  
- **Helps break the problem into smaller, reusable units of code.**  

### **Names, Types, and Values**  

- Computers store everything as `bits` (no difference between data and instructions).  
- `Types` help interpret bits as **numbers, characters, or booleans**.  
- **Type rules define:**  
  - Allowed values (e.g., `integers`, `floats`).  
  - Valid operations (e.g., `addition`, `comparison`).  
- **Strict type-checking** prevents errors:  
  - **Wrong expressions** (e.g., **dimension mismatch** in math).  
  - **Incorrect assignments** (e.g., assigning `text` to a `number` variable).  

## 🚀 Abstract Data Types & Object-Oriented Programming  

### 📦 Collections Matter  
- Examples: `📚 Arrays`, `📋 Lists`, `📖 Dictionaries`.  

### 🏗️ Abstract Data Types (ADTs)  
- A **structured collection** with a fixed interface.  
- **Example:** A `🗂️ Stack` allows only `⬆️ push` and `⬇️ pop` operations.  
- **Priority Queue** supports `➕ insert` and `❌ delete-max`.  
- Can be implemented using **sorted/unsorted lists** or a **heap**.  

### 🏛️ Object-Oriented Programming (OOP)  
- Focuses on 🔹 `data types` and their behavior.  
- Functions are called **through objects** instead of passing data.  
- **Example in Python:**  
  - `my_list.sort()`🔄 (modifies the list).  
  - `sorted(my_list)` 🆕 (returns a new sorted list).  
  
### **What's Next?** 🚀  

- Explore **programming language concepts**.  
- Learn **OOP, exception handling, concurrency, and event-driven programming**.  
- Use **Java** as the main example (**imperative + OOP**).  
- Discuss **design choices**—every language has trade-offs.  
- Understand why there are **so many languages** (and why new ones keep coming! 😆).  

