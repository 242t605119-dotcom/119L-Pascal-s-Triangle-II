# LeetCode 119 – Pascal's Triangle II

## Problem

Given an integer `rowIndex`, return the `rowIndex`th row of **Pascal's Triangle**.

The row index is **0-based**, meaning:

* Row `0` → `[1]`
* Row `1` → `[1,1]`
* Row `2` → `[1,2,1]`
* Row `3` → `[1,3,3,1]`

The solution should use **O(rowIndex)** extra space.

## Example 1

**Input:**

```text
rowIndex = 3
```

**Output:**

```text
[1,3,3,1]
```

## Example 2

**Input:**

```text
rowIndex = 0
```

**Output:**

```text
[1]
```

## Example 3

**Input:**

```text
rowIndex = 1
```

**Output:**

```text
[1,1]
```

## Approach

Instead of generating the entire Pascal's Triangle, we only need the requested row.

We can build the row gradually using the previous values. Starting with `[1]`, each new element can be calculated using the values already present in the row.

Another simple approach is to use the mathematical relationship between consecutive elements:

```text
next = current × (rowIndex - i) / (i + 1)
```

This allows the required row to be generated directly without storing all previous rows.

## Algorithm

1. Start the result with `1`.
2. Calculate each following value using the previous value.
3. Continue until all elements of the required row are generated.
4. Return the resulting list.

## Complexity

* **Time Complexity:** `O(rowIndex)`
* **Space Complexity:** `O(rowIndex)`

Only the requested row is stored.

## Difference from LeetCode 118

| LeetCode 118                    | LeetCode 119                    |
| ------------------------------- | ------------------------------- |
| Returns multiple rows           | Returns only one row            |
| Generates the complete triangle | Generates only the required row |
| `O(n²)` result space            | `O(n)` space                    |
| Pascal's Triangle               | Pascal's Triangle II            |

## LeetCode Details

* **Problem Number:** 119
* **Problem Name:** Pascal's Triangle II
* **Difficulty:** Easy
* **Language:** Python 3
* **File:** `solution.py`

## Topics

* Array
* Dynamic Programming

## Key Learning

This problem demonstrates how a problem can be optimized by calculating **only the required portion of the result** instead of constructing the entire Pascal's Triangle.

## Author

T.Nandhini
