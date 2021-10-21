# Method to Solve Increment Decrement Problem

## Method
1) First, write all the operation from right to left in a vertical way
2) Make a table with columns: `Input`, `Operation`, `Output`, `Preorder-check`, `Printing value`
3) For the first row initial value of `i` will be the `Input` and `Output` will be according to the `Operation`
4) Next row's `Input` will be the `Output` of its previous row
5) Last row's of `Output` value will be the last value of `i`
6) If the operation is pre-increment or pre-decrement then preorder-check will be marked as `1` otherwise `0`
7) If `Prorder-check` is marked as `1` then the `Printing value` for that row will be the last value of `i`, Otherwise the `Printing value` will be the `Input value` of that row
8) Writing `Printing values` from bottom to top will provide the answer

## Example

```C
    int i = 5;
    printf("%d %d %d %d %d", --i, ++i, i++, i--, i++);   // Output: 6 6 5 6 5
```

## Steps
### 1) First, write all the operation from right to left in a vertical way
| Operation |
| --- |
| i++ |
| i-- |
| i++ |
| ++i |
| --i |

### 2) Make a table with columns: `Input`, `Operation`, `Output`, `Preorder-check`, `Printing value`
| Input | Operation | Output | Preorder-check | Printing value |  
| ----- | -------- | ------ | -------------- | -------------- |
|  | i++ |  |  |  |
|  | i-- |  |  |  |
|  | i++ |  |  |  |
|  | ++i |  |  |  |
|  | --i |  |  |  |

### 3) For the first row initial value of `i` will be the `Input` and `Output` will be according to the `Operation`
- Initial value of `i` is `5`

| Input | Operation | Output | Preorder-check | Printing value |  
| ----- | -------- | ------ | -------------- | -------------- |
| 5 | i++ | 6 |  |  |
|  | i-- |  |  |  |
|  | i++ |  |  |  |
|  | ++i |  |  |  |
|  | --i |  |  |  |

### 4) Next row's `Input` will be the `Output` of its previous row
| Input | Operation | Output | Preorder-check | Printing value |  
| ----- | -------- | ------ | -------------- | -------------- |
| 5 | i++ | 6 |  |  |
| 6 | i-- | 5 |  |  |
| 5 | i++ | 6 |  |  |
| 6 | ++i | 7 |  |  |
| 7 | --i | 6 |  |  |

### 5) Last row's of `Output` value will be the last value of `i`
- Last value of `i` is `6`

### 6) If the operation is pre-increment or pre-decrement then preorder-check will be marked as `1` otherwise `0`
| Input | Operation | Output | Preorder-check | Printing value |  
| ----- | -------- | ------ | -------------- | -------------- |
| 5 | i++ | 6 | 0 |  |
| 6 | i-- | 5 | 0 |  |
| 5 | i++ | 6 | 0 |  |
| 6 | ++i | 7 | 1 |  |
| 7 | --i | 6 | 1 |  |

### 7) If `Prorder-check` is marked as `1` then the `Printing value` for that row will be the last value of `i`, Otherwise the `Printing value` will be the `Input value` of that row
| Input | Operation | Output | Preorder-check | Printing value |  
| ----- | -------- | ------ | -------------- | -------------- |
| 5 | i++ | 6 | 0 | 5 |
| 6 | i-- | 5 | 0 | 6 |
| 5 | i++ | 6 | 0 | 5 |
| 6 | ++i | 7 | 1 | 6 |
| 7 | --i | 6 | 1 | 6 |

### 8) Writing `Printing values` from bottom to top will provide the answer
`6, 6, 5, 6, 5`
