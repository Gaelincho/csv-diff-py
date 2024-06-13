# csv-diff-py

A python script that searches for differences between two csv's.

# Example

1st csv:
| id | value1 | value2 | value3 |
|----|--------|--------|--------|
| 1  | a      | x      | one    |
| 2  | b      | y      | two    |
| 3  | c      | z      | three  |

2nd csv:
| id | value1 | value2 | value3 |
|----|--------|--------|--------|
| 2  | b      | z      | abc    |
| 1  | a      | x      | one    |
| 3  | c      | w      | three  |

(you can see that the id's are in different positions, it doesn't matter)

- executing the script with the arguments "value2,value3", will output something like this:

```
--> 3 diff found
id: 2   diff-field: value2   1st csv: y   2nd csv: z 
id: 2   diff-field: value3   1st csv: two   2nd-csv: abc 
id: 3   diff-field: value2   1st csv: z   2nd-csv: w 
```

It also saves the output to a txt file in the "diff" folder.

