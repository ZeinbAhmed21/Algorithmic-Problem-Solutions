# 🔢 Project 9 — Distinct Values in a Stream

## 📖 Description
Given a **zero-indexed array A** consisting of `N` integers, write a function to **return the number of distinct values** in `A`.

**Constraints:**
1. Memory is limited; you cannot store the entire array at once.
2. The array is processed sequentially, one element at a time (stream processing).

Assumptions:
- N is within `[0..100,000]`
- Each element is within `[−1,000,000..1,000,000]`

---

## 🧠 Example

### Input
```
A = [2, 1, 1, 2, 3, 1]
```

### Output
```
Number of distinct values: 3
Unique elements: [1, 2, 3]
```

---

## ⚙️ Input / Output Format

- **Input:**
  - Integer `N` (number of elements)
  - Elements of the array one by one

- **Output:**
  - Number of distinct values
  - List of unique elements

---

## 🧩 Algorithm Steps

1. Read integer `N` for the number of elements.  
2. Initialize an empty set to store distinct values.  
3. Read each element from the stream:
   - If element is not in the set, add it.  
4. After processing all elements, return the size of the set and the distinct elements.  

---

## 🧾 Pseudo-code
```text
FUNCTION count_distinct_stream()
{
    READ n
    distinct_values := empty set

    FOR i := 0 TO n-1 DO
        READ num
        IF num NOT IN distinct_values THEN
            ADD num TO distinct_values
        END IF
    END FOR

    PRINT "Distinct values found:", LENGTH(distinct_values)
    PRINT "Unique elements:", distinct_values
    RETURN LENGTH(distinct_values)
}
```

---

## 💻 Sample Run
```bash
Enter number of elements (N): 6
A[0]: 2
A[1]: 1
A[2]: 1
A[3]: 2
A[4]: 3
A[5]: 1

=========================================
Distinct values found: 3
Unique elements: [1, 2, 3]
=========================================
```

---

## 🧮 Time & Space Complexity

| Step | Complexity |
|------|-------------|
| Processing each element in the stream | O(n) |
| Storing distinct elements | O(k) |
| **Total Time Complexity** | **O(n)** |
| **Space Complexity** | O(k) where k ≤ n |

---

## ⚠️ Edge Cases
| Input | Output |
|-------|--------|
| A = [] | 0 |
| A = [5,5,5,5] | 1 |
| A = [1,2,3,4,5] | 5 |

---

## 👨‍💻 Author
- **Name:** Zeinab Ahmed 
- **Role:** Helwan National University  
- **Email:** zeinb21ahmed@gmail.com

