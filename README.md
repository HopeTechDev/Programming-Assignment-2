# Programming Assignment 2 – NumPy Array Manipulations

**Author:** SAEZ, Eljenzal Hoper U.  
**Course:** Advanced Computer Programming and Algorithms / ECE2112

---

## 📌 Description

This Jupyter Notebook provides solutions to two foundational array-processing problems using **NumPy**, a powerful library for numerical computing in Python. This assignment demonstrates:

- Creating and manipulating multi-dimensional arrays  
- Performing normalization using statistical measures  
- Filtering elements based on conditions  
- Saving processed data to `.npy` binary files  

The problems solved include:

1. **Normalization Problem** – Normalize a random 5×5 array using mean and standard deviation.  
2. **Division by 3 Problem** – Extract numbers divisible by 3 from a 10×10 array of squares.

---

## ⚙️ Requirements

- Python 3.x  
- Jupyter Notebook  
- NumPy (Install with `pip install numpy` if needed)

---

## ▶️ How to Run

1. Install [Jupyter Notebook](https://jupyter.org/install) if not already installed.  
2. Open the file **SAEZ_PA2.ipynb**.  
3. Run all cells to view the output directly in the notebook.  

---

## 💡 Examples w/ Explanation

### 01 🧪 Normalization Problem

```python

import numpy as np

X = np.random.rand(5, 5)  # Create a 5x5 array of random float values between 0 and 1

# Compute mean and standard deviation
mean = X.mean()  # Compute the mean of all elements
std_dev = X.std()  # Compute the standard deviation of all elements


# Normalize the array
X_normalized = (X - mean) / std_dev  # Normalize each element using the formula


# Save the result
np.save('X_normalized.npy', X_normalized)  # Save the normalized array to a file

# Print outputs
print("Original Array:\n", X)
print("\nNormalized Array:\n", X_normalized)

```

##### - Generates a 5×5 array of random floating-point numbers between 0 and 1 using np.random.rand(5, 5).

##### - X.mean() → computes the mean of all elements in the array.

##### - X.std() → computes the standard deviation of the array.

#####  *Normalization formula:*

  <img width="80" height="49" alt="image" src="https://github.com/user-attachments/assets/36b95403-e79f-47cc-8921-859d9a73a847" />

##### - (X - mean) / std_dev → normalizes each element by subtracting the mean and dividing by the standard deviation.

##### - np.save('X_normalized.npy', X_normalized) → saves the normalized array to a binary .npy file.

##### *Output:*


<img width="573" height="271" alt="image" src="https://github.com/user-attachments/assets/dd3a7be2-9fab-442f-a5bd-56f56c095a35" />

 ---

 ### 02 ➗ Division by 3 Problem

 ```python

import numpy as np  # Import NumPy

X = (np.arange(1, 101).reshape(10, 10)) ** 2  # Create a 10x10 matrix of squared numbers

divisible = X[X % 3 == 0]  # Filter elements divisible by 3

np.save("div_by_3.npy", divisible)  # Save the result to file

print("Original Array:\n", X)
print("\nElements Divisible by 3:\n", divisible)

```

- Creates a 10×10 array of squared numbers from 1² to 100² using (np.arange(1, 101).reshape(10, 10)) ** 2.

- X % 3 == 0 → creates a Boolean mask for numbers divisible by 3.

- X[X % 3 == 0] → filters and extracts only those elements.

- np.save("div_by_3.npy", divisible) → saves the filtered numbers into a .npy file.
  

*Output:*

<img width="651" height="335" alt="image" src="https://github.com/user-attachments/assets/7a58b673-1cea-404c-9a83-2f52c1576b5c" />

---

##### *- 🌱 "Don’t let yesterday take up too much of today."*

---


### 📝 Version History

- **v1.0** – Initial draft  
  - Wrote and tested core logic for the normalization and division‑by‑3 tasks  
  - Confirmed basic output with print statements

- **v1.1** – Clean-up and tweaks  
  - Renamed variables for clarity (e.g., `std_dev`)  
  - Improved print formatting and verified `.npy` file saving/loading

- **v1.2** – Final polish  
  - Added concise explanations for each code step  
  - Clean Markdown layout for easy readability
 
---


