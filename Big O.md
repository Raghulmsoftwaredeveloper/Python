Big-O notation is a **mathematical way of describing how the runtime (or space) of an algorithm grows as the input size increases**.
It helps us analyze and compare algorithms without worrying about machine speed or programming language.

---

## 🔹 What Big-O Measures

* **Time Complexity** → How the number of operations grows with input size (`n`).
* **Space Complexity** → How memory usage grows with input size (`n`).

---

## 🔹 Common Big-O Complexities

| **Big-O**      | **Name**          | **Explanation**                                          | **Example**                           |
| -------------- | ----------------- | -------------------------------------------------------- | ------------------------------------- |
| **O(1)**       | Constant Time     | Execution time does not depend on input size.            | Accessing an array element            |
| **O(log n)**   | Logarithmic Time  | Grows slowly as input size increases.                    | Binary search                         |
| **O(n)**       | Linear Time       | Time grows directly with input size.                     | Traversing a list                     |
| **O(n log n)** | Linearithmic Time | Slightly worse than linear, common in efficient sorting. | Merge sort, Quick sort (average case) |
| **O(n²)**      | Quadratic Time    | Time grows proportional to square of input.              | Nested loops (e.g., Bubble sort)      |
| **O(n³)**      | Cubic Time        | Triple nested loops.                                     | Floyd-Warshall algorithm              |
| **O(2ⁿ)**      | Exponential Time  | Doubles with each additional input size.                 | Solving recursive subset problems     |
| **O(n!)**      | Factorial Time    | Grows extremely fast, impractical for large n.           | Generating all permutations           |

---

## 🔹 Visual Growth (approximate)

* **O(1)** → ⚡ constant
* **O(log n)** → 📉 very slow growth
* **O(n)** → 📈 steady growth
* **O(n log n)** → 🚀 faster than linear but manageable
* **O(n²)** → 🔥 steep growth (bad for large n)
* **O(2ⁿ), O(n!)** → 💀 impossible for large n

---

## 🔹 Quick Examples

1. **O(1) Constant**

   ```python
   arr = [1, 2, 3, 4]
   print(arr[2])  # Direct access
   ```

2. **O(n) Linear**

   ```python
   for x in arr:
       print(x)
   ```

3. **O(n²) Quadratic**

   ```python
   for i in arr:
       for j in arr:
           print(i, j)
   ```

4. **O(log n) Logarithmic**

   ```python
   def binary_search(arr, target):
       low, high = 0, len(arr)-1
       while low <= high:
           mid = (low+high)//2
           if arr[mid] == target:
               return mid
           elif arr[mid] < target:
               low = mid+1
           else:
               high = mid-1
       return -1
   ```

---
