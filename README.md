# Experiment: Call by Value and Call by Reference in C++

**Aim:**
To study **Call by Value** and **Call by Reference** in C++.

**Software Used:**
Visual Studio Code (VS Code)

---

## THEORY

### 🔹 Introduction

Functions in C++ allow passing data between different parts of a program. The way data (arguments) is passed determines whether the **original variables are modified** or not.

There are two major methods of passing arguments in C++:

1. **Call by Value**
2. **Call by Reference**

---

### 1️⃣ Call by Value

* A **copy of the actual argument** is passed to the function.
* Changes inside the function affect only the copy, not the original variable.
* The original data remains **unmodified**.

**Example:**

```cpp
#include <iostream>
using namespace std;

void change(int x) {
    x = x + 10;   // modifies only local copy
}

int main() {
    int a = 5;
    change(a);
    cout << "Value of a after function call: " << a << endl;
    return 0;
}
```

---

### 2️⃣ Call by Reference

* Instead of copying, the **reference (or address)** of the variable is passed.
* The function works on the **actual variable**, so changes reflect in the original data.

**Example:**

```cpp
#include <iostream>
using namespace std;

void change(int &x) {
    x = x + 10;   // modifies the original variable
}

int main() {
    int a = 5;
    change(a);
    cout << "Value of a after function call: " << a << endl;
    return 0;
}
```

---

### Importance in Programs

* **Call by Value** → Safer when original data should not change.
* **Call by Reference** → Useful when:

  * Original data must be updated.
  * Passing large data structures (avoid copying overhead).
  * Efficient operations on arrays and objects.

---

## PROGRAMS & ALGORITHMS

### ✅ Program 1: Salary Increment using Call by Reference

**Algorithm:**

1. Start.
2. Define function that accepts `salary` by reference.
3. Check conditions for increment.
4. If at least 3 conditions are true → increase salary by 20%.
5. Display updated salary.
6. Stop.

---

### ✅ Program 2: Swap Two Numbers using Call by Value

**Explanation:**
Swapping happens inside function but **original values remain unchanged**.

**Algorithm:**

1. Start.
2. Define swap function with call by value.
3. Swap inside function.
4. Print numbers before and after call.
5. Stop.

---

### ✅ Program 3: Swap Two Numbers using Call by Reference

**Explanation:**
Swapping happens inside function and **original values are modified**.

**Algorithm:**

1. Start.
2. Define swap function with call by reference.
3. Swap numbers inside function.
4. Print numbers before and after call.
5. Stop.

---

### ✅ Program 4: Modify Array using Pointers

**Explanation:**
Arrays are always passed as pointers, so changes inside the function affect the original array.

**Algorithm:**

1. Start.
2. Define function to update array elements.
3. Use pointer arithmetic to assign values.
4. Print array before and after modification.
5. Stop.

---

## CONCLUSION

* **Call by Value** → Passes a copy of data, **original remains unchanged**.
* **Call by Reference** → Passes the actual reference, **original data is modified**.
* Arrays and pointers are naturally passed by reference, making them efficient for large data handling.
* Understanding both concepts is crucial for writing **memory-efficient, safe, and effective C++ programs**.
