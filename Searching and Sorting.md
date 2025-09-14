# 🔍 Searching Methods

### 1. **Linear Search**

* Check each element one by one.
* Works on **unsorted/sorted** data.
* **Time:** O(n)

```python
def linear_search(arr, x):
    for i in range(len(arr)):
        if arr[i] == x:
            return i
    return -1
```

---

### 2. **Binary Search**

* Works only on **sorted** data.
* Divide array into halves.
* **Time:** O(log n)

```python
def binary_search(arr, x):
    low, high = 0, len(arr)-1
    while low <= high:
        mid = (low+high)//2
        if arr[mid] == x:
            return mid
        elif arr[mid] < x:
            low = mid+1
        else:
            high = mid-1
    return -1
```

---

# 🔄 Sorting Methods

### 1. **Bubble Sort**

* Repeatedly swap adjacent elements.
* **Time:** O(n²), Best O(n)

```python
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
```

---

### 2. **Selection Sort**

* Select minimum and place at correct position.
* **Time:** O(n²)

```python
def selection_sort(arr):
    n = len(arr)
    for i in range(n):
        min_idx = i
        for j in range(i+1, n):
            if arr[j] < arr[min_idx]:
                min_idx = j
        arr[i], arr[min_idx] = arr[min_idx], arr[i]
```

---

### 3. **Insertion Sort**

* Insert element into its correct position in sorted part.
* **Time:** O(n²), Best O(n)

```python
def insertion_sort(arr):
    for i in range(1, len(arr)):
        key = arr[i]
        j = i-1
        while j >= 0 and arr[j] > key:
            arr[j+1] = arr[j]
            j -= 1
        arr[j+1] = key
```

---

### 4. **Merge Sort**

* Divide & Conquer, merge sorted halves.
* **Time:** O(n log n)

```python
def merge_sort(arr):
    if len(arr) > 1:
        mid = len(arr)//2
        L, R = arr[:mid], arr[mid:]
        merge_sort(L)
        merge_sort(R)

        i = j = k = 0
        while i < len(L) and j < len(R):
            if L[i] < R[j]:
                arr[k] = L[i]; i += 1
            else:
                arr[k] = R[j]; j += 1
            k += 1
        while i < len(L): arr[k] = L[i]; i += 1; k += 1
        while j < len(R): arr[k] = R[j]; j += 1; k += 1
```

---

### 5. **Quick Sort**

* Pick pivot, partition, recurse.
* **Time:** Avg O(n log n), Worst O(n²)

```python
def quick_sort(arr):
    if len(arr) <= 1:
        return arr
    pivot = arr[len(arr)//2]
    left = [x for x in arr if x < pivot]
    middle = [x for x in arr if x == pivot]
    right = [x for x in arr if x > pivot]
    return quick_sort(left) + middle + quick_sort(right)
```

---

# 📊 Complexity Cheat Sheet

| Algorithm      | Best       | Avg        | Worst      |
| -------------- | ---------- | ---------- | ---------- |
| Linear Search  | O(1)       | O(n)       | O(n)       |
| Binary Search  | O(1)       | O(log n)   | O(log n)   |
| Bubble Sort    | O(n)       | O(n²)      | O(n²)      |
| Selection Sort | O(n²)      | O(n²)      | O(n²)      |
| Insertion Sort | O(n)       | O(n²)      | O(n²)      |
| Merge Sort     | O(n log n) | O(n log n) | O(n log n) |
| Quick Sort     | O(n log n) | O(n log n) | O(n²)      |

---

