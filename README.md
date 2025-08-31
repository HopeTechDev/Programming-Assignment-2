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

# Create a random 5x5 ndarray
X = np.random.rand(5, 5)

# Compute mean and standard deviation
mean = X.mean()
std_dev = X.std()

# Normalize the array
X_normalized = (X - mean) / std_dev

# Save the result
np.save('X_normalized.npy', X_normalized)

# Print outputs
print("Original Array:\n", X)
print("\nNormalized Array:\n", X_normalized)

```

- A 5x5 array of random values between 0 and 1 is generated using np.random.rand(5, 5).

- The mean and standard deviation of the array are computed.

- Normalization is done with the formula:
  <img width="73" height="48" alt="image" src="https://github.com/user-attachments/assets/9204a8ac-84ff-416c-8c0e-c1b647d3e8c5" />
	
- The resulting normalized array is saved to X_normalized.npy.

Sample Output: 
<img width="582" height="280" alt="image" src="https://github.com/user-attachments/assets/795492b6-f901-45a3-99f5-5072a5281658" />
