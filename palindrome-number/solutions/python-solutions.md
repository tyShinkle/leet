# Python Solutions

## Solution One: Reverse String Comparison

### Code
```python3
def IsPalindrome(x:int) -> bool:
    x_str = str(x)
    return x_str == x_str[::-1]
```

### Explanation

This algorithm utilizes the string slicing and stride syntax in python.

```python3
#    indices
#    01234
#  -(54321) 
s = "Test!"
print(s[1])     #=> e
print(s[-4])    #=> e (negative indexing does not utilize 0)
print(s[1:4])   #=> est (the first index is included while the second is sliced off. Indices are always 'sliced' on the left)
print(s[1:])    #=> est! (no second slice index sill only have a 'first slice')
print(s[:3])    #=> Tes (no first slice index will only have a 'second slice')
print(0::2)     #=> Ts! (stride by two skips every other character)
print(::-1)     #=> !tesT (negative stride starts at the end and no slicing means we'll print the whole string)

```
## Solution Two: Reverse Integer Comparison
