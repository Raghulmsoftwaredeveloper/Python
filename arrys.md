# 📘 Python Arrays 

---

## 🔹 1. Python **List** (Dynamic Array)

### ✅ List Methods

1. **`append(x)`** – Adds element at end

```python
arr = [1, 2]
arr.append(3)  
print(arr)   # [1, 2, 3]
```

2. **`extend(iterable)`** – Adds multiple elements

```python
arr = [1, 2]
arr.extend([3, 4])  
print(arr)   # [1, 2, 3, 4]
```

3. **`insert(i, x)`** – Inserts element at index

```python
arr = [1, 3]
arr.insert(1, 2)  
print(arr)   # [1, 2, 3]
```

4. **`remove(x)`** – Removes first occurrence of element

```python
arr = [1, 2, 3, 2]
arr.remove(2)  
print(arr)   # [1, 3, 2]
```

5. **`pop([i])`** – Removes & returns element at index (default: last)

```python
arr = [1, 2, 3]
print(arr.pop())   # 3
print(arr)         # [1, 2]
```

6. **`clear()`** – Removes all elements

```python
arr = [1, 2, 3]
arr.clear()  
print(arr)   # []
```

7. **`index(x)`** – Returns index of first occurrence

```python
arr = [10, 20, 30]
print(arr.index(20))   # 1
```

8. **`count(x)`** – Returns number of occurrences

```python
arr = [1, 2, 2, 3]
print(arr.count(2))   # 2
```

9. **`sort(reverse=False)`** – Sorts list

```python
arr = [3, 1, 2]
arr.sort()  
print(arr)   # [1, 2, 3]
arr.sort(reverse=True)  
print(arr)   # [3, 2, 1]
```

10. **`reverse()`** – Reverses list order

```python
arr = [1, 2, 3]
arr.reverse()  
print(arr)   # [3, 2, 1]
```

11. **`copy()`** – Returns shallow copy

```python
arr = [1, 2, 3]
b = arr.copy()
print(b)     # [1, 2, 3]
```

---

## 🔹 2. Python **array Module**

```python
import array
arr = array.array('i', [10, 20, 30])   # 'i' = integer
```

### ✅ Array Methods

When we use **Python’s built-in `array` module**, we need to specify a **type code** that defines what type of elements the array can hold.

---

# 📘 Python Array Type Codes (`array` module)

| Type Code | C Type Equivalent                         | Python Type  | Size (bytes) |
| --------- | ----------------------------------------- | ------------ | ------------ |
| `'b'`     | signed char                               | int          | 1            |
| `'B'`     | unsigned char                             | int          | 1            |
| `'u'`     | Py\_UNICODE (deprecated after Python 3.3) | Unicode char | 2/4          |
| `'h'`     | signed short                              | int          | 2            |
| `'H'`     | unsigned short                            | int          | 2            |
| `'i'`     | signed int                                | int          | 2 / 4        |
| `'I'`     | unsigned int                              | int          | 2 / 4        |
| `'l'`     | signed long                               | int          | 4            |
| `'L'`     | unsigned long                             | int          | 4            |
| `'q'`     | signed long long                          | int          | 8            |
| `'Q'`     | unsigned long long                        | int          | 8            |
| `'f'`     | float                                     | float        | 4            |
| `'d'`     | double                                    | float        | 8            |

---

### ✅ Example Usage

```python
import array

# Integer array
arr_int = array.array('i', [10, 20, 30])
print(arr_int)   # array('i', [10, 20, 30])

# Float array
arr_float = array.array('f', [1.5, 2.5, 3.5])
print(arr_float) # array('f', [1.5, 2.5, 3.5])

# Unsigned int array
arr_uint = array.array('I', [100, 200, 300])
print(arr_uint)  # array('I', [100, 200, 300])
```

---


1. **`append(x)`** – Adds single element

```python
arr.append(40)
print(arr)   # array('i', [10, 20, 30, 40])
```

2. **`extend(iterable)`** – Adds multiple elements

```python
arr.extend([50, 60])
print(arr)   # array('i', [10, 20, 30, 40, 50, 60])
```

3. **`insert(i, x)`** – Inserts at index

```python
arr.insert(1, 15)
print(arr)   # array('i', [10, 15, 20, 30, 40, 50, 60])
```

4. **`remove(x)`** – Removes first occurrence

```python
arr.remove(30)
print(arr)   # array('i', [10, 15, 20, 40, 50, 60])
```

5. **`pop([i])`** – Removes element (default: last)

```python
print(arr.pop())   # 60
```

6. **`index(x)`** – Returns index of element

```python
print(arr.index(20))   # 2
```

7. **`reverse()`** – Reverses array

```python
arr.reverse()
print(arr)   # array('i', [50, 40, 20, 15, 10])
```

8. **`buffer_info()`** – Returns memory address & length

```python
print(arr.buffer_info())   # (address, length)
```

9. **`count(x)`** – Number of occurrences

```python
print(arr.count(20))   # 1
```

10. **`fromlist(list)`** – Extend array with list

```python
arr.fromlist([70, 80])
print(arr)   # array('i', [50, 40, 20, 15, 10, 70, 80])
```

11. **`tolist()`** – Convert to list

```python
print(arr.tolist())   # [50, 40, 20, 15, 10, 70, 80]
```

12. **`byteswap()`** – Swaps byte order

```python
arr.byteswap()
print(arr)   # swapped values (machine dependent)
```

---

## 🔹 3. **NumPy Arrays**

```python
import numpy as np
arr = np.array([[1, 2, 3], [4, 5, 6]])
```

### ✅ NumPy Array Methods

1. **`shape`** – Returns dimensions

```python
print(arr.shape)   # (2, 3)
```

2. **`ndim`** – Number of dimensions

```python
print(arr.ndim)    # 2
```

3. **`size`** – Total number of elements

```python
print(arr.size)    # 6
```

4. **`dtype`** – Data type

```python
print(arr.dtype)   # int64 (depends on system)
```

5. **`reshape(m, n)`** – Change shape

```python
print(arr.reshape(3, 2))
```

6. **`flatten()`** – Convert to 1D

```python
print(arr.flatten())   # [1 2 3 4 5 6]
```

7. **`astype(type)`** – Change data type

```python
arr2 = arr.astype(float)
print(arr2)
```

8. **Math Functions** – `sum()`, `min()`, `max()`, `mean()`

```python
print(arr.sum())   # 21
print(arr.min())   # 1
print(arr.max())   # 6
print(arr.mean())  # 3.5
```

9. **`sort()`** – Sort elements

```python
print(np.sort(arr))
```

10. **`concatenate()`** – Join arrays

```python
a = np.array([1, 2])
b = np.array([3, 4])
print(np.concatenate((a, b)))   # [1 2 3 4]
```

11. **`split()`** – Split array

```python
arr = np.array([1,2,3,4,5,6])
print(np.split(arr, 3))   # [array([1,2]), array([3,4]), array([5,6])]
```

12. **`unique()`** – Unique elements

```python
arr = np.array([1,2,2,3,3,3])
print(np.unique(arr))   # [1 2 3]
```

---

# ✅ Summary

* **Lists** – General purpose, dynamic, many methods.
* **`array` module** – Type-restricted, memory efficient.
* **NumPy arrays** – Best for scientific computing, very fast.

---
