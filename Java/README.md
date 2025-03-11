# 📅 Week 1  

## 💻 Programming Languages  

#### Lecture - 1

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

#### Lecture - 2 
### 🔹 The Role of Types  

- Ensure **consistent interpretation** of binary data.  
- Define **how bits are viewed** (e.g., `integers`, `floats`, `characters`).  
- Control:  
  - **Allowed values** (range, precision).  
  - **Valid operations** (e.g., addition for numbers, not for text).  
- Help **structure computation** by defining concepts:  
  - **Example:** `Point → (Float, Float)`, `Banking → Account Types & Customers`.  
- **Catch bugs early** 🐞:  
  - Prevent **incorrect expressions** (e.g., mismatched types).  
  - Avoid **wrong assignments** (e.g., assigning text to a number).  

### 🔹 Dynamic vs Static Typing  

- Every **variable** has a **type**.  
- How is the **type** determined?  

#### 🔹 Dynamic Typing (`Python` 🐍)  
- Type is based on the **current value**.  
- Example:  
  ```python
  x = 10    # x is an `int`
  x = 7.5   # now x is a `float`
  ```
  ```c
  int x;     // `x` must always store an integer
  float a;   // `a` must always store a float
  ```

### 🔹 Static Typing Helps Catch Errors Early  

- In **dynamically typed languages** like `Python`, typos can cause subtle bugs.  
- Example:  

  ```python
  def factors(n):
      factorlist = []
      for i in range(1, n + 1):
          if n % i == 0:
              factorlst = factorlist + [i]  # ❌ Typo here! (`factorlst` instead of `factorlist`)
      return factorlist

### 🔹 Empty User-Defined Objects  

- A **linked list** is a sequence of objects of type `Node`.  
- In `Python`, an **empty linked list** is often represented by `None`.  
- Example:  
  ```python
  class Node:
      def __init__(self, value):
          self.value = value
          self.next = None

  l = None  # Represents an empty linked list

### 🔹 Types of Organizing Concepts  

- **Type synonyms** make code clearer.  
  - Example:  
    ```python
    Point2D = tuple[float, float]  # A 2D point
    Point3D = tuple[float, float, float]  # A 3D point
    ```
  - Using `Point2D` and `Point3D` improves readability ✅.  

- **Advanced types** help structure programs.  
  - Example: In **banking**, `Account` and `Customer` are **separate types**.  
  - **Deposits, withdrawals, and transfers** apply to `Account`, not `Customer`.  
  - **Updating details** applies to `Customer`, not `Account`.  

### 🔹 Static Analysis  

- **Find errors early** to save time & effort ✅.  
- **Compilers can't guarantee correctness** (Halting problem – Alan Turing).  
- **Static typing** detects errors at **compile time** 🛠️.  
  - Dynamic typing catches them **only at runtime**.  
  - Runtime checks **slow down execution** ⏳.  
- **Optimizations with static analysis** 🚀:  
  - Re-order statements for efficient reads/writes.  
  - Reuse previously computed expressions.  

### 🔹 Summary  

- **Why are types important?**  
  - Help interpret **bit sequences** in memory.  
  - Organize **code in a meaningful way** 🏗️.  
  - Allow compilers to **catch bugs early** & **optimize performance** 🚀.  

- **Automatic Type Inference** 🔍  
  - Some languages **guess types** based on usage.  
  - Example:  
    ```python
    x = 7  
    y = x + 15  # y is inferred as int
    ```
  - If types remain **consistent**, the program works smoothly ✅.  
